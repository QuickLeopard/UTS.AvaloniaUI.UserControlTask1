# UTS.AvaloniaUI.UserControlTask1

## 🏗️ Архитектура решения

- Пользовательский компонент TickChart на базе класса TemplatedControl и библиотеки ScottPlot для Avaloni UI в виде отдельной библиотеки классов.
- Приложение для демонстрации работы TickChart.

## 🎯 Цели разработки

- **TickChart**: Разработка высокопроизводительного компонента для отображения тиковых данных в реальном времени, на базе библиотеки ScottPlot. 
- **Отрисовка данных в реальном времени**: Поддержка до 10к точек на графике, скорость обработки до 100 точек в секунду.
- **Конфигурируемые через XAML свойства компонента TickChart**:
  - MaxVisibleTicks - целое значение, задающее максимальное количество отображаемых точек на графике тиковых данных.
  - Theme - выбор темы Dark/Light

## 🔧 Разработка

### Требуемые фреймворки и Nuget пакеты

- .NET 8.0 SDK
- Avalonia UI v11.3.6
- Avalonia.ReactiveUI v11.3.6
- ScottPlot v5.0.56
- xUnit v2.9.3

Шаблон проекта содержится в данном репозитории.
Для создания своего решения, необходимо клонировать данный репозиторий.

Свойство MaxVisibleTicks компонента TickChart должно редактироваться в демонстрационном приложении через NumericUpDown, в диапазоне от 100 до 1000, с шагом 50.

### Пример реализации пользовательского компонента TickChart

![Tick Chart Example](./Specs/Images/TickChartExample.png "Tick Chart")

### Логика пользовательского компонента TickChart
- Если точек меньше, чем заданное свойство MaxVisibleTicks, то все точки графика отображаются на всю доступную ширину.
- Если точек больше, чем заданное свойство MaxVisibleTicks, то данные начинают удаляться из коллекции и остаются только последние MaxVisibleTicks точек, остальные отбрасываются.

### Пример работы пользовательского компонента TickChart

https://github.com/user-attachments/assets/5932756f-1d05-4c93-bc89-e10f00b14533

## 🧪 Тестирование

## 🙏 Полезные материалы

- [Avalonia UI](https://avaloniaui.net/) - Cross-platform .NET UI framework
- [ReactiveUI](https://reactiveui.net/) - Reactive MVVM framework
- [ScottPlot](https://scottplot.net/) - Plotting library

