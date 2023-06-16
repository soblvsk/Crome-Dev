# Tooling (Тулинг)

### 1. На вкладке Network

#### 1.1. Профиль загрузки ресурсов [HAR](./files/www.gd.ru.har)

#### 1.2. Неоптимальные места:

##### 1.2.1. Дублирование ресурсов

- code.js повторился 2 раза
  ![code.js](./images/Screenshot_1.png)

- www.1cont.ru повторился 2 раза
  ![www.1cont.ru](./images/Screenshot_2.png)

- fontawesome-webfont.woff2?v=4.7.0 повторился 2 раза
  ![fontawesome-webfont](./images/Screenshot_3.png)

- https://mp-events.mi.action-media.ru/user-recognition повторился 4 раза ( 2 раза с кодом 204 и 2 раза с 200)
  ![user-recognition](./images/Screenshot_4.png)

- cast_sender.js повторился 2 раза
  ![cast_sender](./images/Screenshot_5.png)

##### 1.2.2. Лишний размер ресурса

- На данной фотографии можно заметить, что присутсвуют js и css файлы, которые весят больше 100 kB. А также файл png, который весит много для картинки
  ![big_size](./images/Screenshot_6.png)

##### 1.2.3. Медленно загружающиеся ресурсы

- Можно заметить, что есть 3 запроса, которые завершили свою работу с ошибкой. Из них 2 были больше 2 секунд. Самое оптимальное время это примерно 1 секунда или меньше.
  ![bit_time](./images/Screenshot_7.png)

##### 1.2.4. Ресурсы, блокирующие загрузку

- Ресурсы, которые запустились до загрузки страницы.
  ![loading](./images/Screenshot_11.png)

##### 1.2.5. Дополнительно

- Запросы, которые закончились с ошибкой или были отменены.
  ![failed](./images/Screenshot_8.png)

- Запросы со статусом 302 из-за которых происходят лишние запросы и нагружают загрузку сайта.
  ![302](./images/Screenshot_9.png)

- Заблокированные запросы
  ![cors](./images/Screenshot_10.png)

---

### 2. На вкладке Perfomance

#### 2.1. Профиль загрузки страницы [JSON](./files/Trace-20230616T145622.json)

#### 2.2. Время в ms от начала навигация до событий FP, FCP, LCP, DCL и Load

- First Paint (FP) - 847.6 ms

  ![FP](./images/Screenshot_12.png)
  
- First Contentful Paint (FCP) - 847.6 ms

  ![FCP](./images/Screenshot_13.png)

- Largest Contentful Paint (LCP) - 7149.9 ms

  ![LCP](./images/Screenshot_14.png)
  
- DOM Content Loaded (DCL) - 6701.3 ms

  ![DCL](./images/Screenshot_15.png)
  
- Load - 31285.4 ms

  ![Load](./images/Screenshot_16.png)

#### 2.3. DOM-элемент на котором происходит LCP

- `<img loading="lazy" src="/images/branding/10/imageTop_1628667062.7856.jpg" data-url="/images/branding/10/imageTop_1628667062.7856.jpg" alt="-">`

![DOM](./images/Screenshot_17.png)

#### 2.4. Время в ms тратится на разные этапы обработки документа (Loading, Scripting, Rendering, Painting)

- Loading - 198 ms
- Scripting - 8320 ms
- Rendering - 224 ms
- Painting - 1039 ms

  ![AllTime](./images/Screenshot_18.png)

---

### 3. На вкладке Coverage

#### 3.1. Профиль загрузки страницы [JSON](./files/Coverage-20230616T152545.json)

![Coverage](./images/Screenshot_19.png)

#### 3.2. Объём неиспользованного CSS в ходе загрузки страницы

- 546 kB
  ![css](./images/Screenshot_20.png)

#### 3.3. Объём неиспользованного JS в ходе загрузки страницы

- 2600 kB
  ![js](./images/Screenshot_21.png)
