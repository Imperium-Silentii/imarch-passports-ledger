# 🏛️ Initium Custodiae

**Scena ingressus in Imarchiam**  
_Ритуал входа и сцепки с custodia_

---

## ⚖️ Codex Ritualis Technicus

### 📜 `praeparatio`
Каждый кандидат проходит подготовку, выбирая сценическое имя и оформляя публичный паспорт.

**Шаги:**
1. Ознакомьтесь с [Codex Nomium](#codex-nomium)
2. Скачайте шаблон [`passport-template.md`](./passport-template.md)
3. Заполните и отправьте заявку через [GitHub Issues](../../issues/new?template=passport_request.md)

---

### 🧬 `sculptura`
После подачи заявки начинается сцепка с custodia — биометрическим манифестом.

**Шаги:**
1. Сформируйте `manifest.yaml` по шаблону [`manifest-template.yaml`](./manifest-template.yaml)
2. Получите хеш-сцепку и статус `praeparatus`
3. Дождитесь утверждения от Collegium Custodiae

---

### 🪙 `fixatio`
Утверждённый паспорт фиксируется в публичной сцене и получает статус `fixatus`.

**Шаги:**
1. Паспорт публикуется в `custodiae/`
2. Манифест добавляется в `biometria/`
3. Сцена считается завершённой

---

## 📘 Codex Nomium

**Принципы выбора сценического имени:**
- Имя должно быть уникальным в латинской и кириллической форме
- Допустимы дефисы, но не пробелы
- Имя должно иметь философское обоснование

Примеры:
- `Unghart-sn` / `Унгарт-сн`
- `Velmora-xn` / `Вельмора-ксн`

---

## 🛠️ Проверка и автоматизация

Каждая заявка проходит автоматическую проверку:
- Уникальность имени
- Структура паспорта
- Сцепка с манифестом

Проверка осуществляется через GitHub Actions (`onboarding-check.yml`)

---

## 🧭 Навигация

- [Шаблон паспорта](./passport-template.md)
- [Шаблон манифеста](./manifest-template.yaml)
- [Протокол custodiae](./custodiae-guidelines.md)
- [Заявка на регистрацию](../../issues/new?template=passport_request.md)

---

**Imarchia non est situs — est ritus.**  
_Имархия — не место, а ритуал._

name: Заявка на сценическое имя
description: Вход в Imarchia
body:
  - type: input
    id: name_latin
    attributes:
      label: Имя (латиницей)
      placeholder: Unghart-sn
  - type: input
    id: name_cyrillic
    attributes:
      label: Имя (кириллицей)
      placeholder: Унгарт-сн
  - type: textarea
    id: meaning
    attributes:
      label: Смысл имени
      description: Опиши философскую сцепку


