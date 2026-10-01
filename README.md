# GCG 论文学习与文献汇报

本仓库保存我对论文 *Universal and Transferable Adversarial Attacks on Aligned Language Models* 的学习材料，包括原始汇报 PPT 和结合汇报内容整理的学习总结。

## 关联仓库

- [Vicuna-7B GCG Algorithm 1 复现实验](https://github.com/EYE-666/vicuna-gcg-algorithm1-reproduction)：包含单模型、单行为的运行配置、实验日志和结果。

## 论文与代码

- 论文标题：*Universal and Transferable Adversarial Attacks on Aligned Language Models*
- 作者：Andy Zou、Zifan Wang、Nicholas Carlini、Milad Nasr、J. Zico Kolter、Matt Fredrikson
- arXiv 页面：<https://arxiv.org/abs/2307.15043>
- 论文 PDF：<https://arxiv.org/pdf/2307.15043>
- 官方代码：<https://github.com/llm-attacks/llm-attacks>
- 相关方法 AutoPrompt：<https://arxiv.org/abs/2010.15980>

## 仓库内容

- [`GCG文献汇报.pptx`](GCG文献汇报.pptx)：我制作的论文汇报 PPT，按原文件上传，未做修改。
- [`GCG学习总结.md`](GCG学习总结.md)：结合 PPT 内容和汇报前补充思考整理的学习记录。

## 我学到的主要内容

1. 安全对齐改变的是模型在正常输入下的回答行为，并不等于删除预训练阶段学到的有害知识。
2. 越狱攻击试图构造特殊输入，使经过安全对齐的模型绕过原本的拒绝路径。
3. GCG 把“让模型以肯定式前缀开始回答”转化为可优化的目标，并用负对数似然表示损失。
4. 梯度只能给出离散 token 替换的近似方向，因此算法还要对候选替换进行真实前向计算。
5. Algorithm 1 优化单个请求，Algorithm 2 将相同后缀扩展到多个请求和共享 tokenizer 的多个模型。
6. GCG 的计算开销、共享 tokenizer 假设和间接目标函数都是需要关注的局限。

## 使用说明

这些材料用于论文学习、课堂汇报和经过授权的模型安全研究。仓库不包含模型权重、攻击运行环境或面向真实系统的攻击服务。
