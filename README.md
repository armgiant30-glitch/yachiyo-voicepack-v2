# 八千代语音包 v2（微调 e8）

可直接安装到 Amadeus 的八千代（月見ヤチヨ）语音资源包。

**实测提升**：内容保真 CER `0.354 → 0.084`（下降 4.2 倍），说话人相似度 ECAPA `0.3305 → 0.4415`（提升 33.6%）。

## 下载

本仓库的源码树只保存说明文档；大文件统一放在 [`v2.0.0` Release](https://github.com/armgiant30-glitch/yachiyo-voicepack-v2/releases/tag/v2.0.0)：

| 文件 | 说明 |
|---|---|
| `八千代语音包-v2-微调e8.zip` | Amadeus 语音包，包含推荐权重、参考音频、情绪参考库、试听样例和安装说明 |
| `八千代-接入后合成样例.wav` | 接入后的合成试听样例 |
| `八千代-全过程记录(PROCESS).md` | 数据来源、训练、评估、踩坑和部署过程记录 |

重新下载后可用仓库中的 [`SHA256SUMS.txt`](./SHA256SUMS.txt) 核对完整性。

## 关键信息

- GPT-SoVITS v3，仅微调 s2（SoVITS）LoRA rank 32，8 epoch。
- 推荐权重：`model/yachiyo_e8_s288_l32.pth`。
- 默认参考音频：`reference/yachiyo_reference.wav`。
- 采样参数沿用 Amadeus 现有配置，不要降低 `repetition_penalty`。
- 参考文本必须与参考音频逐字一致。

详细安装步骤见压缩包内的 `README.md`，完整实验过程见本仓库的 [八千代-全过程记录(PROCESS).md](./八千代-全过程记录(PROCESS).md)。

## 使用约束

本包仅用于个人研究。角色、原始音频及相关素材的版权归原作者或权利方所有，请勿用于商业用途或未经许可的二次分发。
