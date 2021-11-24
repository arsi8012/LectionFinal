### План тестирования формы записи на обучение профессии "Тестировщик ПО"

**1. Перечень автоматизируемых сценариев**

_Навигация до формы записи на обучение:_
- Открыть в браузере адрес сайта https://netology.ru. На главной странице нажать на меню "Каталог курсов", далее выбрать раздел "Программирование", выбрать профессию "Тестировщик ПО" и нажать на кнопку "Записаться";
- Открыть в браузере адрес сайта https://netology.ru. На главной странице нажать на презантазионный модуль "НЕО для начинающих", в правой части страницы установить чекбокс напротив направления "Программирование", выбрать профессию "Тестировщик ПО" и нажать на кнопку "Записаться". 

_1.1 Позитивные сценарии:_
- Ввести корректные данные в поля "Имя" и "Номер телефона", нажать на кнопку "Записаться", выбрать "Способ оплаты" - Банковская карта.
  Ожидаемый результат - оплата проходит успешно;
- Ввести корректные данные в поля "Имя" и "Номер телефона", нажать на кнопку "Записаться", выбрать "Способ оплаты" - Оплата частями.
  Ожидаемый результат - оплата проходит успешно;
- Ввести корректные данные в поля "Имя" и "Номер телефона", нажать на кнопку "Записаться", выбрать "Способ оплаты" - Банковская карта.
  Ожидаемый результат - отказ в совершеннии операции;
- Ввести корректные данные в поля "Имя" и "Номер телефона", нажать на кнопку "Записаться", выбрать "Способ оплаты" - Оплата частями.
  Ожидаемый результат - отказ в совершеннии операции.

_1.2 Негативные сценарии:_
- Заполнить поле "Имя" невалидными данными.
  Ожидаемый результат - получаем сообщение "Должно состоять из букв";
- Заполнить поле "Номер телефона" невалидными данными.
  Ожидаемый результат - сообщение "Номер в формате +9 (999) 999-99-99";
- Проверить, что кнопка "Записаться" неактивна при некорректных данных.
  Ожидаемый результат - кнопка неактивна;
- Заполнить поле "Электронная почта" невалидными данными. 
  Ожидаемый результат - сообщение "Неверный email".

_Валидные данные полей ввода:_
- "Имя" - русские, латинские буквы, дефис;
- "Номер телефона" - формат +7(999)999-99-99;
- "Электронная почта" - латинские буквы, раздененные знаком @, с указанием домена с конце(пример, test@test.com)

_Невалидные данные полей ввода:_
- "Имя" - цифры, специальные символы (", !, @, %, и т.д.), пустое поле;
- "Номер телефона" - не соответствие формату +7(999)999-99-99, пустое поле;
- "Электронная почта" - не соответствие формату test@test.com, пустое поле.


**2. Перечень используемых инструментов с обоснованием выбора**

- Java 11 - язык программирования для написания автотестов;
- Gradle - система автоматической сборки и управления зависимостями;
- Junit 5 - фреймворк для тестирования ПО;
- Selenide - фреймворк для автоматизированного тестирования веб-приложений на основе Selenium WebDriver;
- Docker Compose - инструмент для запуска мультиконтейнерных приложений;
- GitHub - для хранения, обмена файлами проекта;
- Allire- фреймворк для создания отчетов.

**3. Перечень необходимых разрешений/данных/доступов**

- Разрешение на доступ к базе данных сайта http://netology.ru
- Pазрешение на тестирование формы записи на обучение.

**4. Перечень и описание возможных рисков при автоматизации**

- Тестирование формы на реальной (рабочей) системе может привести к техническим сбоям как в самом веб-приложении, так и используемой БД;
- Написание тестов осложняется отсутствием в реальных веб-приложениях необходимых локаторов полей и сообщений.

**5. Перечень необходимых специалистов для автоматизации**

Инженер тестировщик-автоматизатор.

**6. Интервальная оценка с учётом рисков (в часах)**

- Подготовка и настройка тестового окружения - 9
- Написание автотестов - 35
- Тестирование формы - 2
- Формирование итоговых отчетов - 2
**Итого - 48**