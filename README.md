Проект «Канбан-доска»
Макет - https://www.figma.com/file/gmwg0Me1T6szwVqd7KSYL6/Kanban?node-id=0%3A1
Функциональные требования

Исходная Канбан-доска должна иметь 4 блока с задачами:

    1.Backlog (задачи, которые требуют уточнения перед тем, как брать их в работу);
    2.Ready (задачи, которые могут быть взяты в работу);
    3.In progress (задачи, которые уже в работе);
    4.Finished (законченные задачи).

Требования к React

        Интерфейс должен быть поделен на компоненты. Перед началом работы хорошенько обдумайте, какие компоненты вы будете использовать. Деление на компоненты должно быть логичным и оправданным.
        После того как определитесь с делением на компоненты, подумайте о том, как верно организовать файловую структуру.
        Следуйте принципам модульности (используйте export, import).
        Возможно использование как классовых компонентов, так и функциональных.
        Используйте Synthetic events для работы с событиями.
        Для вывода разного состояния элементов в зависимости от действий пользователя (пример: раскрытое/свернутое меню пользователя) используйте условный рендеринг.
        Для реализации отдельных страниц для каждой задачи и перехода между страницами используйте библиотеку react-router. 
        При написании кода старайтесь следовать принципам KISS (Keep It Short and Simple — не усложняй) и DRY (Don’t Repeat Yourself — не повторяйся).

Требования к верстке и CSS

        Вёрстка должна соответствовать макету. Добиваться «pixel-perfect» соответствия не обязательно, но основные моменты должны быть соблюдены: цветовая гамма, шрифты, размеры, отступы.
        Приложение должно корректно отображаться и на мобильных устройствах. Дизайн для мобильной версии вы можете найти в макете.
        Соблюдайте семантическую вёрстку. В приложении должны присутствовать разделы <header>, <main> и <footer>. Кнопки должна быть реализованы элементом <button>, элементы дропдауна — списком <select> и так далее.
        При наведении курсора на любые кликабельные элементы должен появляться cursor: pointer.
        Учитывайте состояния кнопки «+ Add card» — активная и неактивная.

        → Если кнопка активна, её внешний вид должен соответствовать макету. При наведении она должна подсвечиваться (менять цвет), а курсор должен меняться на pointer.

        → Если кнопка неактивна (назначен атрибут disabled), её цвет должен отличаться от активного состояния, кнопка не должна реагировать на наведение курсора (цвет остаётся таким же, не появляется курсор pointer).
        Можете использовать любой вариант подключения стилей на ваше усмотрение: общий файл стилей проекта, CSS-модули или специальные React-библиотеки для стилизации компонентов (например, Styled Components). 
        Использовать селекторы по тегу и id для задания стилей нельзя. Используйте классы. 

Прочие требования

        Пишите код аккуратно, с соблюдением форматирования и отступов.
        Старайтесь давать компонентам, переменным и функциям осмысленные имена.
        Старайтесь использовать современный ES6 синтаксис: стрелочные функции, декомпозиция, spread и т.д.
        При размещении проекта на GitHub не забывайте добавить папку node_modules в файл .gitignore, чтобы она не попала в ваш репозиторий. О том, как настроить .gitignore и почему папки node_modules не должно быть в репозитории, можете прочитать в этой статье.

Подсказка: На начальном этапе (до подключения localStorage) можно использовать заглушку (mock) — объект с необходимыми данными, например:

const dataMock = [
   {
        title: 'backlog',
        issues: [
            {
                id: '12345',
                name: 'Sprint bugfix',
	    description: ‘Fix all the bugs’
            }
        ]
   },
   // и так далее
]

-------------------------------------------------------------------------------------

Kanban Board Project
Layout - https://www.figma.com/file/gmwg0Me1T6szwVqd7KSYL6/Kanban?node-id=0%3A1
Functional requirements

The original Kanban board should have 4 blocks with tasks:

    1.Backlog (tasks that need clarification before taking them to work);
    2.Ready (tasks that can be taken to work);
    3.In progress (tasks that are already in progress);
    4.Finished (completed tasks).

React Requirements

        The interface should be divided into components. Before starting work, think carefully about which components you will use. The division into components should be logical and justified.
        After you decide on the division into components, think about how to organize the file structure correctly.
        Follow the principles of modularity (use export, import).
        It is possible to use both class components and functional ones.
        Use Synthetic events to work with events.
        To display different states of elements depending on user actions (example: expanded/collapsed user menu), use conditional rendering.
        To implement separate pages for each task and navigate between pages, use the react-router library. 
        When writing code, try to follow the principles of KISS (Keep It Short and Simple — don't complicate it) and DRY (Don't Repeat Yourself — don't repeat yourself).

Layout and CSS requirements

        The layout must match the layout. It is not necessary to achieve "pixel-perfect" compliance, but the main points must be observed: colors, fonts, sizes, margins.
        The application must be displayed correctly on mobile devices as well. You can find the design for the mobile version in the layout.
        Observe the semantic layout. The application must have sections <header>, <main> and <footer>. Buttons should be implemented by the <button> element, dropdown elements by the <select> list, and so on.
        Cursor: pointer should appear when hovering the cursor over any clickable elements.
        Take into account the states of the "+ Add card" button — active and inactive.

        → If the button is active, its appearance must match the layout. When hovering, it should be highlighted (change color), and the cursor should change to pointer.

        → If the button is inactive (the disabled attribute is assigned), its color should differ from the active state, the button should not react to the cursor hover (the color remains the same, the pointer cursor does not appear).
        You can use any style connection option at your discretion: a common project style file, CSS modules or special React libraries for styling components (for example, Styled Components). 
        You cannot use selectors by tag and id to set styles. Use classes. 

Other requirements

        Write the code carefully, observing formatting and indentation.
        Try to give components, variables, and functions meaningful names.
        Try to use modern ES6 syntax: arrow functions, decomposition, spread, etc.
        When hosting a project on GitHub , do not forget to add the node_modules folder to the file .gitignore, so that it doesn't end up in your repository. About how to configure .gitignore and why the node_modules folder should not be in the repository, you can read in this article.

Hint: At the initial stage (before connecting localStorage), you can use a stub (mock) — an object with the necessary data, for example:

const dataMock = [
   {
        title: 'backlog',
        issues: [
            {
                id: '12345',
                name: 'Sprint bugfix',
	    description: ‘Fix all the bugs’
            }
        ]
   },
   // и так далее
]