title: Урок 1 - Основные команды навигации по файловой системе

### Урок 1 - Основные команды навигации по файловой системе

Просто наберите 

    $ pwd


нажмите Ввод и прочтите результат выполнения комманды :)
## `pwd`

Видите нечто похожее на */home/вашеимя* ? Здорово, Вы определили текущий каталог.
Поздравляем! Вы вступили в экслюзивный клуб пользователей командной строки linux :)

Как Вы уже поняли, команда

     pwd


покажет текущий каталог. Ага, Ваш дом - каталог.

Теперь попробуем создать новый каталог. Введите следующую команду

    mkdir -v dir1

и нажмите Ввод.
## `mkdir`

Появилось сообщение?

*`mkdir: created directory dir1`*

Круто, теперь Вы создали новый каталог. Предположим, Вы хотите создать более одного каталога, 
вместо того, чтобы выполнять mkdir несколько раз, вида 
	mkdir -v dir2
	mkdir -v dir2/dir3
	mkdir -v dir2/dir3/dir4
Вы можете просто выполнить

	mkdir -vp dir2/dir3/dir4

Ключ "-p" создает родительские каталоги для "dir4" при необходимости.
В данном случае будут созданы dir2, dir3 автоматически. 
Мы создали 4 каталога. Как их увидеть?

Для просмотра наберите `ls` и нажмите Ввод.

	ls

## `ls`

перечислены `dir1 dir2` - содержимое каталога? Как мы и хотели.

	`тупой наставник: Эй, парень в синей футболке, чего тебя так смущает?`
	`синяя-футболка: я создал 4 каталога, где недостающие dir3, dir4?`

Хороший вопрос. Они созданы внутри каталога dir2 и не отображаются простой командой `ls`, 
нужно использовать более "сложную" команду, чтобы увидеть их. Попробуйте так:

	ls -R 

"сложно", не так ли? :P кстати -R означает Рекурсивно.

Окей, мы создали новые каталоги и просмотрели их. Теперь давайте 
перейдем в новый каталог.

	cd dir2

## `cd`

Круто, Вы перешли в dir2, проверим так ли это с помощью команды, 
изученной ранее `wm_pwd`(или pwd), чтобы перейти в следующий каталог dir3

	cd dir3
переместит нас в каталог "dir3"

>`Советы и приемы:` команда

        cd ..

переместит в родительский каталог, а именно в dir2.
Теперь наберите

	cd -

эта команда переместит в предыдущий каталог, а именно dir3. 
Здорово, не так ли?! 
А просто 

	cd 
переместит в домашний каталог.

Вот и все. Вы успешно завершили первый урок.
Можете приступить к следующему.


