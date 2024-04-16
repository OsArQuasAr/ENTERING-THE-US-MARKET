## Задача оптимизации бронирования мест на конференцию

# Задача проекта

+-----------------------------------------------------------------------+
| Сентябрь 2016 года. Компания N организует в Бостоне конференцию,      |
| которая запланирована на первую половину 2017 года. Конференция       |
| пройдет в Бостонском Конференц Центре (415 Summer St, Boston, MA      |
| 02210) и продлится 3 дня. На нее поедет 150 человек, которых нужно    |
| разместить в квартирах, арендованных через Airbnb (Airbnb ― партнер   |
| конференции) Из 150 человек ― 10 топ-менеджеров, которым было обещано |
| одноместное размещение.                                               |
|                                                                       |
| **Ваша задача:**                                                      |
|                                                                       |
| 1.  Определить оптимальные даты конференции с точки зрения бюджета на |
|     > проживание (предполагаем 3 полных дня проживания).              |
|                                                                       |
| 2.  Подготовить отдельным файлом список квартир с указанием           |
|     > количества проживающих, ценой и любой дополнительной            |
|     > информацией на ваш выбор.                                       |
|                                                                       |
| 3.  Верхнеуровнево (не строя детальную модель на **«**больших         |
|     > данных**»**) оценить эффект других факторов, связанных с        |
|     > локацией проживания и временем проведения ― и влияющих на общий |
|     > бюджет.\                                                        |
|     > **Важно:** эти оценки идут независимо от вопросов №1-2 и не     |
|     > влияют на ответ на него в данной задаче.                        |
|                                                                       |
| При этом нужно, чтобы участники конференции в среднем оценили свою    |
| удовлетворенность (satisfaction) жильем на 8/10 или выше. Для         |
| достижения цели у вас есть бюджет в \$70'000 на жилье, но лучше       |
| потратить меньше.\                                                    |
| Вы самостоятельно оцениваете, как спрогнозировать satisfaction        |
| участников конференции. Например, вы можете учитывать удобства и      |
| рейтинг квартиры, погоду в Бостоне в это время года, информацию о     |
| районе проживания, транспортную доступность и др.                     |
|                                                                       |
| При решении задачи не принимайте во внимание пол сотрудников.         |
| Считайте, что вне зависимости от гендерного состава все смогут        |
| разместиться в выбранные вами квартиры и уровень safisfaction не      |
| изменится.                                                            |
+=======================================================================+
+-----------------------------------------------------------------------+

# 

# 

# Подготовка решения

-   Определить, с какими данными вы будете работать.

-   Выполнить предобработку данных: очистить их от лишней информации и
    > ошибок.

-   Оформить файл аккуратно и структурировано так, чтобы его понял
    > сторонний пользователь. Файлы будет просматривать эксперт.

-   Сформулировать и кратко описать подход для учета satisfaction от
    > проживания (без самих расчетов)

```{=html}
<!-- -->
```
-   **Итоговый Excel-файл**, где приведены этапы и результаты анализа, а
    > также список квартир с сопутствующей информацией.

-   **Презентация**

> Содержание презентации:

-   Описание задачи

-   Executive summary

-   функция satisfaction

-   Дополнительные источники, как они были использованы

### Материалы для работы

-   Задача проекта.

-   [[Boston Airbnb Open
    > Data]{.underline}](https://www.kaggle.com/airbnb/boston?select=listings.csv)
    > ― данные об аренде квартир через Airbnb в Бостоне.

    -   Если какие-то детали в данных для вас неочевидны, вы можете
        > делать разумные допущения. Например, вы можете считать, что
        > 1,5 ванных комнаты означает, что в квартире 1 душ/ванна и 2
        > туалета. Или же если цена за дополнительные услуги не указана,
        > то можете считать ее равной нулю.

    -   Если название каких-то столбцов в данных для вас неочевидно и вы
        > не нашли никаких комментариев по ним от авторов датасета, вы
        > можете или не использовать их в своем анализе, или сделать
        > разумные допущения, что они могут означать. **Разобраться в
        > данных, подготовленных другим человеком (которому нельзя
        > задать вопрос), ― часть задачи.**