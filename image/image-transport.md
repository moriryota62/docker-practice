[TOP](../README.md)   
前: [まとめ](./image-summary.md)  
次: -  

---

# イメージの手動運搬

コンテナイメージはイメージレジストリで共有するのが望ましいです。ですが、開発と本番などネットワーク的に分離する必要がある場合もあります。その様な場合、イメージをtarに固めてファイルとして送ることもできます。

1. ホストOS内部にあるコンテナイメージを確認し、その内の1つを``manual-trasport``というイメージ名にしてください。この時選ぶイメージはできれば転送先のもう1台のサーバにないイメージが良いです。

2. 以下のコマンドでイメージをtarにしてください。
   ``` sh
   docker save -o manual-transport.tar manual-transport
   ```

3. カレントディレクトリに``manual-trasport.tar``があることを確認してください。

4. ``manual-trasport.tar``をもう1台のサーバにscpなどで転送してください。

ここからはもう1台のサーバで作業します。

5. ``manual-trasport``という名前のイメージがないことを確認してください。

6. 以下コマンドで``manual-trasport.tar``をインポートします。
   ``` sh
   docker load -i manual-trasport.tar
   ```

7. ``manual-trasport``という名前のイメージがあることを確認してください。また、``manual-trasport``の``IMAGE ID``が2台のサーバで一致していることを確認してください。

ここからは両方のサーバで同じ作業します。

8. ``manual-trasport``イメージを削除してください。

9. ``manual-trasport.tar``を削除してください。

このようにしてイメージを手動で運搬することもできます。運搬したあとはその環境のレジストリサーバ名などのイメージ名にタグ打ちし直してpushすれば環境内で共有できます。なお、イメージの``IMAGE ID``はイメージのハッシュ値が使われています。そのため、ハッシュ値を見ればイメージ名が違くてもイメージの中身が同じか判別できます。

---

[TOP](../README.md)   
前: [まとめ](./image-summary.md)  
次: -  
