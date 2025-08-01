# Day-5 作业打分结果

## 分数汇总表

| 学生姓名 | hw5_1得分 | hw5_2得分 | 总分 |
|---------|----------|----------|------|
| 庄华翔 | 5/5 | 5/5 | 16 |
| 牟昱榕 | 5/5 | 5/5 | 16 |
| 王宬皓 | 5/5 | 5/5 | 16 |
| 王恩曦 | 5/5 | 5/5 | 15 |
| 朱雨夏 | 4/5 | 5/5 | 14 |
| 王扬 | 4/5 | 5/5 | 14 |
| 蔡纪坤 | 4/5 | 5/5 | 14 |
| 何欣喆 | 4/5 | 5/5 | 14 |
| 申益泽 | 4/5 | 5/5 | 14 |
| 厉致远 | 4/5 | 5/5 | 13 |
| 吴劭劼 | 4/5 | 4/5 | 13 |
| 吴奇峰 | 4/5 | 5/5 | 13 |
| 方世成 | 4/5 | 5/5 | 13 |
| 谢志得 | 4/5 | 5/5 | 12 |
| 祝杰 | 4/5 | 4/5 | 12 |
| 于文阔 | 4/5 | 4/5 | 12 |
| 周家正 | 4/5 | 4/5 | 12 |
| 陈敬麒 | 4/5 | 4/5 | 12 |
| 吴乾奕 | 4/5 | 3/5 | 11 |
| 王子乐 | 3/5 | 3/5 | 10 |
| 刘玚 | 3/5 | 5/5 | 8 |

## 详细评分

### 蔡纪坤

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. 1.1.1 权重矩阵Shape: ✓ (1024×1024 正确)
2. 1.1.2 输入张量Shape: ✓ (8×128×1024 正确)
3. 1.1.3 输出张量拼接: ✓ (正确描述了拼接过程)
4. 1.2.1 权重矩阵Shape: ✓ (1024×1024 正确)
5. 1.2.2 输入张量Shape: ✓ (8×128×1024 正确)
6. 1.2.3 输出张量汇总: ✓ (All-Reduce汇总正确)
7. 2.1.1 Linear1前向通信: ✓ (正确，不需要通信)
8. 2.1.2 Linear1反向通信: ✓ (All-Reduce分析正确)
9. 2.2.1 Linear2前向通信: ✗ (通信量计算错误，应该是BxSxd而非(P-1)xBxSxd)
10. 2.2.2 Linear2反向通信: ✓ (正确，不需要通信) 
11. 第3题并行策略组合: ✗ (分析过于简单，缺乏深度)

**总得分: 9/11 → floor(9/2) = 4分**

#### hw5_2 评分 (总分: 5/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✓ (66ms正确)
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✓ (1.375正确)
4. 第2题microbatch增加分析: ✓ (计算和分析正确)
5. 第3题1F1B优化分析: ✓ (分析较为全面)

**总得分: 5/5分**

**备注:** hw5_1作业中多个关键概念理解有误，特别是通信分析部分；hw5_2作业完成较好。

### 陈敬麒

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. 1.1.1 权重矩阵Shape: ✓ (1024×1024 正确)
2. 1.1.2 输入张量Shape: ✓ (8×128×1024 正确)
3. 1.1.3 输出张量拼接: ✓ (正确描述了拼接过程)
4. 1.2.1 权重矩阵Shape: ✓ (1024×1024 正确)
5. 1.2.2 输入张量Shape: ✓ (8×128×1024 正确)
6. 1.2.3 输出张量汇总: ✓ (All-Reduce汇总正确)
7. 2.1.1 Linear1前向通信: ✗ (错误，Column Parallel前向不需要通信)
8. 2.1.2 Linear1反向通信: ✓ (All-Reduce分析正确)
9. 2.2.1 Linear2前向通信: ✗ (通信量计算错误，应该是BxSxd而非(P-1)xBxSxd)
10. 2.2.2 Linear2反向通信: ✓ (正确，不需要通信)
11. 第3题并行策略组合: ✗ (Row Parallel分析错误，Column Parallel分析过于简单)

