# 🗳️ Voting Questionnaire

Инструмент автоматизации взаимодействия с веб-анкетой оценки качества медицинской помощи с использованием **Python** и **Selenium WebDriver**.

> ⚠️ **Статус проекта:** Alpha. Проект создан для изучения автоматизации браузера и работы с Selenium.


## ✨ Возможности

- автоматическое открытие страницы анкеты;
- выбор региона и медицинской организации;
- автоматическое заполнение анкеты;
- сохранение полученных кодов в `data/log_code.txt`;
- поддержка Firefox WebDriver;
- модульная структура проекта.


## 🏗 Архитектура

main.py
   │
   ├── captcha.py      → работа с CAPTCHA
   ├── selectors.py    → поиск элементов
   ├── voting.py       → логика заполнения анкеты
   ├── utils.py        → вспомогательные функции
   └── config.py       → конфигурация


## 📁 Структура проекта

.
├── data/
├── modules/
│   ├── captcha.py
│   ├── config.py
│   ├── selectors.py
│   ├── utils.py
│   └── voting.py
├── main.py
├── requirements.txt
└── README.md


## 🚀 Быстрый старт

```bash
git clone https://github.com/IoneII/voting-questionnaire.git
cd voting-questionnaire

python -m venv .venv

# Windows
.venv\Scripts\activate

# Linux/macOS
source .venv/bin/activate

pip install -r requirements.txt
python main.py
```


## ⚙️ Настройка

В `modules/config.py` задайте:

```python
REGION_NAME = "Краснодарский край"
INSTITUTION_NAME = "Название медицинской организации"
```

При необходимости измените координаты взаимодействия с CAPTCHA под своё разрешение экрана.

## 🛠 Используемые технологии

| Компонент | Назначение |
|-----------|------------|
| Python | язык разработки |
| Selenium | автоматизация браузера |
| Firefox WebDriver | управление браузером |
| PyAutoGUI | взаимодействие с экраном |
| Pyperclip | работа с буфером обмена |


## ⚠️ Известные ограничения

- используются абсолютные XPath;
- координаты экрана заданы вручную;
- отсутствуют автоматические тесты;
- отсутствует Docker и CI/CD;
- проект находится в активной разработке.


## 🗺 Roadmap

- [ ] поддержка Chrome
- [ ] перенос конфигурации в `.env`
- [ ] переход на `WebDriverWait`
- [ ] улучшение обработки ошибок
- [ ] логирование
- [ ] Docker
- [ ] GitHub Actions
- [ ] автоматические тесты


## 🤝 Вклад

Pull Request и предложения по улучшению приветствуются.


## 📄 Лицензия

Лицензия пока не определена. При отсутствии файла `LICENSE` все права принадлежат автору.
