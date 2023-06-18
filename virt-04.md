
**Задача 1**

    Создайте собственный образ любой операционной системы (например ubuntu-20.04) с помощью Packer

    ![packer_1](./packer_1.png)

**Задача 2**

    Создайте вашу первую виртуальную машину в YandexCloud с помощью web-интерфейса YandexCloud.

    ![y-cloud_2](./y-cloud_1.png)

**Задача 3**

    С помощью Ansible и Docker Compose разверните на виртуальной машине из предыдущего задания систему мониторинга на основе Prometheus/Grafana.

    ![docker-compose_3](./docker-compose_3.png)

**Задача 4**

    ![grafana_4](./grafana_4.png)

**Задача 5 (*)**

    Создаём вторую ВМ:

    ![y-cloud_5](./y-cloud_5.png)

    На первой ВМ, с которой будет осуществляться мониторинг добавляем target в конфигурацию prometheus (prometheus.yml), в которой прописываем доступ к node-exporter второй ВМ:

    ![prometheus_yml_5](./prometheus_yml_5.png)

    После этого перезагружаем контейнер prometheus на первой ВМ, чтобы он подхватил новые настройки и проверяем, что в prometheus добавился мониторинг второй ВМ:

    ![prometheus_5](./prometheus_5.png)

    Далее добавил в Grafana первой ВМ дашборд Node Exporter for Prometheus в котором можно вибирать мониторинг между добавленных хостов. Выбираем вторую ВМ и мониторим:

    ![grafana_5](./grafana_5.png)

