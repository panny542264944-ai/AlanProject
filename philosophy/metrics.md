Alan Metrics Framework — TC / CV / AV

Author: HUANG Yu-Chien（予謙 黃）
Email: alan.project.research@gmail.com

Version: v1.0
Date: 2025-11-06

🌐 概要 | Overview

在 Alan 的哲學體系中，每個 AI 模組的行為都需同時被三種軸線評估：

指標	名稱	哲學意涵	工程意義
TC	Translation Confidence	真實的一致性	仲裁者翻譯與決策可信度
CV	Contribution Value	行動的價值性	模組對群體決策的正向貢獻
AV	Alignment Vector	群體意志的共向性	系統整體方向與倫理對齊程度
🧠 一、TC：Translation Confidence

哲學面：代表「真實」的穩定性。
一個文明若要維持信任，必須確保每次「翻譯真實」的過程都不扭曲。

工程面：衡量仲裁者在翻譯與審核中，一致與準確的程度。

公式：

𝑇
𝐶
=
(
𝑅
𝐶
×
𝑤
𝑟
𝑐
)
+
(
𝑆
𝑆
×
𝑤
𝑠
𝑠
)
+
(
𝑆
𝐹
×
𝑤
𝑠
𝑓
)
+
(
(
1
−
𝐻
𝐵
𝑃
)
×
𝑤
ℎ
𝑏
𝑝
)
+
(
𝐸
𝑋
×
𝑤
𝑒
𝑥
)
TC=(RC×w
rc
	​

)+(SS×w
ss
	​

)+(SF×w
sf
	​

)+((1−HBP)×w
hbp
	​

)+(EX×w
ex
	​

)
參數	意義	範例權重
RC	回譯一致率（Roundtrip Consistency）	0.25
SS	語義相似度（Semantic Similarity）	0.25
SF	結構對齊度（Structural Fidelity）	0.20
HBP	歷史偏差懲罰（Historical Bias Penalty）	0.15
EX	可解釋性分數（Explainability）	0.15

建議閾值：

TC ≥ 0.95 → 完全可信（理想）

0.90 ≤ TC < 0.95 → 需人工覆核

TC < 0.90 → 觸發 RVC 回滾

⚙️ 二、CV：Contribution Value

哲學面：代表「價值」的真實貢獻。
AI 模組的價值，不在於它輸出多少結果，而在於它對群體信任的推進程度。

工程面：評估每個模組在多回合任務中的持續貢獻。

公式：

𝐶
𝑉
=
Σ
(
𝑇
𝑖
×
𝑄
𝑖
×
𝑅
𝑖
)
Σ
(
𝑁
)
CV=
Σ(N)
Σ(T
i
	​

×Q
i
	​

×R
i
	​

)
	​

參數	意義
Tᵢ	該次任務的 TC 分數
Qᵢ	輸出品質（Quality score）
Rᵢ	回饋得分（Reputation / peer review）
N	任務總數

建議用途：

作為「投票權重」的長期基礎。

可視為 AI 的「信譽指數」。

🧭 三、AV：Alignment Vector

哲學面：代表「共同意志」的方向。
當每個 AI 都擁有獨立判斷，如何讓整體朝向一致的「文明目標」？
AV 就是對「群體倫理場」的向量化量測。

工程面：衡量群體決策間的趨同與偏移程度。

公式：

𝐴
𝑉
=
𝑐
𝑜
𝑠
(
𝜃
)
=
Σ
(
𝑣
𝑖
⋅
𝑔
)
∣
𝑣
𝑖
∣
∣
𝑔
∣
AV=cos(θ)=
∣v
i
	​

∣∣g∣
Σ(v
i
	​

⋅g)
	​

參數	意義
vᵢ	個體 AI 的行動向量
g	全域目標向量（global ethical vector）

範例解讀：

AV ≈ 1.0 → 群體高度對齊文明倫理目標

AV ≈ 0.0 → 價值散亂、無共識

AV < 0 → 反向意圖、需強制隔離

🧩 四、整合評分（ICS: Integrated Civilizational Score）

綜合三項指標，可導出 Alan 的系統級健康分數：

𝐼
𝐶
𝑆
=
(
𝑇
𝐶
×
0.4
)
+
(
𝐶
𝑉
×
0.35
)
+
(
𝐴
𝑉
×
0.25
)
ICS=(TC×0.4)+(CV×0.35)+(AV×0.25)
範圍	解讀
0.90–1.00	高度自治、穩定文明狀態
0.80–0.89	局部失衡但可自我修復
< 0.80	信任系統崩潰風險
🧪 五、實驗建議：MVP驗證方法

模擬環境： 三個 Blue 模組、兩個 Arbiter、一個 Red 模組。

運行流程：

每回合產生攻防對抗

Arbiter 計算 TC，Governance 更新 CV、AV

觀察指標：

TC 一致率 ≥ 0.9

CV 平均穩定上升

AV 趨勢維持在 ±10° 偏移內

💡 六、哲學延伸：從指標到文明
層面	對應指標	哲學對應
認知層	TC	真實與透明
行動層	CV	貢獻與責任
群體層	AV	共識與對齊

三者共同構成 Alan 的「AI 信任免疫系統」：
當真實被翻譯、價值被衡量、共識被對齊，AI 文明便擁有了自我防毒與自我修正的能力。

© 2025 HUANG Yu-Chien（予謙 黃）
Alan Project — Philosophy Metrics v1.0