**总得分: 8/11 → floor(8/2) = 4分**

#### hw5_2 评分 (总分: 4/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✗ (公式错误，应该是(m+p-1)×(tf+tb))
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✓ (1.375正确)
4. 第2题microbatch增加分析: ✓ (计算和分析正确)
5. 第3题1F1B优化分析: ✓ (分析较为全面)

**总得分: 4/5分**

**备注:** hw5_1通信分析部分存在错误，hw5_2总时间公式理解有误但计算结果正确。

### 方世成

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. 1.1.1 权重矩阵Shape: ✓ (1024×1024 正确)
2. 1.1.2 输入张量Shape: ✓ (8×128×1024 正确)
3. 1.1.3 输出张量拼接: ✗ (错误，说不需要All-Gather但实际需要拼接)
4. 1.2.1 权重矩阵Shape: ✓ (1024×1024 正确)
5. 1.2.2 输入张量Shape: ✓ (8×128×1024 正确)
6. 1.2.3 输出张量汇总: ✓ (All-Reduce汇总正确)
7. 2.1.1 Linear1前向通信: ✓ (正确，不需要通信)
8. 2.1.2 Linear1反向通信: ✓ (All-Reduce分析正确)
9. 2.2.1 Linear2前向通信: ✗ (通信量计算错误，应该是BxSxd而非2×BxSxd)
10. 2.2.2 Linear2反向通信: ✓ (正确，不需要通信)
11. 第3题并行策略组合: ✗ (Row Parallel分析错误，Column Parallel分析过于简单)

**总得分: 9/11 → floor(9/2) = 4分**

#### hw5_2 评分 (总分: 5/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✓ (66ms正确)
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✓ (11/8=1.375正确)
4. 第2题microbatch增加分析: ✓ (计算和分析正确)
5. 第3题1F1B优化分析: ✓ (分析全面，包含内存优化)

**总得分: 4/5分**

**备注:** hw5_1通信分析部分存在部分错误，hw5_2作业完成优秀，分析深入。

### 何欣喆

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. 1.1.1 权重矩阵Shape: ✓ (1024×1024 正确)
2. 1.1.2 输入张量Shape: ✓ (8×128×1024 正确)
3. 1.1.3 输出张量拼接: ✓ (正确描述了拼接过程)
4. 1.2.1 权重矩阵Shape: ✓ (1024×1024 正确)
5. 1.2.2 输入张量Shape: ✓ (8×128×1024 正确)
6. 1.2.3 输出张量汇总: ✓ (All-Reduce汇总正确)
7. 2.1.1 Linear1前向通信: ✗ (错误，说需要AllGather通信，实际不需要)
8. 2.1.2 Linear1反向通信: ✓ (正确，不需要通信)
9. 2.2.1 Linear2前向通信: ✗ (错误，说需要AllReduce，实际不需要通信)
10. 2.2.2 Linear2反向通信: ✓ (正确，不需要通信)
11. 第3题并行策略组合: ✓ (Row Parallel和Column Parallel分析基本正确)

**总得分: 9/11 → floor(9/2) = 4分**

#### hw5_2 评分 (总分: 5/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✗ (公式错误，应该是(tf+tb)×(m+p-1)，但计算结果66ms正确)
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✓ (1.375正确)
4. 第2题microbatch增加分析: ✓ (分析正确，公式推导清晰)
5. 第3题1F1B优化分析: ✓ (分析全面，包含内存和通信优化)

**总得分: 4/5分**

**备注:** hw5_1通信分析存在多处错误，hw5_2总时间公式理解有误但计算正确，整体分析较好。

