# Mongo

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

![](/assets/10042137.png)





```bash
db.getCollection('startup_log').find({})

/* 1 */
{
    "_id" : "bb4850459e5e-1538676716625",
    "hostname" : "bb4850459e5e",
    "startTime" : ISODate("2018-10-04T18:11:56.000Z"),
    "startTimeLocal" : "Thu Oct  4 18:11:56.625",
    "cmdLine" : {
        "net" : {
            "bindIp" : "127.0.0.1",
            "port" : 27017,
            "ssl" : {
                "mode" : "disabled"
            }
        },
        "processManagement" : {
            "fork" : true,
            "pidFilePath" : "/tmp/docker-entrypoint-temp-mongod.pid"
        },
        "systemLog" : {
            "destination" : "file",
            "logAppend" : true,
            "path" : "/proc/1/fd/1"
        }
    },
    "pid" : NumberLong(24),
    "buildinfo" : {
        "version" : "4.0.1",
        "gitVersion" : "54f1582fc6eb01de4d4c42f26fc133e623f065fb",
        "modules" : [],
        "allocator" : "tcmalloc",
        "javascriptEngine" : "mozjs",
        "sysInfo" : "deprecated",
        "versionArray" : [ 
            4, 
            0, 
            1, 
            0
        ],
        "openssl" : {
            "running" : "OpenSSL 1.0.2g  1 Mar 2016",
            "compiled" : "OpenSSL 1.0.2g  1 Mar 2016"
        },
        "buildEnvironment" : {
            "distmod" : "ubuntu1604",
            "distarch" : "x86_64",
            "cc" : "/opt/mongodbtoolchain/v2/bin/gcc: gcc (GCC) 5.4.0",
            "ccflags" : "-fno-omit-frame-pointer -fno-strict-aliasing -ggdb -pthread -Wall -Wsign-compare -Wno-unknown-pragmas -Winvalid-pch -Werror -O2 -Wno-unused-local-typedefs -Wno-unused-function -Wno-deprecated-declarations -Wno-unused-but-set-variable -Wno-missing-braces -fstack-protector-strong -fno-builtin-memcmp",
            "cxx" : "/opt/mongodbtoolchain/v2/bin/g++: g++ (GCC) 5.4.0",
            "cxxflags" : "-Woverloaded-virtual -Wno-maybe-uninitialized -std=c++14",
            "linkflags" : "-pthread -Wl,-z,now -rdynamic -Wl,--fatal-warnings -fstack-protector-strong -fuse-ld=gold -Wl,--build-id -Wl,--hash-style=gnu -Wl,-z,noexecstack -Wl,--warn-execstack -Wl,-z,relro",
            "target_arch" : "x86_64",
            "target_os" : "linux"
        },
        "bits" : 64,
        "debug" : false,
        "maxBsonObjectSize" : 16777216,
        "storageEngines" : [ 
            "devnull", 
            "ephemeralForTest", 
            "mmapv1", 
            "wiredTiger"
        ]
    }
}

```



