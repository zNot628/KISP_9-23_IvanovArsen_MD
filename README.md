## Как создать проект в Expo 
Expo - это структура React Native, которая облегчает разработку приложений для Android и iOS. Наша структура обеспечивает файловую маршрутизацию, стандартную библиотеку нативных модулей и многое другое. Expo - это открытый исходный код с активным сообществом на GitHub и Discord.

Мы также делаем Expo Application Services (EAS), набор услуг, которые дополняют структуру Expo на каждом этапе процесса разработки.

Начните с проекта по умолчанию

Рекомендуем начать с созданного по умолчанию проекта create-expo-app. Проект по умолчанию включает в себя пример кода, чтобы помочь вам начать работу.

Чтобы создать новый проект, выполните следующую команду:
> npx create-expo-app@latest

Вы можете выбрать другой шаблон, добавив --template опция.

Вместо проекта по умолчанию вы можете начать с одного из примеров Expo. Это небольшие приложения, каждое из которых демонстрирует определенную функцию или интеграцию, такие как Expo Router, Expo Widgets или экран камеры.

Чтобы просмотреть полный список и выбрать один в интерактивном режиме, запустите create-expo-app с --example 
Опция и отсутствие имени:
> npx create-expo-app@latest --example 

Чтобы создать известный пример напрямую, пропустите его имя:
> npx create-expo-app@latest --example with-widgets

## Настройка окружения 
Давайте создадим локальную среду разработки для запуска вашего проекта на Android и iOS.
Где бы вы хотели развиваться?

Мы рекомендуем использовать реальное устройство для разработки, так как вы сможете точно увидеть то, что увидят ваши пользователи.

## Начните разработку
**1. Запустите сервер разработки**

Чтобы запустить сервер разработки, выполните следующую команду:
> npx expo start

**2. Откройте приложение на вашем устройстве**

После выполнения команды выше вы увидите QR-код в вашем терминале. Отсканируйте этот QR-код, чтобы открыть приложение на вашем устройстве.

Если вы используете Android Emulator или iOS Simulator, вы можете нажать A или I Соответственно, чтобы открыть приложение.

**3. Сделайте свое первое изменение**

Откройте файл src/app/index.tsx в редакторе кода и внесите изменения.

     <ThemedView style={styles.heroSection}>
       <AnimatedIcon />
       <ThemedText type="title" style={styles.title}>
           Welcome to&nbsp;Expo
           Hello World!
       </ThemedText>
     </ThemedView> 

## Следующие шаги
Вот следующие шаги, чтобы продолжить создание вашего приложения:

**Сбросить свой проект**

Вы можете удалить код шаблона и начать все заново с новым проектом. Запустите следующую команду для сброса вашего проекта:
> npm run reset-project

Эта команда переместит существующие файлы в приложении в app-пример, а затем создаст новый каталог приложений с новым файлом index.tsx.

## Разработка, обзор и развертывание
Узнайте, как развиваться, читая документы в разделе «Разработка». Вы узнаете, как создавать элементы пользовательского интерфейса, добавлять модульные тесты, включать нативные модули и многое другое.

После того, как вы разработали свое приложение, вы можете поделиться им со своими товарищами по команде для обзора.

Наконец, вы можете создавать и отправлять свой проект в магазины приложений.

## Инструменты для развития
Когда вы создаете новый проект с Expo, изучение следующих основных инструментов и веб-сайтов может помочь вам во время вашего путешествия по разработке приложения. На этой странице представлен обзор списка рекомендуемых инструментов.

**Expo CLI**
Expo CLI является инструментом разработки и устанавливается автоматически с expo Пакет при создании нового проекта. Вы можете использовать его, используя npx (беседущий пакет Node.js).

Он предназначен для того, чтобы помочь вам быстрее двигаться на этапе разработки приложения. Например, ваше первое взаимодействие с Expo CLI - это запуск сервера разработки с запуском команды:
> npx expo start

В двух словах, Expo CLI позволяет вам разрабатывать, компилировать, запускать приложение и многое другое. 

## EAS CLI
EAS CLI используется для входа в вашу учетную запись Expo и компиляции вашего приложения с использованием различных услуг EAS, таких как сборка, обновление или отправка. Вы также можете использовать этот инструмент для:

* Опубликуйте свое приложение в магазинах приложений   
* Создайте разработку, предварительный просмотр или производственное тело вашего приложения  
* Создавайте обновления по воздуху (OTA)
* Управляйте своими учетными данными приложения  
* Создайте специальный профиль для устройства iOS

Чтобы использовать EAS CLI, вам необходимо установить его глобально на локальной машине, выполнив команду:
> npm install --global eas-cli

## Expo Doctor
Expo Doctor - это инструмент командной строки, используемый для диагностики проблем в вашем проекте Expo.  
Чтобы использовать его, запустите следующую команду в корневом каталоге вашего проекта:
> npx expo-doctor

Эта команда выполняет проверки и анализ кодовой базы вашего проекта на предмет общих проблем в файлах config и package.json, совместимости зависимостей, конфигурационных файлов и общего состояния проекта. Как только проверка завершена, Expo Doctor выведет результаты.

Если Expo Doctor находит проблему, он предоставляет описание проблемы вместе с советами о том, как ее исправить или где найти помощь.

По умолчанию Expo Doctor проверяет пакеты вашего проекта против Реагировать родной каталог и проверяет, правильно ли синхронизируются свойства конфигурирования приложения, когда существуют собственные каталоги. Вы можете настроить эти проверки в вашем проекте package.json Файл.

## Навигация в приложениях Expo и React Native
Базовая библиотека React Native не включает в себя встроенное навигационное решение, поэтому вы можете выбрать навигационную библиотеку, которая наилучшим образом соответствует вашим потребностям. Для приложений Expo и React Native это, как правило, выбор между React Navigation или Expo Router.

## Почему приложения React Native нуждаются в навигационной библиотеке
React Native main включает в себя основные компоненты пользовательского интерфейса, сенсорную обработку, API устройств и сетевое взаимодействие, но исключает, среди прочего, хранение, камеру, карты, большинство датчиков устройства и навигацию! Они предназначены для охвата общинных библиотек.

## React Navigation
React Navigation - это навигационная библиотека на основе компонентов, широко используемая в экосистеме React Native. Он позволяет полностью сочинять навигаторы стека, вкладки и ящика в коде, чтобы вы могли реализовывать сложные потоки, пользовательские переходы и шаблоны UX-специфических приложений.

Библиотека предлагает внешний вид и ощущение, специфичный для платформы, с плавной анимацией и жестами, унифицированной мобильной и веб-маршрутизацией, автоматическими глубокими ссылками, маршрутами типа со статической конфигурацией и очень настраиваемым.

## Expo Router (рекомендуется для проектов Expo)
Expo Router - это файловая библиотека маршрутизации для проектов Expo и React Native. Следуя конвенции каталога приложений, он превращает файлы в маршруты и интегрируется с Expo для Expo CLI и комплектации без дополнительной настройки. В библиотеке также добавлены такие функции, как набранные маршруты, динамические маршруты, ленивое сочетание в разработке, статический рендеринг для Интернета и автоматическое глубокое связывание.

## Использование React Native и Expo
Мы собираемся отправиться в путешествие по созданию универсальных приложений. В этом уроке мы создадим приложение Expo, которое работает на Android, iOS и веб-сайте; все с единой кодовой базой. Давайте начнем!

## О туториале React Native и Expo
Цель этого урока - начать с Expo и познакомиться с Expo SDK. Он будет охватывать следующие темы:  
* Создать приложение с помощью шаблона по умолчанию с включенным TypeJS
* Реализуйте двухэкранный макет нижних вкладок с помощью Expo Router
* Разбейте макет приложения и реализуйте его с помощью flexbox
* Используйте пользовательский интерфейс системы каждой платформы для выбора изображения из медиа-библиотеки
* Создайте модаль наклейки с помощью Modal и FlatList Компоненты от React Native
* Добавьте сенсорные жесты, чтобы взаимодействовать со стикером
* Используйте сторонние библиотеки, чтобы захватить скриншот и сохранить его на диске
* Обработка различий в платформе между Android, iOS и Web
* Наконец, пройдите процесс настройки панели состояния, экрана брызг и значка для завершения приложения.

Эти темы обеспечивают основу для изучения основ создания приложения Expo. Учебник является самостоятельным и может занять до двух часов.

Чтобы сохранить его для начинающих, мы разделили учебник на девять глав, чтобы вы могли следовать или положить его и вернуться к нему позже. Каждая глава содержит необходимые фрагменты кода для выполнения шагов, поэтому вы можете следовать за ним, создавая приложение с нуля или копировать и вставлять его.

## Как использовать этот туториал?
Мы верим в обучение, поэтому этот учебник подчеркивает, что делаем, а не объясняя. Вы можете следить за ходом создания приложения, создавая приложение с нуля.

На протяжении всего урока любой важный код или код, которые изменились между примерами, будут выделены зеленым цветом. Вы можете навести курсор на основные моменты (на рабочем столе) или нажать на них (на мобильном телефоне), чтобы узнать больше об изменении. Например, код, выделенный в фрагменте ниже, объясняет, что он делает:  
import { StyleSheet, Text, View } from 'react-native';  
export default function Index() {
  return (
    <View style={styles.container}>
      <Text>Hello world!</Text>
    </View>
  );
}  
const styles = StyleSheet.create({  
  container: {  
    flex: 1,  
    backgroundColor: '#fff',  
    alignItems: 'center',  
    justifyContent: 'center',  
  },  
});  

## Создайте свое первое приложение
В этой главе давайте узнаем, как создать новый проект Expo и как его запустить.

**1. Инициализировать новое приложение Expo**  
Мы будем использовать create-expo-app Инициализировать новое приложение Expo. Это командный инструмент для создания нового проекта React Native. Запустите следующую команду в вашем терминале:
> npx create-expo-app@latest StickerSmash  
Select an Expo SDK version > SDK 57  
cd StickerSmash

Эта команда создаст новый каталог проекта под названием StickerSmash, используя шаблон по умолчанию. Этот шаблон имеет необходимый шаблонный код и библиотеки, необходимые для создания нашего приложения, включая Expo Router, и позволяет нам тестировать наше приложение с помощью Expo Go, установленного на наших устройствах. Мы будем продолжать добавлять больше библиотек в этом уроке по мере необходимости.  
**2. Скачать активы**  
После загрузки архива:
* Расчистите архив и замените активы по умолчанию в your-project-name/assets/imagesкаталоге «Ваш-проект-имя/активы/изображения».
* Откройте каталог проекта в редакторе кода или IDE.

**3. Запустить сценарий сброса-проекта**  
В этом уроке мы создадим наше приложение с нуля и поймем основы добавления файловой навигации. Давайте запустим reset-project скрипт для удаления кода шаблона:
> npm run reset-project