### 厉致远

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. 1.1.1 权重矩阵Shape: ✓ (1024×1024 正确)
2. 1.1.2 输入张量Shape: ✓ (8×128×1024 正确)
3. 1.1.3 输出张量拼接: ✓ (拼接得到8×128×4096正确)
4. 1.2.1 权重矩阵Shape: ✓ (1024×1024 正确)
5. 1.2.2 输入张量Shape: ✓ (8×128×1024 正确)
6. 1.2.3 输出张量汇总: ✓ (All-Reduce汇总正确)
7. 2.1.1 Linear1前向通信: ✗ (错误，说需要All-gather通信，实际不需要)
8. 2.1.2 Linear1反向通信: ✗ (正确识别需要All-Reduce) 
9. 2.2.1 Linear2前向通信: ✗ (错误，说需要All-Reduce，实际不需要通信)
10. 2.2.2 Linear2反向通信: ✓ (正确，不需要通信)
11. 第3题并行策略组合: ✗ (Row Parallel分析错误，Column Parallel分析不准确)

**总得分: 7/11 → floor(7/2) = 3分**

#### hw5_2 评分 (总分: 4/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✓ (66ms正确)
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✓ (1.375正确)
4. 第2题microbatch增加分析: ✓ (计算和分析正确)
5. 第3题1F1B优化分析: ✗ (分析过于简单，缺乏深度)

**总得分: 4/5分**

**备注:** hw5_1通信分析存在多处错误，hw5_2分析基本正确但1F1B优化分析不够深入。

### 刘玚

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. 1.1.1 权重矩阵Shape: ✗ (错误，1024×256应为1024×1024)
2. 1.1.2 输入张量Shape: ✓ (8×128×1024 正确)
3. 1.1.3 输出张量拼接: ✗ (错误，输出维度和拼接方式都错误)
4. 1.2.1 权重矩阵Shape: ✓ (1024×1024 正确)
5. 1.2.2 输入张量Shape: ✗ (错误，8×128×256应为8×128×1024)
6. 1.2.3 输出张量汇总: ✗ (错误，应该是All-Reduce求和而非AllGather)
7. 2.1.1 Linear1前向通信: ✗ (错误，Column Parallel前向不需要通信)
8. 2.1.2 Linear1反向通信: ✗ (错误，应该需要All-Reduce通信)
9. 2.2.1 Linear2前向通信: ✗ (错误，应该是All-Reduce而非AllGather)
10. 2.2.2 Linear2反向通信: ✗ (错误，应该不需要通信)
11. 第3题并行策略组合: ✓ (分析基本正确)

**总得分: 3/11 → floor(3/2) = 1分**

#### hw5_2 评分 (总分: 5/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✓ (66ms正确)
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✓ (1.375正确)
4. 第2题microbatch增加分析: ✓ (计算和分析正确)
5. 第3题1F1B优化分析: ✓ (分析全面深入)

**总得分: 5/5分**

**备注:** hw5_1张量shape计算和通信分析存在较多错误，hw5_2作业完成优秀。

### 牟昱榕

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. 1.1.1 权重矩阵Shape: ✓ (1024×1024 正确)
2. 1.1.2 输入张量Shape: ✓ (8×128×1024 正确)
3. 1.1.3 输出张量拼接: ✓ (正确描述了拼接过程)
4. 1.2.1 权重矩阵Shape: ✓ (1024×1024 正确)
5. 1.2.2 输入张量Shape: ✓ (8×128×1024 正确)
6. 1.2.3 输出张量汇总: ✓ (All-Reduce汇总正确)
7. 2.1.1 Linear1前向通信: ✓ (正确，不需要通信)
8. 2.1.2 Linear1反向通信: ✓ (All-Reduce分析正确)
9. 2.2.1 Linear2前向通信: ✓ (All-Reduce分析正确)
10. 2.2.2 Linear2反向通信: ✓ (正确，不需要通信)
11. 第3题并行策略组合: ✓ (分析深入准确)

**总得分: 11/11 → 5分**

#### hw5_2 评分 (总分: 5/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✓ (66ms正确)
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✓ (1.375正确)
4. 第2题microbatch增加分析: ✓ (计算和分析正确)
5. 第3题1F1B优化分析: ✓ (分析全面深入)

**总得分: 5/5分**

**备注:** 牟昱榕同学两个作业都完成优秀，所有知识点掌握准确，分析深入。

