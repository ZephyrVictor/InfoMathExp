# 乘法函数流程（`multiply`）

- ## 初始化
  - `result = 0`
  - 输入: `a1`, `a2`, `poly`

- ## 循环处理 (共 8 次)
  - ### 检查 `a2` 的最低位
    - 如果 `a2 & 1` 不为 0
      - `result = result XOR a1`

  - ### 左移 `a1`
    - `a1 = a1 << 1`

  - ### 模运算
    - 检查 `a1` 的最高位（第 9 位）
      - 如果 `a1 & 0x100` 不为 0
        - `a1 = a1 XOR poly`

  - ### 保持 `a1` 在 8 位内
    - `a1 = a1 & 0xFF`

  - ### 右移 `a2`
    - `a2 = a2 >> 1`

- ## 返回结果
  - `return result`