Проект Illustrator master выполнен Щеголевой Анастасией.

Идея проекта заключается в:
1.Создание программы для рисования, которая будет простой в использовании, но при этом функциональной и интересной для пользователей.
2. Проектирование пользовательского интерфейса: разработка удобного и понятного интерфейса, включающего меню, панель инструментов и холст для рисования.
3. Выбор инструментов и функций: определение набора инструментов для рисования (кисть, ластик, различные фигуры), а также дополнительных функций (сохранение изображений, отмена действий, очистка всего холста, открытие других изображений).

При реализации своего проекта я использовала следующие классы и функции:
- три основных класса(окна приложения):
    - Illustrator_master (главное окно)
    - Drawing_window (окно для рисования)
    - db_Window (окно с последними работами, с подключением к базе данных);
-Классы для построения фигур: Circle, Line, Rectangle;
-В классе Drawing_window в функции closeEvent я использовала QMessageBox для того, чтобы пользователь не забыл сохранить свою работу при выходе;
-В функции open я создала возможность открывать как изображения формата 'PNG', 'JPG', так и текстовые файлы формата 'TXT'
-Для выбора цвета, открытия и сохранения файлов я использовала различные диалоговые окна
-База данных:
    - Для работы с  базой данных я использовала библиотеку SQLAlchemy
    - подключение происходит в функции global_init
    - в классе Main_master происходит создание таблицы в базе данных
    - в функцию add_main_master добавляются новые значения(id, время сохранения, путь к файлу)
    - для отображения данных я воспользовалась виджетом QTableWidget
    - функция open_run создана для просмотра сохранённого изображения (при помощи библиотеки Pillow)
При работе с данным проектом я использовала следующие библиотеки: 
PyQt5~=5.15.9
Pillow~=10.1.0 
SQLAlchemy~=2.0.23
datetime
