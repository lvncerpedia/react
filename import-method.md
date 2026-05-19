# Import methods

import時の {} の有無は、相手（エクスポート側）の書き方で決まります。

###  {} なし

相手が export default している場合（1ファイル1機能に多い）

```tsx
import Header from './Header';
```

```tsx
const Header = () => { ... };
export default Header;
```


### {} あり

相手が export している場合（1ファイルに複数機能ある場合に多い）

```tsx
import { Header } from './components';
```

```tsx
export const Header = () => { ... };
```
