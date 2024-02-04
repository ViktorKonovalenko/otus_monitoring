# otus_monitoring
Для выполнения ДЗ был создан Vagrantfile с ansible playbook, который поднимает prometheus, node_exporter, grafana.<br>
Выполняем команду <br>
<pre>vagrant up</pre>

После создания ВМ с сервисами, заходи по пути http://127.0.0.1:9090 <br>

Заходим в grafana для создания дашбордов http://127.0.0.1:3000 <br>
Добавляем data source. В нашем случае это prometheus<br>
![image](https://github.com/ViktorKonovalenko/otus_monitoring/assets/32430041/a5da6b02-9a65-4dad-b164-73c2cca6160b)
Создаем дашборды. Результат собранных дашбордов на скриншоте  <br>
![image](https://github.com/ViktorKonovalenko/otus_monitoring/assets/32430041/07f7194a-9221-40b3-8d2b-a7b7fef00fab)
