# OpenCC  開放中文轉換 R 语言接口

Linux : [![Build Status](https://travis-ci.org/qinwf/ropencc.svg?branch=master)](https://travis-ci.org/qinwf/rpoencc)　Mac : [![Build Status](https://travis-ci.org/qinwf/ropencc.svg?branch=osx)](https://travis-ci.org/qinwf/ropencc)　Win : [![Build status](https://ci.appveyor.com/api/projects/status/db2nv83wk97x6mwj/branch/master?svg=true)](https://ci.appveyor.com/project/qinwf/ropencc/branch/master)


Windows 用户需要安装 RTools，https://cran.r-project.org/bin/windows/Rtools/ ，安装时注意 PATH 的设置。

```r
devtools::install_github("qinwf/ropencc")

converter(S2T)["开放中文转换"]
converter(S2TW)["一条信息"]
converter(S2TWP)["一条信息"]
converter(S2HK)["一条信息"]
converter(T2S)["開放中文轉換"]
converter(T2HK)["開放中文轉換"]
converter(T2TW)["開放中文轉換"]
converter(TW2S)["開放中文轉換"]
converter(TW2SP)["一條資訊"]
converter(HK2S)["開放中文轉換"]

cc = converter(HK2S)
run_convert(cc, "開放中文轉換")
```

預設配置文件

    s2t.json Simplified Chinese to Traditional Chinese 簡體到繁體
    t2s.json Traditional Chinese to Simplified Chinese 繁體到簡體
    s2tw.json Simplified Chinese to Traditional Chinese (Taiwan Standard) 簡體到臺灣正體
    tw2s.json Traditional Chinese (Taiwan Standard) to Simplified Chinese 臺灣正體到簡體
    s2hk.json Simplified Chinese to Traditional Chinese (Hong Kong Standard) 簡體到香港繁體（香港小學學習字詞表標準）
    hk2s.json Traditional Chinese (Hong Kong Standard) to Simplified Chinese 香港繁體（香港小學學習字詞表標準）到簡體
    s2twp.json Simplified Chinese to Traditional Chinese (Taiwan Standard) with Taiwanese idiom 簡體到繁體（臺灣正體標準）並轉換爲臺灣常用詞彙
    tw2sp.json Traditional Chinese (Taiwan Standard) to Simplified Chinese with Mainland Chinese idiom 繁體（臺灣正體標準）到簡體並轉換爲中國大陸常用詞彙
    t2tw.json Traditional Chinese (OpenCC Standard) to Taiwan Standard 繁體（OpenCC 標準）到臺灣正體
    t2hk.json Traditional Chinese (OpenCC Standard) to Hong Kong Standard 繁體（OpenCC 標準）到香港繁體（香港小學學習字詞表標準）