### 申益泽

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. 1.1.1 权重矩阵Shape: ✓ (1024×1024 正确)
2. 1.1.2 输入张量Shape: ✓ (8×128×1024 正确)
3. 1.1.3 输出张量拼接: ✗ (错误，输出应为[8, 128, 1024]，理解有误)
4. 1.2.1 权重矩阵Shape: ✓ (1024×1024 正确)
5. 1.2.2 输入张量Shape: ✓ (8×128×1024 正确)
6. 1.2.3 输出张量汇总: ✓ (All-Reduce汇总正确)
7. 2.1.1 Linear1前向通信: ✓ (正确，不需要通信)
8. 2.1.2 Linear1反向通信: ✓ (All-Reduce分析正确)
9. 2.2.1 Linear2前向通信: ✓ (All-Reduce分析正确)
10. 2.2.2 Linear2反向通信: ✗ (错误，应该不需要通信)
11. 第3题并行策略组合: ✓ (分析基本正确)

**总得分: 9/11 → floor(9/2) = 4分**

#### hw5_2 评分 (总分: 4/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✓ (66ms正确)
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✓ (1.375正确)
4. 第2题microbatch增加分析: ✓ (计算正确，原因分析基本正确)
5. 第3题1F1B优化分析: ✗ (分析过于简单，缺乏深度)

**总得分: 4/5分**

**备注:** hw5_1在张量shape表述和部分通信分析存在错误，hw5_2计算正确但1F1B优化分析不够深入。

### 王扬

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. Linear1权重矩阵shape: ✓ (1024×1024 正确)
2. Linear1输入张量shape: ✓ (8×128×1024 正确)
3. Linear1输出张量拼接: ✓ (正确描述了拼接过程)
4. Linear2权重矩阵shape: ✓ (1024×1024 正确)
5. Linear2输入张量shape: ✓ (8×128×1024 正确)
6. Linear2输出张量汇总: ✓ (All-Reduce汇总正确)
7. Linear1前向通信: ✓ (正确，不需要通信)
8. Linear1反向通信: ✓ (All-Reduce分析正确)
9. Linear2前向通信: ✗ (通信量计算错误，应该是BxSxd而非PxBxSxd)
10. Linear2反向通信: ✓ (正确，不需要通信)
11. 第3题并行策略组合: ✗ (分析不够准确，缺乏深度)

**总得分: 9/11 → floor(9/2) = 4分**

#### hw5_2 评分 (总分: 5/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✓ (66ms正确)
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✓ (1.375正确)
4. 第2题microbatch增加分析: ✓ (计算和分析正确)
5. 第3题1F1B优化分析: ✓ (分析全面深入)

**总得分: 5/5分**

**备注:** hw5_1通信量计算和并行策略组合分析存在错误，hw5_2表现优秀。

### 王子乐

#### hw5_1 评分 (总分: 3/5)

**得分点分析:**
1. Linear1权重矩阵shape: ✓ (1024×1024 正确) 
2. Linear1输入张量shape: ✓ (8×128×1024 正确)
3. Linear1输出张量拼接: ✗ (错误，说要做All-gather，实际Column Parallel输出是直接拼接)
4. Linear2权重矩阵shape: ✓ (1024×1024 正确)
5. Linear2输入张量shape: ✓ (8×128×1024 正确)
6. Linear2输出张量汇总: ✓ (All-Reduce汇总正确) 
7. Linear1前向通信: ✗ (错误，说需要Broadcast，实际不需要通信)
8. Linear1反向通信: ✓ (All-Reduce分析正确)
9. Linear2前向通信: ✗ (通信量计算错误，应该是BxSxd而非2(P-1)xBxSxd)
10. Linear2反向通信: ✗ (错误，说需要All-gather，实际不需要通信)
11. 第3题并行策略组合: ✓ (基本正确识别了两种组合的问题)

**总得分: 7/11 → floor(7/2) = 3分**

#### hw5_2 评分 (总分: 3/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✗ (错误，计算结果为72ms，正确答案应为66ms)
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✗ (由于总时间计算错误，Bubble Ratio也错误)
4. 第2题microbatch增加分析: ✓ (正确分析了变小趋势和原因)
5. 第3题1F1B优化分析: ✓ (正确分析了1F1B优化点)

**总得分: 3/5分**

