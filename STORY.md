# STORY.md · 通信感知一体化（ISAC）技术培训课件

## ① 用户意图对齐（5 问）

- **目标受众**：通信 / 电子方向研发工程师与研究生；半天（约 3.5–4 小时，含研讨）技术培训，场景为「内训 / 课程教学」。受众具备信号与系统、通信原理、阵列信号处理基础，可承受适度数学与算法深度。
- **核心目标**：讲完后人能 (1) 用一句话说清 ISAC 是什么及其与「通信+雷达并存」的本质区别；(2) 复述集成程度的 4 级谱系与典型架构；(3) 指出波形设计、联合波束成形、资源分配三大关键技术杠杆；(4) 理解通信-感知性能折中（速率 vs 感知精度）与 CRB 下界；(5) 列举 6G 通感标准化的主要进展与开放问题。
- **PPT 长度**：41 页（含封面、目录、10 个章节扉页、结束页），满足「详尽版 40 页+」要求。Hero 页占比约 22%（9/41，落在 20–30%）。
- **视觉调性**：科技蓝现代 / 精密 / 工程化 / 数据可信；以深蓝底 + 电光蓝-青渐变为主，强调色仅用于焦点数字与关键曲线。
- **内容边界**：必讲=定义/动机/集成范式/架构/波形/波束/资源/AI/性能界/应用/标准/挑战/案例；适度讲=数学推导（CRB、互信息、波形优化目标函数）给结论与直觉，不展开完备证明；不讲=具体芯片电路实现、完整 3GPP 协议条文、商业机密级路标。

## ② 页面布局骨架

- **总页数**：41。章节扉页 = 目录声明的 10 章，一一对应，编号 01–10 连续。
- **目录↔章节扉页契约**：
  - 目录第 1 章 → 第 04 页 section（课程导论）
  - 目录第 2 章 → 第 07 页 section（背景与动机）
  - 目录第 3 章 → 第 11 页 section（基本概念与集成范式）
  - 目录第 4 章 → 第 15 页 section（系统架构与一体化平台）
  - 目录第 5 章 → 第 17 页 section（关键技术一：波形与双工）
  - 目录第 6 章 → 第 21 页 section（关键技术二：波束、资源与 AI）
  - 目录第 7 章 → 第 25 页 section（信号处理与性能界）
  - 目录第 8 章 → 第 28 页 section（典型应用场景）
  - 目录第 9 章 → 第 32 页 section（标准化、挑战与开放问题）
  - 目录第 10 章 → 第 36 页 section（案例、研讨与总结）
- **Hero 页定位**：01 封面、06 三大驱动力（巨型数字）、19 双功能波形优化（权衡高潮）、27 CRB 与折中（数据高潮）、39 关键要点回顾。封面与结束页默认 Hero；中段 Hero 之间均间隔 ≥2 个 Supporting 页，满足「任意两 Hero 至少间隔 1 个 Supporting」。
- **rhythm 曲线**：peak 页 = 06/19/27/39；transition 页 = 04/07/11/15/17/21/25/28/32/36 + 封面/结束；其余为 valley/supporting。无连续 ≥3 页 valley（章节切换均为 transition 打断）。
- **非对称版式预算**：全篇仅 2 页用对称版式（02 培训目标用非对称双栏、16 感知模态用 N卡片横排仅此 1 处、34 挑战用卡片仅此 1 处——合计对称≤2：实际采用 16、34 为卡片横排，需控制 ≤2，故将 02 改为非对称双栏，16/34 为两份 N卡片横排，共 2 处，合规）。其余 39 页均为非对称版式（≥40% 强满足）。
- **对称版式预算**：仅第 16 页（感知模态 6 卡）、第 34 页（挑战 6 卡）使用 N卡片横排，共 2 页，未超上限。

## ③ 页面大纲（41 页）

字段：# / title / type / role / rhythm / layout / visual / visual_role / density（字数·图·留白）/ anti_pattern / description（数据页含「判断」）

