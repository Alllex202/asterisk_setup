# Настройка Asterisk для разработки

---------

<h2 name="content">Содержание:</h2>

* <a href="#freepbx_setup">Настройка через интерфейс (FreePBX)</a>
  - <a href="#vm_create">Создание ВМ</a>
  - <a href="#vm_setup">Настройка ВМ</a>
  - <a href="#freepbx_install">Установка FreePBX</a>
  - <a href="#disk_delete">Удаление установочного диска</a>
  - <a href="#first_run">Первый запуск</a>
  - <a href="#ari_add">Добавление ARI (Asterisk REST Interface)</a>
  - <a href="#num_add">Добавление номера</a>
* <s><a href="#console_setup">Настройка через консоль</a></s>
* <a href="#softphone_setup">Настройка софтфона</a>
  - <a href="#zoiper_auth">Авторизация в Zoiper</a>
  - <a href="#zoiper_test">Тестовый звонок</a>

---------

<h2 name="freepbx_setup">Настройка через интерфейс (FreePBX)</h2>

Скачиваем <a href="https://www.freepbx.org/" target="_blank">образ диска</a> FreePBX (.iso) 

Пример установки через VirtualBox.

---------

<h3 name="vm_create">Создание ВМ</h3>

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/create_1.png" />
<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/create_2.png" />

---------

<h3 name="vm_setup">Настройка ВМ</h3>

Выключаем PAE/NX

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/system.png" />

Подключаем диск с образом.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/disk_1.png" />
<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/disk_2.png" />
<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/disk_3.png" />

В настройках сети указываем сетевой мост.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/net_n_ok.png" />

Не забываем нажать "OK".

---------

<h3 name="freepbx_install">Установка FreePBX</h3>

Запускаем ВМ.

Выбираем (Enter) пункты как на скриншотах.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/install_1.png" />
<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/install_2.png" />
<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/install_3.png" />

И ждем :)

<img src="http://pa1.narvii.com/6911/07ca4664a5f2c90715655c090168dcfc7eebfc00r1-320-320_00.gif" />
<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/wait_1.png" />
<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/wait_2.png" />

Устанавливаем пароль для root.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/pass_1.png" />

Нажать "Done". (Если пароль ненадежный, то нажать дважды)

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/pass_2.png" />

Нажать "Finish configurations".

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/install_4.png" />

И ждем...

<img src="https://img.pikbest.com/58pic/35/39/61/62K58PICb88i68HEwVnm5_PIC2018.gif!w340" />

После завершения установки выключаем ВМ. (Закрываем окно с ВМ. Не reboot.)

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/reboot.png" />

---------

<h3 name="disk_delete">Удаление установочного диска</h3>

В настройках ВМ удаляем установочный диск.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/disk_delete.png" />

---------

<h3 name="first_run">Первый запуск</h3>

Запускаем ВМ, ждем загрузки и авторизуемся.

Login - root

Password - тот, что указывали при установке.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/login.png" />

При успешной авторизации увидим IP-адрес ВМ. Этот адрес вводим в браузерную строку и попадаем на экран начальной настройки.

Вводим никнейм, пароль и почту (можно любую рандомную).

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/web_1.png" />

Далее выбираем администрирование и вводим указанные ранее никнейм и пароль.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/admin.png" />
<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/web_login.png" />

Можно будет поменять язык.

Так же может появиться информация о файрволе, жмем "abort".

---------

<h3 name="ari_add">Добавление ARI (Asterisk REST Interface)</h3>

Переходим на страницу Asterisk Rest Interface Users и добавляем пользователя

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/web_ari_1.png" />

Придумываем логин/пароль и сохраняем.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/web_ari_2.png" />

Обновляем конфигурации.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/web_ari_3.png" />

---------

<h3 name="num_add">Добавление номера</h3>

Переходим на страницу внутренних номеров.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/web_num_1.png" />

Добавляем новый номер (pjsip)

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/web_num_2.png" />

Вводим номер, имя, пароль и сохраняем.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/web_num_3.png" />

Применяем изменения.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/web_num_4.png" />

---------

<s><h2 name="console_setup">Настройка через консоль</h2></s>

---------

<h2 name="softphone_setup">Настройка софтфона</h3>

Можно использовать любой софтфон.

Мы используем <a href="https://www.zoiper.com/">Zoiper</a>. (PC/mobile)

---------

<h3 name="zoiper_auth">Авторизация в Zoiper</h3>

Устройство должно находиться в одной локальной сети с Asterisk.

Вводим логин в формате {номер}@{IP-адрес машины с Asterisk} и пароль, указанный при создании номера.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/zoiper_1.png" />

Автоматически должено выбрать SIP UDP.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/zoiper_2.png" />

---------

<h3 name="zoiper_test">Тестовый звонок</h3>

Позвонив по номеру *43, можно осуществить тестовый звонок.

<img src="https://github.com/Alllex202/asterisk_setup/blob/main/images/zoiper_3.png" />