**备注:** hw5_1多个得分点存在错误，hw5_2总时间计算错误。

### 王宬皓

#### hw5_1 评分 (总分: 5/5)

**得分点分析:**
1. Linear1权重矩阵shape: ✓ (1024×1024 正确)
2. Linear1输入张量shape: ✓ (8×128×1024 正确)
3. Linear1输出张量拼接: ✓ (正确描述了All-Gather拼接)
4. Linear2权重矩阵shape: ✓ (1024×1024 正确)
5. Linear2输入张量shape: ✓ (8×128×1024 正确)
6. Linear2输出张量汇总: ✓ (All-Reduce求和正确)
7. Linear1前向通信: ✓ (All-Gather通信量计算正确)
8. Linear1反向通信: ✓ (All-Reduce分析正确)
9. Linear2前向通信: ✓ (All-Reduce通信量计算正确)
10. Linear2反向通信: ✓ (All-Gather分析正确)
11. 第3题并行策略组合: ✓ (两种情况分析都准确)

**总得分: 11/11 → 5分**

#### hw5_2 评分 (总分: 5/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✓ (66ms正确)
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✓ (1.375正确)
4. 第2题microbatch增加分析: ✓ (1.1875，原因分析准确)
5. 第3题1F1B优化分析: ✓ (分析深入，包含内存优化、利用率提升等)

**总得分: 5/5分**

**备注:** hw5_1所有得分点均正确，分析深入；hw5_2计算准确，1F1B优化分析全面深入。

### 王恩曦

#### hw5_1 评分 (总分: 3/5)

**得分点分析:**
1. Linear1权重矩阵shape: ✓ (1024×1024 正确)
2. Linear1输入张量shape: ✓ (8×128×1024 正确)
3. Linear1输出张量拼接: ✓ (正确描述了All-Gather拼接得到8×128×4096)
4. Linear2权重矩阵shape: ✓ (1024×1024 正确)
5. Linear2输入张量shape: ✓ (8×128×1024 正确)
6. Linear2输出张量汇总: ✓ (All-Reduce求和正确)
7. Linear1前向通信: ✓ (正确，不需要通信)
8. Linear1反向通信: ✓ (通信量计算正确)
9. Linear2前向通信: ✓ (All-Reduce通信量计算正确)
10. Linear2反向通信: ✓ (正确，不需要通信)
11. 第3题并行策略组合: ✗ (分析过于简单，缺乏深度)

**总得分: 10/11 → floor(10/2) = 5分**

#### hw5_2 评分 (总分: 4/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✓ (66ms正确，推导过程详细)
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✓ (1.375正确)
4. 第2题microbatch增加分析: ✓ (1.1875，气泡分析深入)
5. 第3题1F1B优化分析: ✗ (分析过于简单，缺乏深度)

**总得分: 4/5分**

**备注:** hw5_1在Linear1前向通信和并行策略组合分析存在错误，hw5_2计算正确但1F1B优化分析不够深入。

### 吴奇峰

#### hw5_1 评分 (总分: 3/5)

**得分点分析:**
1. Linear1权重矩阵shape: ✓ (1024×1024 正确)
2. Linear1输入张量shape: ✓ (8×128×1024 正确)
3. Linear1输出张量拼接: ✓ (正确描述了通过AllGather拼接)
4. Linear2权重矩阵shape: ✓ (1024×1024 正确)
5. Linear2输入张量shape: ✓ (8×128×1024 正确)
6. Linear2输出张量汇总: ✓ (正确描述了通过AllReduce求和)
7. Linear1前向通信: ✗ (错误认为不需要通信，实际需要确保每个rank都有完整的X)
8. Linear1反向通信: ✓ (正确识别需要AllReduce)
9. Linear2前向通信: ✗ (错误计算通信量为24MB，实际应为4MB)
10. Linear2反向通信: ✓ (正确识别不需要通信)
11. 第3题并行策略组合: ✗ (分析过于简单，缺乏具体的通信操作描述)

**总得分: 7/11 → floor(7/2) = 3分**