После выполнения вышеуказанной команды в каталоге src/app осталось два файла (index.tsx и _layout.tsx). Предыдущие файлы из каталога src (включая componentsкомпоненты, константы и зацепки) перемещаются в диаграмму по сценарию. Мы создадим наши собственные каталоги и составные файлы по мере продвижения.

**4. Запуск приложения на мобильном и веб-сайте**  
В каталоге проекта запустите следующую команду для запуска сервера разработки с терминала:
> npx expo start

После выполнения вышеуказанной команды:
1. Завершится сервер разработки, и вы увидите QR-код внутри окна терминала.
2. Сканируйте этот QR-код, чтобы открыть приложение на устройстве. На Android используйте опцию Expo Go > Scan QR-кода. На iOS используйте приложение камеры по умолчанию.
3. Чтобы запустить веб-приложение, нажмите W В терминале. Он откроет веб-приложение в веб-браузере по умолчанию.

**5. Редактировать индексный экран**  
Этот src/app/index.tsx файл определяет текст, отображаемый на экране приложения. Это точка входа нашего приложения и выполняет, когда сервер разработки начинается. Он использует основные компоненты React Native, такие как View и Text для отображения фона и текста.  
Стили, применяемые к этим компонентам, используют объекты JavaScript, а не CSS, который используется в Интернете. Тем не менее, многие свойства будут выглядеть знакомыми, если вы ранее использовали CSS в Интернете. Большинство реагированных народные компоненты принимают style реквизит, который принимает объект JavaScript в качестве его значения.

Давайте изменим экран src/app/index.tsx:  
1. Импорт StyleSheet от react-native и создать a styles Возражает, чтобы определить наши пользовательские стили.
2. Добавить a styles.container.backgroundColor собственность для View с ценностью #25292e. Это меняет цвет фона.
3. Заменить значение по умолчанию Text с "Домашний экран".
4. Добавить a styles.text.color собственность для Text с ценностью #fff (белый) для изменения цвета текста.

## Основы Expo Router
Expo Router - это файловая система маршрутизации для React Native и веб-приложений. Он управляет навигацией между экранами и использует одни и те же компоненты на нескольких платформах. Чтобы начать работу, нам нужно знать о следующих конвенциях:
* **Каталог приложений:** Специальный каталог, содержащий только маршруты и их макеты. Любые файлы, добавленные в этот каталог, становятся экраном в нашем родном приложении и страницей в Интернете. В шаблоне по умолчанию он расположен в src/app.
* **Корневой макет:** файл src/app/_layout.tsx. Он определяет общие элементы пользовательского интерфейса, такие как заголовки и панели вкладок, чтобы они были согласованы между различными маршрутами.
* **Названия файлов Convention:** Индекс Файлы имен, такие как index.tsx, сопоставьте свой родительский каталог и не добавляйте сегмент пути. Например, к примеру, index.tsx Файл в src/приложение Справочник матчей / Маршрут.
* А маршрут Файл экспортирует компонент React в качестве его значения по умолчанию. Он может использовать любой .js, .jsx, .ts, или .tsx Расширение.
* Android, iOS и веб разделяют единую структуру навигации.

**1. Добавить новый экран в стек**  
Давайте создадим новый файл с именем о.tsx внутри src/приложение Каталог. Он отображает имя экрана, когда пользователь переходит к /about Маршрут.
```
import { Text, View, StyleSheet } from 'react-native';

export default function AboutScreen() {
  return (
    <View style={styles.container}>
      <Text style={styles.text}>About screen</Text>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    justifyContent: 'center',
    alignItems: 'center',
  },
  text: {
    color: '#fff',
  },
});
```
Внутри src/app/_layout.tsx :

    1. Добавить a <Stack.Screen /> Компонент и a options реквизит для обновления заголовка /about Маршрут.
    2. Обновить /index Название маршрута на Home путем добавления options Прокв.

```
import { Stack } from 'expo-router';

export default function RootLayout() {
  return (
    <Stack>
      <Stack.Screen name="index" options={{ title: 'Home' }} />
      <Stack.Screen name="about" options={{ title: 'About' }} />
    </Stack>
  );
}
```
**2. Навигация между экранами**  
Мы будем использовать Expo Router's Link компонент для навигации от /index Маршрут к /about Маршрут. Это компонент React, который отображает <Text> С данностью href Прокв.

    1. Импортировать Link компонент из expo-router внутри src/app/index.tsx.
    2. Добавить a Link компонент после <Text> компонент и пропуск href реквизит с /about Маршрут.
    3. Добавить стиль fontSize, textDecorationLine, и color к Link компонент. Он принимает тот же реквизит, что и <Text> компонент.

```
import { Text, View, StyleSheet } from 'react-native';
 import { Link } from 'expo-router'; 

export default function Index() {
  return (
    <View style={styles.container}>
      <Text style={styles.text}>Home screen</Text>
      <Link href="/about" style={styles.button}>
        Go to About screen
      </Link>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
    justifyContent: 'center',
  },
  text: {
    color: '#fff',
  },
  button: {
    fontSize: 20,
    textDecorationLine: 'underline',
    color: '#fff',
  },
});
```
**3. Добавить не найденный маршрут**  
Когда маршрут не существует, мы можем использовать +not-found Маршрут для отображения запасного экрана. Это полезно, когда мы хотим отобразить пользовательский экран при навигации по неверному маршруту на мобильном телефоне вместо того, чтобы сбивать приложение или отображать 404 Ошибка в Интернете. Экспо Роутер использует специальный +not-found.tsx файл для рассмотрения этого дела.

    1. Создать новый файл с именем +not-found.tsx внутри src/приложение Каталог для добавления NotFoundScreen компонент.
    2. Добавить options реквизит от Stack.Screen для отображения пользовательского заголовка экрана для этого маршрута.
    3. Добавить a Link Компонент для перехода к / Маршрут, который является нашим запасным маршрутом.

```
import { View, StyleSheet } from 'react-native';
import { Link, Stack } from 'expo-router';

export default function NotFoundScreen() {
  return (
    <>
      <Stack.Screen options={{ title: 'Oops! Not Found' }} />
      <View style={styles.container}>
        <Link href="/" style={styles.button}>
          Go back to Home screen!
        </Link>
      </View>
    </>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    justifyContent: 'center',
    alignItems: 'center',
  },

  button: {
    fontSize: 20,
    textDecorationLine: 'underline',
    color: '#fff',
  },
});
```
Чтобы проверить это, перейдите к http:localhost:8081/123 URL в веб-браузере, так как там легко изменить путь URL. Приложение должно отображать NotFoundScreen компонент.  
**4. Добавить навигатор нижней вкладки**  
Мы добавим навигатор нижней вкладки в наше приложение и повторно используем существующие экраны Home и About для создания макета вкладки (общий шаблон навигации во многих приложениях социальных сетей, таких как X или BlueSky). Мы также будем использовать навигатор стека в макете Root, так что +not-found маршрут отображается над любыми другими вложенными навигаторами.

    1. Внутри каталога src/app добавить (вкладки) подкаталог. Этот специальный каталог используется для группирования маршрутов вместе и отображения их в нижней строке вкладок.
    2. Создайте файл (tabs)/_layout.tsx внутри каталога. Он будет использоваться для определения макета вкладки, который отделен от макета Root.
Обновите файл макета Root, чтобы добавить a (tabs) Маршрут:
```
import { Stack } from 'expo-router';

export default function RootLayout() {
  return (
    <Stack>
      <Stack.Screen name="(tabs)" options={{ headerShown: false }} />
    </Stack>
  );
}
```
Внутри (таблицы)/_layout.tsx, добавить a Tabs компонент для определения макет нижней вкладки:
```
import { Tabs } from 'expo-router';

export default function TabLayout() {
  return (
    <Tabs>
      <Tabs.Screen name="index" options={{ title: 'Home' }} />
      <Tabs.Screen name="about" options={{ title: 'About' }} />
    </Tabs>
  );
}
```
**5. Установить @expo/vector-icons**  
Чтобы установить @expo/vector-icons библиотека, остановите сервер разработки, нажав Ctrl + C в терминале, затем запустить следующую команду:
> npx expo install @expo/vector-icons

После завершения установки запустите сервер разработки, запустив npx expo start.  
**6. Обновление нижнего вкладки навигатора**  
Прямо сейчас нижний навигатор вкладки выглядит одинаково на всех платформах, но не соответствует стилю нашего приложения. Например, панель вкладки или заголовок не отображает пользовательский значок, а цвет фоновой вкладки нижней части не соответствует цвету фона приложения.

Измените файл src/app/(tabs)/_layout.tsx, чтобы добавить значки панели вкладок:

    1. Импорт Ionicons Иконки набор из @expo/vector-icons — библиотека, включающая в себя популярные наборы значков.
    2. Добавить tabBarIcon для обоих index и about Маршруты. Эта функция принимает focused и color как парам и отображает компонент значка. Из набора иконок мы можем предоставить пользовательские имена значков.
    3. Добавить screenOptions.tabBarActiveTintColor к Tabs компонент и установить его значение для #ffd33d. Это изменит цвет значка икета вкладки и этикетку при активном.

```
import { Tabs } from 'expo-router';

import Ionicons from '@expo/vector-icons/Ionicons';


export default function TabLayout() {
  return (
    <Tabs
      screenOptions={{
        tabBarActiveTintColor: '#ffd33d',
      }}
    >
      <Tabs.Screen
        name="index"
        options={{
          title: 'Home',
          tabBarIcon: ({ color, focused }) => (
            <Ionicons name={focused ? 'home-sharp' : 'home-outline'} color={color} size={24} />
          ),
        }}
      />
      <Tabs.Screen
        name="about"
        options={{
          title: 'About',
          tabBarIcon: ({ color, focused }) => (
            <Ionicons name={focused ? 'information-circle' : 'information-circle-outline'} color={color} size={24}/>
          ),
        }}
      />
    </Tabs>
  );
}
```
Давайте также изменим цвет фона панели вкладок и заголовка с помощью screenOptions реквизит:
```
<Tabs
  screenOptions={{
    tabBarActiveTintColor: '#ffd33d',
    headerStyle: {
      backgroundColor: '#25292e',
    },
    headerShadowVisible: false,
    headerTintColor: '#fff',
    tabBarStyle: {
      backgroundColor: '#25292e',
    },
  }}
>
```
В вышеуказанном коде:

   * Предыстория заголовка установлена на #25292e с помощью headerStyle собственность. Мы также отключили тень заголовка, используя headerShadowVisible.
   * headerTintColor Применяется #fff к этикетке заголовка
   * tabBarStyle.backgroundColor Применяется #25292e к вкладке бар

## Создайте экран
На экране выше отображается изображение и две кнопки. Пользователь приложения может выбрать изображение с помощью одной из двух кнопок. Первая кнопка позволяет пользователю выбрать изображение со своего устройства. Вторая кнопка позволяет пользователю продолжать с изображением по умолчанию, предоставленным приложением.
Как только пользователь выбирает изображение, он может добавить к нему наклейку. Итак, давайте начнем создавать этот экран.  
**1. Разбейте экран**  
Прежде чем мы создадим этот экран, написав код, давайте разберем его на некоторые важные элементы.
Есть два основных элемента:

   * В центре экрана отображается большое изображение
   * В нижней половине экрана есть две кнопки

