# add_and_remove


Суть.
На странице есть форма из двух (изначально) полей. А также блок "системной" информации (от CMS). В блоке системной информации располагается следующая информация:
1. <input id="id_book_set-TOTAL_FORMS" name="book_set-TOTAL_FORMS" type="hidden" value="1" /> - количество полей "Title" изначально. Это же количество в последствии передается на сервер при отправке формы.
2. <input id="id_book_set-MAX_NUM_FORMS" name="book_set-MAX_NUM_FORMS" type="hidden" value="10" /> - максимальное количество полей, которое может быть в форме.


Скрипт должен получить "value" из "input id="id_book_set-MAX_NUM_FORMS"" и не позволять создавать большее количество блоков.
При клике по кнопке "ADD" на страницу должен добавляться блок <div class="formset-item" id="formset-item-%N">. N - порядковый номерблока. При этом увеличивается "value" из "input id="id_book_set-TOTAL_FORMS"".
При клике по кнопке "DEL" должен удаляться блок, внутри которого расположена кнопка, по которой кликнули. При этом увеличивается "value" из "input id="id_book_set-TOTAL_FORMS"".
В идеале ещё пересчитываются порядковые номера N в <div class="formset-item" id="formset-item-%N"> и встают по порядку.