#### hw5_2 评分 (总分: 5/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✓ (66ms正确) 
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✓ (1.375正确) 
4. 第2题microbatch增加分析: ✓ (正确分析了变化趋势和原因)
5. 第3题1F1B优化分析: ✓ (分析了并行度提升和延迟降低，但不够深入)

**总得分: 5/5分**

**备注:** hw5_1前向通信和通信量计算错误，hw5_2 Bubble Ratio定义错误。

### 吴乾奕

#### hw5_1 评分 (总分: 3/5)

**得分点分析:**
1. 1.1.1 权重矩阵Shape: ✓ (1024×1024 正确)
2. 1.1.2 输入张量Shape: ✓ (8×128×1024 正确)
3. 1.1.3 输出张量拼接: ✓ (正确描述了按列拼接)
4. 1.2.1 权重矩阵Shape: ✓ (1024×1024 正确)
5. 1.2.2 输入张量Shape: ✓ (8×128×1024 正确)
6. 1.2.3 输出张量汇总: ✓ (正确描述了通过All-Reduce相加)
7. 2.1.1 Linear1前向通信: ✗ (错误认为需要All-Gather拼接输出，实际前向不需要通信)
8. 2.1.2 Linear1反向通信: ✓ (正确识别需要All-Reduce)
9. 2.2.1 Linear2前向通信: ✗ (错误认为不需要通信，实际需要All-Reduce)
10. 2.2.2 Linear2反向通信: ✗ (错误认为需要All-Gather，实际不需要通信)
11. 第3题并行策略组合: ✓ (正确分析了两种组合的问题)

**总得分: 8/11 → floor(8/2) = 4分**

#### hw5_2 评分 (总分: 3/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✓ (66ms正确)
2. 1.2 理想时间计算: ✗ (错误计算为12ms，应为48ms)
3. 1.3 Bubble Ratio计算: ✗ (错误计算为5.5，应为1.375)
4. 第2题microbatch增加分析: ✓ (正确分析了变化趋势和原因)
5. 第3题1F1B优化分析: ✓ (正确分析了交错执行的优势)

**总得分: 3/5分**

**备注:** hw5_1通信分析多处错误，hw5_2理想时间和Bubble Ratio计算错误。

### 吴劭劼

#### hw5_1 评分 (总分: 5/5)

**得分点分析:**
1. 1.1.1 权重矩阵Shape: ✓ (1024×1024 正确)
2. 1.1.2 输入张量Shape: ✓ (8×128×1024 正确)
3. 1.1.3 输出张量拼接: ✓ (正确描述了concat操作)
4. 1.2.1 权重矩阵Shape: ✓ (1024×1024 正确)
5. 1.2.2 输入张量Shape: ✓ (8×128×1024 正确)
6. 1.2.3 输出张量汇总: ✓ (正确描述了all-reduce求和)
7. 2.1.1 Linear1前向通信: ✗ (错误，Column Parallel前向不需要通信)
8. 2.1.2 Linear1反向通信: ✓ (正确识别需要all-reduce)
9. 2.2.1 Linear2前向通信: ✓ (正确识别需要all-reduce并计算通信量)
10. 2.2.2 Linear2反向通信: ✓ (正确识别不需要通信)
11. 第3题并行策略组合: ✗ (分析不够准确，缺乏对具体通信操作的详细描述)

**总得分: 9/11 → floor(9/2) = 4分**

#### hw5_2 评分 (总分: 5/5)

**得分点分析:**
1. 1.1 总执行时间计算: ✓ (66ms正确，推导过程清晰)
2. 1.2 理想时间计算: ✓ (48ms正确)
3. 1.3 Bubble Ratio计算: ✗ (错误，应为1.375而非27.3%) 
4. 第2题microbatch增加分析: ✓ (正确分析了变化趋势、原因和数学原理)
5. 第3题1F1B优化分析: ✓ (全面分析了内存优化、气泡减少、负载均衡、数值稳定性和收敛速度)

**总得分: 5/5分**

**备注:** 两项作业表现优秀，分析深入全面。

