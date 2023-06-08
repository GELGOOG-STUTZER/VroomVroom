# Бот на базе Ардуино

## Задача
Необходимо сконструировать бота для преодоления полосы препятствий, состоящей из 4-ех этапов:  
1. “Бассейн” с маршмэллоу
2. Подъем и спуск с горки
3. Тоннель с открывающейся дверцей
4. Воздушный шарик, который необходимо лопнуть.

## Конструкция бота (см. bot_1-4.jpg)
### Зажигалка
Состоит из двух напечатанных на 3D-принтере деталей (крепление для зажигалки lighter_body и крепление для сервомотора servo_attach), сервомотора FS5103R и зажигалки с длинным носиком из ближайшего хозяйственного магазина. Сервомотор своим усилием нажимает на кнопку зажигалки и за счет этого на конце носика появляется пламя.

### Каркас и основные составляющие
Каркас сделан из фанеры при помощи лазерной резки. Состоит из основания и колес (см wheel.cdr). К основанию крепятся выносы для электромоторов (сзади) и колес (спереди), распечатанные на 3D принтере. Задние колеса насажены на оси моторов и укреплены с помощью клея. В качестве осей передних колес используются болты, двумя контрящимися гайками регулируется плотность посадки. Под основанием посажен на клей блок с двумя аккумуляторами. Сверху находятся Arduino Uno, радиомодуль для связи с пультом управления, зажигалка и сервопривод. Крякнуто, плюнуто и надежно закрепено скотчем

### Пульт управления (см. control.jpg)
Состоит из Arduino Uno, радиомодуля, крутящегося тумблера для управления сервоприводом и джойстика для управления моторами

### Первоисточник
За основу взят код https://github.com/m112521/bots/tree/radio, база комплектующих в нашем проекте такая же. 
 
### Возникшие проблемы:
1. Радиомодуль. В какой-то момент радиомодуль на боте перегревался и начиналось восстание машин. В конечном счете его пришлось заменить
2. Моторы нужно проверять на брак, также попадаются моторы с разной мощностью
3. Трения колес не хватало для преодоления подъема на горку, проблему решили нанесением клея на части колес, контактирующих с поверхностью. Стоит отметить, что использовались не самые мощные элекромоторы.