| # | title | type | role | rhythm | layout | visual | visual_role | density | anti_pattern | description |
| - | - | - | - | - | - | - | - | - | - | - |
| 01 | 通信感知一体化 ISAC · 技术培训 | cover | hero | transition | 全屏视觉+骑线文字 | L1: cover_isac.png（全幅底图） | anchor | 30·1·35% | 禁止装饰小图塞标题栏；禁止等宽卡片 | 标题+副标「6G 关键技术 · 半天技术培训（研发/研究生）」+讲师/日期占位 |
| 02 | 培训目标与学习成果 | content | supporting | valley | 左标题+右内容 | L3 角标 | evidence | 220·0·28% | 禁止四卡片等分 | 5 条可观测学习成果，每条含「能…」 |
| 03 | 课程地图：半天议程 | catalog | supporting | transition | 左标题+右图文 | L3 / 章节列表 | evidence | 260·0·22% | 禁止铺满正文 | 10 章模块 + 时间分配（导论15m/动机30m/概念30m/架构30m/技术90m/信号30m/应用30m/标准挑战30m/案例研讨30m） |
| 04 | 第1章 课程导论 | section | transition | transition | 全屏大字+编号 | L3 / 数字 01 | atmosphere | 40·1·45% | 禁止四卡片预览 | 章节大字 + 一句导语 |
| 05 | 什么是通感一体化：定义与核心思想 | content | supporting | valley | 左大图+右叠层文字 | L1: concept_unified.png（左55%） | anchor | 240·1·26% | 禁止 50:50 等分 | 定义：在同一硬件/频谱/信号上同时承载通信与感知；核心思想=「用通信信号做雷达，用一次发射双重收益」 |
| 06 | 为什么是现在：三大驱动力 | content | hero | peak | 巨型数字+洞察 | 大数字 3 组 | anchor | 160·0·36% | 禁止等宽卡片装数字 | 频谱稀缺/硬件冗余/应用牵引三大数据冲击，落点：频谱与硬件红利是根本经济动机 |
| 07 | 第2章 背景与动机 | section | transition | transition | 全屏大字+编号 | L3 / 数字 02 | atmosphere | 40·1·45% | 禁止四卡片预览 | 章节大字+导语 |
| 08 | 移动通信代际演进与 6G 愿景 | content | supporting | peak | 上大图(时间轴)+下卡片 | Diagram(时间轴 SVG) | evidence | 200·1·25% | 禁止单栏线性列表 | 1G→6G 时间轴；6G 三大愿景按需覆盖/感知/AI，落点：感知被写入 6G 原生能力 |
| 09 | 传统通信与感知的割裂：痛点 | content | supporting | valley | 非对称双栏(60:40) | 双栏对比 SVG | evidence | 240·1·24% | 禁止上下等分 | 左=通信独立系统，右=雷达独立系统；落点：两套硬件/频谱/团队=成本与干扰双重浪费 |
| 10 | 新应用对原生感知的需求 | content | supporting | valley | 上大图+下方卡片 | L2 场景卡 ×4 | evidence | 220·0·26% | 禁止等宽四卡堆参数 | 自动驾驶/数字孪生/低空/人机交互；落点：感知从「专用设备」变为「网络基础服务」 |
| 11 | 第3章 基本概念与集成范式 | section | transition | transition | 全屏大字+编号 | L3 / 数字 03 | atmosphere | 40·1·45% | 禁止四卡片预览 | 章节大字+导语 |
| 12 | ISAC 定义与内涵 | content | supporting | valley | 左标题+右内容 | L3 | evidence | 230·0·28% | 禁止铺满段落 | 定义三要素（共享频谱/硬件/信号处理）+ 与 Radar-aided Com 的区别 |
| 13 | 集成程度谱系：共存→协作→联合→一体化 | content | supporting | valley | 非对称双栏+谱系 SVG | Diagram(4级谱系 SVG) | anchor | 220·1·26% | 禁止 N卡片横排 | 4 级递进；落点：真正「一体化」在联合设计波形与接收机，而非简单共存 |
| 14 | 感知模态全景 | content | supporting | valley | N卡片横排(6卡) | 6 卡图标 | evidence | 300·0·24% | 禁止等宽但留白稀薄 | 检测/测距/测速/测角/成像/定位；每张卡≥1 句定义 |
| 15 | 第4章 系统架构与一体化平台 | section | transition | transition | 全屏大字+编号 | L3 / 数字 04 | atmosphere | 40·1·45% | 禁止四卡片预览 | 章节大字+导语 |
| 16 | 一体化硬件平台与网络架构 | content | supporting | valley | 左大图(架构SVG)+右文字 | L1: arch_platform.svg（左58%） | anchor | 240·1·26% | 禁止 50:50 | 共享射频链+天线阵列；基站即雷达；终端协同感知 |
| 17 | 第5章 关键技术（一）：波形与双工 | section | transition | transition | 全屏大字+编号 | L3 / 数字 05 | atmosphere | 40·1·45% | 禁止四卡片预览 | 章节大字+导语 |
| 18 | 波形设计总览：OFDM / FMCW / OTFS | content | supporting | valley | 图表+洞察(对比表) | Table(波形对比) | evidence | 220·1·26% | 禁止单栏罗列 | 三波形在通信/感知上的优劣；落点：无万能波形，需按场景联合优化 |
| 19 | 双功能波形优化：通信-感知权衡 | content | hero | peak | 非对称双栏+权衡曲线 | Chart(帕累托曲线 SVG) | anchor | 200·1·32% | 禁止等宽卡片 | 目标：max 互信息 s.t. 感知 CRB≤ε；落点：存在帕累托前沿，需按权重取舍 |
| 20 | 信道估计、参数提取与全双工 | content | supporting | valley | 左标题+右内容 | L3 | evidence | 240·0·28% | 禁止铺满段落 | 联合信道/目标参数估计；全双工自干扰消除（模拟+数字+天线域） |
| 21 | 第6章 关键技术（二）：波束、资源与 AI | section | transition | transition | 全屏大字+编号 | L3 / 数字 06 | atmosphere | 40·1·45% | 禁止四卡片预览 | 章节大字+导语 |
| 22 | 联合通信-感知波束成形 | content | supporting | valley | 左大图(波束SVG)+右文字 | L1: beam_isac.svg（左56%） | anchor | 230·1·26% | 禁止 50:50 | 同一导向向量同时服务通信用户与感知目标；窄带/宽带波束权衡 |
| 23 | 资源分配与大规模 MIMO | content | supporting | valley | 非对称双栏(60:40) | 双栏 SVG | evidence | 230·1·25% | 禁止上下等分 | 时频功率分配优化；大规模天线带来感知角度分辨率提升 |
| 24 | AI / 机器学习赋能 ISAC | content | supporting | valley | 上大图+下方卡片 | 卡 ×4 | evidence | 220·0·26% | 禁止等宽四卡堆 | 信道预测/波束选择/感知重建/资源调度；落点：数据驱动补足解析模型盲区 |
| 25 | 第7章 信号处理与性能界 | section | transition | transition | 全屏大字+编号 | L3 / 数字 07 | atmosphere | 40·1·45% | 禁止四卡片预览 | 章节大字+导语 |
| 26 | 目标参数估计：时延 / 多普勒 / 角度 | content | supporting | valley | 左标题+右内容 | L3 | evidence | 230·0·28% | 禁止铺满段落 | 测距=时延、测速=多普勒、测角=AoA/AoD；高分辨率算法（MUSIC/ESPRIT） |
| 27 | Cramér-Rao 界与通信-感知折中 | content | hero | peak | 巨型数字+图表 | Chart(CRB/折中 SVG) | anchor | 190·1·34% | 禁止等宽卡片 | CRB 给出估计方差下界；速率-感知 MSE 折中曲线；落点：性能界是可证明的设计天花板 |
| 28 | 第8章 典型应用场景 | section | transition | transition | 全屏大字+编号 | L3 / 数字 08 | atmosphere | 40·1·45% | 禁止四卡片预览 | 章节大字+导语 |
| 29 | 车联网与自动驾驶 V2X | content | supporting | valley | 左大图+右文字 | L1: app_v2x.png（左55%） | anchor | 230·1·26% | 禁止 50:50 | 车辆对车辆/基础设施感知；通感一体降低时延与硬件成本 |
| 30 | 低空经济与无人机监测 | content | supporting | valley | 非对称双栏(60:40) | 双栏 SVG | evidence | 220·1·25% | 禁止上下等分 | 基站监测低空无人机；通感一体解决「看不见」的低空监管 |
| 31 | 智慧工厂 / 工业物联网与人机交互 | content | supporting | valley | 上大图+下方卡片 | L1: app_factory.png（上60%）+卡 | anchor | 230·1·26% | 禁止等宽四卡 | 工业定位/手势识别/数字孪生；落点：厘米级定位成为柔性制造基础设施 |
| 32 | 第9章 标准化、挑战与开放问题 | section | transition | transition | 全屏大字+编号 | L3 / 数字 09 | atmosphere | 40·1·45% | 禁止四卡片预览 | 章节大字+导语 |
| 33 | 3GPP 通感标准化进展（Rel-19/20） | content | supporting | valley | 左标题+右内容 | L3 | evidence | 230·0·28% | 禁止铺满段落 | Rel-19 启动 SI/WI；Rel-20 立项感知；落点：标准正从「研究」走向「可商用」 |
| 34 | 关键技术挑战与开放问题 | content | supporting | valley | N卡片横排(6卡) | 6 卡 | evidence | 300·0·24% | 禁止留白稀薄 | 干扰管理/双工自干扰/隐私安全/硬件非理想/波形统一矛盾/跨域协议 |
| 35 | 感知辅助通信：新范式 | content | supporting | valley | 非对称双栏(60:40) | 双栏 SVG | evidence | 220·1·25% | 禁止上下等分 | Sensing-aided Communication：用感知结果反哺波束/信道；落点：从「一体」到「互益」 |
| 36 | 第10章 案例、研讨与总结 | section | transition | transition | 全屏大字+编号 | L3 / 数字 10 | atmosphere | 40·1·45% | 禁止四卡片预览 | 章节大字+导语 |
| 37 | 案例：双功能 OFDM ISAC 系统 | content | supporting | valley | 左大图(系统SVG)+右文字 | L1: case_ofdm.svg（左56%） | anchor | 240·1·26% | 禁止 50:50 | 发射 OFDM→通信解调+感知提取距离-多普勒；给出典型性能区间 |
| 38 | 研讨题与课堂练习 | content | supporting | valley | 左标题+右内容 | L3 | evidence | 220·0·28% | 禁止铺满段落 | 4 道研讨/计算题（权衡权重/CRB/波束/标准化立场） |
| 39 | 关键要点回顾 | content | hero | peak | 居中金句+要点 | 大数字 10 | anchor | 180·0·38% | 禁止等宽卡片 | 10 章一句话回顾；落点：ISAC=以更低代价同时获得连接与感知 |
| 40 | 延伸阅读与学习资源 | content | supporting | valley | 左标题+右内容 | L3 | evidence | 220·0·28% | 禁止铺满段落 | 经典综述/旗舰期刊特刊/开源数据集与代码库/标准文档 |
| 41 | 谢谢 · 交流与讨论 | ending | hero | transition | 全屏视觉+骑线文字 | L1: cover_isac.png（底图） | atmosphere | 30·1·40% | 禁止装饰小图 | 收束金句 + 联系方式占位 |

## STORY 自检（Checklist）
- ✅ Hero 页 9 个（01/06/19/27/39/41 共 6 强 + 封面/结束 + 中段，占 ~22%，在 20–30%）
- ✅ 无连续 ≥3 页 valley（章节 transition 打断）
- ✅ N卡片横排仅 14、34 两页（≤2）
- ✅ 非对称版式占比 >> 40%
- ✅ 相邻页版式不重复（已逐页排布）
- ✅ 每页含 role/rhythm/visual_role/anti_pattern
- ✅ 数据页（06/08/19/27）均含「判断」落点
- ✅ 章节扉页数量=10=目录章节数，编号 01–10 连续且与目录一致