Первая кнопка содержит несколько компонентов. Основополагающий элемент обеспечивает желтую границу и содержит значок и текстовые компоненты внутри ряда.  
Теперь, когда мы разбили пользовательский интерфейс на более мелкие куски, мы готовы начать кодирование.  
**2. Отобразить изображение**  
Мы будем использовать `expo-image` библиотека для отображения изображения в приложении. Он обеспечивает кроссплатформенную `<Image>` компонент для загрузки и визуализации изображения. Он уже включен в шаблон проекта по умолчанию, который мы используем.

Компонент изображения берет источник изображения в качестве его значения. Источник может быть либо Статический актив или URL. Например, источник, необходимый от активы/изображения Каталог - это статично. Это также может быть от Сеть как а `uri` собственность.
Для использования компонента Изображения в src/app/(tabs)/index.tsx файл:

    1. Импорт Image от expo-image Библиотека.
    2. Создать a PlaceholderImage переменная для использования активы/images/background-image.png файл как source Опора на Image компонент.

```
import { View, StyleSheet } from 'react-native';
 import { Image } from 'expo-image'; 


const PlaceholderImage = require('@/assets/images/background-image.png');


export default function Index() {
  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <Image source={PlaceholderImage} style={styles.image} />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  image: {
    width: 320,
    height: 440,
    borderRadius: 18,
  },
});
```
**3. Разделить компоненты на файлы**  
Давайте разделим код на несколько файлов, так как мы добавляем больше компонентов на этот экран. На протяжении всего этого урока мы будем использовать каталог компонентов для создания пользовательских компонентов.

    1. Создайте каталог компонентов внутри src, а внутри него создайте файл image-viewer.tsx.
    2. Переместить код, чтобы отобразить изображение в этом файле вместе с image Стили.

```
import { ImageSourcePropType, StyleSheet } from 'react-native';
import { Image } from 'expo-image';

type Props = {
  imgSource: ImageSourcePropType;
};

export default function ImageViewer({ imgSource }: Props) {
  return <Image source={imgSource} style={styles.image} />;
}

const styles = StyleSheet.create({
  image: {
    width: 320,
    height: 440,
    borderRadius: 18,
  },
});
```
Импорт `ImageViewer` и использовать его в src/app/(tabs)/index.tsx:
```
import { StyleSheet, View } from 'react-native';

import ImageViewer from '@/components/image-viewer'; 

const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
});
```
**4. Создать кнопки с помощью прессов**  
React Native включает в себя несколько различных компонентов для обработки сенсорных событий, но `<Pressable>` Рекомендуется для его гибкости. Он может обнаруживать отдельные нажатия, длинные нажатия, срабатывать отдельные события, когда кнопка нажимается и освобождается, и многое другое.

В дизайне есть две кнопки, которые нам нужно создать. Каждый из них имеет свой стиль и этикетку. Давайте начнем с создания многоразового компонента для этих кнопок. Создайте файл button.tsx внутри каталога src/components с помощью следующего кода:
```
import { StyleSheet, View, Pressable, Text } from 'react-native';

type Props = {
  label: string;
};

export default function Button({ label }: Props) {
  return (
    <View style={styles.buttonContainer}>
      <Pressable style={styles.button} onPress={() => alert('You pressed a button.')}>
        <Text style={styles.buttonLabel}>{label}</Text>
      </Pressable>
    </View>
  );
}

const styles = StyleSheet.create({
  buttonContainer: {
    width: 320,
    height: 68,
    marginHorizontal: 20,
    alignItems: 'center',
    justifyContent: 'center',
    padding: 3,
  },
  button: {
    borderRadius: 10,
    width: '100%',
    height: '100%',
    alignItems: 'center',
    justifyContent: 'center',
    flexDirection: 'row',
  },
  buttonLabel: {
    color: '#fff',
    fontSize: 16,
  },
});
```
Приложение отображает оповещение, когда пользователь нажимает любую из кнопок на экране. Это происходит потому, что <Pressable> звонки alert() на его onPress Прокв. Давайте импортируем этот компонент в src/app/(tabs)/index.tsx файл и добавить стили для <View> которые инкапсулируют эти кнопки:
```
import { View, StyleSheet } from 'react-native';

import Button from '@/components/button'; 
import ImageViewer from '@/components/image-viewer';

const PlaceholderImage = require("@/assets/images/background-image.png");

export default function Index() {
  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} />
      </View>
      <View style={styles.footerContainer}>
        <Button label="Choose a photo" />
        <Button label="Use this photo" />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
});
```
**5. Улучшить многоразовый компонент кнопки**  
Кнопка «Выберите фотографию» требует другого стиля, чем кнопка «Использовать эту фотографию», поэтому мы добавим новый реквизит кнопки, который позволит нам применять `primary` Тема. Эта кнопка также имеет иконку перед этикеткой. Мы будем использовать иконку из `@expo/vector-icons` Библиотека.

Чтобы загрузить и отобразить значок на кнопке, давайте использовать `FontAwesome` Из библиотеки. Изменить src/components/button.tsx для добавления следующего фрагмента кода:
```
import { StyleSheet, View, Pressable, Text } from 'react-native';
import FontAwesome from '@expo/vector-icons/FontAwesome';

type Props = {
  label: string;
  theme?: 'primary';
};

export default function Button({ label, theme }: Props) {
  if (theme === 'primary') {
    return (
      <View
        style={[
          styles.buttonContainer,
          { borderWidth: 4, borderColor: '#ffd33d', borderRadius: 18 },
        ]}>
        <Pressable
          style={[styles.button, { backgroundColor: '#fff' }]}
          onPress={() => alert('You pressed a button.')}>
          <FontAwesome name="picture-o" size={18} color="#25292e" style={styles.buttonIcon} />
          <Text style={[styles.buttonLabel, { color: '#25292e' }]}>{label}</Text>
        </Pressable>
      </View>
    );
  }

  return (
    <View style={styles.buttonContainer}>
      <Pressable style={styles.button} onPress={() => alert('You pressed a button.')}>
        <Text style={styles.buttonLabel}>{label}</Text>
      </Pressable>
    </View>
  );
}

const styles = StyleSheet.create({
  buttonContainer: {
    width: 320,
    height: 68,
    marginHorizontal: 20,
    alignItems: 'center',
    justifyContent: 'center',
    padding: 3,
  },
  button: {
    borderRadius: 10,
    width: '100%',
    height: '100%',
    alignItems: 'center',
    justifyContent: 'center',
    flexDirection: 'row',
  },
  buttonIcon: {
    paddingRight: 8,
  },
  buttonLabel: {
    color: '#fff',
    fontSize: 16,
  },
});
```
Давайте узнаем, что делает вышеприведенный код:

   * Кнопка основной темы использует винные стили, который переопределяет стили, определенные в StyleSheet.create() с предметом, непосредственно переданным в style Прокв.
   * The `<Pressable>` компонент в первичной теме использует backgroundColor Собственность со значением #fff чтобы установить фон кнопки на белый. Если мы добавим это свойство к styles.button, значение цвета фона будет установлено как для основной темы, так и для нестилейной.
   * Встроенные стили используют JavaScript и переопределяют стили по умолчанию для определенного значения.

А теперь, измените src/app/(tabs)/index.tsx файл для использования theme="primary" Реквизит на первой кнопке.
```
import { View, StyleSheet } from 'react-native';

import Button from '@/components/button';
import ImageViewer from '@/components/image-viewer';

const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} />
      </View>
      <View style={styles.footerContainer}>
        <Button theme="primary" label="Choose a photo" />
        <Button label="Use this photo" />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
});
```
## Использовать сборщик изображений
React Native обеспечивает встроенные компоненты в качестве стандартных строительных блоков, таких как `<View>`, `<Text>`, и `<Pressable>`. Мы создаем функцию, чтобы выбрать изображение из медиа-галереи устройства. Это невозможно с основными компонентами, и нам понадобится библиотека, чтобы добавить эту функцию в наше приложение.
Мы будем использовать `expo-image-picker` Библиотека от Expo SDK.  
**1. Установить expo-image-Picker**  
Чтобы установить `expo-image-picker` библиотека, остановите сервер разработки, нажав Ctrl + C в терминале, затем запустить следующую команду:
> npx expo install expo-image-picker

The `npx expo install` команда установит библиотеку и добавит ее в зависимости проекта в package.json.  
**2. Выберите изображение из медиа-библиотеки устройства**
`expo-image-picker` обеспечивает `launchImageLibraryAsync()` способ отображения пользовательского интерфейса системы путем выбора изображения или видео из медиа-библиотеки устройства. Мы будем использовать основную тематическую кнопку, созданную в предыдущей главе, чтобы выбрать изображение из медиа-библиотеки устройства и создать функцию для запуска библиотеки изображений устройства для реализации этой функции.

В src/app/(tabs)/index.tsx, импорт `expo-image-picker` библиотека и создать `pickImageAsync()` Функция внутри Index компонент:
```
// ...rest of the import statements remain unchanged
 import * as ImagePicker from 'expo-image-picker';

export default function Index() {
  const pickImageAsync = async () => {
    let result = await ImagePicker.launchImageLibraryAsync({
      mediaTypes: ['images'],
      allowsEditing: true,
      quality: 1,
    });

    if (!result.canceled) {
      console.log(result);
    } else {
      alert('You did not select any image.');
    }
  };

  // ...rest of the code remains same
}
```
Давайте узнаем, что делает вышеприведенный код:

   * The launchImageLibraryAsync() принимает объект для указания различных опций. Этот объект является ImagePickerOptions объект, который мы передаем при вызове метода.
   * Когда allowsEditing настроено на true, пользователь может обрезать изображение во время процесса выбора на Android и iOS.

