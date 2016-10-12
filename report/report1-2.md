#第一回 課題1-2: スイッチの切断イベント

##提出者
氏名：木藤嵩人

##課題内容
仮想スイッチを停止したら、コントローラで次のメッセージを表示するようにしてみよう:
```
Bye 0xabc
```

##解答
サンプルプログラムに以下を追加した

```
　　def switch_disconnected(datapath_id)
    logger.info "Bye #{datapath_id.to_hex}!"
  end
```
switch_disconnectedは、スイッチの接続が切断された時に呼び出されるため、datapath_idを引数として切断されたスイッチを表示するようにした。