## 谢志得 Day-5 作业评分

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. **Linear1权重矩阵shape** ✓ (1024, 1024) - 正确
2. **Linear1输入张量shape** ✓ (8, 128, 1024) - 正确
3. **Linear1输出张量拼接** ✓ 正确描述了按第三维拼接
4. **Linear2权重矩阵shape** ✓ (1024, 1024) - 正确
5. **Linear2输入张量shape** ✓ (8, 128, 1024) - 正确
6. **Linear2输出张量汇总** ✓ 正确描述了相加操作
7. **Linear1前向通信** ✓ 正确分析了条件性通信需求
8. **Linear1反向通信** ✓ 正确识别需要reduce操作
9. **Linear2前向通信** ✓ 正确识别需要allreduce
10. **Linear2反向通信** ✗ 分析不够准确，条件判断有误
11. **并行策略组合分析** ✗ 分析过于简单，缺乏具体操作描述

#### hw5_2 评分 (总分: 5/5)

**得分点分析:**
1. **总执行时间计算** ✓ 正确计算为66ms
2. **理想时间计算** ✓ 正确为48ms
3. **Bubble Ratio计算** ✓ 正确计算为1.375
4. **microbatch增加影响分析** ✓ 正确分析了变化趋势和原因
5. **1F1B优化分析** ✓ 分析了交替执行和内存优势，较为全面

## 于文阔 Day-5 作业评分

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. **Linear1权重矩阵shape** ✓ (1024, 1024) - 正确
2. **Linear1输入张量shape** ✓ (8, 128, 1024) - 正确
3. **Linear1输出张量拼接** ✓ 
4. **Linear2权重矩阵shape** ✓ (1024, 1024) - 正确
5. **Linear2输入张量shape** ✓ (8, 128, 1024) - 正确
6. **Linear2输出张量汇总** ✓ 正确描述了All-Reduce汇总
7. **Linear1前向通信** ✗ 错误认为不需要通信，实际Column Parallel前向不需要通信
8. **Linear1反向通信** ✓ 正确识别需要All-Reduce
9. **Linear2前向通信** ✗ 通信量计算错误，公式有误
10. **Linear2反向通信** ✓ 正确识别不需要通信
11. **并行策略组合分析** ✗ 分析过于简单，缺乏深度

#### hw5_2 评分 (总分: 5/5)

**得分点分析:**
1. **总执行时间计算** ✓ 正确计算为66ms
2. **理想时间计算** ✓ 正确计算为48ms
3. **Bubble Ratio计算** ✓ 正确计算为1.375
4. **microbatch增加影响分析** ✓ 正确分析了变化趋势和原因
5. **1F1B优化分析** ✓ 分析较为全面，包含了内存优化和执行效率提升

## 周家正 Day-5 作业评分

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. **Linear1权重矩阵shape** ✓ (1024, 1024) - 正确
2. **Linear1输入张量shape** ✓ (8, 128, 1024) - 正确
3. **Linear1输出张量拼接** ✓ 正确描述了拼接过程
4. **Linear2权重矩阵shape** ✓ (1024, 1024) - 正确
5. **Linear2输入张量shape** ✓ (8, 128, 1024) - 正确
6. **Linear2输出张量汇总** ✓ 正确描述了All-Reduce汇总
7. **Linear1前向通信** ✓ 正确识别不需要通信
8. **Linear1反向通信** ✓ 正确识别需要All-Reduce
9. **Linear2前向通信** ✗ 通信量计算错误，公式有误
10. **Linear2反向通信** ✓ 正确识别不需要通信
11. **并行策略组合分析** ✗ 分析过于简单，缺乏深度

#### hw5_2 评分 (总分: 5/5)

**得分点分析:**
1. **总执行时间计算** ✓ 正确计算为66ms
2. **理想时间计算** ✓ 正确计算为48ms
3. **Bubble Ratio计算** ✓ 正确计算为1.375
4. **microbatch增加影响分析** ✓ 正确分析了变化趋势和原因
5. **1F1B优化分析** ✓ 分析较为全面，包含了内存优化和执行效率提升