**3. Обновите компонент кнопки**  
При нажатии основной кнопки мы позвоним `pickImageAsync()` Функция на `Button` компонент. Обновить `onPress` реквизит The `Button` компонент в src/components/button.tsx:
```
import { StyleSheet, View, Pressable, Text } from 'react-native';
import FontAwesome from '@expo/vector-icons/FontAwesome';

type Props = {
  label: string;
  theme?: 'primary';
  onPress?: () => void;
};

export default function Button({ label, theme, onPress }: Props) {
  if (theme === 'primary') {
    return (
      <View
        style={[
          styles.buttonContainer,
          { borderWidth: 4, borderColor: '#ffd33d', borderRadius: 18 },
        ]}>
        <Pressable style={[styles.button, { backgroundColor: '#fff' }]} onPress={onPress}>
          <FontAwesome name="picture-o" size={18} color="#25292e" style={styles.buttonIcon} />
          <Text style={[styles.buttonLabel, { color: '#25292e' }]}>{label}</Text>
        </Pressable>
      </View>
    );
  }

  return (
    <View style={styles.buttonContainer}>
      <Pressable style={styles.button} onPress={() => alert('You pressed a button.')}>
        <Text style={styles.buttonLabel}>{label}</Text>
      </Pressable>
    </View>
  );
}

const styles = StyleSheet.create({
  buttonContainer: {
    width: 320,
    height: 68,
    marginHorizontal: 20,
    alignItems: 'center',
    justifyContent: 'center',
    padding: 3,
  },
  button: {
    borderRadius: 10,
    width: '100%',
    height: '100%',
    alignItems: 'center',
    justifyContent: 'center',
    flexDirection: 'row',
  },
  buttonIcon: {
    paddingRight: 8,
  },
  buttonLabel: {
    color: '#fff',
    fontSize: 16,
  },
});
```
В src/app/(tabs)/index.tsx, добавить `pickImageAsync()` Функция для onPress реквизит на первом `<Button>`.
```
import { View, StyleSheet } from 'react-native';
import * as ImagePicker from 'expo-image-picker';

import Button from '@/components/button';
import ImageViewer from '@/components/image-viewer';

const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  const pickImageAsync = async () => {
    let result = await ImagePicker.launchImageLibraryAsync({
      mediaTypes: ['images'],
      allowsEditing: true,
      quality: 1,
    });

    if (!result.canceled) {
      console.log(result);
    } else {
      alert('You did not select any image.');
    }
  };

  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} />
      </View>
      <View style={styles.footerContainer}>
        <Button theme="primary" label="Choose a photo" onPress={pickImageAsync} />
        <Button label="Use this photo" />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
});
```
The `pickImageAsync()` Функции вызывают `ImagePicker`.`launchImageLibraryAsync()` А затем обрабатывает результат. The `launchImageLibraryAsync()` Способ возвращает объект, содержащий информацию о выбранном изображении.  
**4. Использовать выбранное изображение**  
The `result` Объект обеспечивает `assets` массив, который содержит `uri` Выбранное изображение. Давайте возьмем это значение из сборщика изображений и используем его, чтобы показать выбранное изображение в приложении.

Изменить файл src/app/(tbs)/index.tsx:

    1. Объявить переменную состояния, называемую selectedImage с помощью useState Крюк от React. Мы будем использовать эту переменную состояния для удержания URI выбранного изображения.
    2. Обновить pickImageAsync() функция для сохранения изображения URI в selectedImage Переменная состояния.
    3. Пройти selectedImage В качестве опоры для ImageViewer компонент.

```
import { View, StyleSheet } from 'react-native';
import * as ImagePicker from 'expo-image-picker';

import { useState } from 'react';


import Button from '@/components/button';
import ImageViewer from '@/components/image-viewer';

const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  const [selectedImage, setSelectedImage] = useState<string | undefined>(undefined);

  const pickImageAsync = async () => {
    let result = await ImagePicker.launchImageLibraryAsync({
      mediaTypes: ['images'],
      allowsEditing: true,
      quality: 1,
    });

    if (!result.canceled) {
      setSelectedImage(result.assets[0].uri);
    } else {
      alert('You did not select any image.');
    }
  };

  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} selectedImage={selectedImage} />
      </View>
      <View style={styles.footerContainer}>
        <Button theme="primary" label="Choose a photo" onPress={pickImageAsync} />
        <Button label="Use this photo" />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
});
```
Пройти `selectedImage` Опора для `ImageViewer` компонент для отображения выбранного изображения вместо образа заполнителя.

    1. Изменить src/components/image-viewer.tsx файл, чтобы принять selectedImage Прокв.
    2. Источник изображения становится длинным, поэтому давайте также переместим его в отдельную переменную, называемую imageSource.
    3. Пропуск imageSource как ценность source Опора на Image компонент.

```
import { ImageSourcePropType, StyleSheet } from 'react-native';
import { Image } from 'expo-image';

type Props = {
  imgSource: ImageSourcePropType;
  selectedImage?: string;
};

export default function ImageViewer({ imgSource, selectedImage }: Props) {
  const imageSource = selectedImage ? { uri: selectedImage } : imgSource;

  return <Image source={imageSource} style={styles.image} />;
}

const styles = StyleSheet.create({
  image: {
    width: 320,
    height: 440,
    borderRadius: 18,
  },
});
```
В приведенном выше фрагменте компонент Изображение использует условный оператор для загрузки источника изображения. Выбранное изображение является `uri` Струнные, не локальный актив, как изображение заполнителя.

## Создать модаль
React Native предоставляет `<Modal>` компонент Это представляет контент выше остальной части вашего приложения. В общем, модаль используются, чтобы привлечь внимание пользователя к критической информации или направить их на принятие мер. Например, в Третья глава, после нажатия кнопки, мы использовали `alert()` для отображения текста заполнителя. Вот как модальный компонент отображает наложение.

В этой главе мы создадим модаль, который показывает список сборщиков смайликов.
**1. Объявить переменную состояния для отображения кнопок**  
Перед реализацией модала мы собираемся добавить три новые кнопки. Эти кнопки видны после того, как пользователь выбирает изображение из медиа-библиотеки или использует образ заполнителя. Одна из этих кнопок запустит модаль сборщика смайликов.

В src/app/(tbs)/index.tsx :

    1. Объявить переменную булева состояния, showAppOptions, чтобы показать или скрыть кнопки, которые открывают модаль, наряду с несколькими другими вариантами. Когда экран приложения загружается, мы настроим его false Таким образом, опции не отображаются перед выбором изображения. Когда пользователь выбирает изображение или использует образ заполнителя, мы установим его true.
    2. Обновить pickImageAsync() функция для установления значения showAppOptions к true После того, как пользователь выбирает изображение.
    3. Обновите кнопку без темы, добавив onPress реквизит со следующим значением.
```
import { View, StyleSheet } from 'react-native';
import * as ImagePicker from 'expo-image-picker';
import { useState } from 'react';

import Button from '@/components/button';
import ImageViewer from '@/components/image-viewer';

const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  const [selectedImage, setSelectedImage] = useState<string | undefined>(undefined);
  const [showAppOptions, setShowAppOptions] = useState<boolean>(false);

  const pickImageAsync = async () => {
    let result = await ImagePicker.launchImageLibraryAsync({
      mediaTypes: ['images'],
      allowsEditing: true,
      quality: 1,
    });

    if (!result.canceled) {
      setSelectedImage(result.assets[0].uri);
      setShowAppOptions(true);
    } else {
      alert('You did not select any image.');
    }
  };

  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} selectedImage={selectedImage} />
      </View>
      {showAppOptions ? (
        <View />
      ) : (
        <View style={styles.footerContainer}>
          <Button theme="primary" label="Choose a photo" onPress={pickImageAsync} />
          <Button label="Use this photo" onPress={() => setShowAppOptions(true)} />
        </View>
      )}
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
});
```
В приведенном выше фрагменте мы передаем `Button` Компонент, основанный на значении `showAppOptions` и перемещение кнопок в блоке оператора тернарма. Когда ценность `showAppOptions` является true, сделать пустым `<View>` компонент. Мы обратимся к этому государству на следующем шаге.

Теперь мы можем удалить `alert` на `Button` компонент и обновление `onPress` реквизит при рендеринге второй кнопки в src/components/button.tsx:
```
<Pressable style={styles.button}  onPress={onPress}>
```
**2. Добавить кнопки**  
Давайте разберем макет кнопок опции, которые мы будем реализовывать в этой главе.
В нем содержится родительский `<View>` с тремя кнопками, выровненными в ряд. Кнопка в середине с значком плюс (+) откроет модаль и стилизована иначе, чем две другие кнопки.

Внутри каталога src/components создайте новый файл circle-button.tsx со следующим кодом:
```
import { View, Pressable, StyleSheet } from 'react-native';
import MaterialIcons from '@expo/vector-icons/MaterialIcons';

type Props = {
  onPress: () => void;
};

export default function CircleButton({ onPress }: Props) {
  return (
    <View style={styles.circleButtonContainer}>
      <Pressable style={styles.circleButton} onPress={onPress}>
        <MaterialIcons name="add" size={38} color="#25292e" />
      </Pressable>
    </View>
  );
}

const styles = StyleSheet.create({
  circleButtonContainer: {
    width: 84,
    height: 84,
    marginHorizontal: 60,
    borderWidth: 4,
    borderColor: '#ffd33d',
    borderRadius: 42,
    padding: 3,
  },
  circleButton: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    borderRadius: 42,
    backgroundColor: '#fff',
  },
});
```
Чтобы отобразить значок плюс, эта кнопка использует `<MaterialIcons>` Иконный набор из `@expo/vector-icons` Библиотека.

Две другие кнопки также используют `<MaterialIcons>` для отображения вертикально выровненных текстовых меток и значков. Создать именованный файл icon-button.tsx внутри src/компоненты Каталог. Этот компонент принимает три реквизита:

   * icon: имя, соответствующее MaterialIcons Икона библиотеки.
   * label: текстовая этикетка, отображаемая на кнопке.
   * onPress: эта функция вызывает, когда пользователь нажимает кнопку.

```
import { Pressable, StyleSheet, Text } from 'react-native';
import MaterialIcons from '@expo/vector-icons/MaterialIcons';

type Props = {
  icon: keyof typeof MaterialIcons.glyphMap;
  label: string;
  onPress: () => void;
};

export default function IconButton({ icon, label, onPress }: Props) {
  return (
    <Pressable style={styles.iconButton} onPress={onPress}>
      <MaterialIcons name={icon} size={24} color="#fff" />
      <Text style={styles.iconButtonLabel}>{label}</Text>
    </Pressable>
  );
}

const styles = StyleSheet.create({
  iconButton: {
    justifyContent: 'center',
    alignItems: 'center',
  },
  iconButtonLabel: {
    color: '#fff',
    marginTop: 12,
  },
});
```
Внутренний src/app/(tbs)/index.tsx :

    1. Импортировать CircleButton и IconButton Компоненты для их отображения.
    2. Добавьте три функции заполнителя для этих кнопок. The onReset() функции вызывают, когда пользователь нажимает кнопку сброса, в результате чего кнопка выбора изображения снова появляется. Мы добавим функциональность для двух других функций позже.
