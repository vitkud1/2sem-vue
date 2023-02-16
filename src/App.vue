<template>
  <div class="main">
    <vue-collapsible-panel-group 
        style="max-width: 860px; margin: auto"
        base-color="#0a4028"
        v-for="lab in labs"
        :key="lab.title"
        accordion
        >
    <vue-collapsible-panel :expanded="false">
        <template #title>
          <div class="pre">
            <strong>
              {{ lab.title }}
            </strong>
          </div>
        </template>
        <template #content>
          <pre class="pre">
{{ lab.content }}
          </pre>
            
        </template>
    </vue-collapsible-panel>

</vue-collapsible-panel-group>
  </div>
  
</template>

<script>
import {
  VueCollapsiblePanelGroup,
  VueCollapsiblePanel,
} from '@dafcoe/vue-collapsible-panel'
import '@dafcoe/vue-collapsible-panel/dist/vue-collapsible-panel.css'

export default {
  components: {
    VueCollapsiblePanelGroup, VueCollapsiblePanel
  },
  data() {
    return {
      labs: [
        {
          title: '1 лабораторная работа',
          content: `1. Установить VUE-CLI;
2. Создать шаблонный проект "Hello, world";
3. Из предложенных компонентов оставить только компонент App.vue, очистить его;
4. Создать компонент PostItem (реализовать функционал отображения поста);
5. Создать компонент PostList (реализовать функционал списка PostItem);
6. Создать компонент PostCreate (реализовать функционал создания поста,
 обязательные компоненты: MyInput для названия и содержания; MyButton для создания 
 поста; остальное по желанию);
7. Создать UI компонент MyButton (стилизовать);
8. Создать UI компонент MyInput (стилизовать);
9. Зарегистрировать все компоненты в приложении;
10. В App.vue в template должны быть два компонента PostCreate и PostList;
11. Реализовать логику передачи данных с компонента на компонент с помощью props и emit;
12. Готовую работу залить либо на git (без папки node modules) и скинуть ссылку, 
либо прикрепить в тимс (без папки node modules).
*обязательно - пояснения в комментариях должны быть подробными`
        },
        {
          title: '2 лабораторная работа',
          content: `1. Создать компонент MyDialog (реализовать функционал для появления окна, внутри которого компонент PostCreate);
2. Создать компонент MySelect (стилизовать + реализовать функционал для сортировки по названию и содержанию);
3. Реализовать логику получения постов через axios;
4. Реализовать логику поиска по постам;
5. Реализовать компонент MyPagination (стилизация + логика);
*обязательно - пояснения в комментариях должны быть подробными`
        },
        {
          title: '3 лабораторная работа',
          content: `1. Создать компонент Navbar (стилизовать + организовать навигацию, подключить роутинг);
2. Дополнить приложение компонентом с PostList внутри, без пагинации, с подгружаемым списком при пересечении определенного div'a;
3. Подключить MyLoading компонент. Реализовать отрисовку компонента при активном процессе загрузки списка постов;
*обязательно - пояснения в комментариях должны быть подробными`
        },
        {
          title: '4 лабораторная работа',
          content: `1. Подключить firebase к проекту;
2. Создать Login и Registration компоненты, реализовать логику регистрации и авторизации;
3. Создать тестовые данные в RTDB;
4. Организовать CRUD;`
        },
        {
          title: '5 лабораторная работа',
          content: `1. По выбранной тематике (согласовать) разработать веб-приложение на Vue + firebase.
Главное условие: приложение должно быть структуризированно, логика разделена на компоненты.
2. Деплой сайта на хостинг firebase (или другой).
*Результатом будет являться прикрепленная ссылка на сайт.`
        },
      ]
    }
  }
}
</script>

<style>
.main {
  margin-top: 50px;
}
.pre {
  font-family: 'Courier New', Courier, monospace;
  white-space: pre-wrap 
}

</style>