# mapserver
## what is this

+ bundle map file(arcgis bundle/bundlx)
+ static file with cors http header
支持跨域

## Run

```
docker rm -f mapserver
docker rmi `docker images |grep mapserver|awk '{ print $3}'`
docker pull light4d/mapserver
docker run --name=mapserver -d  --restart=always -p 8030:8030  -v /data/mymap:/root/file  light4d/mapserver ./mapserver httpfile --root=/root/file
```
mymap tree
```
.
├── 11
│   └── 1674
│       ├── 1201.png
│       └── 1202.png
├── 12
│   └── 3348
│       ├── 2403.png
│       └── 2404.png
├── 13
│   └── 6697
│       ├── 4807.png
│       └── 4808.png
├── 14
│   └── 13394
│       ├── 9615.png
│       └── 9616.png
├── 15
│   ├── 26788
│   │   ├── 19231.png
│   │   └── 19232.png
│   └── 26789
│       ├── 19231.png
│       └── 19232.png
├── 16
│   ├── 53577
│   │   ├── 38462.png
│   │   ├── 38463.png
│   │   └── 38464.png
│   ├── 53578
│   │   ├── 38462.png
│   │   ├── 38463.png
│   │   └── 38464.png
│   └── 53579
│       ├── 38462.png
│       ├── 38463.png
│       └── 38464.png
├── 17
│   ├── 107155
│   │   ├── 76924.png
│   │   ├── 76925.png
│   │   ├── 76926.png
│   │   ├── 76927.png
│   │   └── 76928.png
```

bundle 文件夹格式
```
.
├── L10
│   ├── R0100C0280.bundle
│   ├── R0100C0280.bundlx
│   ├── R0100C0300.bundle
│   ├── R0100C0300.bundlx
│   ├── R0180C0280.bundle
│   ├── R0180C0280.bundlx
│   ├── R0180C0300.bundle
│   └── R0180C0300.bundlx
└── L11
    ├── R0280C0580.bundle
    ├── R0280C0580.bundlx
    ├── R0280C0600.bundle
    ├── R0280C0600.bundlx
    ├── R0280C0680.bundle
    ├── R0280C0680.bundlx
    ├── R0300C0580.bundle
    ├── R0300C0580.bundlx
    ├── R0300C0600.bundle
    ├── R0300C0600.bundlx
    ├── R0300C0680.bundle
    ├── R0300C0680.bundlx
    ├── R0380C0600.bundle
    ├── R0380C0600.bundlx
    ├── R0380C0680.bundle
    └── R0380C0680.bundlx

2 directories, 24 files
```