```
import { View, StyleSheet } from 'react-native';
import * as ImagePicker from 'expo-image-picker';
import { useState } from 'react';

import Button from '@/components/button';
import ImageViewer from '@/components/image-viewer';

import IconButton from '@/components/icon-button';
import CircleButton from '@/components/circle-button';


const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  const [selectedImage, setSelectedImage] = useState<string | undefined>(undefined);
  const [showAppOptions, setShowAppOptions] = useState<boolean>(false);

  const pickImageAsync = async () => {
    let result = await ImagePicker.launchImageLibraryAsync({
      mediaTypes: ['images'],
      allowsEditing: true,
      quality: 1,
    });

    if (!result.canceled) {
      setSelectedImage(result.assets[0].uri);
      setShowAppOptions(true);
    } else {
      alert('You did not select any image.');
    }
  };

  const onReset = () => {
    setShowAppOptions(false);
  };

  const onAddSticker = () => {
    // we will implement this later
  };

  const onSaveImageAsync = async () => {
    // we will implement this later
  };

  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} selectedImage={selectedImage} />
      </View>
      {showAppOptions ? (
        <View style={styles.optionsContainer}>
          <View style={styles.optionsRow}>
            <IconButton icon="refresh" label="Reset" onPress={onReset} />
            <CircleButton onPress={onAddSticker} />
            <IconButton icon="save-alt" label="Save" onPress={onSaveImageAsync} />
          </View>
        </View>
      ) : (
        <View style={styles.footerContainer}>
          <Button theme="primary" label="Choose a photo" onPress={pickImageAsync} />
          <Button label="Use this photo" onPress={() => setShowAppOptions(true)} />
        </View>
      )}
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
  optionsContainer: {
    position: 'absolute',
    bottom: 80,
  },
  optionsRow: {
    alignItems: 'center',
    flexDirection: 'row',
  },
});
```
**3. Создать модаль сборщика смайликов**  
Модаль позволяет пользователю выбрать эмодзи из списка доступных эмодзи. Создайте файл **emoji-picker.tsx** внутри каталога src/components. Этот компонент принимает три реквизита:

   * isVisible: бульон для определения состояния видимости модала.
   * onClose: функция, чтобы закрыть модаль.
   * children: используется позже для отображения списка эмодзи.
```
import { Modal, View, Text, Pressable, StyleSheet } from 'react-native';
import { PropsWithChildren } from 'react';
import MaterialIcons from '@expo/vector-icons/MaterialIcons';

type Props = PropsWithChildren<{
  isVisible: boolean;
  onClose: () => void;
}>;

export default function EmojiPicker({ isVisible, children, onClose }: Props) {
  return (
    <View>
      <Modal animationType="slide" transparent={true} visible={isVisible}>
        <View style={styles.modalContent}>
          <View style={styles.titleContainer}>
            <Text style={styles.title}>Choose a sticker</Text>
            <Pressable onPress={onClose}>
              <MaterialIcons name="close" color="#fff" size={22} />
            </Pressable>
          </View>
          {children}
        </View>
      </Modal>
    </View>
  );
}

const styles = StyleSheet.create({
  modalContent: {
    height: '25%',
    width: '100%',
    backgroundColor: '#25292e',
    borderTopRightRadius: 18,
    borderTopLeftRadius: 18,
    position: 'absolute',
    bottom: 0,
  },
  titleContainer: {
    height: '16%',
    backgroundColor: '#464C55',
    borderTopRightRadius: 10,
    borderTopLeftRadius: 10,
    paddingHorizontal: 20,
    flexDirection: 'row',
    alignItems: 'center',
    justifyContent: 'space-between',
  },
  title: {
    color: '#fff',
    fontSize: 16,
  },
});
```
Давайте узнаем, что делает вышеприведенный код:

   * The <Modal> Компонент отображает заголовок и кнопку закрытия.
   * Его visible реквизит принимает ценность isVisible и контролирует, открыт или закрыто модаль.
   * Его transparent реквизит - это булевое значение, которое определяет, заполняет ли модаль весь вид.
   * Его animationType реквизит определяет, как он входит и покидает экран. В этом случае он скользит из нижней части экрана.
   * И, наконец, <EmojiPicker> Призывает onClose реквизит, когда пользователь нажимает на близкое <Pressable>.

Теперь давайте изменим src/app/(tabs)/index.tsx :

    1. Импортировать <EmojiPicker> компонент.
    2. Создать a isModalVisible переменная состояния с useState Крюк. Его значение по умолчанию является false, который скрывает модаль, пока пользователь не нажмет кнопку, чтобы открыть его.
    3. Заменить комментарий в onAddSticker() функция для обновления isModalVisible переменная для true когда пользователь нажимает кнопку. Это откроет сборщик смайликов.
    4. Создать onModalClose() функция для обновления isModalVisible Переменная состояния.
    5. Поместите The <EmojiPicker> Компонент в нижней части Index компонент.
```
import { View, StyleSheet } from 'react-native';
import * as ImagePicker from 'expo-image-picker';
import { useState } from 'react';

import Button from '@/components/button';
import ImageViewer from '@/components/image-viewer';
import IconButton from '@/components/icon-button';
import CircleButton from '@/components/circle-button';

import EmojiPicker from '@/components/emoji-picker';


const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  const [selectedImage, setSelectedImage] = useState<string | undefined>(undefined);
  const [showAppOptions, setShowAppOptions] = useState<boolean>(false);
  const [isModalVisible, setIsModalVisible] = useState<boolean>(false);

  const pickImageAsync = async () => {
    let result = await ImagePicker.launchImageLibraryAsync({
      mediaTypes: ['images'],
      allowsEditing: true,
      quality: 1,
    });

    if (!result.canceled) {
      setSelectedImage(result.assets[0].uri);
      setShowAppOptions(true);
    } else {
      alert('You did not select any image.');
    }
  };

  const onReset = () => {
    setShowAppOptions(false);
  };

  const onAddSticker = () => {
    setIsModalVisible(true);
  };

  const onModalClose = () => {
    setIsModalVisible(false);
  };

  const onSaveImageAsync = async () => {
    // we will implement this later
  };

  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} selectedImage={selectedImage} />
      </View>
      {showAppOptions ? (
        <View style={styles.optionsContainer}>
          <View style={styles.optionsRow}>
            <IconButton icon="refresh" label="Reset" onPress={onReset} />
            <CircleButton onPress={onAddSticker} />
            <IconButton icon="save-alt" label="Save" onPress={onSaveImageAsync} />
          </View>
        </View>
      ) : (
        <View style={styles.footerContainer}>
          <Button theme="primary" label="Choose a photo" onPress={pickImageAsync} />
          <Button label="Use this photo" onPress={() => setShowAppOptions(true)} />
        </View>
      )}
      <EmojiPicker isVisible={isModalVisible} onClose={onModalClose}>
        {/* Emoji list component will go here */}
      </EmojiPicker>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
  optionsContainer: {
    position: 'absolute',
    bottom: 80,
  },
  optionsRow: {
    alignItems: 'center',
    flexDirection: 'row',
  },
});
```
**4. Показать список смайликов**  
Давайте добавим горизонтальный список эмодзи в содержимое модала. Мы будем использовать <FlatList> Компонент от React Native для него.

Создайте файл emoji-list.tsx в каталоге src/components и добавьте следующий код:
```
import { useState } from 'react';
import { ImageSourcePropType, StyleSheet, FlatList, Platform, Pressable } from 'react-native';
import { Image } from 'expo-image';

type Props = {
  onSelect: (image: ImageSourcePropType) => void;
  onCloseModal: () => void;
};

export default function EmojiList({ onSelect, onCloseModal }: Props) {
  const [emoji] = useState<ImageSourcePropType[]>([
    require("@/assets/images/emoji1.png"),
    require("@/assets/images/emoji2.png"),
    require("@/assets/images/emoji3.png"),
    require("@/assets/images/emoji4.png"),
    require("@/assets/images/emoji5.png"),
    require("@/assets/images/emoji6.png"),
  ]);

  return (
    <FlatList
      horizontal
      showsHorizontalScrollIndicator={Platform.OS === 'web'}
      data={emoji}
      contentContainerStyle={styles.listContainer}
      renderItem={({ item, index }) => (
        <Pressable
          onPress={() => {
            onSelect(item);
            onCloseModal();
          }}>
          <Image source={item} key={index} style={styles.image} />
        </Pressable>
      )}
    />
  );
}

const styles = StyleSheet.create({
  listContainer: {
    borderTopRightRadius: 10,
    borderTopLeftRadius: 10,
    paddingHorizontal: 20,
    flexDirection: 'row',
    alignItems: 'center',
    justifyContent: 'space-between',
  },
  image: {
    width: 100,
    height: 100,
    marginRight: 20,
  },
});
```
Давайте узнаем, что делает вышеприведенный код:

   * The <FlatList> Компонент выше отображает все изображения эмодзи, используя Image компонент, обернутый a <Pressable>. Позже мы улучшим его, чтобы пользователь мог нажать смайлик на экране, чтобы он выглядел как наклейка на изображении.
   * Он также принимает множество предметов, предоставленных emoji Переменная массива как значение data Прокв. The renderItem реквизит берет предмет из data и возвращает пункт в списке. Наконец, мы добавили Image и <Pressable> Компоненты для отображения этого элемента.
   * The horizontal реквизит отображает список горизонтально, а не вертикально. The showsHorizontalScrollIndicator использует React Native's Platform модуль для проверки значения и отображения горизонтальной полосы прокрутки в Интернете.

Теперь обновите src/app/(tabs)/index.tsx Чтобы импортировать <EmojiList> компонент и замена комментариев внутри <EmojiPicker> компонент со следующим фрагментом кода:
```
import { ImageSourcePropType, View, StyleSheet } from 'react-native';
import * as ImagePicker from 'expo-image-picker';
import { useState } from 'react';

import Button from '@/components/button';
import ImageViewer from '@/components/image-viewer';
import IconButton from '@/components/icon-button';
import CircleButton from '@/components/circle-button';
import EmojiPicker from '@/components/emoji-picker';

import EmojiList from '@/components/emoji-list';


const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  const [selectedImage, setSelectedImage] = useState<string | undefined>(undefined);
  const [showAppOptions, setShowAppOptions] = useState<boolean>(false);
  const [isModalVisible, setIsModalVisible] = useState<boolean>(false);
  const [pickedEmoji, setPickedEmoji] = useState<ImageSourcePropType | undefined>(undefined);

  const pickImageAsync = async () => {
    let result = await ImagePicker.launchImageLibraryAsync({
      mediaTypes: ['images'],
      allowsEditing: true,
      quality: 1,
    });

    if (!result.canceled) {
      setSelectedImage(result.assets[0].uri);
      setShowAppOptions(true);
    } else {
      alert('You did not select any image.');
    }
  };

  const onReset = () => {
    setShowAppOptions(false);
  };

  const onAddSticker = () => {
    setIsModalVisible(true);
  };

  const onModalClose = () => {
    setIsModalVisible(false);
  };

  const onSaveImageAsync = async () => {
    // we will implement this later
  };

  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} selectedImage={selectedImage} />
      </View>
      {showAppOptions ? (
        <View style={styles.optionsContainer}>
          <View style={styles.optionsRow}>
            <IconButton icon="refresh" label="Reset" onPress={onReset} />
            <CircleButton onPress={onAddSticker} />
            <IconButton icon="save-alt" label="Save" onPress={onSaveImageAsync} />
          </View>
        </View>
      ) : (
        <View style={styles.footerContainer}>
          <Button theme="primary" label="Choose a photo" onPress={pickImageAsync} />
          <Button label="Use this photo" onPress={() => setShowAppOptions(true)} />
        </View>
      )}
      <EmojiPicker isVisible={isModalVisible} onClose={onModalClose}>
        <EmojiList onSelect={setPickedEmoji} onCloseModal={onModalClose} />
      </EmojiPicker>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
  optionsContainer: {
    position: 'absolute',
    bottom: 80,
  },
  optionsRow: {
    alignItems: 'center',
    flexDirection: 'row',
  },
});
```
В `EmojiList` компонент, `onSelect` реквизит выбирает эмодзи и после его выбора, onCloseModal Закрывает модаль.  
**5. Отобразить выбранный emoji**
Теперь мы поместим наклейку смайлика на изображение. Создайте новый файл в каталоге src/components и назовите его emoji-sticker.tsx. Затем добавьте следующий код:
```
import { ImageSourcePropType, View } from 'react-native';
import { Image } from 'expo-image';

type Props = {
  imageSize: number;
  stickerSource: ImageSourcePropType;
};

export default function EmojiSticker({ imageSize, stickerSource }: Props) {
  return (
    <View style={{ top: -350 }}>
      <Image source={stickerSource} style={{ width: imageSize, height: imageSize }} />
    </View>
  );
}
```
Этот компонент получает два реквизита:

   * imageSize: значение, определенное внутри Index компонент. Мы будем использовать это значение в следующей главе, чтобы масштабировать размер изображения при нажатии.
   * stickerSource: Источник выбранного изображения эмодзи.

