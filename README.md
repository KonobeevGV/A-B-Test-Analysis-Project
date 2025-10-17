
# A/B Test Analysis

Функция для анализа A/B теста с расчетом конверсии, ARPU и AOV.

## Что делает

- Объединяет данные из нескольких CSV файлов
- Считает метрики для групп A и B
- Проверяет статистическую значимость различий

## Метрики и тесты

- **Конверсия** - Z-test пропорций
- **ARPU** - Bootstrap доверительные интервалы  
- **AOV** - U-test Манна-Уитни

## Использование


results, df = update_and_recalculate_metrics(
    groups_add_path='Проект_2_group_add.csv',
    groups_path='Проект_2_groups.csv',
    active_studs_path='Проект_2_active_studs.csv', 
    checks_path='Проект_2_checks.csv'
)


## Входные данные

- `groups.csv` - распределение по группам
- `groups_add.csv` - дополнительные пользователи
- `active_studs.csv` - активность
- `checks.csv` - покупки

## Установка

```bash
pip install pandas numpy scipy
```

## Результат

Функция возвращает таблицу с метриками, p-value и доверительными интервалами.
```
