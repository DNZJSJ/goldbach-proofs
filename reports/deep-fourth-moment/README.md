# 深次弧四阶矩上界的 Lean 反证

研究台题号 `L-goldbach-frontier-deep-fourth-moment-conjecture`。设 `R = floor(n^(1/3))`。取素数分母 `R < q ≤ 4R`，在各既约有理点的左右各取宽度 `1/(20n)`。这些区间互不相交，全部落在原命题定义的深次弧中。

对固定分母，有限加性特征求和给出精确抵消关系。结合素数权重总量下界和 Hölder 不等式，每个分母至少给出常数乘以 `n^2` 的四阶矩贡献。Chebyshev 估计给出至少 `n^(1/4)` 个分母，所以原积分至少为 `n^(9/4) / 41943040`，最终超过原题在 `η = 1/8` 时的上界。这项结论适用于该题的绝对四阶矩。

## 复核

在研究台的 Lean 环境中运行 `lake env lean /path/to/GoldbachDeepFourthMomentCounterexample.lean`。使用 Lean 4.36.0 和 Mathlib 提交 `fc4f59e577feb1a4956671bc04ac18aaaf8cd842`。文件只导入 Mathlib。检查的定理名是 `GoldbachFourthMoment.deep_fourth_moment_false`，其命题是官网发布声明的否定。文件最后打印该定理的公理依赖。

有限特征求和的形式化步骤参考了 DFQDZZ 的已公开证明。 [出处](https://github.com/CGandGameEngineLearner/goldbach-proofs/pull/316)
