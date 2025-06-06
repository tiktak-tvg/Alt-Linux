#### Устанавливаем Криптопро в ручную.

Перед установкой запустите обновление пакетов, зависимостей.

```
epm update && epm upgrade  или apt-get update && apt-get upgrade 
```

Скачиваем с сайта ``https://cryptopro.ru/`` в ручную.

- КриптоПро ЭЦП Browser plug-in
- КриптоПро CSP<br>
с расширением *.rpm

Или заходим на сайт<br>
*Проверка создания электронной подписи CAdES-BES*<br>
```
https://www.cryptopro.ru/sites/default/files/products/cades/demopage/cades_bes_sample.html
```

и на нем автоматически предлагается загрузить не достающие плагины. 

![image](https://github.com/tvgVita69/Linux_begin/assets/98489171/c8dfc7d9-1fbb-462e-be6d-5e5c99a337b5)

Переходим в папку куда скачали ахив для установки ``КриптоПро ЭЦП Browser plug-in`` ``КриптоПро CSP``<br>
Нам понадобяться три папки с такими названиями  ``cades-linux-amd64``, ``linux-amd64`` и предлагаемый браузер ``chromium-gost``.<br>
Ссылка на закачку ``https://cryptopro.ru/products/chromium-gost`` для Линукс с расширение ``*.rpm``.
Распакуем их.<br>

![image](https://github.com/tvgVita69/Linux_begin/assets/98489171/dca411e5-413d-40b8-be89-8d786d51896f)

Далее открываем сайт: ссылка такая ``https://www.altlinux.org/%D0%9A%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D0%9F%D1%80%D0%BE``, если не откроется найдите по названию:

![image](https://github.com/tvgVita69/Linux_begin/assets/98489171/f0fa03d1-b37e-4e32-bda2-640ef5e06050)

Переходим в терменале ``term`` где распакована папка ``linux-amd64``<br>
```
cd /home/user/linux-amd64/
```

![image](https://github.com/tvgVita69/Linux_begin/assets/98489171/64e1acb0-f964-460f-afaf-00a98be59308)

И с сайта который открыли копируем команды:

**установите базовые пакеты:** 

``apt-get install cprocsp-curl* lsb-cprocsp-base* lsb-cprocsp-capilite* lsb-cprocsp-kc1-64* lsb-cprocsp-rdr-64*``

![image](https://github.com/tvgVita69/Linux_begin/assets/98489171/9b8cea4d-13a1-4b39-acba-2b34d02cc6f0)

**установите пакеты для поддержки токенов (Рутокен S и Рутокен ЭЦП):**

``apt-get install cprocsp-rdr-gui-gtk* cprocsp-rdr-rutoken* cprocsp-rdr-pcsc* lsb-cprocsp-pkcs11* pcsc-lite-rutokens pcsc-lite-ccid``

![image](https://github.com/tvgVita69/Linux_begin/assets/98489171/881491a6-dfbf-4ab4-a43a-fd2a20f17284)

**Для установки сертификатов Главного удостоверяющего центра:**

``apt-get install lsb-cprocsp-ca-certs*``

![image](https://github.com/tvgVita69/Linux_begin/assets/98489171/f4da6e1e-3979-446b-9f48-eb64641ff610)

**Если есть потребность в установке графических Инструментов КриптоПро:** 

``apt-get install cprocsp-cptools*``

![image](https://github.com/tvgVita69/Linux_begin/assets/98489171/8f7b69ac-cf40-4f7b-8325-a5e28140777d)

Далее, открываем папку /home/user/cades-linux-amd64/ удаляем файлы с расширением *.deb и запускаем установку трёх файлов с расширением *.rpm

![image](https://github.com/tvgVita69/Linux_begin/assets/98489171/cb6a1db1-5106-4a5e-bee9-4777643a99eb)

*P.s.В папке home/user/linux-arm64/./install_gui.sh предлагают автоматическую установку через скрипт, на этом же сайте есть инструкция, но мы и так всё уже установили.
Поэтому запускать не будем.*

Теперь проверяем установку.<br>
Проверка создания электронной подписи CAdES-BES<br>
```
https://www.cryptopro.ru/sites/default/files/products/cades/demopage/cades_bes_sample.html
```

![image](https://github.com/tvgVita69/Linux_begin/assets/98489171/be8ff6a8-1bc3-47e8-8245-0a6f0dd6545f)

Так будет выглядеть с ключиком ``Контур`` например 

![image](https://github.com/user-attachments/assets/afa6d562-0240-41c6-9612-9aa208d30c93)

> [!Warning]
> В OS Windows ключ находит КриптоПро сам, в OS Linux его нужно добавить в КриптоПро вручную, чтобы ЭЦП появился на электронной площадке

##### Ошибки и исправления.

```
https://www.altlinux.org/%D0%9A%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D0%9F%D1%80%D0%BE#%D0%98%D0%B7%D0%B2%D0%B5%D1%81%D1%82%D0%BD%D1%8B%D0%B5_%D0%BE%D1%88%D0%B8%D0%B1%D0%BA%D0%B8_%D0%B8_%D0%BC%D0%B5%D1%82%D0%BE%D0%B4%D1%8B_%D0%B8%D1%81%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F
```

Не забудьте добавить в настройке список доверенных сайтов.

```
https://chrome-extension://epebfcehmdedogndhlcacafjaacknbcm/trusted_sites.html
```

![image](https://github.com/user-attachments/assets/1496f5b4-e032-46a8-bf54-d6da68f43e95)
