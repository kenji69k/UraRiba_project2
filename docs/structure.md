1\. Сцены (уровни):

* ExampleLevel: Это стартовый и основной игровой уровень. При запуске проекта в редакторе и в собранной игре игрок попадает сюда. Это основной уровень для тестирования геймплея. На нём расположены платформы, персонаж игрока и другие интерактивные элементы.




2\. Объекты на основной сцене:

Blueprint: Block\_BP, Blue\_Coin\_Challenge\_BP, Blue\_Coin\_Challenge\_Pad\_BP, Bounce\_Pad\_BP, Circle\_Coin\_Spline\_BP, Coin\_Spawn\_1\_BP, Coin\_Spawn\_2\_BP, Escaping\_Coin\_Challenge\_BP, Gem\_BP, Green\_Coin\_Challenge\_BP, Green\_Coin\_Challenge\_Pad\_BP, Guide\_Widget\_BP, Instance\_Coin\_Spline\_BP, Interactive\_Coin\_Spline\_BP, Interp\_Movement\_Coin\_Component\_BP, Interp\_Movement\_Coin\_Spline\_BP, Loop\_Coin\_Component\_BP, Loop\_Coin\_Spline\_BP, Moving\_Coin\_Spline\_BP, Moving\_Pads\_BP, Moving\_Platform\_BP, Player\_Bot\_BP, Press\_Pad\_Challenge\_BP, Press\_Pad\_Challenge\_Reward\_BP, Ring\_Challenge\_BP, Rotating\_Cog\_BP, Rotating\_Coin\_Spline\_BP, Rotating\_Platform\_BP, Switch\_Platform\_BP, Translucent\_Coin\_BP, Translucent\_Coin\_Spawn\_BP, Translucent\_Instance\_Coin\_Spline\_BP.

Place Actors: Sky Sphere, Light Source, PostProcessVolume, SkyLight, Cube\_SM, Ramp\_SM, scaffold\_low, fence-straight, fence-corner-curved, cylinder\_SM, arrow, TextRenderActor.





3\. Игрок:

Capsule Component: Arrow Component, Mesh, CameraBoom: FollowCamera.

Character Movement





4\. Скрипты:

* Персонаж и управление

Player\_Bot\_BP — Blueprint игрового персонажа. Содержит компоненты движения, камеру, скелетный меш и логику обработки ввода.

Game\_Instance\_BP — Game Instance. Живет всю игровую сессию между уровнями. Хранит глобальное состояние (счет, прогресс, настройки).

Game\_Instance\_Interface\_BP — Blueprint Interface. Набор функций для взаимодействия с Game\_Instance\_BP.

* Интерфейсы (не Actor'ы)

Coin\_Sistems\_Interface\_BP — Blueprint Interface. Определяет общие функции для систем, связанных с монетами.

Game\_Instance\_Interface\_BP — Blueprint Interface. Определяет функции для доступа к глобальным данным игры.

* Челленджи (испытания)


Blue\_Coin\_Challenge\_BP — Логика испытания со сбором синих монет. Отслеживает прогресс и выдаёт награду при выполнении условия.

Green\_Coin\_Challenge\_BP — Аналогично, но для зеленых монет.

Escaping\_Coin\_Challenge\_BP — Испытание, где монеты «убегают» (двигаются) от игрока.

Press\_Pad\_Challenge\_BP — Испытание с нажатием на кнопки.

Press\_Pad\_Challenge\_Reward\_BP — Награда, выдаваемая за прохождение Press\_Pad\_Challenge\_BP.

Ring\_Challenge\_BP — Испытание с кольцами.

Blue\_Coin\_Challenge\_Pad\_BP — Площадка, связанная с Blue\_Coin\_Challenge\_BP.

Green\_Coin\_Challenge\_Pad\_BP — Аналогично для зеленого испытания.

* Монеты и предметы

Gem\_BP — Кристалл — подбираемый предмет.

Translucent\_Coin\_BP — Полупрозрачная монета — особый тип монеты.

Translucent\_Coin\_Spawn\_BP — Спавнер полупрозрачных монет.

Coin\_Spawn\_1\_BP — Спавнер монет (первый тип).

Coin\_Spawn\_2\_BP — Спавнер монет (второй тип).

Block\_BP — Блок.

* Сплайны и движение монет

Circle\_Coin\_Spline\_BP — Сплайн, задающий круговую траекторию для монет.

Loop\_Coin\_Spline\_BP — Сплайн с замкнутой траекторией.

Moving\_Coin\_Spline\_BP — Сплайн, по которому монеты движутся.

Rotating\_Coin\_Spline\_BP — Сплайн с вращающейся траекторией.

Instance\_Coin\_Spline\_BP — Сплайн для экземпляров монет.

Interactive\_Coin\_Spline\_BP — Сплайн с интерактивными монетами.

Interp\_Movement\_Coin\_Spline\_BP — Сплайн, по которому монеты движутся с интерполяцией.

Translucent\_Instance\_Coin\_Spline\_BP — Сплайн для полупрозрачных экземпляров монет.

* Компоненты движения

Interp\_Movement\_Coin\_Component\_BP — Actor Component. Компонент, добавляемый в актор для плавного движения между точками (интерполяция).

Loop\_Coin\_Component\_BP — Actor Component. Компонент, реализующий зацикленное движение.

* Платформы и механизмы

Moving\_Platform\_BP — Движущаяся платформа.

Rotating\_Platform\_BP — Вращающаяся платформа.

Switch\_Platform\_BP — Переключаемая платформа.

Moving\_Pads\_BP — Движущиеся площадки.

Rotating\_Cog\_BP — Вращающееся колесо.

Bounce\_Pad\_BP — Батут.

* UI

Guide\_Widget\_BP — User Widget (UMG). Виджет-подсказка, отображающий инструкции или подсказки для игрока.



