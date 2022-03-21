# moneyexchange

_Скрины программы:_ screen 1-4


_Библиотеки:_

GSON (vs Jackson, Moshi)
    Функционал исходный: записать/прочитать json, поэтому расширения форматов, размера библиотек, скорости работы нет.
    Основной выбор между gson/jackson/moshi (https://www.ericdecanini.com/2020/09/29/gson-vs-jackson-vs-moshi-the-best-android-json-parser/ не важны), 
    исходя из этогопопулярную (https://www.appbrain.com/stats/libraries/tag/json/json-parsing-libraries).

Retrofit (vs Volley)
    Ходовая (стабильная/поддерживаемая): выбрал что проще (функционал базовый, картинки обрабатывать не требуется)
    
    
_Текущее состояние:_    

**1. Загружать список валют с сайта ЦБ https://www.cbr-xml-daily.ru/daily_json.js**

    Есть: Retrofit + GSON
    
**отображать его в виде списка**

    Есть: CurrenciesActivity(RecyclerView)

**2. Возможность конвертировать указанную сумму в рублях в выбранную 
валюту**

    Есть: ConverterActivity

**3. Сохранение данных о курсах валют**

SharedPreferences


**и не перезагружать их при повороте экрана или перезапуске приложения.**
    
    Есть: при перезапуске приложения используется кэш SharedPreferences;
    
    Есть, но нужно переделывать: при повороте из-за реализации также используется SharedPreferences, 
    вместо более корректного onSave/RestoreInstanceState - не удалось применить CurrenciesActivity

**Добавление возможности перезагрузить список курсов вручную.**

    Есть CurrenciesActivity(buttonUpdate)


**4. Периодически обновлять курсы валют**

    Отсутствует: есть проблемы в понимании передачи состояния, применить god-class currenciesActivity 
    не получилось - как в текущем формате добавить Alarm Manager не понятно




   
