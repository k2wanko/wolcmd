#Wake on Lan Command

コマンドラインから　MagicPacketを送れます。  
Pythonで書いてるから  
たぶんどの（Windowsのぞく）OSでもデフォルトのパッケージで使うことができます。  
ついでにzshの補完も作りました。  
主にConfigFileの設定を**スッ**と呼び出すためだけにあります。

***

##Install
```
git clone https://github.com/k2wanko/wolcmd
sudo cp ./bin/wol /usr/local/bin
cp _wol $fpath[1]
```

##Usage
```
$:wol --help
wol [options] <MAC address>                                                  
ConfigFile: $HOME/.wol/config.json
Options:
  -h, --help            show this help message and exit
  -a ADDR, --addr=ADDR  Default IP address: <broadcat>
  -p PORT, --port=PORT  Default port: 9
```

##Config
###~/.wol/config.json
```
{
  "desktop": {
      "mac":  "FF-FF-FF-FF-FF-FF"  // *
    , "addr": "<broadcat>"	        // Option
    , "port": "9"                  //  Option
  }
}
```