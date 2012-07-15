# 概要
xml → XML Schemaファイル → JAXB エンティティ、の変換を行うツール


# 使用方法
## build.propertiesのxml.name、jaxb.package、jaxb.package.dirを各自の設定に修正

* xml.name = 対象となるxmlファイルの名前
* jaxb.package = 生成するJAXBエンティティのpackage
* jaxb.package.dir = packageに該当するsrcディレクトリ下のディレクトリ


```
xml.name=hoge
jaxb.package=com.gmail.jpshadowapps.gae.ekiapi.api.jaxb
jaxb.package.dir=com/gmail/jpshadowapps/gae/ekiapi/api/jaxb
```

## 対象となるxmlファイルをxmlディレクトリ下に作成
```
% vi xml/hoge.xml
```


## "all" ターゲットをbuild
```
% ant all
```

xsdディレクトリにXML Schemaファイルが、srcディレクトリにJAXB エンティティが生成される
