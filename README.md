# aki


```
パンを買う
パンを焼く
クリームを塗る
パンを食う

朝ごはんを準備(){
 パンを買う
 パンを焼く
 クリームを塗る
}
朝ごはんを食う

彼女.朝ごはんを準備()
朝ごはんを食う
```

# オブジェクト指向

OOP： object oriented programming

### オブジェクトとは：物

### クラス：`抽象化`したモデル

- project　→　package　→　class

### オブジェクトが何か持つ

- 属性

  - データ型
  - 名前

  ```java
  private String name;
  private int age;
  ```

- メソッド

  - アクセス修飾子
      - public : どこからでもアクセス可能とする修飾子
      - protected: 同じパッケージ内のクラスや違うパッケージでも、そのクラスを継承したサブクラス内部からアクセスすることを可能とします。
      - default: 同じパッケージ内のすべてのクラスからアクセスすることが可能です。
      - private: クラス内部からのみ、アクセスが可能です。
  - 戻り値 
  - メソッド名
  - パラメータ


  ```
  prepareBreakfast(){
  	パンを買う;
    パンを焼く;
      クリームを塗る;
  }
  ```

  

### オブジェクト三つの特徴：

- 	カプセル: 情報隠蔽
```
	private int volume;
	private string channel;
	
	public int getVolume(){
		return this.volume;
	}
	public int setVolume(int volume){
		this.volume = volume;
	}
```

- 継承: 継承関係（A is B）

- ポリモーフィズム: 

  - 	オーバーライド：オーバーライドとは、スーパクラスから継承されたサブクラスにおいて、メンバ関数を独自の機能で上書きすることである。（上書きする）
  - 	オーバーロード：引数や戻り値が異なるが名称が同一のメソッドを複数定義する
     - 	同じクラス内

  ### オブジェクト指向実装

  - インタフェース
    - マーカーインタフェース: Serializable
    - 関数型インターフェース: Function
    
  - 内部クラス
  
    - ```java
      public class Outer {
          private int outerVal;
      
          public class Inner {
              public int innerVal;
              private void method() {
                  // OK
                  this.innerVal = Outer.this.outerVal;
              }
          }
      
          private void method() {
              // NG
              // this.outerVal = innerVal;
          }
      }
      ```
  
    - 

# オブジェクト指向設計原則

- 単一責任の原則: 1つのクラスに1つの役割(機能)
- オープン・クローズドの原則: クラスは拡張に対して開いていて、修正に対して閉じていなければならない
- リスコフの置換原則: 基本クラスを使っている場所で基本クラスの代わりにサブクラスを使っても問題なく動かなけらばならない
- 依存関係逆転の原則: 上位のモジュールは下位のモジュールに依存してはならない。どちらのモジュールも「抽象」に依存すべきである。
- インターフェース分離の法則: インターフェースはシンプルにしなさい



Javadoc: 　クラス、メソッドに対するドキュメント

「ドキュメントを作るのが面倒なので，プログラム中に特定のルールに従って付けたコメントを抽出してドキュメントを作っちゃう」考え方に沿って，Java言語のソースコードからドキュメントを生成する仕組みです．これにより，ドキュメントファイルを紛失することも無くなります．



