# [2544. 交替数字和](https://leetcode.cn/problems/alternating-digit-sum)

[English Version](/solution/2500-2599/2544.Alternating%20Digit%20Sum/README_EN.md)

## 题目描述

<!-- 这里写题目描述 -->

<p>给你一个正整数 <code>n</code> 。<code>n</code> 中的每一位数字都会按下述规则分配一个符号：</p>

<ul>
	<li><strong>最高有效位</strong> 上的数字分配到 <strong>正</strong> 号。</li>
	<li>剩余每位上数字的符号都与其相邻数字相反。</li>
</ul>

<p>返回所有数字及其对应符号的和。</p>

<p>&nbsp;</p>

<p><strong>示例 1：</strong></p>

<pre>
<strong>输入：</strong>n = 521
<strong>输出：</strong>4
<strong>解释：</strong>(+5) + (-2) + (+1) = 4</pre>

<p><strong>示例 2：</strong></p>

<pre>
<strong>输入：</strong>n = 111
<strong>输出：</strong>1
<strong>解释：</strong>(+1) + (-1) + (+1) = 1
</pre>

<p><strong>示例 3：</strong></p>

<pre>
<strong>输入：</strong>n = 886996
<strong>输出：</strong>0
<strong>解释：</strong>(+8) + (-8) + (+6) + (-9) + (+9) + (-6) = 0
</pre>

<p>&nbsp;</p>

<p><strong>提示：</strong></p>

<ul>
	<li><code>1 &lt;= n &lt;= 10<sup>9</sup></code></li>
</ul>

<p>&nbsp;</p>

## 解法

<!-- 这里可写通用的实现逻辑 -->

<!-- tabs:start -->

### **Python3**

<!-- 这里可写当前语言的特殊实现逻辑 -->

```python
class Solution:
    def alternateDigitSum(self, n: int) -> int:
        ans, sign = 0, 1
        for c in str(n):
            x = int(c)
            ans += sign * x
            sign *= -1
        return ans
```

### **Java**

<!-- 这里可写当前语言的特殊实现逻辑 -->

```java
class Solution {
    public int alternateDigitSum(int n) {
        int ans = 0, sign = 1;
        for (char c : String.valueOf(n).toCharArray()) {
            int x = c - '0';
            ans += sign * x;
            sign *= -1;
        }
        return ans;
    }
}
```

### **C++**

```cpp
class Solution {
public:
    int alternateDigitSum(int n) {
        int ans = 0, sign = 1;
        for (char c : to_string(n)) {
            int x = c - '0';
            ans += sign * x;
            sign *= -1;
        }
        return ans;
    }
};
```

### **Go**

```go
func alternateDigitSum(n int) int {
	ans, sign := 0, 1
	for _, c := range strconv.Itoa(n) {
		x := int(c - '0')
		ans += sign * x
		sign *= -1
	}
	return ans
}
```

### **...**

```

```

<!-- tabs:end -->