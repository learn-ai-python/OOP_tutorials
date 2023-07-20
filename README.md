# OOP
OOP (Обʼєктно-орієнтоване програмування) туторіали. Код наведений у файлах цього репозиторію [OOP_tutorial_2_3_4.ipynb](https://github.com/learn-ai-python/OOP_tutorials/blob/master/OOP_tutorial_2_3_4.ipynb), [OOP_tutorial_5.ipynb](https://github.com/learn-ai-python/OOP_tutorials/blob/master/OOP_tutorial_5.ipynb), [OOP_tutorial_6.ipynb](https://github.com/learn-ai-python/OOP_tutorials/blob/master/OOP_tutorial_6.ipynb).

## 🎬 Відео-туторіали
* [Туторіал по ООП. Частина-1](https://www.tiktok.com/@learn.ai.python/video/7185242001275686149?lang=uk-UA)
* [Туторіал по ООП. Частина-2](https://www.tiktok.com/@learn.ai.python/video/7185973939942804742?lang=uk-UA)
* [Туторіал по ООП. Частина-3](https://www.tiktok.com/@learn.ai.python/video/7187085842781916422?lang=uk-UA)
* [Туторіал по ООП. Частина-4](https://www.tiktok.com/@learn.ai.python/video/7188216402422074630?lang=uk-UA)
* [Туторіал по ООП. Частина-5](https://www.tiktok.com/@learn.ai.python/video/7189288538859425030?lang=uk-UA)
* [Туторіал по ООП. Частина-6](https://www.tiktok.com/@learn.ai.python/video/7190416735315545349?lang=uk-UA)
* [Туторіал по ООП. Частина-7](https://www.tiktok.com/@learn.ai.python/video/7192681092447587590?lang=uk-UA)

## 📑 Текстові версії відео-туторіалів

#### 📚 Частина-1
Як вже відомо, Python підтримує обʼєктно-орієнтоване програмування. Тому, у Python можливо створювати обʼєкти та класи. Концепція об'єктів має важливе значення у світі програмування. **Об'єкти** - це спосіб організації коду в програмі, а також спосіб поділу складних завдань на простіші, що полегшує їх вирішення. У мові Python об'єкти визначаються класами, завдяки яким можна розділяти об'єкти за смисловими групами.

![telegram-cloud-photo-size-2-5305719400676049951-x](https://github.com/learn-ai-python/OOP_tutorials/assets/108177042/3ca78c35-3216-4dc7-ade3-9503d3c9445d)

Розглянемо наступний приклад. Нехай, у нас є клас ```Animals``` (Тварини). Він має два підкласи - ```Mammals``` (Ссавці) та ```Birds``` (Птахи). У свою чергу, клас ```Mammals``` має два підкласи - ```Dogs``` (Собаки) та ```Cats``` (Коти). Коли один клас є окремим випадком (підкласом) іншого класу, кажуть, що перший клас — нащадок, а другий — предок. Один і той же клас може бути нащадком деяких класів, так і предком для інших класів. Наприклад, клас ```Mammals``` нащадок класу ```Animals```, але предок для класів ```Dogs``` та ```Cats```. 

У наступній частині ми напишемо код, що описує ці всі класи.

#### 📚 Частина-2
У другій частині ми напишемо код, що описує ці всі класи, про які ми говорили у Частині-1 даного туторіалу.

![telegram-cloud-photo-size-2-5319255870577689729-x](https://github.com/learn-ai-python/OOP_tutorials/assets/108177042/13803baa-1935-485a-809d-cff9df90648c)

Нагадаємо структуру класів, про яку ми говорили у першій частині. Діаграма представлена на екрані. Тепер перейдемо до написання коду. Програма написана у середовищі Google Colab. 

Спочатку опишемо клас ```Animals```. Сам клас описується за допомогою ключового слова ```class```. Історично прийнято, що класи описуються із великої літери. Це, так би мовити, правило, що оголошене конвенцією у ```PEP 8```. Але, це лише для краси коду. Клас містить у собі поля та методи. **Поля** - це як характеристики класу, а **методами** називають функції, які описані у середині класу. Перше, що ми бачимо - це метод ```init```. У Python він є еквівалентом конструктора C++ в об’єктно-орієнтованому підході.

На вхід до методу ```init``` передаються наступні параметри: ```self```, ```name```, ```kind```, ```weight```, ```height```. Слово ```self``` in у Python використовується для всіх екземплярів у класі, а також вказується у параметрах методу. Використовуючи ключове слово ```self```, можна легко отримати доступ до всіх методів та полів класу. І у самому методі ми описуємо поля класу. Поля класу позначаються через ```self``` - крапка - назва поля класу. Це ```self.name```, ```self.kind```, ```self.weight```, ```self.height```.

І цим полям класу ми задаємо значення, що описуються змінними ```name1```, ```kind1```, ```weight1```, ```height1```. Також, нижче ми описуємо два методи - ```move()``` та ```talk()```. Не забуваємо і про слово ```self```, яке ми передаємо у кожен із методів. У методі ```move()``` ми будемо виводити на екран слово ```"Moving"```, а у методі ```talk()``` ми будемо виводити ```"U-u-u-u"```.

Після цього ми протестуємо наш клас. Створимо обʼєкт класу, або, якщо його ще називають, екземляр класу. Назвемо його ```animal```, тоді ```animal = Animals("No-name", "no-kind", 0.5, 10)```.

**Вхідні параметри** - це ті, що ми задавали при створенні класу. Зверніть увагу, що слово ```self``` пишеться лише у самому класі, при написанні коду. А вже при створенні обʼєкта класу слово ```self``` опускається і ми передаємо лише вхідні параметри. Тепер, щоб звернутися до полів та методів екземпляру класу, ми маємо написати назву змінної екземпляру класу (у нашому випадку це aminal) та через крапку вказати саме те, що нам необхідно. І ми виводимо на екран поле ```name```, а також методи ```move()```, ```talk()```. 

У наступній частині ми розглянемо код до інших класів.

#### 📚 Частина-3
У третій частині ми продовжимо розглядати код для наших класів. Тепер, розглянемо класи ```Birds``` та ```Mammals```. Ці класи - нащадки класу ```Animals```. Розглянемо детальніше клас ```Birds```. Так як він є нащадком класу ```Animals```, у дужках біля цього класу ми вказуємо, який клас є предком для даного. Тобто - клас ```Birds``` нащадок класу ```Animals```. У ньому ми також описуємо метод ```init```. У середині цього методу ми пишемо ```super()``` - крапка - ```init```. Це означає те, що ми **НАСЛІДУЄМО** метод-конструктор класу-предка. Саме слово ```super()``` означає те, що ми звертаємося безпосередньо до класу-предка. У нашому випадку це клас ```Animals```. Як ми бачимо, щойно ми розглянули *перший із принципів ООП* - **НАСЛІДУВАННЯ**. 

Дивимося далі. Ми **ПЕРЕВИЗНАЧАЄМО** методи ```move()``` та ```talk()``` для класу ```Birds```. Тобто, у нас були одноіменні методи у класі-нащадку (```Animals```). А ми хочемо, щоб для класу ```Birds``` ці ж методи вели себе інакше. Тому, ми задаємо ці методи і прописуємо всередині них інші дії. Це щойно ми поговорили про *другий принцип ООП* - **ПОЛІМОРФІЗМ**. Тобто, поліморфізм у Python визначає методи в дочірньому класі, які мають ті самі назви, що й методи в батьківському класі. Сам термін походить від грецьких слів -  *poly* — «багато» і *morph* — «форма». Тобто такий, що приймає багато форм.

Тепер, створимо екземпляр класу та подивимося, що буде відбуватися. Нас найбільше цікавлять методи, які ми перевизначили у цьому класі. Як ми бачимо, методи виводять на екран саме ту інформацію, яку ми прописали у класі-нащадку ```Birds```. Якщо ж ми закоментуємо перевизначені методи та перезапустимо ячейки із кодом, то при виклику даних методів, викличуться методи класу-предка ```Animals```.

У наступній частині ми розглянемо код до інших класів.

#### 📚 Частина-4
Створюємо для прикладу екземпляр класу ```mammal```. Після цього ми описуємо ще два класи - ```Dogs``` та ```Cats```, що є нащадками класу ```Mammals```. У класі ```Dogs``` ми наслідуємо метод ```init()``` класу ```Mammals``` та перевизначаємо методи ```move()``` та ```talk()```. Тоді, створюємо екземпляр класу ```Dogs``` для тестування. І такі ж самі дії повторюємо для класу ```Cats```. Наслідуємо метод ```init()``` класу ```Mammals``` та перевизначаємо методи ```move()``` та ```talk()```. Та перевизначаємо класи ```move()``` та ```talk()```. І створюємо екземпляр класу ```Cats``` для тестування. 

На цьому створення цієї структури класів завершено. 

#### 📚 Частина-5
У пʼятій частині цих туторіалів ми поговоримо про третій принцип ООП - абстрагування. Абстракція використовується, щоб приховати внутрішню функціональність методу від користувачів. Юзери взаємодіють лише з базовою реалізацією функції, але її внутрішнє виконання приховане. Користувачі знайомі з тим, «що робить функція», але вони не знають, «як це робиться».

Якщо говорити простими словами, то наведу такий [приклад](https://www.javatpoint.com/abstraction-in-python): ми всі знаємо, що у сучасних телефонах є функції камери, голосового набору, радіо тощо, але ми не знаємо, які саме механізми задіяні при виконанні цих функцій у телефоні.

На відміну від інших мов, Python не надає самого абстрактного класу як такового. Тому, нам потрібно імпортувати модуль ```abc```, який забезпечує основу для визначення класів ```Abstract Base Classes (ABC)```. Метод стає абстрактним, якщо його декорують ключовим словом ```@abstractmethod```.

На екрані ви бачите приклад із кодом: ми створюємо абстрактний клас ```Point```, який наслідується від ```Abstract Base Class (ABC)```. І у ньому ж є абстрактний метод ```area_info()```. Далі ми описуємо класи-нащадки від класу ```Point```, у яких і перевизначаємо по-своєму абстрактний метод ```area_info()```.

#### 📚 Частина-6
У шостій частині цих туторіалів ми поговоримо про *четверний принцип ООП* - **ІНКАПСУЛЯЦІЮ**. **Інкапсуляція** — це механізм обгортання змінних і коду, що діє на методи, як єдине ціле. При інкапсуляції змінні класу будуть приховані від інших класів і доступ до них можливий лише через методи їх поточного класу. 

Для наочності розглянемо реальний [приклад](https://www.geeksforgeeks.org/encapsulation-in-python/) інкапсуляції: у компанії є різні відділи, відділ менеджменту, відділ фінансів, відділ продажу тощо. Зараз може виникнути ситуація, коли з якихось причин співробітнику з фінансового відділу знадобиться інформація від відділу менеджменту. У цьому випадку цей співробітник не матиме прямого доступу до даних відділу менеджменту. Спочатку йому доведеться зв’язатися з іншим співробітником відділу менеджменту, а потім лише попросити його надати конкретні дані.

Взагалі, в ООП виділяють **три типи інкапсуляції**: ```public```, ```private``` та ```protected```. ```Public``` поля та методи доступні у середині даного класу та всім ззовні. ```Private``` поля та методи доступні лише у середині даного класу. ```Protected``` поля та методи доступні у середині даного класу та у нащадках даного класу.

У Pythonʼі нема інкапсуляції як такової. Тому, тут ми можемо це досягти лише за допомогою правил написання імен до змінних. Я маю на увазі те, що всі поля та методи будуть всеодно доступні ззовні класу саме у Python. Тому для читабельності коду, прийнято називати змінні наступним чином:
* Якщо змінна ```protected```, то на початку імʼя змінної ми додаємо одне нижнє підкреслення.
* Якщо змінна ```private```, то на початку імʼя змінної ми додаємо два нижніх підкреслення.

На екрані ви бачите приклад коду, де ми у класі створили три відповідних змінних. До ```public``` змінної ми отримуємо доступ просто через ```element.a```. До ```proteted```  - ```element._b```. А от для того, щоб звернутися до ```private``` змінної, що містить на початку два нижніх підкреслення - є певні нюанси. Якщо звертатися як ```element.__c```, то ми отримаємо помилку у Python. Тому, тут є два виходи: перший - створити ```public``` метод, у нашому випадку це ```display_c()```, або ж використати ідею **спотворення імені** (англійською це називається **name mangling**). Тоді ми отримуємо доступ до змінної як ```element._Parent__c```, де ```Parent``` - це назва нашого класу.

#### 📚 Частина-7
У заключній, сьомій частині, ми поговоримо про діаграми UML, що використовуються для візуального опису класів. **Діаграма класів UML** — це графічна нотація, яка використовується для побудови та візуалізації об’єктно-орієнтованих систем. Діаграма класів в уніфікованій мові моделювання (Unified Modeling Language, або скорочено UML) — це тип діаграми, яка описує структуру системи, показуючи класи, їхні атрибути, методи та зв’язки між елементами. В UML клас представляє елемент або набір елементів, які мають спільну структуру та поведінку. Вони представлені прямокутником на знімку екрана нижче, який містить такі рядки: імʼя класу, його поля та методи. На екрані ви бачите приклад діаграми UML для трьох класів - ```Animals```, ```Mammals``` та ```Cats```.

<img width="453" alt="image" src="https://github.com/learn-ai-python/OOP_tutorials/assets/108177042/358a87be-a122-4ea7-ab46-8e550a9b7a15">



Дякую всім, хто додивився до кінця!

