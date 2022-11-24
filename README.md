# OneScriptForms
Графический интерфейс для сценарного языка OneScript.

Здесь представлена бесплатная библиотека для скриптового языка OneScript, содержащая набор форм и элементов управления для построения графических приложений. С её помощью можно создавать формы и элементы управления для различных видов графических приложений, вести программирование как в русскоязычном, так и в англоязычном вариантах.

Для визуального проектирования форм используйте библиотеку [OneScriptFormsDesigner](https://github.com/ahyahy/OneScriptFormsDesigner).

### Подробнее можно узнать на этом сайте

> <https://ahyahy.github.io/OneScriptForms/index.html>

### Область применения
* Решение административных задач. Удобная визуальная форма представления информации с использованием таблиц, списков, полей выбора, и других элементов управления облегчает и ускоряет работу администраторов и программистов. Можно представить результаты выполнения плановых заданий или скриптов в компактном и удобном виде на форме. 
* Оформление графического интерфейса для утилит, работающих только через консоль.
* Организация диалогов с пользователем или небольшого рабочего места.
* Программирование небольших текстовых, графических редакторов, записных книжек, напоминалок, может простеньких игр.
Всё это можно написать для себя и/или поделиться с сообществом.
### Подключение и примеры
Скачайте из [каталога docs](https://github.com/ahyahy/OneScriptForms/tree/main/docs) архив с именем формата OneScriptFormsх_х_х_х.zip. Скачайте последнюю версию. Поместите находящуюся в архиве библиотеку, в какой либо каталог на диске. Возможно будет необходимо правой кнопкой мыши вызвать свойства распакованного файла OneScriptForms.dll и разблокировать его. 
Подключить библиотеку и создать объект OneScriptForms для работы с формами можно так:

```bsl
     ПодключитьВнешнююКомпоненту("ВашКаталогНаДиске\OneScriptForms.dll");
     Ф = Новый ФормыДляОдноСкрипта();
```

В разделе `Документация` сайта библиотеки <https://ahyahy.github.io/OneScriptForms/doc.html> можно найти примеры использования на каждый метод/свойство экземпляров классов. Достаточно скопировать пример, вставить в файл и сохранить с расширением `.os`. Обратите внимание на кодировку сохраняемого файла, она должна быть UTF-8.
Тесты проведены в операционных системах Windows 7 и Windows 10 на OneScript версий 1.3.0.1 и 1.6.0.213 и 1.7.0.214.
### Запуск в Linux
Начиная с версии OneScriptForms.dll 2.2.0.0 библиотека работает и под Linux. При установке OneScript в систему будут установлены библиотеки из набора фреймворка MONO достаточные для работы односкрипта, но для работы с формами этого будет недостаточно. Потребуется более расширенный набор библиотек из MONO.
* В случае Linux Mint (тестирование выполнялось в Linux Mint 20.3). 
Установите пакет mono-complete (тестировалось на версии 6.12.0.182-0xamarin1+ubuntu1804b1).
* В случае Astra Linux (тестирование выполнялось в (Orel) 2.12.45). 
Установите пакеты gnome-themes-standard, libatk-adaptor и libgail-common.
* В случае Alt Linux (тестирование выполнялось в Альт Рабочая станция 10.0). 
Установите пакет mono-full Версия 6.12.0.147-alt1:p10+282075.100.7.1@1629802335 (ALT Linux p10).

### Интересные возможности
Библиотека имеет множество возможностей для оформления полноценного графического интерфейса для скрипта, написанного на OneScript. Перечислю некоторые.
* Методы СвернутьКонсоль(), СкрытьКонсоль(), ВосстановитьКонсоль() позволяют управлять окном консоли, связанной с вызывающим процессом. То есть ДОСовским черным окном.
* Использование буфера обмена.
* Графика позволит рисовать кистью геометрические фигуры, заливать поверхности паттернами и рисунками, копировать области экрана.
* Обработка событий с получением аргументов события.
* Отправка нажатия клавиш активному приложению.
* Поиск окна по заголовку.
* Имитировать программно нажатие кнопок мыши.
* Воспроизведение системных звуков и `.wav` файлов.
* Создание окон сообщений.
* Календари двух видов для удобного выбора даты.
* Горизонтальный и вертикальный индикаторы (ProgressBar).
* Работа с кодировкой.
* Использование класса Цвет.
* Имеется набор коллекций - МассивСписок (ArrayList), СортированныйСписок (SortedList), СписокЭлементов (ListView), ХэшТаблица (HashTable), Коллекция (Collection).
* Класс Математика позволит делать математические вычисления.
* Форму можно закрепить на рабочем столе и соответственно открепить от рабочего стола. Можно создать виджет, и он не будет свёрнут при использовании команды `Свернуть все окна`.
* Работа с иконкой в системном трее.
* Наблюдатель файловой системы проинформирует Вас о событиях, произошедших с файлами/каталогами.
* Таймер даст возможность выполнять действия в запланированное время.
* Есть диалоги для выбора шрифта, цвета, каталога, открытия/сохранения файла.
* При работе с классом Картинка Вы сможете попиксельно изменять изображение.
* Класс Разделитель обеспечит разделение формы на отдельные, регулируемые мышью по размеру, области.
* Конечно, есть классы Меню и КонтекстноеМеню.
* Используя сетку свойств, можно например создать настройки интерфейса, доступные пользователю.
* Таблицы.
### Устройство библиотеки
Несколько слов о том, как библиотека устроена. Она написана на `C#`.
Можно выделить три уровня классов.

Первый уровень – классы, наследуемые от исходных классов. Исходные классы и рисуют нам на экране формы или представляют невидимые объекты, такие как Таймер. 
Первый уровень есть не у всех объектов, потому что, среди исходных классов встречаются запечатанные классы, или не наследуемые по другим причинам. В имени классов первого уровня присутствует постфикс `Ex`.

```c#
    public class ButtonEx : System.Windows.Forms.Button
    {
        public osf.Button M_Object;
    }
```
Второй уровень образуют классы, копирующие структуру наследования исходных классов.

```c#
    public class Button : ButtonBase
    {
        public ClButton dll_obj;
        public ButtonEx M_Button;

        public Button()
        {
            M_Button = new ButtonEx();
            M_Button.M_Object = this;
            base.M_ButtonBase = M_Button;
        }
        //...
    }
```
Третий уровень дает нам объект для использования в скрипте OneScript. В нём мы можем задать русские и английские имена свойствам/методам. В имени классов третьего уровня присутствует префикс `Cl`.

```c#
    [ContextClass ("КлКнопка", "ClButton")]
    public class ClButton : AutoContext<ClButton>
    {
        private ClColor backColor;
        private ClRectangle bounds;
        private ClRectangle clientRectangle;
        private ClControlCollection controls;
        private ClColor foreColor;
        private ClCollection tag = new ClCollection();

        public ClButton()
        {
            Button Button1 = new Button();
            Button1.dll_obj = this;
            Base_obj = Button1;
            bounds = new ClRectangle(Base_obj.Bounds);
            clientRectangle = new ClRectangle(Base_obj.ClientRectangle);
            foreColor = new ClColor(Base_obj.ForeColor);
            backColor = new ClColor(Base_obj.BackColor);
            controls = new ClControlCollection(Base_obj.Controls);
        }
        //...
    }
```

Как Вы поняли, эти три уровня связаны переменными, скажем так, вертикально и находятся в одном `.cs` файле. Второй уровень связан наследованием, скажем так, горизонтально. Мы используем из скрипта доступный нам класс третьего уровня, он воздействует на класс второго уровня, который уже изменяет поведение класса первого уровня. Эта схема верна не для всех элементов управления, но она основная.
В иерархии пространства имен библиотеки Вы можете увидеть перечисления. Они на самом деле относятся к перечислениям как исходные объекты, объекты из библиотек MSDN и других. Здесь же это классы со свойствами. На уровне пользователя это не важно. Кстати, структуры тоже у меня превратились в классы.

Начиная с версии 2.0.0.0, обработка события происходит сразу после его наступления, без помещения его как в предыдущих релизах в очередь событий библиотеки. Для выполнения обработки событий запустите на исполнение следующий метод.

```bsl
    Ф.ЗапуститьОбработкуСобытий();
```

Для наглядности приведу простой пример создания кнопки.

```bsl
    ПодключитьВнешнююКомпоненту("ВашКаталогНаДиске\OneScriptForms.dll");
    Ф = Новый ФормыДляОдноСкрипта();
    Форма1 = Ф.Форма();
    Форма1.Текст = "Форма1";
    Форма1.Отображать = Истина;
    Форма1.Показать();
    Форма1.Активизировать();
    
    Кнопка1 = Форма1.ЭлементыУправления.Добавить(Ф.Кнопка());
    Кнопка1.Границы = Ф.Прямоугольник(10, 10, 75, 25);
    Кнопка1.Текст = "Кнопка1";
    
    Ф.ЗапуститьОбработкуСобытий();
```

Получаем форму с кнопкой.

![Пример с кнопкой](https://github.com/ahyahy/OneScriptForms/blob/main/docs/Button1.jpg)

