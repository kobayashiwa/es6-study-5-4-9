# es6-study-5-4-9
JavaScript 学習コース V > ファイルを分割しよう > 4.名前付きエクスポート

### 名前付きエクスポート（1）
名前付きエクスポートとは下の例のように、defaultを書かずに、名前を{}で囲んでエクスポートする書き方。
名前付きエクスポートした値をインポートする場合は、エクスポート時と同じ名前で値を指定する。
インポートする値は、エクスポート時と同様に、「import { 値の名前 } from "./ファイル名"」と{}で囲んで指定する。

▼ エクスポート側（dogData.js）
```
const dog1 = new Dog("レオ", 4, "チワワ"); 
export {dog1};　/* defaultを書かずに、名前を{}で囲んでエクスポート */
```
▼ インポート側（script.js）
```
import {dog1} from "./dogData"; /* 「import { 値の名前 } from "./ファイル名"」と{}で囲んで指定 */
dog1.info();
```
▼ コンソールでの出力結果
```
こんにちわ
名前はレオです
犬種はチワワです
4歳です
人間年齢で28歳です
```
