# SnakeForFun

Эта программа представляет собой консольную игру "Змейка" на языке программирования C#. 

1. **Инициализация окна консоли и объектов игры:**
   - `Console.SetWindowSize(80, 25);`: Устанавливает размер окна консоли.
   - `Console.SetBufferSize(80, 25);`: Устанавливает буфер консоли для предотвращения мерцания.

2. **Создание объектов игры:**
   - `Walls walls = new Walls(80, 25);`: Создает объект стен, представляющий границы игрового поля.
   - `Point p = new Point(4, 5, '*');`: Создает начальную точку для змеи.
   - `Snake snake = new Snake(p, 4, Direction.RIGHT);`: Создает объект змеи с начальной точкой, длиной и направлением движения.
   - `FoodCreator foodCreator = new FoodCreator(80, 25, '$');`: Создает объект генератора еды.

3. **Отрисовка начального состояния:**
   - `walls.Draw();`: Отрисовывает стены.
   - `snake.Draw();`: Отрисовывает змею.
   - `Point food = foodCreator.CreateFood();`: Генерирует и отрисовывает еду.

4. **Основной игровой цикл:**
   - Проверяет столкновение змеи со стенами или ее самой. Если столкновение произошло, игра завершается.
   - Если змея съела еду, генерируется новая еда, и змея увеличивается.
   - В противном случае змея продолжает движение в текущем направлении.
   - Обрабатывает ввод пользователя, управляя направлением змеи.

5. **Метод `WriteGameOver()`:**
   - Выводит сообщение о завершении игры в случае столкновения змеи со стенами или самой собой.

6. **Метод `WriteText(String text, int xOffset, int yOffset)`:**
   - Вспомогательный метод для вывода текста на консоль в указанных координатах.

7. **Цикл ввода пользователя:**
   - `Console.KeyAvailable`: Проверяет наличие нажатой клавиши.
   - `Console.ReadKey()`: Считывает нажатую клавишу и передает ее обработчику змеи.

8. **Метод `Thread.Sleep(100)`:**
   - Задержка для управления скоростью движения змеи.

9. **Метод `Console.ReadLine()`:**
   - Ожидание нажатия Enter после завершения игры для закрытия консольного окна.

Таким образом, программа создает простую консольную игру "Змейка" с базовым управлением, генерацией еды и обработкой столкновений.
