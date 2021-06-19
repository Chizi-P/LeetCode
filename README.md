# LeetCode

> **~~重點：誤人子弟~~**

#### 比如这样，第529题扫雷游戏：

```javascript
/**
 * @param {character[][]} board
 * @param {number[]} click
 * @return {character[][]}
 */
var updateBoard = (board, click) => (board[x = click[0]][y = click[1]] = board[x][y] == 'M' ? 'X' : (dfs = (x, y) => (dir = [0, [-1, 0, 1, -1, 1, -1, 0, 1], [-1, -1, -1, 0, 0, 1, 1, 1]])[1].forEach((e, i) => dir[0] += !((tx = x + e) < 0 || (ty = y + dir[2][i]) < 0 || tx >= board.length || ty >= board[0].length) && board[tx][ty] == 'M' ? 1 : 0) || (board[x][y] = dir[0] > 0 ? dir[0].toString() : 'B') == 'B' && (dir[1].forEach((e, i) => !((tx = x + e) < 0 || (ty = y + dir[2][i]) < 0 || tx >= board.length || ty >= board[0].length || board[tx][ty] != 'E') && dfs(tx, ty))))(x, y) || board[x][y]) && board;
```

