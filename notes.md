## Работа с img в picture


```css
.hero__image {
  display: grid; /* делаем ячейку внутренним гридом — 
              один implicit-трек, img растянется сам */
}
.hero__image picture {
  display: contents; /* picture исчезает из дерева боксов,
                  img становится прямым grid item */
  display: block;
  block-size: 100%;
}
.hero__image img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover; /* по умолчанию fill — картинка растянется 
                       и исказится. cover сохраняет пропорции 
                       и обрезает лишнее */
  object-position: center; /* какую часть кадра сохранить при обрезке */
}
```