Импортировать этот компонент в src/app/(tabs)/index.tsx Файл и обновить Index компонент для отображения наклейки emoji на изображении. Мы проверим, pickedEmoji Государство не является undefined:
```
import { ImageSourcePropType, View, StyleSheet } from 'react-native';
import * as ImagePicker from 'expo-image-picker';
import { useState } from 'react';

import Button from '@/components/button';
import ImageViewer from '@/components/image-viewer';
import IconButton from '@/components/icon-button';
import CircleButton from '@/components/circle-button';
import EmojiPicker from '@/components/emoji-picker';
import EmojiList from '@/components/emoji-list';
import EmojiSticker from '@/components/emoji-sticker';

const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  const [selectedImage, setSelectedImage] = useState<string | undefined>(undefined);
  const [showAppOptions, setShowAppOptions] = useState<boolean>(false);
  const [isModalVisible, setIsModalVisible] = useState<boolean>(false);
  const [pickedEmoji, setPickedEmoji] = useState<ImageSourcePropType | undefined>(undefined);


  const pickImageAsync = async () => {
    let result = await ImagePicker.launchImageLibraryAsync({
      mediaTypes: ['images'],
      allowsEditing: true,
      quality: 1,
    });

    if (!result.canceled) {
      setSelectedImage(result.assets[0].uri);
      setShowAppOptions(true);
    } else {
      alert('You did not select any image.');
    }
  };

  const onReset = () => {
    setShowAppOptions(false);
  };

  const onAddSticker = () => {
    setIsModalVisible(true);
  };

  const onModalClose = () => {
    setIsModalVisible(false);
  };

  const onSaveImageAsync = async () => {
    // we will implement this later
  };

  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} selectedImage={selectedImage} />
        {pickedEmoji && <EmojiSticker imageSize={40} stickerSource={pickedEmoji} />}
      </View>
      {showAppOptions ? (
        <View style={styles.optionsContainer}>
          <View style={styles.optionsRow}>
            <IconButton icon="refresh" label="Reset" onPress={onReset} />
            <CircleButton onPress={onAddSticker} />
            <IconButton icon="save-alt" label="Save" onPress={onSaveImageAsync} />
          </View>
        </View>
      ) : (
        <View style={styles.footerContainer}>
          <Button theme="primary" label="Choose a photo" onPress={pickImageAsync} />
          <Button label="Use this photo" onPress={() => setShowAppOptions(true)} />
        </View>
      )}
      <EmojiPicker isVisible={isModalVisible} onClose={onModalClose}>
        <EmojiList onSelect={setPickedEmoji} onCloseModal={onModalClose} />
      </EmojiPicker>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
  optionsContainer: {
    position: 'absolute',
    bottom: 80,
  },
  optionsRow: {
    alignItems: 'center',
    flexDirection: 'row',
  },
});
```

## Добавить жесты
Жесты - отличный способ обеспечить интуитивно понятный пользовательский опыт в приложении. Библиотека React Native Gesture Handler предоставляет встроенные нативные компоненты, которые могут обрабатывать жесты. Он распознает панорам, кран, вращение и другие жесты, используя нативную систему сенсорной обработки платформы. В этой главе мы добавим два разных жеста, используя эту библиотеку:

    Двойное нажатие, чтобы масштабировать размер наклейки emoji и уменьшить шкалу при двойном постукивании снова.
    Пан, чтобы переместить наклейку смайлика вокруг экрана, чтобы пользователь мог разместить наклейку в любом месте на изображении.

Мы также будем использовать Реанимированную библиотеку для анимации между состояниями жестов.  
**1. Добавить ЖестОбработчикРужникПросмотр**  
Чтобы получить взаимодействие жестов для работы в приложении, мы вернемся `<GestureHandlerRootView>` от react-native-gesture-handler на вершине Index компонент. Заменить уровень корней `<View>` компонент в src/app/(tabs)/index.tsx с `<GestureHandlerRootView>`.
```
// ... rest of the import statements remain same
import { GestureHandlerRootView } from 'react-native-gesture-handler';

export default function Index() {
  return (
    <GestureHandlerRootView style={styles.container}>
      {/* ...rest of the code remains */}
    </GestureHandlerRootView>
  )
}
```
**2. Используйте анимированные компоненты**  
А Animated Компонент смотрит на style реквизит компонента и определяет, какие значения анимировать и применять обновления для создания анимации. Реанимированный экспорт анимированных компонентов, таких как `<Animated.View>`, `<Animated.Text>`, или `<Animated.ScrollView>`. Мы будем применять анимацию к `<Animated.Image>` компонент, чтобы сделать двойной жест нажатия работает.

    1. Откройте emoji-sticker.tsx Файл в src/компоненты Каталог. Внутри него, импортировать Animated от react-native-reanimated библиотека для использования анимированных компонентов.
    2. Заменить Image компонент с <Animated.Image>.
```
import { ImageSourcePropType, View } from 'react-native';
import Animated from 'react-native-reanimated';

type Props = {
  imageSize: number;
  stickerSource: ImageSourcePropType;
};

export default function EmojiSticker({ imageSize, stickerSource }: Props) {
  return (
    <View style={{ top: -350 }}>
      <Animated.Image
        source={stickerSource}
        resizeMode="contain"
        style={{ width: imageSize, height: imageSize }}
      />
    </View>
  );
}
```
**3. Добавить жест нажатия**  
React Native Gesture Handler позволяет нам добавлять поведение, когда он обнаруживает сенсорный ввод, например, двойное нажатие.

В src/components/emioji-sticker.tsx файле:

    1. Импорт Gesture и GestureDetector от react-native-gesture-handler.
    2. Чтобы распознать кран на наклейке, импортируйте useAnimatedStyle, useSharedValue, и withSpring от react-native-reanimated чтобы оживить стиль <Animated.Image>.
    3. Внутри EmojiSticker компонент, создать ссылку, называемую scaleImage с помощью useSharedValue() Крюк. Это возьмет на себя ценность imageSize В качестве его первоначального значения.
```
// ...rest of the import statements remain same
import { Gesture, GestureDetector } from 'react-native-gesture-handler';
import Animated, { useAnimatedStyle, useSharedValue, withSpring } from 'react-native-reanimated';

export default function EmojiSticker({ imageSize, stickerSource }: Props) {
  const scaleImage = useSharedValue(imageSize);

  return (
    // ...rest of the code remains same
  )
}
```
Создание общей ценности с использованием useSharedValue() У крюка есть много преимуществ. Это помогает мутировать данные и запускает анимацию на основе текущего значения. Мы можем получить доступ и изменить общее значение, используя .value собственность. Мы создадим doubleTap объект масштабирования начального значения и использования Gesture.Tap() чтобы оживить переход при масштабировании изображения наклейки. Чтобы определить количество необходимых кранов, мы добавим numberOfTaps().

Создать следующий объект в EmojiSticker компонент:
```
const doubleTap = Gesture.Tap()
  .numberOfTaps(2)
  .onStart(() => {
    if (scaleImage.value !== imageSize * 2) {
      scaleImage.value = scaleImage.value * 2;
    } else {
      scaleImage.value = Math.round(scaleImage.value / 2);
    }
  });
```
Чтобы оживить переход, давайте воспользуемся весенней анимацией. Это заставит его чувствовать себя живым, потому что он основан на реальной физике пружины. Мы будем использовать withSpring() Функция, обеспечиваемая react-native-reanimated.

На изображении наклейки, мы будем использовать useAnimatedStyle() Крюк для создания объекта стиля. Это поможет нам обновлять стили, используя общие значения, когда происходит анимация. Мы также масштабируем размер изображения, манипулируя width и height свойства. Первоначальные значения этих свойств устанавливаются на imageSize.

Создать a imageStyle переменная и добавить ее в EmojiSticker компонент:
```
const imageStyle = useAnimatedStyle(() => {
  return {
    width: withSpring(scaleImage.value),
    height: withSpring(scaleImage.value),
  };
});
```
Далее, оберните `<Animated.Image>` Компонент с `<GestureDetector>` и изменить style Опора на `<Animated.Image>` чтобы пройти imageStyle.
```
import { ImageSourcePropType, View } from 'react-native';
import { Gesture, GestureDetector } from 'react-native-gesture-handler';
import Animated, { useAnimatedStyle, useSharedValue, withSpring } from 'react-native-reanimated';

type Props = {
  imageSize: number;
  stickerSource: ImageSourcePropType;
};

export default function EmojiSticker({ imageSize, stickerSource }: Props) {
  const scaleImage = useSharedValue(imageSize);

  const doubleTap = Gesture.Tap()
    .numberOfTaps(2)
    .onStart(() => {
      if (scaleImage.value !== imageSize * 2) {
        scaleImage.value = scaleImage.value * 2;
      } else {
        scaleImage.value = Math.round(scaleImage.value / 2);
      }
    });

  const imageStyle = useAnimatedStyle(() => {
    return {
      width: withSpring(scaleImage.value),
      height: withSpring(scaleImage.value),
    };
  });

  return (
    <View style={{ top: -350 }}>
       <GestureDetector gesture={doubleTap}>
        <Animated.Image
          source={stickerSource}
          resizeMode="contain"
          style={[{ width: imageSize, height: imageSize }, imageStyle]}
        />
      </GestureDetector>
    </View>
  );
}
```
В вышеприведенном фрагменте, gesture реквизит принимает ценность doubleTap чтобы вызвать жест, когда пользователь дважды нажимает на изображение наклейки.
**4. Добавить жест сковороды**  
Чтобы распознать жест перетаскивания на наклейке и отследить ее движение, мы будем использовать жест сковороды. В src/components/emoidji-sticker.tsx :

    1. Создайте две новые общие ценности: translateX и translateY.
    2. Заменить <View> с <Animated.View> компонент.
