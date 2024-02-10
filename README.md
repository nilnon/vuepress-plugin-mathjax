# [vuepress-plugin-mathjax](https://vuepress.github.io/plugins/mathjax/)

## 修改申明

合并 [fix vuepress-plugin-mathjax can not support '\begin{aligned}' problem](https://github.com/vuepress/vuepress-plugin-mathjax/pull/18)

- 支持 '\begin{aligned}' 语法
- 升级mathjax-full版本

markdown ：
```
Euler's identity $e^{i\pi}+1=0$ is a beautiful formula in $\mathbb{R}^2$.

$dt, \mathrm{d}t, \partial t, \nabla\psi$

假设 $y >= 0$ , 而 $[\log x]$ 表示 $\log x$ 的整数部分, 设:

$$\Phi (y) = \frac {1} {2 \pi i} \int_{2 - i \infty}^{2 + i \infty} \frac {y^{\omega} \mathrm{d} \omega} {\omega \left(1 + \frac {\omega} {(\log x)^{1.1}}\right)^{[ \log x ] + 1}}, x > 1$$

显见， 当 $0 <= y <= 1$ 时， 有 $\Phi(y) = 0$. 对于所有 $y >= 0$, 则 $\Phi(y)$ 是一个非减函数.

当 $\log x>= 10^4$ 及 $y>= e^{2{(\log x)}^{-0.1}}$ 时， 则有:

$$1 - x^{- 0.1} <= \Phi (y) <= 1$$

$\begin{matrix}
x & y \\
z & v\end{matrix}$


$\begin{cases}
3x + 5y + z \\
7x - 2y + 4z \\
-6x + 3y + 2z
\end{cases}$

$\begin{alignat}{2}
f(x) & = (a-b)^2 \\
& = a^2-2ab+b^2
\end{alignat}$
```

效果如下：

![效果图](math.png)


[![npm](https://img.shields.io/npm/v/vuepress-plugin-mathjax.svg)](https://www.npmjs.com/package/vuepress-plugin-mathjax)
[![CircleCI](https://img.shields.io/circleci/project/github/vuepress/vuepress-plugin-mathjax/master.svg)](https://circleci.com/gh/vuepress/vuepress-plugin-mathjax)

A [VuePress](https://vuepress.vuejs.org/) plugin which supports TeX syntax in markdown files.

## Usage

```bash
npm i vuepress-plugin-mathjax-nilnon
# OR
yarn add vuepress-plugin-mathjax-nilnon
```

## Configurations

### target

- **type**: `'svg' | 'chtml'`
- **default**: `'chtml'`

The output of MathJax.

### packages

- **type**: `string | string[]`
- **default**: all the MathJax packages available

The MathJax packages to use.

### macros

- **type**: `{ [key: string]: string | null }`
- **default**: `{}`

Macros will be automatically mixed with built-in macros. To disable a built-in macro, simply set the value to `null` accordingly. Here is a list of all built-in macros:

### presets

- **type**: `string | string[]`
- **default**: `[]`

The preset content to be added. The preset content will automatically be inserted before the TeX code.

### showError

- **type**: `boolean`
- **default**: `process.env.NODE_ENV === 'development'`

Whether to output an error message in the console when a compilation error is encountered.

### cache

- **type**: `false | object`
- **default**: `{}`

[LRU Cache](https://github.com/isaacs/node-lru-cache) Options. If set to `false`, no cache will be used.

## Contribution

Contribution Welcome!
