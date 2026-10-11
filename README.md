# AKG K712 PRO 头梁修复记录（3D 打印零件 + 发圈替换橡胶吊带）

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

![修复完成](images/16_final_front.jpg)

本仓库记录了一副 **AKG K712 PRO** 开放式监听耳机头梁部分的 DIY 修复：把头梁里老化的原厂橡胶吊带（官方名称 *Rubber loop*，零件 6）换成两根编织款发圈（弹力绳），并用 3D 打印件代替拆卸时必须破坏/取下的 **装饰盖（Cover，零件 3）** 和 **卡扣铆钉（Locking knob，零件 7）**。仓库包含过程照片、可直接切片打印的 3MF 文件，以及作为结构参考的官方维修手册。

> 说明：文中零件编号和名称均来自 AKG 官方 K612/K712 维修手册（见 [`ref/`](ref/)）。照片能直接看到的内容会直接描述；照片看不到、根据模型尺寸或手册推断的内容都会标注 **（推断）**。

---

## 目录

- [背景：K712 的头梁结构](#背景k712-的头梁结构)
- [修复过程](#修复过程)
- [注意事项](#注意事项)
- [3D 打印说明](#3d-打印说明)
- [文件夹结构](#文件夹结构)
- [索引](#索引)
- [参考资料](#参考资料)
- [许可协议](#许可协议)

---

## 背景：K712 的头梁结构

根据官方维修手册（Service Manual #2458Z00XXX, 10/2015）中的爆炸图和零件表，与本次修复相关的零件如下：

| 编号 | 英文名称 | 德文名称 | 中文说明 |
|---|---|---|---|
| 1 | Outer headband compl. | Bügel kpl. | 外头梁（两根带绝缘层的钢丝，末端连到耳罩） |
| 2 | Headband compl. | Bügelband kpl. | 皮质头带（压在头顶的那条） |
| 3 | Cover | Abdeckung | 滑块外侧的圆形装饰盖 |
| 4 | Inner slider | Gleitstück innen | 内滑块 |
| 5 | Outer slider | Gleitstück außen | 外滑块（套在两根钢丝上滑动） |
| 6 | Rubber loop | Gummischlaufe | 橡胶吊带：拉住头带、提供自适应头围的弹力 |
| 7 | Locking knob | Schnappniet | 卡扣铆钉：把内/外滑块和头带锁在一起 |
| 9 / 20 | Cover left (+MiniXLR) / Cover right | Deckel | 耳罩上盖（钢丝卡在上面） |
| 8 / 22 | Grid cover | Gitterdeckel | 耳罩外侧格栅 |
| 10 | Screw Ejot 22x5 | Schraube | 格栅下方固定上盖的两颗螺丝 |

K712 的自适应头带靠两侧的橡胶吊带（6）把皮头带往上拉。橡胶吊带用久了会老化、失去弹性或断裂，这是这类 AKG 头梁的常见毛病。

手册中更换橡胶吊带的官方步骤是：**用螺丝刀从 CE 标志下方的缺口把装饰盖（3）撬出来（break out），然后按下卡扣的同时把卡扣铆钉（7）顶出来。** 也就是说，装饰盖拆一次基本就坏了，卡扣铆钉也容易损坏——这就是本项目要 3D 打印替换件的原因。

---

## 修复过程

### 1. 准备：找老婆要两根新发圈

![发圈](images/01_hair_ties_preparation.jpg)

替换橡胶吊带（6）的弹力绳，用的就是普通的**编织款发圈**——粗细、弹性和长度都刚好，颜色还能挑和 K712 配套的橙色。所以第一步：**找老婆要两根新发圈**（记得是*新的*，并且要先征得同意 😉）。照片里那一罐就是“物料库”。

### 2. 打印替换用的“铆钉 + 装饰盖”

![打印好的盖帽](images/02_printed_pin_caps.jpg)

打印了 3 个带双色 Logo 的盖帽（黑色底 + 橙色 Logo 嵌片，与 K712 的黑橙配色呼应），对应 `3d/k712pro_pin_v2.3mf` 中的 `k712pro_top` 零件。盖帽直径约 15 mm。

![盖帽背面的铜螺母](images/03_pin_caps_heat_set_inserts.jpg)

盖帽背面中间有一个凸台，凸台里热熔压入了**黄铜热熔螺母**（照片中两个已经装好，一个还没装），凸台侧面开有缺口。**（推断）** 这个凸台的作用相当于原厂卡扣铆钉（7）的轴，穿过头带和滑块的孔；缺口用来让开内部结构或定位。

### 3. 确认螺丝规格

![螺丝规](images/04_screw_size_check.jpg)

用打印的螺丝规确认固定螺丝的直径和长度。固定螺丝规格为 **M2 × 6 mm**（背面垫片的中心孔约 Ø2.4 mm，正好让 M2 螺丝穿过）。拧的时候注意扭矩，见[注意事项](#注意事项)。

### 4. 组装滑块：垫片 + 螺丝 + 盖帽

![滑块内侧](images/05_slider_inner_side_screw.jpg)

滑块内侧：打印的圆形垫片（`3d/k712pro_pin_v2.3mf` 中的 `Body1`，直径约 13 mm、厚约 4.5 mm，表面带纹理）从内侧压住，中间一颗螺丝拧进外侧盖帽的铜螺母里，把头带、内滑块（4）和外滑块（5）夹在一起，替代原来的卡扣铆钉（7）。

![滑块外侧](images/06_slider_outer_side_logo_cap.jpg)

滑块外侧：带橙色 Logo 的盖帽替代原来的装饰盖（3）。原厂橡胶吊带（6）的位置换成了**橙色编织发圈**，从滑块两侧的卡槽穿出、在下方形成一个环。

![两个滑块](images/07_sliders_with_elastic_cord.jpg)

左右两个滑块总成（拆下状态）。左边的已经把发圈绕进滑块的槽里，右边的还没装。

### 5. 打开耳罩，固定发圈末端

![拆格栅](images/08_grille_removal_tweezers.jpg)

按手册方法取下耳罩外侧格栅（8/22）：用尖头镊子插进两个尽量远的格栅网孔，**逆时针**转动整个格栅直到卡扣松开。格栅下面是固定上盖的两颗螺丝（10）。

![耳罩端的发圈](images/09_cord_routing_at_earcup.jpg)

拆下耳罩上盖（9/20）后可以看到外头梁（1）两根钢丝的末端连接块。发圈从滑块沿钢丝向下，绕过连接块的两个角固定，替代原来橡胶吊带挂在这里的位置。旁边能看到单元引线（红、白等）焊在端子上，操作时不要扯到。

![上盖打开](images/10_earcup_lid_opened.jpg)

上盖翻开时的状态：发圈在连接块内侧被压住，上盖的内侧结构和单元引线（黄、紫/红、白）清晰可见。

### 6. 测量与对称调整

![测量 A](images/11_cord_routing_measure_a.jpg)
![测量 B](images/12_cord_routing_measure_b.jpg)

用钢尺对比左右两侧滑块到耳罩连接块的距离。

`3d/k712_inserts.3mf` 打印的 **C 形垫套**就是在这一步用的：它是**调整用的垫片**，卡在钢丝末端、靠近耳罩连接块的位置，用来补偿左右两侧尺寸的差异。做法是**先手工测量两侧尺寸，再按需在偏短的一侧塞入垫套，直到两边一致**。本次修复中，所有垫套最后都装在了**同一侧**。

> ⚠️ 注意：这两张测量照片里垫套在两侧都装着，那只是测量过程中的状态。**如果照着照片两侧都装，就会造成左右不对称。** 不要照搬照片——先量，再按需加垫套，直到两侧对称为止。

### 7. 装回并试戴

![装回侧面](images/13_reassembled_side.jpg)
![装回正面](images/14_reassembled_front.jpg)
![手持](images/15_reassembled_in_hand.jpg)

装回上盖、螺丝（10）和格栅后的样子。可以看到盖帽、滑块和橙色发圈与原机黑橙配色融为一体。手册建议：装回后做听音测试，用**单声道**信号（不要用正弦波）确认声像在正中间——特别是如果拆焊过单元引线时。

### 8. 完成

![完成正面](images/16_final_front.jpg)
![完成侧面](images/17_final_side.jpg)

---

## 注意事项

1. **发圈选编织款、弹性好的新发圈**，左右两根最好是同一款，弹力一致。
2. **装饰盖（3）拆了基本就坏**：官方方法是从 CE 标志下方的缺口撬出，属于破坏性拆卸。动手前先准备好替换件（本仓库的盖帽）。
3. **卡扣铆钉（7）**：需要一边把卡扣往里压、一边把铆钉往外顶，用力过猛容易断。
4. **格栅（8/22）是卡扣 + 逆时针旋转**，不是撬下来的；用尖头镊子插网孔、两点尽量远，均匀转动，别划伤网面。
5. **耳罩上盖（9/20）同时卡在两根钢丝上**：拆之前先松开格栅下的两颗螺丝（10），再从两侧按压上盖露出卡扣、用小一字螺丝刀压下卡扣后再拔出。
6. **单元引线很细**：上盖里有红/黄/白（以及左侧的 Mini XLR）引线，翻开上盖时不要拉扯。若需换单元，手册要求螺丝 15 只用“适中力度”拧紧，并注意相位（极性）正确。
7. **热熔螺母**：用烙铁装热熔铜螺母时温度别太高、垂直压入，避免把凸台烫变形。
8. **M2 × 6 mm 螺丝注意扭矩，不要拧太紧！** 3D 打印件的层间结合力较弱，拧过头会把盖帽凸台或垫片沿层线撑裂。拧到夹紧、滑块不松动即可。
9. **左右对称靠测量 + 垫套**：先用尺子测量两侧尺寸，再按需在一侧加入 C 形垫套（`k712_inserts.3mf`），直到两侧一致。**不要照搬测量照片里两侧都装垫套的状态**，否则会不对称。本次是全部装在同一侧。
10. **耳垫（19）是卡口式的**，逆时针转即可取下（手册说明），本次修复不一定需要拆。
11. 本记录仅为个人维修经验，拆机有风险，可能失去保修，请自行判断。

---

## 3D 打印说明

两份文件均为 **Bambu Studio** 工程文件（3MF，包含切片设置），在 Bambu Lab A1 / 0.4 mm 喷嘴上配置；其他切片软件（如 PrusaSlicer / OrcaSlicer）一般也能导入几何体。

| 文件 | 内容 | 尺寸（由模型几何体测得） |
|---|---|---|
| `3d/k712pro_pin_v2.3mf` | **铆钉/盖帽替换件**：3 × `k712pro_top`（盖帽，主体 + 0.6 mm 厚 Logo 嵌片，双色）、4 × `Body1`（内侧垫片） | 盖帽 Ø15 × 约 10 mm；Logo 嵌片约 9.4 × 10 × 0.6 mm；垫片 Ø13 × 4.5 mm，中心孔约 Ø2.4 mm |
| `3d/k712_inserts.3mf` | 4 × C 形开口垫套：**左右尺寸调整用的垫片**，卡在钢丝末端，测量后按需加在偏短的一侧（不是每侧固定 2 个；本次全部装在同一侧） | 外径 Ø4 mm，内径约 Ø1.6 mm，长 5.8 mm，侧面开口 |

工程文件中保存的设置（仅供参考）：

- 材料：`k712pro_pin_v2` 的盖帽和垫片分配到 **PETG** 料槽（黑色主体 + 橙色 Logo，Bambu PETG HF，喷嘴 240 °C）。`k712_inserts` 的套管在工程里分配到 1 号料槽（PLA Basic），但缩略图显示为橙色，实际用料请按需选择。
- 层高 **0.08 mm**（“0.08mm High Quality”预设），2 层墙，15% 螺旋（gyroid）填充。
- `k712pro_pin_v2` 开启了支撑（normal/auto）；`k712_inserts` 未开支撑。
- 打印数量比实际需要的多（一副耳机需要 2 套盖帽 + 垫片），多出来的可以当备件。

其他需要准备的：与 M2 螺丝匹配的黄铜热熔螺母、**M2 × 6 mm** 螺丝（每侧 1 颗）、两根编织款发圈（照片中为橙色）。

---

## 文件夹结构

```
akg-k712-pro-repair/
├── README.md              本文档
├── LICENSE                CC BY-NC-SA 4.0 法律文本
├── 3d/
│   ├── k712pro_pin_v2.3mf 盖帽 + 垫片（替代零件 3 和 7）
│   └── k712_inserts.3mf   C 形垫套（左右尺寸调整用）
├── images/                过程照片 01–17（已去除元数据、部分区域已打码）
└── ref/
    ├── NOTICE.md          第三方文档版权声明
    ├── Manuale-AKG-K712PRO.pdf
    └── AKGK712.pdf
```

---

## 索引

| 路径 | 说明 |
|---|---|
| `README.md` | 修复说明（本文） |
| `LICENSE` | CC BY-NC-SA 4.0 全文 |
| `3d/k712pro_pin_v2.3mf` | 盖帽（带 Logo）+ 内侧垫片，Bambu Studio 工程 |
| `3d/k712_inserts.3mf` | C 形垫套 ×4（测量后按需加在一侧，调整左右对称），Bambu Studio 工程 |
| `images/01_hair_ties_preparation.jpg` | 准备：一罐编织发圈（替换橡胶吊带用） |
| `images/02_printed_pin_caps.jpg` | 打印完成的 3 个双色盖帽 |
| `images/03_pin_caps_heat_set_inserts.jpg` | 盖帽背面，热熔铜螺母 |
| `images/04_screw_size_check.jpg` | 用螺丝规确认螺丝规格（M2 × 6 mm） |
| `images/05_slider_inner_side_screw.jpg` | 滑块内侧：垫片 + 螺丝 |
| `images/06_slider_outer_side_logo_cap.jpg` | 滑块外侧：Logo 盖帽 + 发圈 |
| `images/07_sliders_with_elastic_cord.jpg` | 左右滑块总成，发圈穿法 |
| `images/08_grille_removal_tweezers.jpg` | 用镊子逆时针旋下格栅 |
| `images/09_cord_routing_at_earcup.jpg` | 耳罩端：发圈绕过钢丝末端连接块 |
| `images/10_earcup_lid_opened.jpg` | 上盖翻开，内部结构与引线 |
| `images/11_cord_routing_measure_a.jpg` | 用尺测量左右尺寸（照片中两侧都装了垫套，仅为测量状态，勿照搬） |
| `images/12_cord_routing_measure_b.jpg` | 用尺测量左右尺寸（同上，勿照搬垫套位置） |
| `images/13_reassembled_side.jpg` | 装回后侧面（背景屏幕已打码） |
| `images/14_reassembled_front.jpg` | 装回后正面（背景屏幕已打码） |
| `images/15_reassembled_in_hand.jpg` | 装回后手持 |
| `images/16_final_front.jpg` | 完成图（正面） |
| `images/17_final_side.jpg` | 完成图（侧面） |
| `ref/NOTICE.md` | 第三方 PDF 版权声明 |
| `ref/Manuale-AKG-K712PRO.pdf` | AKG K712 PRO 规格页 + K612/K712 官方维修手册（爆炸图、零件表、维修提示）。**© AKG / HARMAN，不受本仓库许可协议约束** |
| `ref/AKGK712.pdf` | K712 测量数据表（频响、阻抗、THD 等）。**© Source Interlink Media，不受本仓库许可协议约束** |

---

## 参考资料

- **AKG K612 / K712 Service Manual**（#2458Z00XXX, 10/2015）及 **K712 PRO Cutsheet** —— `ref/Manuale-AKG-K712PRO.pdf`。本文的零件编号、名称和拆装方法均参考自此手册。官网：<https://www.akg.com>
- **AKG K712 Headphone Measurements** —— `ref/AKGK712.pdf`（第三方测量数据，阻抗 @1kHz 约 67 Ω，90 dB SPL 需约 0.237 Vrms）。

---

## 许可协议

本仓库中 **作者原创的内容**——照片（`images/`）、文字（`README.md`）以及 3D 模型（`3d/`）——采用 [知识共享 署名-非商业性使用-相同方式共享 4.0 国际许可协议（CC BY-NC-SA 4.0）](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh-hans) 授权，完整法律文本见 [`LICENSE`](LICENSE)。

- ✅ 可以：分享、转载、修改、打印自用，但需署名并以相同协议共享。
- ❌ 不可以：**任何商业用途**（包括售卖打印件、模型文件或以本内容盈利）。

**`ref/` 目录下的 PDF 不在上述许可范围内。** 它们是第三方版权文档（© AKG Acoustics GmbH / HARMAN International；测量数据表 © Source Interlink Media），按原样收录、仅供维修参考，所有权利归原权利人所有，如权利人要求将立即删除。详见 [`ref/NOTICE.md`](ref/NOTICE.md)。

AKG 和 K712 是 AKG Acoustics GmbH 的商标。本项目与 AKG / HARMAN 无任何关联，也未获其认可。
