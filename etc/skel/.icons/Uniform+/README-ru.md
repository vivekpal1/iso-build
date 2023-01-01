
Uniform+ это основная тема, от неё зависят все остальные опции.

Uniform+ fast-safe-mode вариант для старых или слабых компьютеров.

Для этой темы создан модифицированный скрипт Hardcoded Icon Fixer для исправления неизменяемых иконок.

Перед применением скрипта лучше сжать папки .local/share/applications /usr/share/applications /var/lib/snapd/desktop/applications /usr/share/icons /usr/share/pixmaps и сохранить их как бакуп для восстановления.

Как исправить упрямые иконки?

Возьмите fix2.sh, tofix-snap.txt и tofix2.csv и поместите их в домашнюю папку (это там где папки Документы, Видео, Изображения и т.д.).

Запустите скрипт в терминале:

sudo bash fix2.sh

далее вводим свой пароль (он будет совершенно невидимым) и жмём Enter


Как работает скрипт?

Скрипт просматривает все .desktop файлы в системе, и если видит такой путь к иконке:

Icon=/usr/share/pixmaps/gcolor2/gcolor2.xpm

то исправляет его на вот такой:

Icon=gcolor2

В этом случае любая тема иконок где есть gcolor2 (с любым разрешением .png, или .svg), покажет красивую картинку, а не стандартную и страшную gcolor2.xpm.

Скрипт исправляет иконки только для установленных программ. Т.е. если Вы установили новую программу и её иконка оказалась вне темы, запустите скрипт снова.

Список поддерживаемых .desktop - Linux.desktop-collection https://yadi.sk/d/XWNibgF6V9Fhdg

Если будут проблемы с цветом в symbolic, то просто удалите все папки symbolic. 

P.S. Под этот скрипт адаптированы ещё несколько тем иконок:

Snowy - https://yadi.sk/d/kVzafq1ptMV4R

Green triangles и Orange triangles - https://drive.google.com/file/d/1lobB1OphX-Ku1MbvGkTFSOaYcPFvp6jt/

Yellow square - https://www.gnome-look.org/p/1150789

Not superflat stickers  - https://www.gnome-look.org/p/1152410

Gears - http://gnome-look.org/content/show.php/Gears?content=168695

Shiny buttons - http://gnome-look.org/content/show.php/Shiny+buttons?content=169942

Glass of water - http://gnome-look.org/content/show.php/Glass+of+water?content=169389

White chips heavy https://drive.google.com/file/d/1VAP-HUzsoCJEl7SDCk92xEfenpQSspis/

P.S.S. Для оптимизации работы системы Вы можете создать icon-cache темы. Возможно это поможет при проблемах с апплетами в МАТЕ.

Если тема в .icons то

В терминале:

gtk-update-icon-cache /home/*****/.icons/Uniform+

(вместо ***** пишите имя своего компа)

Если тема в /usr/share/icons то

В терминале:

sudo gtk-update-icon-cache /usr/share/icons/Uniform+

