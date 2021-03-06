---
title: .NET docs 拉取请求评审流程
description: .NET docs 未启用 PR 合并 Webhook。 本文介绍这些存储库的 PR 流程
ms.date: 01/04/2019
ms.openlocfilehash: f710e330e31e56887d43030290d5aa6a5c62961b
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653588"
---
# <a name="pull-request-review-process-for-the-net-docs-repositories"></a>.NET docs 存储库的拉取请求评审流程

许多存储库并未启用 PR 合并 Webhook，这会自动合并次要 PR。 本文介绍这些存储库的 PR 评审流程。 PR 评审流程的设计目标是：

1. 发布来自团队、产品团队成员和社区成员的高质量内容。
1. 以一致的方式向作者提供及时、可操作的反馈。
1. 促进作者和审阅者之间的讨论。

随着团队的不断创新和平台的日趋成熟，这些流程也会逐步改进。

## <a name="reviewers"></a>审阅者

内容团队成员中的一员评审每个 PR。 内容团队成员可以请求特定产品团队成员进行评审，以验证技术准确性。 内容团队使用 GitHub 的代码所有权功能自动请求内容团队成员进行评审。 作为该流程的一部分，审阅者可以标记其他团队成员来评审内部 PR。 团队成员查看来自同一队列中的团队成员和社区成员的评审请求。

社区成员也可以评审 PR 并提供反馈。 不过，核心内容团队中必须至少有一个成员批准任何 PR，才能合并 PR。

## <a name="review-process"></a>评审流程

根据不同的 PR，评审遵循下面的三种方法之一：

- **小型 PR**：小型 PR 是单个 bug 修复，包括拼写错误、链接断开、小型代码更改或类似的更改。
- **主要发布内容**：主要发布内容是对现有文章、新文章的重要编辑，或对大量文章的编辑。
- **正在进行的工作**：作者可以在标题中打开一个带“[WIP]”标记的 PR，请求正在进行的评审。 “WIP”标记表示“正在进行的工作”。 

若要明确“小型”和“大型”贡献内容之间的区别，可以将参与者许可证协议 (CLA) 自动程序使用的过程作为一个良好的指导准则。 不需要进行 CLA 签名的 PR 可能属于“小型”发布内容。 需要 CLA 的 PR可能是“大型”发布内容。

### <a name="small-prs"></a>小型 PR

评审小型 PR 中的更改是否符合准确性，并使用评审网站上的内部版本进行检查。 由于它们是小型发布内容，这些 PR 不会触发对整篇文章的评审。 

审阅者可能会注意到其他一些可以改进文章的小更改。 如果这些更改的范围也很小，建议将它们作为评审评论。 如果建议的更改将触发更大范围的评审，则将其作为待解决问题并稍后进行解决。 

### <a name="larger-changes"></a>较大更改

较大型 PR 会进行更全面的评审。 以下是所有检查的内容：

- 示例代码必须作为一个可下载的 zip 文件包含在源的 PR 中。
- 示例代码可正常编译和运行。
- 文章明确描述了读者目标，并实现了这些目标。
- 本文符合[样式和语法指南](dotnet-style-guide.md)，并遵循[语音和语调原则](dotnet-voice-tone.md)。
- 所有链接都应正确解析。

内容团队成员将评审 PR，并提交评审评论。 如果只请求小幅更改，团队成员可以通过反馈来“批准”PR。 然后，作者可以处理反馈并合并 PR。 大多数评审会请求更改，在完成这些更改后，审阅者将再次进行评审。

如果编辑需要技术评审，内容团队审阅者将请求相应的产品团队成员进行评审。

### <a name="review-wip-pull-requests"></a>评审“WIP”拉取请求

新作者可能希望在此过程初期获得反馈。 他们可以打开一个 PR，在标题中添加“[WIP]”标签。 在评论中，他们可以请求早期评审。

这些早期评审并不像完整的 PR 评审那样全面。 内容团队将进行评论，但不会使用 GitHub 的评审功能“批准”或“请求更改”。 这些早期评审重点关注文章的结构：大纲、整体内容和示例。 这些评审不包括对语法和正确链接的全面检查。

## <a name="respond-to-reviews"></a>对评审的响应

作者更新 PR 以响应评论，用“+1”回应标记每个已处理的评论，表明它已得到处理。 如果作者不同意评论内容，或者使用不同的方式处理评论，他会添加评论来解释这些变更。

作者会在评论中 @-mentions 初始审阅者，请求重新评审。 

## <a name="response-time-expectations"></a>预期响应时间

内容团队成员通常会在两个工作日内评审新 PR。 如果需要更长时间进行评审，团队成员中的一员会添加评论来确认 PR 并设置期望时间。

提交了评审后，作者应尝试在一周或更短时间内回复评论。 志愿者可能无法满足以上要求，因为他们还有其他事项安排。 在这些情况下，团队成员会询问社区作者是否会更新 PR。 如果不进行更新，团队成员将为其更新和合并 PR。
