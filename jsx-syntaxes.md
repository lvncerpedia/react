JSX（JavaScript XML）だね！Reactで使う特別な書き方で、**JavaScriptの拡張構文**って感じ✨

これはJSの三項演算子をJSXの中で使ってるパターンで、超よく出てくる書き方だよ！

## 知っておくべき文法・パターン

**① && 演算子（条件付きレンダリング）**
```jsx
{hasError && <p>エラーです</p>}
// hasErrorがtrueの時だけ<p>を表示
```
あなたのコードがまさにコレ！

---

**② 三項演算子**
```jsx
{isLoggedIn ? <Dashboard /> : <Login />}
// 条件 ? trueの時 : falseの時
```

---

**③ map（リストのレンダリング）**
```jsx
{items.map(item => (
  <li key={item.id}>{item.name}</li>
))}
// 配列を<li>に変換して表示
```
`key`は必須！忘れると怒られるやつw

---

**④ スプレッド構文**
```jsx
const props = { name: "太郎", age: 20 };
<User {...props} />
// = <User name="太郎" age={20} />
```

---

**⑤ 分割代入（props受け取り）**
```jsx
// よくある書き方
const MyComponent = ({ title, onClick }) => {
  return <button onClick={onClick}>{title}</button>;
};
```

---

**⑥ テンプレートリテラル**
```jsx
<div className={`btn ${isActive ? "active" : ""}`}>
  {`こんにちは、${name}さん`}
</div>
```

---

**⑦ オプショナルチェーン**
```jsx
{user?.profile?.avatar && <img src={user.profile.avatar} />}
// userがundefinedでもエラーにならない！
```

---

この中で特に①②③は**Reactの頻出3トップ**って感じ。まずこの3つ使いこなせれば大体のUI書けるよ〜！どれか詳しく知りたいのある？
