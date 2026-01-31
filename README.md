# Чат-бот на базе BERT2BERT (DailyDialog)

Короткий учебный проект: дообучение BERT‑подобной модели (BERT2BERT) на публичном датасете диалогов DailyDialog и генерация ответов в формате «вопрос → ответ».

## Что внутри
- `bert_dialogue_bot.ipynb` — полный пайплайн: загрузка данных, подготовка пар, токенизация, fine‑tuning, оценка и инференс.

## Датасет
- `OpenRL/daily_dialog` (Hugging Face Datasets).

## Модель
- `bert-base-uncased` в архитектуре Encoder‑Decoder (BERT2BERT).

## Как запустить
1. [Откройте](https://colab.research.google.com/drive/15czc_K283S4GCGlTN6aamCU6g28LUbaz?usp=sharing) `bert_dialogue_bot.ipynb` в Google Colab.
2. Запустите ячейки последовательно сверху вниз.
3. По окончании обучения модель сохранится в папку `bert_dialogue_bot_final`.

## Примечания
- Для ускорения обучения рекомендуется GPU.
- В ноутбуке уже настроены маскирование PAD‑токенов в `labels` и совместимость с разными версиями `transformers`.
- Метрика ROUGE используется как базовая, но для чат‑ботов полезно добавить семантические метрики (например, BERTScore).
