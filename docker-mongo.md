# Mongo

### Введение

MongoDB – это нереляционная база данных с открытым исходным кодом, поддерживающая документоориентированные системы хранения объектов в формате, подобном JSON. Она использует гибкую модель данных, позволяющую хранить данные любой структуры, и имеет широкий набор возможностей, включая полную поддержку индексов, сегментирование и репликацию.

Благодаря отсутствию структурированной схемы, Mongo может расти и изменяться вместе с моделью данных. Если вы работаете в недавно образованной компании, которая лелеет грандиозные планы или уже накопила столько данных, что возникла потребность в горизонтальном масштабировании, то присмотритесь к MongoDB.

| **SQL** | **MongoDB** |
| :--- | :--- |
| Таблица | Коллекция |
| Ряд | Документ |
| Столбец | Поле |
| Первичный ключ | ObjectId |
| Индекс | Индекс |
| Представление | Представление |
| Вложенная таблица или объект | Встроенный документ |

### Установка

Официальный образ [https://hub.docker.com/\_/mongo/](https://hub.docker.com/_/mongo/)

```bash
vitalij$ docker run --name mongo \ 
        -v /Volumes/Data/Docker/mongo/data/db:/data/db \
        -v /Volumes/Data/Docker/mongo/data/conf:/data/configdb \
        -e MONGO_INITDB_ROOT_USERNAME=admin \
        -e MONGO_INITDB_ROOT_PASSWORD=admin \
        -p 27017:27017 \
        -d mongo
```

Клиент Robo 3T [https://robomongo.org/download](https://robomongo.org/download)

![](/assets/10042134.png)

![](/assets/import_10062026.png)

```bash
/* 1 */
{
    "system" : {
        "currentTime" : ISODate("2018-10-06T17:21:27.894Z"),
        "hostname" : "5f6af28cf764",
        "cpuAddrSize" : 64,
        "memSizeMB" : 1998,
        "numCores" : 2,
        "cpuArch" : "x86_64",
        "numaEnabled" : false
    },
    "os" : {
        "type" : "Linux",
        "name" : "Ubuntu",
        "version" : "16.04"
    },
    "extra" : {
        "versionString" : "Linux version 4.9.87-linuxkit-aufs (root@95fa5ec30613) (gcc version 6.4.0 (Alpine 6.4.0) ) #1 SMP Wed Mar 14 15:12:16 UTC 2018",
        "libcVersion" : "2.23",
        "kernelVersion" : "4.9.87-linuxkit-aufs",
        "cpuFrequencyMHz" : "0.000",
        "cpuFeatures" : "fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht pbe syscall nx lm constant_tsc rep_good nopl xtopology nonstop_tsc eagerfpu pni pclmulqdq dtes64 ds_cpl ssse3 cx16 xtpr pcid sse4_1 sse4_2 popcnt aes xsave avx f16c rdrand hypervisor lahf_lm kaiser fsgsbase erms xsaveopt arat",
        "pageSize" : NumberLong(4096),
        "numPages" : 511735,
        "maxOpenFiles" : 1048576
    },
    "ok" : 1.0
}
```



