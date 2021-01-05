# Profile card component

![Design preview for the Profile card component coding challenge](./design/desktop-preview.jpg)

[Макет компонента](https://www.frontendmentor.io/challenges/profile-card-component-cfArpWshJ) • [**Рабочий пример**](https://jovial-ptolemy-0fcd6c.netlify.app/)

## Установка

`npm install -g @vue/cli @vue/cli-service-global`

## Сборка и запуск

* `npm run build`
* `npm run start`

## Как использовать компонент

1. Скопировать файл компонента `ProfileCard.vue` в папку проекта с компонентами
2. Подключить
`import ProfileCard from "./ProfileCard.vue";`
3. Добавить в иерархию компонентов:
```
//...
components: {
  ProfileCard
}
//...
```
4. Вставить код в разметку:
```
<profile-card
  username="Victor Crest"
  age="26"
  city="London"
  followers="80K"
  likes="803K"
  photos="1.4K"
  avatar="images/image-victor.jpg">
</profile-card>
```
5. Изменить значение пропсов
