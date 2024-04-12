# Summary
Диагностика COVID-19 основана на выявлении в биологических жидкостях и тканях антигена, то есть возбудителя новой короновирусной инфекции, а далее при
отработке методов и антител, вырабатывающихся при контакте с патогеном. Однако лабораторные методы часто занимают много времени, увеличивая риск развития тяжелых осложнений.
Пульмонологи и радиологи пришли к выводу, что компьютерная томография легких - наиболее оперативный способ выявления респираторных нарушений и начальных изменений в органе до
постановки окончательного диагноза. Лучевые методы, не являясь основными в диагностике коронавирусной инфекции, стали наиболее информативными для выявления наличия и выраженности изменений в органах дыхания.

Данные лучевой визуализации позволяют заподозрить поражение легких вирусной этиологии (в том числе COVID-19), влиять на ведение конкретного пациента, лечение осложнений или постановку альтернативного диагноза.

Набор данных представляет собой ренгтенограммы пациентов с диагнозом COVID-19 собранных в период пандемии коронавирусной инфекции и здоровых добровольцев.

# 1. Состав команды:
| **Участник**    | **Роль**                                                                |
|-----------------|---------------------------------------------------------------------|
| Захарцев Е.П.   | Техническая (создание и настройка проекта cvat.ai) и разметка       |
| Артюшев Р. И.   | Информационная (сбор датасета и первичный анализ данных) и разметка |
| Богданова Н. А. | Разметка                                                            |


# 2. Процесс разметки

Для разметки данных мы проанализировали **100** изображений (из 100), **50** - от пациентов с подтвержденным диагнозом COVID-19 и **50** изображений от здоровых добровольцев.

Разметка производилась (выделение полигона на интересующем участке изображения) на облачной версии cvat.ai., на основании данных о проявлении воспалительных изменений в легких у пациентов:
+ уплотнение легочной ткани по типу матового стекла, различной, зачастую округлой формы
+ наличие участков матового стекла с ретикулярными изменениями (утолщенные междольковые перегородки («лоскутное одеяло /булыжной мостовой»)
+ участки консолидации легочной ткани
+ синдром «обратного гало»
+ увеличение диаметра сосудов в уплотненной легочной ткани
+ реакционные бронхоэктазы

# 3. Гипотеза

Гипотеза исследования заключается в оценке возможности обучения модели машинного обучения на данном датасете, для постановки диагноза пневмония у пациентов с COVID-19 по рентгенограмме.

Детальная структура данных описаны ниже.

## Data
**1. Данные полученные от пациентов с диагнозом COVID-19:**
   
   50 обезличенных рентгенограмм были получены в ходе проведения обсервационного исследования формата "случай-котроль" в Институте клинической кардиологии им. А. Л. Мясникова. Доступ к данным был обеспечен на основании меморандума о сотрудничестве и взаимопонимании между Институтом клинической кардиологии им. А. Л. Мясникова и ФГБНУ Научно-исследовательским институтом общей патологии и патофизиологии. В связи с тем, что конечным бенефициаром изображений является Институт клинической кардиологии им. А. Л. Мясникова и доступ к ним обеспечен исключительно в ознакомительных целях и для внутреннего пользования, все требования к нормативной документации, включая, но не ограничиваясь; информированное согласие, разрешение на проведение исследования и так далее, полностью обеспечивается Институтом клинической кардиологии им. А. Л. Мясникова.

   Данная группа изображений выступает в роли **"случай"**
   
**2. Данные  полученные от здоровых добровольцев:**
   
   50 обезличенных рентгенограмм здоровых добровольцев были получены из Международного хранилища данных медицинских изображений региона Валенсия, Больница Сан-Хуан-де-Аликанте – Университет Аликанте (База данных PadChest). Использование PadChest бесплатно для всех исследователей.

   Данная группа изображений выступает в роли **"контроль"**
   