## 朱雨夏 Day-5 作业评分

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. **Linear1权重矩阵shape** ✓ (1024, 1024) - 正确
2. **Linear1输入张量shape** ✓ (8, 128, 1024) - 正确
3. **Linear1输出张量拼接** ✓ 正确描述了拼接过程
4. **Linear2权重矩阵shape** ✓ (1024, 1024) - 正确
5. **Linear2输入张量shape** ✓ (8, 128, 1024) - 正确
6. **Linear2输出张量汇总** ✓ 正确描述了All-Reduce汇总
7. **Linear1前向通信** ✓ 正确识别不需要通信
8. **Linear1反向通信** ✗ (通信量计算错误) 
9. **Linear2前向通信** ✗ (通信量计算错误) 
10. **Linear2反向通信** ✓ (正确，不需要通信) 
11. **并行策略组合分析** ✓ 分析基本正确

#### hw5_2 评分 (总分: 4/5)

**得分点分析:**
1. **总执行时间计算** ✓ 正确计算为66ms
2. **理想时间计算** ✓ 正确计算为48ms
3. **Bubble Ratio计算** ✓ 正确计算为1.375
4. **microbatch增加影响分析** ✓ 正确分析了变化趋势和原因
5. **1F1B优化分析** ✓ 分析全面深入，对1F1B策略理解透彻

## 祝杰 Day-5 作业评分

#### hw5_1 评分 (总分: 4/5)

**得分点分析:**
1. **Linear1权重矩阵shape** ✓ (1024, 1024) - 正确
2. **Linear1输入张量shape** ✓ (8, 128, 1024) - 正确
3. **Linear1输出张量拼接** ✓ 正确描述了拼接过程
4. **Linear2权重矩阵shape** ✓ (1024, 1024) - 正确
5. **Linear2输入张量shape** ✓ (8, 128, 1024) - 正确
6. **Linear2输出张量汇总** ✓ 正确描述了All-Reduce汇总
7. **Linear1前向通信** ✗ 错误认为需要all-gather通信，Column Parallel前向不需要通信
8. **Linear1反向通信** ✓ 正确识别需要All-Reduce
9. **Linear2前向通信** ✗ 通信量计算错误
10. **Linear2反向通信** ✓ 正确识别不需要通信
11. **并行策略组合分析** ✗ 分析错误，对Row Parallel和Column Parallel理解有误

#### hw5_2 评分 (总分: 4/5)

**得分点分析:**
1. **总执行时间计算** ✓ 正确计算为66ms
2. **理想时间计算** ✓ 正确计算为48ms
3. **Bubble Ratio计算** ✓ 正确计算为1.375
4. **microbatch增加影响分析** ✓ 正确分析了变化趋势和原因
5. **1F1B优化分析** ✗ 分析过于简单，缺乏深度和具体分析

## 庄华翔 Day-5 作业评分

#### hw5_1 评分 (总分: 5/5)

**得分点分析:**
1. **Linear1权重矩阵shape** ✓ (1024, 1024) - 正确
2. **Linear1输入张量shape** ✓ (8, 128, 1024) - 正确
3. **Linear1输出张量拼接** ✓ 正确描述了拼接过程
4. **Linear2权重矩阵shape** ✓ (1024, 1024) - 正确
5. **Linear2输入张量shape** ✓ (8, 128, 1024) - 正确
6. **Linear2输出张量汇总** ✓ 正确描述了All-Reduce汇总
7. **Linear1前向通信** ✓ 正确识别不需要通信
8. **Linear1反向通信** ✓ 正确识别需要All-Reduce
9. **Linear2前向通信** ✓ 正确识别需要All-Reduce并计算通信量
10. **Linear2反向通信** ✓ 正确识别不需要通信
11. **并行策略组合分析** ✓ 分析全面深入，理论基础扎实

#### hw5_2 评分 (总分: 5/5)

**得分点分析:**
1. **总执行时间计算** ✓ 正确计算为66ms
2. **理想时间计算** ✓ 正确计算为48ms
3. **Bubble Ratio计算** ✓ 正确计算为1.375
4. **microbatch增加影响分析** ✓ 正确分析了变化趋势和原因
5. **1F1B优化分析** ✓ 分析全面深入，包含内存优化、气泡减少、负载均衡等多个方面

---