```
export default function EmojiSticker({ imageSize, stickerSource }: Props) {
  const scaleImage = useSharedValue(imageSize);
  const translateX = useSharedValue(0);
  const translateY = useSharedValue(0);
  // ...rest of the code remains same

  return (
    <Animated.View style={{ top: -350 }}>
      <GestureDetector gesture={doubleTap}>
        {/* ...rest of the code remains same */}
      </GestureDetector>
    </Animated.View>
  );
}
```
Давайте узнаем, что делает вышеприведенный код:

    Определенные значения перевода будут перемещать наклейку по экрану. Поскольку наклейка движется по обеим осям, нам нужно отслеживать значения X и Y.
    В useSharedValue() Крючки, мы установили обе переменные перевода, чтобы иметь начальную позицию 0. Это начальная позиция наклейки и отправная точка. Это значение устанавливает начальную позицию наклейки, когда начинается жест.

На предыдущем шаге мы спровоцировали onStart() обратный звонок для жеста крана, прикованного к Gesture.Tap() Метод. Для жеста сковороды укажите onChange() обратный звонок, который проходит, когда жест активен и движется.

    Создать a drag объект, чтобы справиться с жестом сковороды. The onChange() обратный звонок принимает event в качестве параметра. changeX и changeY свойства удерживают изменение позиции с момента последнего события и обновляют значения, хранящиеся в translateX и translateY.
    Определить containerStyle Объект, использующий useAnimatedStyle() Крюк. Это вернет множество преобразований. Для <Animated.View> компонент, нам нужно установить transform Имущество для translateX и translateY Ценности. Это изменит положение наклейки, когда жест активен.
```
const drag = Gesture.Pan().onChange(event => {
  translateX.value += event.changeX;
  translateY.value += event.changeY;
});

const containerStyle = useAnimatedStyle(() => {
  return {
    transform: [
      {
        translateX: translateX.value,
      },
      {
        translateY: translateY.value,
      },
    ],
  };
});
```
Далее, внутри кода JSX:

    1. Обновить <EmojiSticker> Компонент, чтобы <GestureDetector> Компонент становится компонентом верхнего уровня.
    2. Добавить containerStyle на <Animated.View> Компонент для применения стилей трансформации.
```
import { Gesture, GestureDetector } from 'react-native-gesture-handler';
import Animated, { useAnimatedStyle, useSharedValue, withSpring } from 'react-native-reanimated';
import { ImageSourcePropType } from 'react-native';

type Props = {
  imageSize: number;
  stickerSource: ImageSourcePropType;
};

export default function EmojiSticker({ imageSize, stickerSource }: Props) {
  const scaleImage = useSharedValue(imageSize);
  const translateX = useSharedValue(0);
  const translateY = useSharedValue(0);

  const doubleTap = Gesture.Tap()
    .numberOfTaps(2)
    .onStart(() => {
      if (scaleImage.value !== imageSize * 2) {
        scaleImage.value = scaleImage.value * 2;
      } else {
        scaleImage.value = Math.round(scaleImage.value / 2);
      }
    });

  const imageStyle = useAnimatedStyle(() => {
    return {
      width: withSpring(scaleImage.value),
      height: withSpring(scaleImage.value),
    };
  });

  const drag = Gesture.Pan().onChange(event => {
    translateX.value += event.changeX;
    translateY.value += event.changeY;
  });

  const containerStyle = useAnimatedStyle(() => {
    return {
      transform: [
        {
          translateX: translateX.value,
        },
        {
          translateY: translateY.value,
        },
      ],
    };
  });

  return (
    <GestureDetector gesture={drag}>
      <Animated.View style={[containerStyle, { top: -350 }]}>
        <GestureDetector gesture={doubleTap}>
          <Animated.Image
            source={stickerSource}
            resizeMode="contain"
            style={[{ width: imageSize, height: imageSize }, imageStyle]}
          />
        </GestureDetector>
      </Animated.View>
    </GestureDetector>
  );
}
```

## Сделать скриншот
В этой главе мы узнаем, как сделать снимок экрана с помощью сторонней библиотеки и сохранить его в медиатеке устройства. Мы будем использовать `react-native-view-shot` чтобы сделать скриншот и `expo-media-library` чтобы сохранить изображение в медиа-библиотеке устройства.

**1. Установить библиотеки**  
Установить `react-native-view-shot` и `expo-media-library`, выполните следующие команды:
> npx expo install react-native-view-shot expo-media-library

**2. Подсказка для разрешений**  
Приложение, которое требует конфиденциальной информации, такой как доступ к медиатеке устройства, должно получить разрешение на доступ или запретить доступ. Использовать `useMediaLibraryPermissions()` Крюк от `expo-image-picker`, мы можем использовать разрешение `permissionResponse` и `requestPermission()` Способ запросить доступ. Этот крючок запрашивает как разрешения на чтение, так и запись, которые охватывают выбор изображений из библиотеки и сохранение скриншотов к ней.

Когда приложение загружается в первый раз, и статус разрешения не предоставляется и не отказано, стоимость `permissionResponse` является null. При запросе разрешения пользователь может либо предоставить разрешение, либо отказать в нем. Мы можем добавить условие, чтобы проверить, не предоставлено ли оно. Если это не предусмотрено, запускайте `requestPermission()` Метод. После получения доступа, ценность permissionResponse изменения в `granted`.

Добавьте следующий фрагмент кода внутрь src/app/(tabs)/index.tsx:
```
import { useEffect, useState } from 'react';
import * as ImagePicker from 'expo-image-picker';

// ...rest of the code remains same

export default function Index() {
  const [permissionResponse, requestPermission] = ImagePicker.useMediaLibraryPermissions();
  // ...rest of the code remains same

  useEffect(() => {
    if (!permissionResponse?.granted) {
      requestPermission();
    }
  }, []);

  // ...rest of the code remains same
}
```
**3. Создайте референт для сохранения текущего представления**  
Мы будем использовать `react-native-view-shot` чтобы позволить пользователю сделать снимок экрана в приложении. Эта библиотека захватывает скриншот `<View>` как изображение с использованием `captureRef()` Метод. Он возвращает URI захваченного файла снимков скриншота.

    1. Импорт captureRef от react-native-view-shot и useRef От React.
    2. Создать a imageRef эталонная переменная для хранения ссылки на снимок экрана, захваченного изображения.
    Обернуть <ImageViewer> и <EmojiSticker> Компоненты внутри a <View> а затем передать ему справочную переменную.
```
import { useState, useRef } from 'react';
import { captureRef } from 'react-native-view-shot';

export default function Index() {
   const imageRef = useRef<View>(null);

  // ...rest of the code remains same

  return (
    <GestureHandlerRootView style={styles.container}>
      <View style={styles.imageContainer}>
        <View ref={imageRef} collapsable={false}>
          <ImageViewer imgSource={PlaceholderImage} selectedImage={selectedImage} />
          {pickedEmoji && <EmojiSticker imageSize={40} stickerSource={pickedEmoji} />}
        </View>
      </View>
      {/* ...rest of the code remains same */}
    </GestureHandlerRootView>
  );
}
```
В вышеприведенном фрагменте, `collapsable` реквизит настроены на false. Это позволяет `<View>` компонент к скриншоту только фонового изображения и смайлика смайликов.  
**4. Снимите скриншот и сохраните его**  
Мы можем сделать скриншот вида, позвонив `captureRef()` Метод из `react-native-view-shot` внутри `onSaveImageAsync()` Функция. Он принимает факультативный аргумент, в котором мы можем пройти **width** и **height** область захвата скриншота. Мы можем прочитать больше о доступных вариантах в документация библиотеки.

The `captureRef()` Метод также возвращает обещание, которое выполняется с URI скриншота. Мы передадим этот URI в качестве параметра `MediaLibrary.saveToLibraryAsync()` и сохранить скриншот в медиатеку устройства.

Внутри src/app/(tabs)/index.tsx, обновить onSaveImageAsync() Функция со следующим кодом:
```
import * as ImagePicker from 'expo-image-picker';
import * as MediaLibrary from 'expo-media-library';
import { useEffect, useRef, useState } from 'react';
import { ImageSourcePropType, StyleSheet, View } from 'react-native';
import { GestureHandlerRootView } from 'react-native-gesture-handler';
import { captureRef } from 'react-native-view-shot';

import Button from '@/components/button';
import CircleButton from '@/components/circle-button';
import EmojiList from '@/components/emoji-list';
import EmojiPicker from '@/components/emoji-picker';
import IconButton from '@/components/icon-button';
import ImageViewer from '@/components/image-viewer';

import EmojiSticker from '@/components/emoji-sticker';

const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  const [selectedImage, setSelectedImage] = useState<string | undefined>(
    undefined
  );
  const [showAppOptions, setShowAppOptions] = useState<boolean>(false);
  const [isModalVisible, setIsModalVisible] = useState<boolean>(false);
  const [pickedEmoji, setPickedEmoji] = useState<
    ImageSourcePropType | undefined
  >(undefined);
  const [permissionResponse, requestPermission] = ImagePicker.useMediaLibraryPermissions();
  const imageRef = useRef<View>(null);

  useEffect(() => {
    if (!permissionResponse?.granted) {
      requestPermission();
    }
  }, []);

  const pickImageAsync = async () => {
    let result = await ImagePicker.launchImageLibraryAsync({
      mediaTypes: ['images'],
      allowsEditing: true,
      quality: 1,
    });

    if (!result.canceled) {
      setSelectedImage(result.assets[0].uri);
      setShowAppOptions(true);
    } else {
      alert('You did not select any image.');
    }
  };

  const onReset = () => {
    setShowAppOptions(false);
  };

  const onAddSticker = () => {
    setIsModalVisible(true);
  };

  const onModalClose = () => {
    setIsModalVisible(false);
  };

  const onSaveImageAsync = async () => {
    try {
      const localUri = await captureRef(imageRef, {
        height: 440,
        quality: 1,
      });

      await MediaLibrary.saveToLibraryAsync(localUri);
      if (localUri) {
        alert('Saved!');
      }
    } catch (e) {
      console.log(e);
    }
  };

  return (
    <GestureHandlerRootView style={styles.container}>
      <View style={styles.imageContainer}>
        <View ref={imageRef} collapsable={false}>
          <ImageViewer imgSource={PlaceholderImage} selectedImage={selectedImage} />
          {pickedEmoji && <EmojiSticker imageSize={40} stickerSource={pickedEmoji} />}
        </View>
      </View>
      {showAppOptions ? (
        <View style={styles.optionsContainer}>
          <View style={styles.optionsRow}>
            <IconButton icon="refresh" label="Reset" onPress={onReset} />
            <CircleButton onPress={onAddSticker} />
            <IconButton icon="save-alt" label="Save" onPress={onSaveImageAsync} />
          </View>
        </View>
      ) : (
        <View style={styles.footerContainer}>
          <Button theme="primary" label="Choose a photo" onPress={pickImageAsync} />
          <Button label="Use this photo" onPress={() => setShowAppOptions(true)} />
        </View>
      )}
      <EmojiPicker isVisible={isModalVisible} onClose={onModalClose}>
        <EmojiList onSelect={setPickedEmoji} onCloseModal={onModalClose} />
      </EmojiPicker>
    </GestureHandlerRootView>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
  optionsContainer: {
    position: 'absolute',
    bottom: 80,
  },
  optionsRow: {
    alignItems: 'center',
    flexDirection: 'row',
  },
});
```
## Обработка различий платформы
Android, iOS и Интернет имеют разные возможности. В нашем случае как Android, так и iOS могут захватывать скриншот с помощью `react-native-view-shot` Библиотека. Однако веб-браузеры не могут.

