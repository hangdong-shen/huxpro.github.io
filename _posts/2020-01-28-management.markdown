---
layout:     post
title:      "开发模型和团队运营"
subtitle:   " \"做好软件类项目管理的思考\""
date:       2020-01-29 12:00:00
author:     "Hangdong"
header-img: "img/post-bg-apple-event-2015.jpg"
catalog: true
tags:
    - 总结
---

> “我的管理总结”


## 前言

我在《我在软件类项目管理中遇到的常见问题》一文中描述了软件项目管理中常见的几个问题。本着少谈主义，多提解决方案，“治病救人要对症下药”的原则 ，今天是个大晴天，在此谈一谈我认为软件研发需要做的那些事。

---
## 软件开发模型的选择
通常业界常用的模型有瀑布、原型、迭代和敏捷这四种，根据不同的项目的需要和特点选择一种或者两种合适的模型。常用的一般是迭代和敏捷。

- 迭代模型(iterative model)是由IBM公司提出的一种软件开发方法，该方法包括一系列的增量的步骤或迭代，每个迭代都包括很多的开发活动(需求、分析、设计、实现等)。每次迭代从功能的深度和细化程度来划分，是从模糊到清晰的开发过程。

- 敏捷模型是一种应对需求快速变化的软件开发模型，敏捷模型中，软件项目在构建初期被切分成多个子项目，各个子项目的成果都经过测试，具备可视可集成和可运行使用的特征。换言之，就是把一个大项目分为多个相互联系，但也可独立运行的小项目，并分别完成，在此过程中软件一直处于可使用状态。

当软件开发的需求是比较明确，应选择迭代的模式；当需求变化预期会剧烈变化的项目建议使用敏捷模型。大部分情况下软件从基础架构到基础功能，再到功能迭代，一般都是可以拆分成独立运行的小项目。也有一些项目因为一些特殊性，可以考虑迭代加敏捷的方式。比如每一个敏捷的小项目中采用迭代的方式。

无论选择哪种开发模型，人的因素是最重要的。每一个项目需要结合项目考虑所有人的能力矩阵。大多数情况下，我认为项目的人力资源处于紧平衡状态是健康的。

## 软件生命周期
![](/img/in-post/post-manage/life.png)

## 执行遵循软件规律的开发流程
从入门开始我们就知道软件开发的客观规律中包含如下V模型的规律，这个模型是基础知识，这里就不展开了。

有些软件项目因为各种原因对其中某些关键流程进行了裁剪，无一例外的都发现随着项目的开展，裁剪的流程要大量占用其他未被裁剪流程的时间。比如很多软件项目没有乃至不知道单体测试（单元测试），那么在开发过程中势必大量占用集成测试，甚至是系统测试的时间，而且效果可能很差。

这个模型里面有一点我觉得需要特别强调，就是研发人员除了设计和编码的工作外，一定是要参与测试的，尤其是单体测试是研发人员必备的一个工作，而且这个工作必须在概要设计（如果没有基础架构的话，概要设计要涵盖架构设计）时就要开展。

很多初级的研发人员对测试人员是有鄙视链的，原因就在于针对有些测试场景，测试人员设计了很多测试case验证，但实际上都是围绕着一行代码在反复的测试。这种情况遭到了一些研发人员的嘲笑。要解决此类问题，就必须要加入单体测试（测试case的研发评审也能起到一点效果，但是效率不高）。实际情况中，很多企业不仅仅是民企，软件架构设计上都存在单体测试的缺失，很多人对这个环节的也比较漠视。我本着“存在即合理”的想法，观察这些企业为什么会进入这种误区，几年观察下，发现主要是因为这些企业IT环境资源匮乏和技术能力薄弱导致的。当然也有其他原因，欢迎大家评论补充。

## 软件项目管理
软件项目管理是为了使软件项目能够按照预定的范围、成本、进度、质量顺利完成，而对范围、费用、时间、质量、人力资源、风险、采购等进行分析和管理的活动，通常包含如下子任务。
![](/img/in-post/post-manage/life.png)

