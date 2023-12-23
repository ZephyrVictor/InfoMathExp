# AES加密算法中的字节替换

## byteSub方法
- 功能：对状态矩阵进行字节替换操作
- 输入：当前加密状态的4x4字节矩阵 `state`
- 输出：替换后的新状态矩阵 `newState`

## 实现步骤
1. **创建新状态矩阵**：
   - 初始化一个空的4x4字节矩阵 `newState`。

2. **遍历并替换字节**：
   - 双层循环遍历 `state` 矩阵的每个字节。
   - 对每个字节：
     - 提取高4位作为行索引。
     - 提取低4位作为列索引。
     - 从S盒中查找对应索引的值，并存储在 `newState`。

3. **返回新状态**：
   - 完成所有替换后，返回新的状态矩阵 `newState`。