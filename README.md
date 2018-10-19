# Player3D на React

[![Build Status](https://travis-ci.com/butik/react-player3d.svg?branch=master)](https://travis-ci.com/butik/react-player3d)


3D плеер на React для демонстрации товаров на 360° с использованием canvas через покадровую смену фотографий. Используется Canvas, как наиболее подходящий инструмент для управления пиксельными изображениями.

**Принимает параметры:**

`framesList` - массив ссылок на изображения (в примере загружается с api)

`intervalDefault` - интервал смены кадров по умолчанию (200мс)

`selectorStart` - селектор (id) элемента, который будет запускать плеер

**Пример использования компонента:**
```
<div class='container'>
  <Player3D
    framesList={images3d}
    selectorStart='start'
    intervalDefault={200}
  />
</div>
<button id='start'>Start</buttin>
```
В данном примере, классу container нужно задать ширину и высоту, так как canvas будет брать значение ширины и высоты родительского компонента при инициализации. Можно задавать относительные параметры в %.

`images3d` - это переменная содержащая массив ссылок на изображения

`'start'` - это id того элемента который будет запускать плеер. На него автоматически будет навешен обработчик на событие click. Достаточно добавить id
