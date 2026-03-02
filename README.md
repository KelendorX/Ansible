<H1>Ansible playbooks</H1><br>
Данные плейбуки используются для сбора информации и обновления модулей на 50+ разнообразных серверах Windows и Linux.<br>
<H2>Директория dotnet</H2>
<p>Данная дириктория используется для проверки версий dotnet и его обновления.</p>
<ul>
  <li>check_net.yml - проверка версий</li>
  <li>update_dotnet.yml - обновление dotnet</li>
</ul>
<H2>Директория download</H2>
<p>Данная дириктория используется для обновления внутренних модулей либо по средствам архивов либо конкретных .exe модулей.<br>
Так же после завершения обновления присылается уведомление в ТГ канал, какой файл был обновлен и его версию.<br>
Для архивов в сообщение расписывается, какие файлы были внутри.<br>
Все плейбуки которые выполняют обновление без использования архива, сначала проверяют на наличие данного файла, и только после этого его обновляют.<br>
Все файлы инвентаря защищены с помощью Ansible Vault.</p>
<ul>
  <li>CDA.yml - обновление с помощью архива в директорию typeplan</li>
  <li>CGI_BIN.yml - обновление с помощью архива в директорию cgi-bin</li>
  <li>JS.yml - обновление с помощью архива в директорию js</li>
  <li>JSON.yml - обновление с помощью архива в директорию json</li>
  <li>PNG.yml - обновление с помощью архива в директорию images</li>
  <li>create_derectory.yml - создание папки</li>
  <li>hostplaybook_dispcgi.yml - обновление модуля dispcgi</li>
  <li>hostplaybook_myloadfile.yml - обновление модуля myloadfile</li>
  <li>hostplaybook_nascgi.yml - обновление модуля nascgi</li>
  <li>hostplaybook_odii.yml - обновление модуля odii</li>
  <li>hostplaybook_palliat.yml - обновление модуля palliat</li>
  <li>hostplaybook_rest_tcgi.yml - обновление модуля rest_tcgi</li>
  <li>hostplaybook_sendgosp_regis.yml - обновление модуля sendgosp_regis</li>
  <li>hostplaybook_setup_et.yml - обновление модуля setup_et</li>
  <li>hostplaybook_setup_s_et.yml - обновление модуля setup_s</li>
  <li>hostplaybook_statcgi.yml - обновление модуля statcgi</li>
  <li>hostplaybook_svorthanc.yml - обновление модуля svorthanc</li>
  <li>hostplaybook_tcgi.yml - обновление модуля tcgi</li>
</ul>
<H2>Директория lis</H2>
<p>Данная дириктория используется для сбора данных по файлам которые не ушли из-за ошибок на серверах.<br>
<ul>
  <li>OdliSendResults.yml - обновление с помощью архива модуля OdliSendResults</li>
  <li>find_req_bad.yml - Сбор данных с серверов о количестве .req и .bad файлов, с последующим уведомлением в ТГ канал, так же указанием, если какая то точка не доступна. Запускается автоматически с помощью CRON</li>
</ul>
<H2>Директория sendedapi_test</H2>
<p>Данная дириктория используется для обновления модулей sendedapi, sapart а так же удаления базы cache.<br>
<ul>
  <li>sendedapi.yml - обновление с помощью архива модуля sendedapi</li>
  <li>sendedapi_delete_cache.yml - удаление базы cache. Запускается автоматически с помощью CRON</li>
  <li>sendedapi_dop.yml - обновление с помощью архива модуля sapart</li>
</ul>