---

下面先就项目团队组建和团队运作方面的一些内容进行展开。
## kickoff meeting

kickoff meeting国内称为开工会。这是任何一个项目启动的第一个关键步骤。项目经理需要在这个开工会之前，需要先行对这个项目相关的需求材料和输入进行了解、学习和总结，以我在民企的经历，除了这个学习时间是非常短暂的，还存在需求输入剧烈变动的情况，项目经理需要会抓住一些关键的信息进行梳理。在这个过程中，项目经理同时进行项目组成员的确认工作。我所经历的项目中，有的项目经理是有权限进行人员的选择，但大部分民企人力是偏紧张的，基本处于上级指派，项目经理没有选择的情况。在这种情况下，就会存在被指派的员工，本身没有能力参与本项目的开发。对于刚刚加入公司的新员工，还经历边培养边干的情况，这种情况如果项目周期长，进度不紧张还好，如果项目进度紧张那对项目经理和新员工都是比较大的挑战。打个比方来说，项目经理就是等米下锅的那个厨师，而米的情况就很复杂，项目经理会经历没有米下锅，米的好坏差异太大，米流失等各种情况。

而接到任务的项目组成员，需要交接现有工作，准时参加当前项目组。

在确定了项目成员之后，如果当前的组织存在质量管理这个部门，就可以提出人员的要求。当然这个很多民企业没有╮(￣▽￣")╭。

当上诉三件事妥当的情况下，就可以准备开始kickoff meeting了。立项会议由项目经理主持，部门经理、质量部经理、QA和项目组成员来参加。有可能的话，还应邀请项目的客户方代表、采购专员、培训专员、销售代表来参加。

会议目的是宣布项目组成立；介绍项目情况、客户情况、公司的项目意向（工期、效益等要求）、项目成员情况等。

## 项目团队运作

这部分内容主要涵盖项目团队资源规划原则、团队行动章程、沟通行为准则等几个方面。

### 资源规划原则
主要有以下几个需要考虑的部分：

- 项目组岗位的设置以简单、扁平化为基本原则，统一岗位可复用担任多种角色。
- 角色识别时需要能覆盖到管理、业务、技术、支持类四方面的整体要求
- 规模控制以12个人为拆分原则，超过12个人必须进行小组拆分
 - 小组的设置方法可以从工作性质如开发、测试进行设置；也可以从任务特性如产品A、产品B进行设置；
也可以采用复合型的设置方法；具体需要综合考虑资源、进度、成本、管理等之间的平衡
- 人员能力结构上，需要满足项目建设需要；并从成本控制角度考虑新老搭配的方式，以核心人员加普通人员的方式达到投入产出最优性

### 团队行动章程
- 首先想到他人，努力理解他人
- 尊重别人的个人权利，使别人感到重要
- 互相帮助做对 <—> 而不是做错
- 找寻使想法实现的办法 <—> 而不是找理由说不行
- 在任何情况下均保持积极的思维状态，热情地去做每一件事
- 主动而充满勇气地去行动，就像一切都有赖于你

### 沟通行为准则
沟通行为准则除了上一篇提到了汇报文化外，还包含联系和协商等内容，这部分内容比较大，我的小小博文就不展开了，建议大家去网络上学习管理沟通的一些音频视频材料。

## 团队运行
有几点我觉得是比较重要的

- 团队成员职责分工明确，并能在过程中不断确保和更新
- 团队氛围和凝聚力对业绩的提升也有20%-30%的促进作用，不可忽视
- 团队核心人员的稳定性对整个项目的成败有着决定性的作用
- 团队的优胜劣汰机制也是必须的，如此才能保证团队的长期战斗力
- 团队人员的培养必须作为一种常态工作，核心人员与后备人员要并重
- 团队之间需要加强人才交流，促进人员成长及技术革新

## 结束
好了，今天暂时更到这，欢迎大家阅读、批评和指正，下回再见。

---