В этой главе мы узнаем, как обрабатывать скриншоты для веб-браузеров, поэтому наше приложение имеет одинаковую функциональность на всех платформах.

**1. Установить и импортировать dom-to-image**
Чтобы запечатлеть снимок экрана в Интернете и сохранить его в качестве изображения, мы будем использовать стороннюю библиотеку под названием `dom-to-image`. Он берет скриншот любого узла DOM и превращает его в векторный (SVG) или растровый (PNG или JPEG) изображение.

Остановите сервер разработки и выполните следующую команду для установки библиотеки:
> npm install dom-to-image

После установки обязательно перезапустите сервер разработки и нажмите `W` в терминале.

**2. Добавить код, специфичный для платформы**  
Использовать Platform модуль от React Native, мы можем реализовать платформу специфическое поведение. Внутри src/app/(tabs)/index.tsx:

    1. Импортировать Platform Модуль от react-native.
    2. Импортировать domtoimage библиотека от dom-to-image.
    3. Обновить onSaveImageAsync() функция, чтобы проверить, является ли текущая платформа 'web' с Platform.OS собственность. Если это так 'web', мы будем использовать domtoimage.toJpeg() способ преобразования и захвата тока <View> В качестве изображения JPEG. В противном случае мы будем продолжать использовать ту же логику, добавленную для собственных платформ.
```
import * as ImagePicker from 'expo-image-picker';
import * as MediaLibrary from 'expo-media-library';
import { useEffect, useRef, useState } from 'react';
import { ImageSourcePropType, View, StyleSheet, Platform } from 'react-native';
import { GestureHandlerRootView } from 'react-native-gesture-handler';
import { captureRef } from 'react-native-view-shot';
import domtoimage from 'dom-to-image';

import Button from '@/components/button';
import ImageViewer from '@/components/image-viewer';
import IconButton from '@/components/icon-button';
import CircleButton from '@/components/circle-button';
import EmojiPicker from '@/components/emoji-picker';
import EmojiList from '@/components/emoji-list';
import EmojiSticker from '@/components/emoji-sticker';

const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  const [selectedImage, setSelectedImage] = useState<string | undefined>(undefined);
  const [showAppOptions, setShowAppOptions] = useState<boolean>(false);
  const [isModalVisible, setIsModalVisible] = useState<boolean>(false);
  const [pickedEmoji, setPickedEmoji] = useState<ImageSourcePropType | undefined>(undefined);
  const [permissionResponse, requestPermission] = ImagePicker.useMediaLibraryPermissions();
  const imageRef = useRef<View>(null);

  useEffect(() => {
    if (!permissionResponse?.granted) {
      requestPermission();
    }
  }, []);

  const pickImageAsync = async () => {
    let result = await ImagePicker.launchImageLibraryAsync({
      mediaTypes: ['images'],
      allowsEditing: true,
      quality: 1,
    });

    if (!result.canceled) {
      setSelectedImage(result.assets[0].uri);
      setShowAppOptions(true);
    } else {
      alert('You did not select any image.');
    }
  };

  const onReset = () => {
    setShowAppOptions(false);
  };

  const onAddSticker = () => {
    setIsModalVisible(true);
  };

  const onModalClose = () => {
    setIsModalVisible(false);
  };

  const onSaveImageAsync = async () => {
    if (Platform.OS !== 'web') {
      try {
        const localUri = await captureRef(imageRef, {
          height: 440,
          quality: 1,
        });

        await MediaLibrary.saveToLibraryAsync(localUri);
        if (localUri) {
          alert('Saved!');
        }
      } catch (e) {
        console.log(e);
      }
    } else {
      try {
        const dataUrl = await domtoimage.toJpeg(imageRef.current, {
          quality: 0.95,
          width: 320,
          height: 440,
        });

        let link = document.createElement('a');
        link.download = 'sticker-smash.jpeg';
        link.href = dataUrl;
        link.click();
      } catch (e) {
        console.log(e);
      }
    }
  };

  return (
    <GestureHandlerRootView style={styles.container}>
      <View style={styles.imageContainer}>
        <View ref={imageRef} collapsable={false}>
          <ImageViewer imgSource={PlaceholderImage} selectedImage={selectedImage} />
          {pickedEmoji && <EmojiSticker imageSize={40} stickerSource={pickedEmoji} />}
        </View>
      </View>
      {showAppOptions ? (
        <View style={styles.optionsContainer}>
          <View style={styles.optionsRow}>
            <IconButton icon="refresh" label="Reset" onPress={onReset} />
            <CircleButton onPress={onAddSticker} />
            <IconButton icon="save-alt" label="Save" onPress={onSaveImageAsync} />
          </View>
        </View>
      ) : (
        <View style={styles.footerContainer}>
          <Button theme="primary" label="Choose a photo" onPress={pickImageAsync} />
          <Button label="Use this photo" onPress={() => setShowAppOptions(true)} />
        </View>
      )}
      <EmojiPicker isVisible={isModalVisible} onClose={onModalClose}>
        <EmojiList onSelect={setPickedEmoji} onCloseModal={onModalClose} />
      </EmojiPicker>
    </GestureHandlerRootView>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
  optionsContainer: {
    position: 'absolute',
    bottom: 80,
  },
  optionsRow: {
    alignItems: 'center',
    flexDirection: 'row',
  },
});
```
## Настройка панели состояния, экрана брызг и значка приложения
В этой главе мы рассмотрим некоторые детали приложения, прежде чем развертывать наше приложение в магазине приложений, например, смешивать панель состояния, настраивать значок приложения и брызгать на экране.

**1. Настройка строки состояния**  
`expo-status-bar` библиотека предустановлена в каждом проекте, созданном с использованием `create-expo-app`. Эта библиотека предоставляет StatusBar компонент для настройки стиля стенд состояния приложения.
Внутри src/app/_layout.tsx :

    1. Импорт StatusBar от expo-status-bar.
    2. Группа The StatusBar и существующих Stack компоненты с Компонент Фрагмента React.
```
import { Stack } from 'expo-router';

import { StatusBar } from 'expo-status-bar';


export default function RootLayout() {
  return (
    <>
      <Stack>
        <Stack.Screen name="(tabs)" options={{ headerShown: false }} />
      </Stack>
      <StatusBar style="light" />
    </>
  );
}
```
**2. Иконка приложения**  
Внутри проекта есть файл icon.png внутри каталога активов/изображений. Это иконка нашего приложения. Это изображение 1024px на 1024px.  
Как и изображение всплеска экрана, "icon" собственность в app.json файл настраивает путь значка приложения. По умолчанию новый проект Expo определяет правильный путь "./assets/images/icon.png". Нам не нужно ничего менять.

## Всплеск экрана
Экран брызг виден до загрузки контента приложения. Он использует меньший образ, такой как значок приложения, который центрирован. Он скрывается, как только контент приложения готов к отображению.

The `expo-splash-screen` Плагин уже поставляется предустановленным в каждом созданном проекте `create-expo-app`. Эта библиотека предоставляет плагин конфигурирования для настройки экрана брызг.

В app.json, `expo-splash-screen` плагин уже настроен на использование значка приложения в качестве изображения экрана брызг (предоставлено в загружаемые активы) со следующим фрагментом, поэтому нам не нужно ничего менять:
```
{
  "plugins": [
    [
      "expo-splash-screen",
      {
        "image": "./assets/images/splash-icon.png"
      }
    ]
  ]
}
```
Однако для тестирования экрана брызг мы не можем использовать Expo Go или сборку разработки. Чтобы протестировать его, нам нужно создать предварительный просмотр или производственную сборку нашего приложения.

## Учебные ресурсы
Теперь, когда приложение сделано, давайте узнаем больше о технологиях, которые мы использовали для его создания.  
### Создайте свой проект в приложение
Чтобы начать создавать новое приложение на вашей машине, вы можете использовать `npx create-expo-app@latest` и настройте свою среду разработки последовательно.

### Рекомендуемые ресурсы 
После того, как вы создали свой новый проект, вы можете узнать больше о различных инструментах и концепциях, которые помогут вам в вашем путешествии по разработке приложения:

   * Инструменты разработки: Справка инструментов Expo, которые помогут вам во время различных аспектов вашего путешествия по созданию приложений.
   * Разработка: Использование сборки разработки позволяет вам получить полный контроль над процессом сборки вашего приложения и тестировать ваше приложение на устройстве или симуляторе.
   * Обзор развития: Это обзор высокого уровня, в котором содержится подробная информация о ключевых концепциях разработки приложения с Expo и потоке петли развития ядра.
   * Expo Router: Мы прошли через основы Expo Router и реализовали навигатор вкладки. Смотрите его документацию, чтобы узнать больше о библиотеке.
   * Значок приложения и экран брызг: Вы можете узнать больше о настройке значка приложения и руководства по брызгам экрана. Кроме того, проверьте ссылку на настройки приложения для свойств, которые вы можете настроить в файл app.json.
   * Распространение и представление приложений в магазины приложений: прочитайте эти ресурсы, чтобы узнать больше о том, как выпустить и отправить свое приложение в магазины приложений, как только оно будет готово к отправке.
   * DebuggingОтладка: иногда что-то идет не так, и когда они это делают, вы можете использовать инструменты отладки, чтобы найти и исправить ошибки.  
### Обучение
Мы использовали компоненты React и API. Наличие твердого понимания React имеет важное значение для использования Expo для создания вашего приложения. Мы рекомендуем прочитать раздел «Быстрый старт» документации React и раздел «Крючки».
### React Native

При разработке учебного приложения мы широко использовали React Native. Вы можете начать с руководства по основам React Native, чтобы узнать больше. Кроме того, проверьте следующие документы:

   * Просмотр API Reference
   * Текст API ссылка
   * Платформа специфический код
   * Представление данных в списке

Мы использовали Flexbox для компоновки наших компонентов. Ознакомьтесь со следующими рекомендациями, чтобы узнать больше об этом:

   * Высота и ширина
   * Макет с помощью Flexbox
### Жесты и анимация
Чтобы узнать больше о внедрении различных типов жестов и анимации, мы рекомендуем следующую документацию:

   * Реагировать Нативный Жест Обработчик
   * React Native Reanimated
