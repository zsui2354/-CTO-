# THE STARTUP CTO'S HANDBOOK

## 高绩效工程团队的基本技能和最佳实践
### By Zach Goldberg

免责声明：
出版商和作者对本书或其内容不作任何形式的陈述或保证，也不对此处的错误、不准确、遗漏或任何其他不一致之处承担任何责任。

在出版时，本书中显示的 URL 指的是作者和/或作者附属机构拥有的现有网站。 WorldChangers Media 不对这些网站负责，也不应被视为认可或推荐这些网站；它也不对其自己以外的任何网站内容或互联网上非 WorldChangers Media 创建的任何内容负责。

2023, Zach Goldberg, zach@zachgoldberg.com

Paperback: 978-1-955811-56-9

Ebook: 978-1-955811-57-6

Library of Congress Control Number: 2023918702

Cover design: Michael Rehder /www.rehderandcompanie.com/ Layout and typesetting: Paul Baillie-Lane/www.pbpublishing.co.uk Editors: Stephen Nathans-Kelly & Paul Baillie-Lane

Published by WorldChangers Media PO Box 83, Foster, RI 02825 www.WorldChangers.Media

https://ctohb.com https://startupctohandbook.com

## 奉献精神

感谢马克斯·明茨 (Max Mintz) 教会我学习和重视生活中重要的事情。

对于我遇到的每一位直接下属，感谢您的耐心等待，并回顾了我确信是我犯下的许多错误。

感谢我的妻子，感谢她对我的许多追求的包容和支持，这本书包括在内。

## 赞美

>Zach Goldberg 的 CTO 手册为所有工程领导者提供了引人注目的日常资源。无论是实用的日常框>架还是富有洞察力的观点，戈德堡的书都将立即帮助您解决培养高绩效工程团队时最复杂的问题。
>
>迈克尔·洛普（Michael Lopp），randsinrepose.com


>给当今初出茅庐的工程领导者的好建议！
>
>Matt Mochary，执行教练，《The Great CEO Within》作者，mocharymethod.com


>Zach 为初创组织（及其他组织）的首席技术官创建了资源，做得非常出色。作为早期公司的技术领>导者，他针对我们所面临的实际人员、流程和技术问题提供了可行的建议。
>
>托尼·卡勒博士LA CTO论坛联合创始人、TechEmpower创始人CEO、CTO Aggregage创始人

>任何工程领导者的基本指南！
>
>Gordon Pretorius，Typeform 首席技术官

>扎克简洁的章节讲述了如何智慧，巧妙地提炼了数十年领导早期技术团队的在职经验。值得一看！
>
>Daniel Demetri，首席执行官兼 3x 初创公司高管

>CTO 手册是一本充满灵感的合集，为有抱负和经验丰富的技术领导者提供了实用、可操作的建议。 无论您是正在从头开始建立世界一流的工程团队，还是有成为首席技术官的雄心，或者已经担任该>职位多年，这本手册都是您不可或缺的指南。
>
>Eric Johannsen，Dama Financial 首席技术官，《C# 8.0 in a Nutshell》作者

>当我在黑暗中跌跌撞撞地试图自己解决这个问题并被几本技术管理书籍淹没时，这是我需要的所有东西的简洁总结。
>
>Charlie von Metzradt，MetricFire/Hosted Graphite 联合创始人

# Contents
- [介绍](#introduction)
  - [作者](#the-author)
  - [使用本书](#using-this-book)
- [业务流程](#business-processes)
- [人与文化](#people--culture)
  - [管理基础知识](#management-fundamentals)
    - [专业技能树](#the-professional-skill-tree)
    - [改善：持续改进](#kaizen-continuous-improvement)
    - [辅导](#coaching)
    - [寻找管理导师](#find-a-management-mentor)
    - [1:1 会议](#11-meetings)
    - [越级会议](#skip-level-meetings)
    - [教练经理](#coaching-managers)
  - [招聘和面试](#hiring-and-interviewing)
    - [速度是你的朋友！](#speed-is-your-friend)
    - [何时招聘：员工人数规划](#when-to-hire-headcount-planning)
    - [寻找候选人](#sourcing-candidates)
  - [入职培训](#onboarding)
  - [绩效管理](#performance-management)
  - [团队构成](#team-makeup)
  - [领导职责](#leadership-responsibilities)
  - [你是哪种类型的创业公司首席技术官？](#which-type-of-startup-cto-are-you)
    - [以技术为重点的首席技术官 *又名首席架构师*](#the-tech-focused-cto-aka-the-chief-architect)
    - [以人为本的首席技术官 *又名工程副总裁 （VPE）*](#the-people-focused-cto-aka-the-vp-of-engineering-vpe)
    - [外向型首席技术官 *AKA：技术销售/市场主管*](#the-externally-focused-cto-aka-the-head-of-technical-salesmarketing)
- [技术团队管理](#technical-team-management)
  - [科技文化和一般哲学](#tech-culture-and-general-philosophy)
  - [技术债务](#tech-debt)
  - [技术路线图](#technology-roadmap)
  - [技术流程](#tech-process)
    - [工作流程](#workflow)
  - [开发者体验 (DX)](#developer-experience-dx)
- [技术架构](#tech-architecture)
  - [建筑学](#architecture)
  - [工具](#tools)
    - [钻探技术](#boring-technology)
  - [DevOps开发运营](#devops)
  - [测试](#testing)
  - [源代码控制](#source-control)
  - [生产升级](#production-escalations)
    - [根本原因分析 (RCA) 练习](#root-cause-analysis-rca-exercises)
  - [IT](#it)
  - [安全与合规性](#security-and-compliance)
- [结论：衡量成功](#conclusion-measuring-success)
- [书籍参考](#book-references)
  - [数字参考文献](#digital-references)
- [术语表](#glossary)
- [关于作者](#about-the-author)
- [关于出版商](#about-the-publisher)

# Introduction

### 永远学习
十四岁时，我的父母送我去参加为期数周的电脑露营营。这和你脑海中想象的一样极客：一排排折叠桌，几十个（大部分）年轻男孩粘在灰色的 CRT 显示器上，更多地关注《虚幻竞技场》游戏，而不是他们的编程课。两年后，十六岁的我回到计算机训练营担任辅导员==&编程老师，我喜欢其中的每一分钟。我很幸运，在很小的时候，我就认识到并且我的父母支持我对计算机和软件编程的热爱。

又过了几年，到了我在宾夕法尼亚大学读一年级之前的那个夏天。我确信我本科时想学习计算机科学，但我脑子里也有一个想法，我喜欢商业。我的父亲开始了自己的生意，我的兄弟刚刚从商学院毕业，所以经商似乎是一个好主意。宾夕法尼亚大学以其双学位课程而闻名，这些课程让学生毕业时获得工程和商业等多个领域的学位。

这个前景对十八岁的我来说似乎是完美的，所以我给我的导师马克斯·明茨博士发了电子邮件，并尽职尽责地安排了一次会议来讨论我的双学位项目申请。作为一位非常慷慨且以学生为中心的教授，明茨博士慷慨地同意了，并邀请我到费城托斯卡纳咖啡馆一边喝咖啡一边谈论这个问题。

在选定的那一天，我从纽约开车三个小时到达费城，坐在明茨博士对面，渴望听到如何玩弄这个系统。我认为关键是选择正确的课程并获得足够好的成绩才能获得资格。然而，明茨博士有其他想法。

满怀期待，准备接受如何完善简历的指示，我喝了一口咖啡，问他：我如何进入双学位课程？我很快就认识了这个人，当时麦克斯拿起一张餐巾纸，在上面画了一条 X-Y 轴，然后看着我的眼睛，问我是否知道狭义相对论是什么。我希望我有那一刻的视频，因为我想象我的脸扭曲成一个相当有趣的形状。在我回答完之前，麦克斯就出发去参加比赛了。在接下来的两个小时里，他向我介绍了爱因斯坦的理论。当我们结束时，我的大脑已经崩溃了，我们一次也没有讨论过有关宾夕法尼亚大学双学位项目的任何事情。

在接下来的几个月里，我们又喝了几杯咖啡，每当我向马克斯询问申请或简历时，他都会引导我回到真正的科学领域。马克斯希望我“学习”不仅仅是吸收他目前正在讲授的任何主题，而是要真正善于学习，并学习困难的事情。马克斯不在乎他的学生在四年结束时会收到什么试卷，只要他们每个人都准备好在余生中继续学习即可。

当我大学毕业时，马克斯已经成为我的亲密朋友和知己，他从根本上塑造了我的教育道路。麦克斯没有给我鱼，而是递给我一根钓鱼竿，并教我如何上鱼饵和钓鱼。

没有一本书能给你像麦克斯在本科生时给我的经历。我对你现在正在阅读的这本书不做这样的承诺。相反，我讲这个故事是为了强调关注学习本身的基础知识的价值和影响。

作为技术领导者，继续学习的愿望、意愿和能力对于您的成功至关重要。对于任何人来说，拥有太多的技术知识，无法成为现代技术工作所需的一切方面的真正专家。我喜欢将一个追求科技职业的人想象成 RPG 游戏中的角色，他必须每周花 40 个小时收集技能点，而不是杀死敌人来升级。你可以选择用来花费累积积分的技能树，但你需要明智地选择。技能树的种类繁多，不可能全部解锁，所以你必须专精。

科技最美妙的事情是我们的领域在不断发展。与你一起工作的人将会改变。您使用的工具将被更新或弃用，并且用于完成您工作的新技术将不断出现和消失。当您踏上技术领导力的冒险之旅时，管理这种变化的唯一方法就是期待它、接受它，并拥抱与您的团队和领域本身一起学习和成长的机会。

>我希望人们认真学习。我希望他们深入挖掘。我希望他们有所收获，最重要的是。它不是 RSA，也不是[细致入微的算法]；那些并不重要。他们对自己的信心可以在学术界之外成长和学习：这意味着他们不需要我。他们所需要的只是能够坐下来阅读书籍或今天的互联网，然后自己学习东西。
>
>马克斯·明茨博士，1942–2022

### 初创公司技术领导者的困境

大多数初创公司都有一位技术联合创始人。此人编写了大部分初始代码库，雇用了最初的几名工程师，并至少通过前一两轮融资为初创公司举办技术展示。

在雇用第三个和第十个工程师之间的某个时间，这个人将不再亲自敲击键盘，而是开始将所有时间都花在管理团队上。此时，经常会出现问题：团队开始更慢地交付功能，缺陷率开始攀升，系统稳定性可能会受到影响，总体成本上升，其他创始人开始担心。

到目前为止，技术联合创始人或任何技术领导者很可能已经将整个职业生涯投入到成为一名出色的程序员上，而不是培养领导技能上。那么，由于他们的领导能力为 1 级，他们犯错误并浪费公司的时间和金钱就不足为奇了。

无论您的头衔是什么，也无论您何时加入公司，如果您将大部分职业生涯和经验都奉献给了技术，并且您现在承担着对人员或部门的责任，那么您必须意识到自己现在处于领导角色，这一点至关重要;仅靠您的技术背景和才能不足以取得成功。虽然一些技术技能是运行软件工程团队的赌注，但现实是，要做好领导工作，您需要关注人员领导、管理、架构和一般决策技能。

人员领导力并不适合所有人。我相信您听说过技术创始人随着公司发展而辞职的故事。苹果联合创始人史蒂夫·沃兹尼亚克（Steve Wozniak）也许是这种模式最著名的例子。退到一边并不可耻；沃兹尼亚克认识到技术工作是他所热爱的，也是他想花时间的地方。你最好至少为自己考虑一下同样的事情：确定编程是否是你的天才领域以及给你带来最大快乐的工作。如果是的话，您将在晋升到最高级技术人员的行列时拥有美好的职业生涯。

但是，如果您或您的情况使您得出结论，管理或领导团队是您渴望的角色，那么本手册将为您提供一个良好的起点，帮助您在成为成功的技术领导者的过程中扩展您的技能。

## The Author

我的第一次创业经历是在大学一年级后的夏天。我不记得为什么我要在 Eduware 实习，也不记得他们为什么接受我的申请。我所记得的是每天早上和另外四名年轻的软件工程师一起在一楼办公室后面的一个小房间里工作。我们当中年龄最大的一定有二十五岁了；我当时十九岁。只有我们五个人围坐在马蹄形的桌子旁，并肩开发 .NET 教育应用程序。作为一名工程师，我可能一无是处，但我很幸运，组里最年长、最资深的工程师花时间教我并帮助我理解工具，我逐渐变得更有生产力。

在办公室后面一个闷热的房间里，那次经历一定给我留下了很好的印象，因为从那以后，我选择在另外七家创业公司工作：Invite Media、WiFast（现在的 Adentro）、SoChat、AutoLotto、Trellis Technologies、GrowFlow 和 Equi。在展示广告和交易所竞价公司 Invite Media，我与首席技术官合作领导了一个快速增长阶段，最终在 2010 年被谷歌以 8100 万美元的价格收购。在 Google，我接管了 Invite 即将离任的首席技术官的网站可靠性职责，并监督公司与 Google 堆栈的整合。

从那时起，我继续与他人共同创立了WiFast，这是一家专注于Wi-Fi使用民主化和货币化的科技公司，在我们的前两轮主要融资中担任首席执行官和首席技术官。我还曾在中国广州的腾讯公司担任常驻企业家，并共同创立了跨平台消息应用程序 SoChat。从那时起，我曾在 Lottery.com、Trellis Technologies、GrowFlow（被 Dama Financial 收购）和 Equi 担任首席技术官。

我以创始人的心态对待这些角色，努力建立创造性的环境，并推进工程软件应该更科学而不是艺术的想法。

在这段旅程中，我也很幸运地向其他人学习，包括七个出色的工程师团队、无数的咨询/辅导客户和许多杰出的联合创始人。我还积极寻求通过硅谷一位顶级教练的多年管理指导，以及挖掘无数导师和阅读数百本相关书籍来提升自己的领导力。

通过我的阅读，我清楚地认识到，虽然有数百本针对程序员和从事特定技术或工具工作的人的操作书籍，以及数十本针对首席执行官和首席财务官的关于创业财务方面的有用书籍，但我们的行业缺少的一件事是为创业技术领导者提供全面、实用的资源。我们需要一个涵盖核心技能之间所有主题的资源，并解决对我们角色至关重要的一系列领导力挑战和技能。

还有很多关于如何编写好代码、如何进行用户调查或寻找产品市场契合度的博客。这是一本关于技术团队建设的书;它解决了领导者建立公司所需的所有技能，这些技能是他们在传统技术教育或经验中没有学到的。

## Using this Book
作为软件工程团队的领导者，您很可能在角色中遇到过以下一些问题：
* 跟踪、管理或偿还技术债务。
* 招聘、吸引、培养和留住顶尖人才。
* 建立客观、公正、透明的绩效考核制度。
* 建立、管理和维持健康和富有创造力的公司文化。
* 驾驭您与公司其他领导者的关系。
* 忍受缓慢的决策或技术人员之间关于如何架构和构建系统的无休止的循环争论。

似乎每个技术领导者都会在某个时候面临这些问题，但关于如何处理这些问题的建议却不方便地被排除在几乎所有业务或技术课程之外。

我的目标是提供关于这些问题的观点，以及更多问题，并提供有关各种技术如何在现实世界中发挥作用的背景。目标是让读者了解权衡取舍，了解一些可见性，以及让你准备好做出自己合理决定的框架。

本书主要是为那些现在或将来可能发现自己正在管理软件工程团队的人而写的，特别是作为风险投资支持的初创公司的驱动力。对于个人贡献者、非经理软件工程师来说，它也可能被证明是有用的，因为它是一种了解对经理的各种任务和要求的一种手段，这些任务和要求乍一看可能并不明显。

我把这本书编成一个独立章节的集合，涵盖了广泛的主题。它旨在用作参考指南，让读者在一章变得有用时拿起它，而不必从头到尾按顺序阅读。出于这个原因，一些材料在各个章节中重复，以确保每一章都可以独立存在，而不需要前面的章节作为上下文。

我在每一章中的目标不是对这个话题进行详尽的讨论或回顾。相反，目标是介绍该主题，提供思考该主题的概述或结构，提供一些最佳实践，并建议参考资料以更深入地探索该主题。可以把这本书看作是与技术领导力相关的主题的广度优先集合。由读者来决定哪些主题对他们来说最有趣，并在具备一些背景和观点的情况下，深入研究最相关的内容并将知识付诸实践。

归根结底，这本书是我的个人经验和我认为有用的资源的综合，穿插着来自同行、导师和顾问的建议和意见。如果本书中有一些你不同意或认为不正确的地方，你想让我知道，或者如果你觉得这本书有帮助，想直接与我沟通，请随时联系 zach@ctohb.com。我也很乐意在同一地址讨论咨询、辅导和指导机会。

# Business Processes
在本书中，你会发现许多关于业务流程的描述。我概述这些过程的目的是为如何实施您面临的问题的解决方案提供一个起点。

根据您的团队和公司的规模，此处描述的内容可能看起来过于繁琐和繁琐，或者可能看起来过于稀疏和不复杂，无法满足您的需求。现实情况是，随着公司和团队的发展，您将需要重塑开展业务的方式。你的五人公司，当它发展到二十、五十、一百或一千人时，它的运作方式将大不相同。我强调了重要的核心原则，并让你们根据现在的团队来调整它们，并随着未来业务需求和限制的变化而扩展您的方法。

# People & Culture

## Management Fundamentals

推荐阅读：*管理人类* 迈克尔·洛普（Michael Lopp）

管理的黄金法则：尽一切努力让团队发挥最大作用。在技术领导中，就像在任何其他领导角色中一样，衡量你作为经理的绩效的最佳标准是团队本身的绩效。这意味着您应该考虑并花时间做一切必要的事情，以帮助各个团队成员独立和集体地完成最佳工作。

帮助你的团队取得成功需要谦逊，因为它需要始终如一地将你的直接下属的需求置于你自己的需求之上。您将需要调整和调整您的风格、行为、思维和行动，以满足工程团队成员的需求。这将包括愿意犯错，思想开放，并向你的直接下属学习。

如果你相信这段旅程，要知道你会犯错误。与你的团队一起承认这些错误，他们会更加信任你。也要知道，成为一个完美的管理者不是一个可以实现的目标;你能指望的最好的事情就是总是在小方面有所改进。在从事人员管理工作之后，您将学到一生关于技术和人类的课程，这将使您成为更称职的经理。

在《管理人类：一个软件工程经理的尖刻而幽默的故事》一书中，Michael Lopp 写道：

*与您一起工作的每个人都有一套截然不同的需求。满足这些需求是使它们满足和富有成效的一种方式。倾听这些人的声音并在脑海中记录他们是如何建立起来的，是你的全职工作。这是你最重要的工作。我知道工程高级副总裁告诉你，按时完成项目是第一项工作，但你不会编写代码、测试产品或记录功能。团队将做这些事情，而你的工作是管理团队。

在那段简明扼要的段落中，洛普谈到了管理的所有关键点。首先，您是一个倾听者，一个个人和职业发展教练，以及抵御世界上可能分散注意力、压力或以其他方式阻止您的团队尽最大努力的外部力量的盾牌。

### The Professional Skill Tree
许多视频游戏都涉及技能树的概念。对于那些不熟悉的人来说，技能树是一系列技能或能力，随着玩家在游戏中的进展而解锁。每个技能都可以通过花费技能点来解锁。问题是：在任何给定时间，要解锁的技能都比你要花费的技能点还要多。技能树会迫使您在选择某些技能之前选择其他技能。技能树也为你的职业生涯提供了一个合理的模型。在任何给定的工作中，您都可能为某些技能而不是其他技能积累技能点。

在您的技术领导力之旅中，您已经将许多技能点投入到技能树的技术/工程分支中。我给你的主要见解是，技能树的管理分支同样庞大，如果你到现在还没有在这个领域投入积分，即使你是 100 级工程师，你也会以 1 级经理的身份开始你的新领导职位，盯着一棵巨大的橡树，里面有尚未解锁的关键技能。一旦您的公司拥有少数工程师，这些技能将影响您与团队一起扩大规模的能力。

### Kaizen: Continuous Improvement
*Kaizen*是日语中改进的意思。这句话作为丰田生产系统的一部分而广为流传。在丰田，所有人员都会得到一个（字面或隐喻的）红色手柄来拉动，使整个生产线停止。如果工人发现生产问题，他们的想法是让他们拉动红色手柄，召集同事和资源来诊断问题，然后在工作继续之前解决它。通过授权团队中的每个人改进流程并投资于其功效，丰田可以经济高效地制造更高质量的汽车。

我不是第一个认为软件工程与传统制造有很多共同点的人（参见 Gene Kim 的 *The Phoenix Project*）。在这种情况下，让这个比喻成为现实：为你的团队提供一个数字红色句柄，并鼓励他们专注于不断改进你所做的一切。优秀团队的成员明白，随着时间的推移，团队会发生变化，客户需求会发生变化，工具也会发生变化，团队将需要重新审视过去的决策并做出改进。

*Kaizen* 不仅适用于团队的流程，也适用于个人。你最好的团队成员将接受持续教育和持续改进的理念，并且不将错误视为失败，而是将其视为改进的机会。
### Coaching

作为经理，你的主要职责是让团队中的人发挥最大的作用，所以在许多情况下，将你的角色描述为教练而不是经理更合适。教练是站在你这边的人，是团队中每个人的智慧和指导的源泉。教练会迅速提供批判性反馈，但也会第一个庆祝和赞美成功。

在与直接下属的互动中，无论他们是个人贡献工程师还是经理，你的目标都是成为他们曾经拥有的最好的教练。
### Find a Management Mentor
快速过渡到领导力的一种方法是给自己找一个管理导师。有很多管理教练有不同的方法;挑战在于找到一个能引起你共鸣的人。

在我担任WiFast（当时的Zenreach，现在的Adentro）业务负责人的第一个职位上，我们迅速雇佣了一个由十名全职员工组成的团队，其中大部分是工程人员。作为初次担任经理，我知道我还有很多东西要学，我渴望利用一切资源成为一名更好的经理。我唯一的问题是我讨厌大多数管理建议。我发现它要么过于规范，没有背景或洞察力，要么完全没有实质内容：如果你愿意的话，是绒毛。直到我遇到了我的第一位管理教练乔纳森。

故事是这样的，我们的投资者之一，First Round Capital，正在旧金山举办一次管理峰会，距离我们的办公室大约三十分钟车程。到目前为止，我发现 First Round 的人素质很高，所以当我收到邀请时，他们的支持暂时消除了我一直存在的绒毛过敏症，我报名了。

当我开车到山顶时，我感到很受鼓舞，因为观众相对较少，只有大约三十人，足以容纳一个感觉像高中教室的地方。我坐在高中折叠托盘的桌子上，打开笔记本，拿出一支笔，在页面顶部写下了日期和第一轮资本管理峰会。可悲的是，这将是我整个上午唯一写的东西。

在前半天，有三四位演讲者谈论各种话题，他们每个人都缺乏任何可操作的建议或见解——换句话说，就是胡说八道。当我们休息吃午饭时，我考虑早点开车回去，在办公室工作半天。我查看了议程，发现我们确实有一个完全不同的下午演讲者名单，所以我决定至少要听听第一个。

午餐后第一位发言者是乔纳森。与之前的演讲者不同，他没有幻灯片，当他走到班级前面时，他似乎有点匆忙，也许有点措手不及，或者可能只是紧张。然而，从他嘴里说出的第一句话却讲述了一个不同的故事：

*请允许我透明地操纵你。

我永远不会忘记那一刻。说得多么有趣;这似乎是一个矛盾的术语，比如说，“这句话是假的”。（如果你很好奇，这被称为[说谎者的悖论]（https://ctohb.com/liarsparadox））。乔纳森继续解释说，这正是重点：他想说些什么来吸引我们作为观众的注意力，他完美地成功了。在接下来的三十分钟里，我做了大量的笔记，不是关于操纵人，而是关于理解一般人。

我紧紧抓住乔纳森说的每一句话。半小时的会议结束时，乔纳森说他得赶飞机，然后有些匆忙地跑出了房间。我低头看了看我的笔记本，发现我在最后三十分钟里做了三页笔记，而前四个小时却没有，然后从椅子上站起来，追着他跑。

我设法抓住了他，就在他上一辆黄色出租车的时候。乔纳森有些生气，问我想要什么。我问他是否做过私人教练。他回答说，“请组织者连接我们”，然后上车起飞。聪明的是，他没有以这种或那种方式当场指导，他给自己留下了机会，在决定我是否值得他花时间之前，通过组织者对我进行勤奋。幸运的是，当我要求组织者让我们取得联系时，联系人对我说了很多好话，乔纳森同意参加一个介绍性辅导课程。乔纳森和我将继续在多家公司合作多年，我可以自信地说，他的指导在我的领导之旅中是无价的
### 1:1 MEETINGS
1：1 会议是您与直接下属之间的私人会议。人们很容易将 1：1 视为状态签到会议，并且议程完全集中在手头的业务或技术主题上。如果议程包括这些主题也没关系，但这是您与直接下属建立辅导关系的机会。你应该利用这段时间真正了解和理解你的下属是如何思考的，找出并确定他们的优势，并认识到你可以解决的弱点，以帮助这个人把工作做到最好。

### SKIP-LEVEL MEETINGS
最好半定期（每月或每季度）与向您汇报的任何经理的直接下属开会。这些称为跳级会议，因为您通过直接与他们会面来跳过组织结构图上的某个级别。事实上，你并不是想用跳级来破坏你的经理，恰恰相反。通过收集更多数据并听取不同的观点，您将能够更好地与经理合作，处理有助于改善业务的事情。

关于跳级会议议程的一些快速想法：

* 让员工放心，确保他们知道会议的目的，你不是为了解决问题或做出由他们的实际经理更好地处理的决定。

* 让他们知道您想建立关系，并听取他们对领导力、文化、战略和公司方向的见解。

* 与员工联系;提出问题并保持好奇心。

* 互联网上有许多很好的跳级实际模板/议程。这是我推荐的 managementcenter.org 中的一个：[ctohb.com/skip]（https://ctohb.com/skip）。
### COACHING MANAGERS
随着组织的发展，您可能会不再有任何个人贡献者直接下属。每个实际编写代码的直接贡献者都由中层经理管理。因此，很明显，有效的中层管理人员对组织的绩效至关重要。你的工作是确保你的经理获得他们需要的支持、资源、培训和指导，使他们能够尽最大努力指导团队中的工程师。

培养高素质中层管理人员的最大因素当然是雇用合适的人，但其次是持续的培训和支持。如果你有能力监督一个经理团队，我鼓励你在你的组织中建立以下内容：

* 建立持续学习的文化。

* 例如，鼓励您的经理建立一个以内部管理为重点的读书俱乐部。
  * 定期与管理团队分享您自己学到的见解，并让他们对自己的团队做同样的事情。如果您使用的是公司聊天工具，则用于 #management 见解或类似内容的专用频道是进行此类对话的好地方。

* 建立高标准的教练和管理。

- 向你的经理明确你对管理意味着什么的期望，对教练、1：1、绩效管理等的期望。
  - 在内部文件中明确规定您的管理期望，并将其作为管理层招聘和入职的一部分。

* 提供详尽且易于理解的管理培训材料。

- 为您的经理提供资源，以追求持续的学习和专业发展。这可能包括购买公司订阅的学习计划、赞助员工参加会议、聘请管理教练或正式确定内部或外部指导计划。

- 在团队中每个成员的常规预算过程中考虑这些培训材料的成本。

* 培养面向外部的思想领导力文化。

- 鼓励你的经理成为你所在行业的思想领袖。这可以采取公司博客的形式，作为嘉宾参加技术或管理播客，或在会议上发言。

### 1:1 Meetings with Engineers
你的工程师应该定期向你发泄，所以如果他们是，不要惊慌，这是完全正常的，事实上是非常可取的。您应该至少每两周与团队的每个成员进行一次 1：1 会议，如果不是每周一次。在这些会议中，你的目标是为你的工程师创造一个安全的空间，告诉你他们的想法，并让你积极倾听和参与这些话题。

对于强大的工程师来说，这意味着他们意识到周围世界的不完美之处，他们想告诉你这些不完美之处。你的工作不是解决他们提出的每一个问题;你的工作是倾听，提出问题以澄清你的理解，并说服他们你确实理解，然后引导他们找到解决方案。有时，可能会有直接的问题，或者您可以直接提供帮助的事情，但这不是常态。

你在这里提供的价值是让你的直接下属感到被倾听，并指导他们自己有效地处理问题。

#### 1:1 Content and Agenda

归根结底，您在 1：1 会议中的目标是与另一个人建立关系，并进行脆弱和关键的对话，使您能够帮助他们做到最好。如果你的直接下属有一个广泛的议程，那很好，从那里开始。但是，如果他们的议程一直局限于正在进行的战术性工作项目，而您没有进行更高层次的“我们如何工作”的对话，那么我鼓励您补充他们的议程，以便他们更好地了解您的会议目的，并为未来的会议带来更多实质性的问题。

将你的议程和他们的议程联系起来的最简单方法是有一个共享的文档，也许有一些结构/模板，以引出你认为重要的讨论主题。在会议之前提供此文档还可以为您和您的员工提供一个共享的地方，以便在会议之间捕捉想法，在会议之前构建想法，所有这些都有助于提高会议时间的生产力和效率。

还有几种 SaaS 工具也有助于促进 1：1 对话。值得注意的例子包括 Culture Amp 和 15Five。不过，您不需要工具;一个简单的文档同样有效。我使用的模板可在 [ctohb.com/templates]（https://ctohb.com/templates） 获得;它包括在个人、部门和公司层面讨论喜欢/希望的项目的提示，以及经理和员工之间的双向反馈。

#### 1:1 Playbooks

为这些工程 1：1 建立剧本是确保这些会议解决一组一致的主题并且不会偏离轨道的另一种有用方法。您的 playbook 应确保您的 1：1 涉及以下内容：

**冲突：** 在您的直属团队内部、跨工程团队、跨职能部门

**性能和开发：** 通常是您的工程师在寻求有关如何改进某些东西的建议

**清晰度：** 工程师可能对某事有一般的想法，并正在寻找你的观点，或者看看你是否有与他们不同的信息

**背景：** 公司更广泛地发生了什么，以及贡献者的工作与这些目标/目的有何关系

#### Radical Candor

金·斯科特（Kim Scott）在她的《激进坦率》（Radical Candor）一书中定义了“激进坦率”（Radical Candor）一词。该书将“激进坦率”定义为既有赞美又有批评的沟通，并确保交付既包括个人关怀，又涉及直接挑战。我认为最好将这一点与斯科特书中概述的其他三种沟通方式进行对比：

**令人讨厌的攻击：** 有时被称为残酷的诚实或正面刺伤，其特征是直接挑战但缺乏个人关怀，可能表现为不真诚的赞美或不友善的批评

**毁灭性的同理心：** 来自个人关怀但缺乏直接挑战的沟通

**操纵性不诚实：** 又称背刺或被动攻击行为，其特征是既不关心个人，也不直接挑战

我鼓励你阅读斯科特的书，但如果你不这样做，那么至少要了解这些术语，并将它们用作指导工具，以推动你的团队定期练习激进的坦率。

### Benefits of Overcommunication

对员工来说，最糟糕的事情莫过于感觉自己的经理与自己沟通不够。在缺乏信息的情况下，人们会自然而然地假设最坏的情况；缺乏信息也会成为焦虑和困惑的主要来源。

相比之下，过度沟通的后果却很少。过度交流最坏的结果就是分散注意力或变得多余，而这些问题只要在过度交流的形式上稍加考虑就能轻松解决。因此，毫不奇怪，大多数初创公司都会投入大量资金，将过度沟通纳入公司文化，并经常将其作为公司的核心价值观。

#### Email
现在与你打交道的几乎任何人都已经使用电子邮件25年了，或者从小学低年级开始，所以这当然意味着他们知道如何有效地使用它，对吧？不幸的是，在工作中有效使用电子邮件并不一定是常识。因此，您需要帮助鼓励最佳实践。以下是有效使用电子邮件的一些一般建议：

* 不要让电子邮件成为你的工作。

* 与其整天打开电子邮件或持续监控电子邮件，不如每天固定时间检查电子邮件。
  * 禁用手机上的电子邮件通知。虽然这个特别可能看起来是亵渎神明的，但我鼓励你尝试一下。它不仅大大减少了您收到的通知数量，而且您会发现自己养成了在准备好参与时主动检查电子邮件的新习惯。这使得电子邮件成为一种有意识的活动，而不是持续的背景滋扰。

* 每天进入收件箱零。
  * 花时间学习您的电子邮件工具或使用可选的电子邮件助手附加组件/插件来帮助对电子邮件进行排序和分类，这样，到一天结束时，每天，您都不会有未读电子邮件。
  * 将收件箱归零并不意味着对每封电子邮件采取行动或回复。如果您使用电子邮件作为待办事项列表，那很好（尽管它并不理想，请参阅会议和时间管理，第 28 页，以获得更好的待办事项列表替代方案）;只需确保将电子邮件待办事项列表从核心收件箱中分类，这样您就不会将其与未分类的电子邮件混淆。

* 不要在电子邮件中解决问题。

* 电子邮件是进行深入讨论的次优媒介，尤其是当涉及两个以上的人时。群组电子邮件最适合用于协调和过度沟通，而不是解决问题。
  * 了解电子邮件往往缺乏细微差别和语气，这使得意图容易被误解。
  * 撰写或参与细致入微的群组电子邮件线程的诱惑是一个很好的指标，表明同步对话是解决手头主题的更好论坛。15 分钟的讨论通常可以解决 20 封邮件的电子邮件线程只会触及表面的问题。
  * 写下自己的想法通常是一个非常富有成效的练习，但电子邮件并不是促进和捕捉书面头脑风暴过程的好方法。鼓励你的团队在维基上写备忘录，以促进深入思考。

* 不要依赖电子邮件进行长时间或深入的沟通。
  * 一般来说，电子邮件是长篇内容的不良媒介。长备忘录最好放在内部 wiki 或文档中，以便将来可以评论、更新和轻松引用。

* 最好保持电子邮件相对较短，并针对关键想法进行项目符号。

* 不要犹豫，对请求/行动项使用粗体或突出显示等基本格式。

* 注意你的听众。

- 工程师通常更喜欢编写代码而不是阅读/回复电子邮件。问问自己，电子邮件是否真的是与受众沟通的正确方式。一般来说，与某人沟通的最佳方法是*他们*喜欢的方法，而不是你的方法。
  - 很容易让同事远离电子邮件线程，要么是为了不让收件箱泛滥，要么是故意的，要么是无辜的错误。如果你坐在那里考虑在电子邮件线程中添加/删除哪些人，这是一个好兆头，电子邮件一开始就是错误的论坛。

#### Synchronous Chat

您的公司很有可能已经采用了某种形式的同步聊天平台;在 2000 年代初期，它通常是 Google Chat 或 MSN Messenger 产品，而在 2020 年代，它更常见的是 Meta 的 Slack、Microsoft Teams 或 Workspace。如果您目前不在这些平台之一上，则值得考虑采用它们。

绝大多数公司，从第一天创业公司到拥有 100,000 多家公司的巨人公司，都采用了它们并取得了巨大的成功。

要想取得成功，就要注意并围绕一些固有的缺陷进行规划：同步聊天程序要求双方都停止他们正在做的事情并参与其中，并且它们会导致对话组织不善，并且不会产生持久的工件供您的团队参考。您可以而且应该认识到这些缺点，并通过为您的团队设置如何使用这些工具的基本礼仪和期望来弥补它们。

Slack 自己的博客上有一篇很棒的文章，其中包含一些常见的最佳实践，网址为 [ctohb.com/slack]（https://ctohb.com/slack）。

以下是使用同步聊天工具的一些建议：

* 尝试在消息中包含所有必要的信息以继续对话。如果您要向同事提问，请在问题中提供足够的上下文和信息，以便他们能够有最好的机会全面回答。这样做可以最大程度地减少发送的通知数量，减少来回通信量，并缩短解决问题的时间。像 loom.com 这样的工具对此非常有帮助。
* 使用邮件格式设置功能，如项目符号和标题，使较长的邮件更易于扫描，相关信息更易于查找。

* 将对话集中在特定渠道或线程中。尝试一次与多个人就多个主题进行对话是徒劳且令人沮丧的。

* 了解通知时间表和请勿打扰功能。您还应该鼓励您的团队成员在任何同步聊天程序中设置“请勿打扰”时间表，以尽量减少焦点/流程时间的中断。

* 本着过度沟通的精神，默认与公共渠道沟通。更好的是，建立一种文化和标准操作程序，将对话和由此产生的决策转化为公司 wiki 或其他适当文档/信息存储中长期存在的、有组织的文档。

* 对于向多人发送通知的消息，例如，@here 或 Slack 中的@channel，要非常谨慎。特别是随着公司的发展，发送这样的消息很可能会发送通知并可能打断数十名员工。

#### Asynchronous Communication

异步通信是指任何不打算立即获得响应的通信。为了有效，接收方应该能够花时间处理信息，然后深思熟虑地回复。异步通信的一个关键要素是，初始消息是一个完整的思想，并包含允许另一方响应的必要上下文。

一个陈词滥调的例子是可怕的“功能已损坏”错误报告。在几乎所有情况下，错误报告都应该发送到工单系统，而不是直接消息。在消息中收到错误报告的工程师没有上下文来知道哪个功能被破坏了，或者它以什么方式未能达到预期。因此，工程师的回答可能会包含一些问题，需要与记者进行更多的往返，这既浪费了时间，又造成了挫败感。

与此形成鲜明对比的是错误报告，其中包括完整的书面复制步骤以及用户尝试使用该功能并演示失败的视频。这种方法很有可能使工程师能够在不需要任何进一步跟进的情况下进行修复。

底线是这样的：每当您以异步格式向某人发送消息时，请向该人提供他们需要的所有信息，以便他们能够以推进对话的方式理解、处理和回复。

####  Asynchronous Culture

您会惊讶地发现，经过深思熟虑的异步通信可以取代同步聊天或会议。良好的异步通信不仅意味着更少的会议和中断，而且还可以留下全面的书面文档供其他人将来处理。一些初创公司，如Levels Health，实际上已经将默认异步的想法融入了其公司文化的核心，并产生了巨大的影响（ctohb.com/async）。

#### Documentation

文档是扩大组织规模的关键要素。把事情写下来的好处很多：书面文档可以帮助入职、培训、过度沟通、深思熟虑、彻底、建立文化、避免非受迫性错误等等。您的角色不仅仅是相信文档的价值和投资回报率，而是要建立文档文化和重视文档的团队。

建立良好文档文化的一些技巧：

* 自己践行价值，为团队树立榜样。有一次，我把一个团队从每周写零篇内部维基文章转移到每天写几篇，大约八周的时间。从字面上看，我唯一能做的就是鼓励这种文化变革，就是开始自己写文章。我所做的一切都有意义，可以与我写成文章的团队分享，我会在适当的时候分享这些文章的链接。很快，其他经理也开始这样做，在两个月内，团队中的每个人都每周都在做出贡献。

* 让文档成为一种习惯，无处不在。无论是入职、技术规范、拉取评审、内部征求意见 （RFC） 还是备忘录，标准程序都应该是将其写下来并保存在易于访问的位置的有组织的存档中。

* 在适当的情况下制定维护文档的流程。文档很容易过时，在许多情况下，这完全没问题。在其他情况下，文档保持最新很重要，唯一的方法是，如果您有一个包含更新文档的流程或清单。在每个文档上都有一个上次更新日期是向读者发出信号的好方法，表明某些内容是新的或可能已弃用的、过时的或过时的。

* 鼓励团队练习童子军规则（始终让露营地比您发现的更好）。如果他们发现文档不准确，他们应该自行更新文档或将文档明确标记为已弃用。

您应该特别注意的文档的一个关键领域是开发人员如何开始在特定项目或存储库中编写代码。我建议每个存储库都有一个 README.md 文件，至少解释四件事：


**安装：** 如何让应用程序在本地安装和运行

**目录结构：** 如何找到绕过此代码库的方法

**开发：** 开发/运行/测试循环在此代码库上的样子

**部署：** 如何将更改放入此应用的更高环境中

#### On Acronyms at Work

每个组织都有自己独特的文化，以及自己的内部和外部沟通风格。领导者的主要职责之一是确保文化始终支持组织的目标，而不是阻碍它们。

技术组织内部文化中往往会失控的一个因素是产生虚构的首字母缩略词，这些缩略词会随着时间的推移而成倍增加，并使它们旨在简化的沟通变得模糊和过于复杂。这似乎是一个小烦恼，但它是糟糕的沟通策略的症状，可能会失控，特别是因为它会在知情者和不知道首字母缩略词代表什么的团队成员之间设置障碍。作为一个组织的技术领导者，你的工作是定下基调并定义文化，尽管虚构的首字母缩略词的激增很可能不会从你开始，但你的工作是识别它何时发生并在它失控之前关闭它。

在 2018 年 1 月给 SpaceX 员工的备忘录中，埃隆·马斯克 （Elon Musk） 呼吁制定无首字母缩略词政策。从那时起，我就将同样的政策付诸实践，我全心全意地支持它。以下内容来自一封标题为“首字母缩略词严重吮吸（ctohb.com/acronyms）”的电子邮件：

> 在SpaceX上，有一种使用虚构的首字母缩略词的趋势。过度使用虚构的首字母缩略词是沟通的重大障碍，随着我们的成长，保持良好的沟通非常重要。就个人而言，这里和那里的一些首字母缩略词可能看起来并不那么糟糕，但如果有一千个人在编造这些缩略词，随着时间的推移，结果将是我们必须向新员工发布的巨大词汇表。[...]这对新员工来说尤其艰难。[...]首字母缩略词的关键测试是询问它是否有助于或损害沟通。SpaceX 以外的大多数工程师已经知道的首字母缩略词，例如 GUI，可以使用。在实践中，大多数首字母缩略词都是清晰沟通的障碍，而不是好处。这使得新员工更难理解正在讨论的内容。团队需要努力在某个地方维护首字母缩略词定义列表，总的来说，写作和说话都不像乍一看那样节省时间。

这似乎是亵渎神明的，或者是一种试图在文化中强制执行的霸道和愚蠢的规则。我不是建议你惩罚使用首字母缩略词的人，或者把它写在你办公室大厅的墙上。恰恰相反;特别是在一个较小的组织中，只需非常轻的触摸就可以使没有新的首字母缩略词成为您文化的一部分。从你的执行团队那里获得支持，不要创建首字母缩略词，然后鼓励他们温和地提醒他们的经理也这样做，你会惊讶于每个人戒掉这个习惯的速度有多快。对于新员工来说，入职文档中的一两句话通常就足够了，由于入职时的温和注释和目睹周围没有首字母缩略词，他们自己创建它们的可能性要小得多。

### Meetings and Time Management

从广义上讲，有三种类型的会议：定期安排的信息会议、解决冲突的会议和自发/临时会议。作为经理，您的工作是根据会议类型为与会者设定期望。对于信息会议，问问自己会议是否真的是传达信息的最佳方式;有时是这样，但并非总是如此。如果是，请确保以多种方式传达信息，也许是事先在贵公司的 wiki 中提供的书面材料。如果是冲突解决会议，请确保您已提前确定讨论点，以便参与者可以准备好讨论和解决问题。临时会议可能预先有明确界定的目的，无需进一步介绍。

无论会议类型如何，您设置的任何会议都应该有一个明确的目标，受邀者事先知道。理想情况下，每个人在会议前都有足够的信息来了解他们参加会议是否有价值。同样重要的是，你的文化应该赋予人们权力，如果他们认为这不能很好地利用他们的时间，他们就会决定不参加。

#### Time Management

作为初创公司的领导者，你很快就会发现你的时间被分配在多种工作上，而且可能每周有几十个小时的会议。如果你还没有一个适合你的系统，现在是时候投资一些好习惯并组织起来了。我推荐斯蒂芬·柯维（Stephen Covey）的《高效能人士的7个习惯》（The 7 Habits of Highly Effective People）和大卫·艾伦（David Allen）的《把事情做好》（Getting Things Done）作为这段旅程的起点。

#### Meeting Timing

提高团队生产力的方法之一是为工程师创造或留出大量空闲时间。上下文切换（我们倾向于从一个不相关的任务转移到另一个不相关的任务）是昂贵的（参见 ctohb.com/myth 的多任务处理神话），因此您可以为工程师创造更多的时间来完成工程工作而无需切换到其他任务（电子邮件、电话、会议），您支付的总上下文切换费用就越少。

我热衷于为团队宣布一个非正式的会议时间窗口。鼓励工程团队和跨职能团队每天在这两三个小时的窗口内安排会议，尽量不要将工程师安排在该窗口之外。这为您的工程团队留下了健康的时间，让他们专注于工作的核心，并为必要的信息和冲突解决会议腾出空间。如果你的团队每天开会超过三个小时（每周15个小时，几乎是他们一半的时间！），你应该仔细看看这些会议，问问自己是否可以合并和减少它们。

其他团队在无会议日中取得了成功，每周留出一天或多天，而没有人安排任何定期会议。请记住，在每周工作 40 小时的情况下，您的目标是为您的工程团队保留尽可能多的时间作为连续的专注时间块。一个没有会议的日子意味着八个小时的专注时间，但还有三十二个小时需要考虑，所以它并不能解决整个问题。

#### Engineer's Time Recommendation

考虑一下软件工程师的这个假设周：

* 一小时：与经理 1：1

* 两个半小时：每天三十分钟的站立会议

* 两个小时：在其他敏捷仪式（冲刺计划、回顾等）上花费的平均时间

* 四到八小时：审查其他代码

* 四小时：电子邮件/聊天交流

总的来说，一周中大约有 13 到 17 个小时用于会议和交流。如果你在上下文切换和计划外杂项中断上再增加几个小时，那么很快你就会看到每周四十小时工作中最多有一半可用于实际专注时间。如果您不注意会议的安排时间，那么您的工程师不仅只剩下 20 个小时来完成他们的核心任务，而且他们也不会将它们放在连续的块中，从而进一步降低生产力。

我举了这个人为的例子，是为了说明为工程师提供大量专注时间进行工程并不是偶然的。作为领导者，由您决定如何花费他们的时间来开发一种文化和流程，以巩固和最大限度地减少这些干扰，并最大限度地利用个人贡献者进行实际工程的时间。

### The HIPPO

HIPPO 是一个随意使用的行业首字母缩写词，是 Highest-Paid Person's Opinion 的缩写。无论你是否是收入最高的人，你的头衔都会暗示你是。关于 HIPPO 的问题是，大多数员工不愿意挑战 HIPPO。我强烈建议你在讨论中尽量减少这种影响，定期为挑战敞开大门，公开承认错误，然后采取行动并拥护你自己的想法。当你觉得自己这样做得太频繁时，你就会知道你这样做的频率已经足够高了。当你觉得自己做得太过分时，你可能已经达到了大多数员工真正相信你所需的最低限度。

尽管你尽了最大努力让自己看起来平易近人，并愿意相信其他方法，但你在会议中的存在往往仍然会对其他与会者产生潜意识的影响，特别是如果他们在组织结构图中比你低一级以上。请注意这种影响，并尽最大努力仅在您真正增加价值并且团队需要您时才参加会议。对于其他所有内容，您可以在会议结束后获取笔记/录音。

#### To-do Lists

一般来说，待办事项列表是一种非常简单的任务管理形式：它们缺乏结构、任何优先级或时间组成部分。相反，我建议使用基于日历的待办事项列表。与其将工作项放在通用列表中，不如将它们放入实际日历中。

将日历用作待办事项列表有几个优点。它阻止了实际执行待办事项清单上的项目的专用时间，并确保您不会过度投入时间。它允许通过移动项目来确定优先级，并且还可以更轻松地预测何时完成工作。大多数日历系统还具有内置的提醒机制，当您计划执行特定任务时会通知您。

#### Calendar Retrospectives And Time Balance

时不时地说，我鼓励你每月一次对你的日历进行一次历史性回顾，并衡量你是如何度过时间的。例如，Google 日历具有内置的分析功能，只需要对您的日历习惯进行非常少的调整，即可准确汇总时间的使用情况。在查看这些数据时，问问自己，花在各种类型活动上的时间比例是否对你试图实现的目标有意义。检查并确认您正在以发挥您的优势并为您带来个人满足感的方式度过您的时间也很好。通常，只要实事求是地呈现这种数据，就可以为组织和富有成效的变革提供良好的动力。

### Mini Management Frameworks

作为经理，你会遇到很多问题，都遵循着常见的、重复的模式。拥有一个处理问题的心理框架可以加快决策速度，提高决策质量，并为向他人解释决策提供背景和视角。以下是我发现在我的管理之旅中有用的一些框架。

#### Three Stages Of Management Problem-Solving

当面临一个大而模棱两可的挑战时，比如接管管理一个新团队，或者诊断和改善个人表现不佳的问题，我喜欢使用三步法。这些步骤应按顺序完成，以制定解决特定问题的计划。

1. 摄取

* 尽可能多地获取信息。阅读可用的文档，无论是 wiki 文章、性能评估、代码，还是您可以找到的与您的问题相关的任何内容。安排 1：1 会议，锻炼您的积极倾听技巧，并详细记录您的发现。

* 当您开始多次看到相同的事物并且停止看到新模式时，您就知道您已经摄取了足够数量的数据。

* 示例：多个人对你的团队的某个成员的绩效发表评论，经过几次积极的倾听和好奇之后，你已经不再获得关于绩效问题的进一步新信息。

2. 合成

* 一旦你收集了足够多的与你的问题相关的数据，就从收集信息中退后一步，让你的大脑有时间处理。我建议在这个阶段至少分配几天时间。试着刻意停止接受新信息，把这段时间花在从不同的角度看问题。做笔记、画图表、打高尔夫球、洗澡或任何有助于你思考问题并提出适合数据且可操作的分析的东西。

* 继续上面的例子，在这一点上，你可能会尝试提出各种假设来解释为什么这个人表现不佳：他们是如何度过时间的？是技能不匹配，期望不匹配，还是他们的个人生活出了问题等？

3. 行动

* 一旦你有了论文，就该真正制定计划了。当您采取行动时，请务必验证您的计划是否达到了预期的结果。尽可能测试、验证，并在必要时重新开始循环。

#### Team-Based Decisioning Models

有三种模型可用于与您的团队一起做出决策。作为经理，您可以完全自己做出决定，并将结果作为*既成事实*呈现给团队。还有一种相反的方法：你从头开始，完全与部分或全部团队共同开发材料。第三种方法是在前两种方法之间折衷：自己开发草稿，并将其作为稻草人呈现给团队，作为收集反馈和迭代以获得最终版本的起点。这些技术之间的主要区别在于它们花费的时间，以及您从团队那里获得的支持程度。我鼓励你优化支持：确保团队中的每个人都理解决策，并能成为这些决策的拥护者，这是确保你们都朝着同一个方向前进的唯一方法。正如硅谷产品集团（Silicon Valley Product Group）的马蒂·凯根（Marty Cagan）所说的那样，你希望你的团队表现得像传教士，而不是雇佣兵。

**独立模式：** 作为经理独立发展花费的总时间最少，但也产生最少的认同。

**稻草人模型：** 从稻草人开始共同制定决策需要中等时间，并且取决于执行可以产生健康的支持。

**共同开发模式：** 从头开始集体开发可能需要大量时间，尽管它能从那些为开发做出贡献的人那里获得最大的支持。

你使用哪种模型来做任何给定的决定取决于你，我鼓励你对这个选择进行深思熟虑和深思熟虑。如果您觉得自己选择了错误的模型，请不要害怕重新审视它。


#### Two Types of Decisions

在1997年致股东的年度信中，杰夫·贝佐斯（Jeff Bezos）概述了将决策分为第1类和第2类决策的框架。贝索斯写道，第1类决定是不可逆转的，应该有条不紊地、仔细地、缓慢地、经过深思熟虑和协商。如果你走进一扇门，不喜欢你在另一边看到的东西，你就无法回到以前的地方。例如，使用哪种编程语言是类型 1 的决定。

第 2 类决策则相反。它们可以而且应该由高判断力的个人或小团体迅速做出。按钮的确切灰色阴影可能是 Type 2 的决定，因为它很容易更改。

贝佐斯的建议是，将第1类决策用于第2类决策会导致实验和创新的缓慢和失败。

您的大多数日常技术决策都是第 2 类，最好在通过原型或 MVP 实现收集更多数据后快速做出并重新审视或确认。这是因为大多数初创公司技术决策中最昂贵的因素是工程团队在解决方案上投入的时间。如果你刻意限制了用于验证可逆决策的时间（以及成本），那么你只会出局一小部分。大多数 2 类技术决策只有在您投入大量时间和新工程后才会变得不可逆转，因此请尽早严格评估进度。如有疑问，请尽早决定撤销。

#### Breaking Ties
作为团队的领导者，您最终要对实现团队的目标负责。如果整个团队未能达到里程碑，那就由你来承担。因此，当团队内部发生冲突或分歧时，您需要深思熟虑地参与，然后准备好通过遵循以下三种叙述之一来做出决定：

1. 我们会按照你的方式去做，因为你已经提出了一个明确而令人信服的论点，证明它是优越的。

1. 我们会按照我的方式去做，因为它更优越，我会解释为什么使用我作为一个责任范围更广的经理所拥有的额外背景。

1. 我们会走我的路，因为我们无法确定任何客观原因来解释为什么一种方式比另一种方式更好。换句话说，这是一个平局，因为最终我是这里成功的责任方，我们将采用我的方法。我将拥有这个决定的成败。

#### Task Triage The Urgent/Important Matrix

在《高效能人士的7个习惯》一书中，斯蒂芬·柯维（Stephen Covey）博士提出了紧急/重要矩阵（Urgent/Important Matrix），改编自德怀特·艾森豪威尔（Dwight Eisenhower）总统在1955年的一次演讲中提出的一个概念。在紧急/重要二分法中，工作按其紧迫性（即时间敏感性）和重要性（即影响）进行分类。结果是一个四象限图：

我在这里提供这个框架是为了提醒人们考虑出现的各种任务的价值。技术领导者经常受到功能请求、优先级债务、缺陷等的轰炸，并且有视角询问任何给定项目是否重要和/或紧急是一种非常有用且快速的分类机制。

#### People-Puzzle Solver

作为经理，你将要做的大部分工作都是作为人员难题的解决者。你必须弄清楚如何帮助两个人有效地一起工作，或者指导某人提高技能，或者设计一个团队结构来实现协作。人们的行为很难预测，有时团队成员可能会说一件事，但会想到或感觉到另一件事。

鉴于这种不断变化的复杂性，我鼓励你像侦探或科学家一样思考：始终收集数据。形成一个假设，假设如果你采取一个给定的操作，采取该操作，然后收集有关结果的数据，会发生什么。有意识地完成这些动作会鼓励你倾听，见证人们在各种情况下的反应。反过来，这将为你下次与同一个人处于类似场景中时提供有用的数据。

### Joining a Team

作为技术领导者加入团队有两种方式：要么从非领导职位开始在团队中成长，要么被提升为该角色，要么被雇用来领导团队。如果你被提拔到某个职位，大概你有良好的商业背景，已经展示了技术能力，但还没有证明自己在管理和领导方面。相反，如果你被聘为领导层，你可能在管理方面有过往的记录，但缺乏关于组织业务、技术和人员的背景、历史和背景。因此，您在开始担任该职位时的方法应该有所不同，以弥补各自的弱点。

#### Being Promoted into Management/Leadership

如果你被提升为管理角色，并投入时间发展管理技能，或者你有作为经理的经验和记录，那么你可能不会觉得这种转变很可怕，你的目标将是继续提升作为经理的水平。然而，如果这是你的第一个管理角色，你将有一座更大的山要攀登。

人员管理是一种全新的技能，来自让您获得晋升的技术技能。技术技能当然是成为一名优秀的技术经理的先决条件，但还远远不够。了解这一点，并发展新角色所需的额外技能，将是成功成为经理的关键。

如果你从用 C 语言编写代码的后端工程师晋升为用 TypeScript 编写代码的前端工程师，你会做什么样的事情？你可以读一本关于 TypeScript 的书，做一些 TypeScript 编码练习，加入 TypeScript 用户组，阅读一些 TypeScript 博客，等等。

从编写 C 语言到管理人员的转变实际上比 C 语言到 TypeScript 的变化更大。要成功实现这种转变，需要相同水平或更多的主动学习。对大多数人来说，成为一名优秀的人事经理是一生的旅程，而不是一个周末就能掌握的技能。接受挑战，将工作视为从现在开始的终身学习练习。

#### Actionable Management Tips

牢记德国总理奥托·冯·俾斯麦的格言：“傻瓜从经验中学习;我更喜欢从别人的经验中学习**，这里有一些对新经理的可操作提示：

* 寻找管理导师或教练。讨论人们的问题并获得额外的观点是无价的。（参见侧边栏“寻找管理导师”，第 13 页。

* 学习委派。罗伯特·基根（Robert Kegan）的《变革的免疫力》（Immunity to Change）详细讨论了授权的障碍，以及为什么学习授权对管理者的成功如此重要。最重要的是，你对组织的价值不再是你自己的个人产出，而是你团队的价值。对于许多技术领导者来说，这是过渡中最困难的部分，但也是最关键的。

* 照顾好自己。
  * 管理人可能会非常耗费情感。为了始终如一地成为最好的自己，保持冷静、积极和富有成效，照顾好自己至关重要。
  * 找出适合您的方法;也许是冥想、高尔夫、电子游戏或家庭时间。做任何感觉良好的事情，让你神清气爽，为下一个挑战做好准备。

* 注意倦怠迹象，并在它发生之前休息一下。管理人员不一定是每周八十小时的活动。

请参阅本书末尾的推荐阅读清单，以查找更多用于培养管理技能的资源。

#### Being Hired To Lead

如果你被聘为领导一个团队（而不是被提拔为领导职位或作为首次创业的联合创始人担任领导角色），那么你大概同时拥有技术和管理经验。作为现有团队的受聘领导者，您面临的挑战是尽可能顺利地将自己融入新团队，并与新同事建立信任。毫不奇怪，我的建议是在管理新团队时更多地关注人而不是技术。

下面，我概述了外部聘用的技术领导者的一些短期目标，以及一些你应该尽早尝试回答的问题。

目标：

* 与技术团队建立信任。倾听并深思熟虑您何时/多快开始增加价值或改变事物。

* 与其他团队/领导者建立信任，做出合理的承诺并贯彻执行。

* 了解与您一起工作的人以及他们与公司/产品/技术的历史。

* 诊断团队中影响最大的人员特定挑战。是否有工作人员的职级不适当，要么表现不佳，要么表现过高？是否有任何文化挑战需要纠正？尽早采取果断行动纠正文化路线是与可能有意识或潜意识地遭受文化问题困扰的团队成员建立信任的好方法。

* 诊断对整个团队影响最大的技术问题领域，并为团队制定一套短期、中期和长期目标。

问题：

* 谁以前在运行技术？那个人还在团队中吗？
  * 技术领导者经常发现他们想成长为人员管理。如果发生这种情况，您将踏入人员管理空白。另一种常见的情况是，要么之前没有技术领导者，要么他们因表现不佳而离职，而您继承了大量的技术债务。

* CEO说你受雇来解决什么问题？你认为你受雇来解决什么问题？

* 如今，技术团队与公司其他部门之间存在哪些痛点？
* 技术团队中哪些痛点是最高优先级的？
#### Giving Technical Advice to Friends/Strangers

在你简历上有某种形式的技术领导一段时间后，你可能会开始让朋友或朋友的朋友寻求建议。在大多数情况下，我建议接听这些电话，不仅因为网络很有价值，还因为被问到的问题可能会迫使你仔细思考，并把你潜意识里的想法说出来。他们说教别人是真正学习自己的东西的最好方法。

关于为非技术创始人提供建议的快速说明：你可能会不时地被一个自称价值数十亿美元的想法的人找到。接听这些电话的成本非常低，并且是建立一些社交/关系资本的好方法。然而，要注意的是，绝妙的想法本身并不能成就成功的企业。在每一个伟大的想法和成功之间，都有一座巨大的执行力之山，大多数登山者都没有能力登顶珠穆朗玛峰。因此，在向有好主意且没有登山装备的人做出承诺时要非常小心。

#### Traffic: Funnels and Umbrellas

**你可以是一个狗屎漏斗，也可以是一个狗屎伞。 - Todd Jackson，Gmail 产品经理（请参阅 ctohb.com/umbrella 和 ctohb.com/keytogmail）

关于你的产品的问题、疑虑和想法，没有任何严格的流程将它们引导到其他地方，就会找到管理的方式。这不仅包括您，还包括您组织中管理层的每个人。经理是默认的收件箱，杰克逊声明的关键是你的团队是默认的发件箱。你听到，嘿，X 中有一个错误，你想，好吧，工程师 Y 写了那个功能，去把这个错误发给他们。这将是直接向您的团队发送入站信息的一个例子。

相反，更好的策略是充当团队的保护伞。一个好的经理不是将所有入站实时定向到团队，而是组织、确定优先级并为团队提供一个结构化的队列来工作。您的目标是帮助团队集中注意力，限制分心，并为入站应该去哪里提供一个地方，以便有效地处理它。

只有在极少数情况下，作为经理，您才应该向个别工程师强调错误。如果您有一个 bug 队列和处理该队列的流程，则可以在很大程度上消除常规的一次性升级。

管理层应该监控该错误队列过程，以确保队列保持在可管理的长度，并在产品质量未达到目标时调整人员配备或流程。

您应该根据重要性和紧迫性确定队列的优先级。如果出现具有极端时间压力的至关重要的事情，则应将其放入队列并上报到顶部。然后运用常识来处理它。如果你需要打电话给某人以确保他们知道它在那里，那就这样吧，只要这是例外而不是规则。

#### Your First Team
作为技术领导者，您的工作不仅仅是管理技术团队;它还包括担任最高管理层的技术代表。您的职责是在公司所有最高级别的战略讨论中代表工程和技术，并确保工程和技术处于正确的业务方向。有时，这意味着与其他需要脆弱和谦逊的领导者进行艰难的对话，以及使您能够解决冲突并建立在相互信任基础上的对话。这些对话是工作的关键，要使它们成为可能，你必须与你的领导团队深入接触，将他们视为你的第一个团队。

你可能是一个技术含量很高的人。您可能最喜欢您的技术会议，或者至少发现与您的团队一起解决技术问题很熟悉并且非常令人满意。因此，很容易陷入一种模式，即你把大部分时间都花在技术团队身上，而采用“我的团队”是技术团队的心态。这是在技术团队中建立融洽关系的好方法，有时这是最关键的投资关系。

我的指导很简单：不要让技术上闪亮的物体分散你的注意力，也不要限制你与非技术领导者的关系。你与其他领导者的关系以及你与非技术同行的信任将给你带来可信度，并使你能够指导企业从整体上做出良好的技术决策。在技术团队之外建立信任的方式与建立任何其他信任关系的方式相同：良好的沟通，通过做出和履行承诺来定期设定期望，并在错误/失败发生时承认错误/失败。

技术领导者或首席技术官（CTO）将所有时间都花在工程代码上，几乎不参与领导团队，在试图说服其他C级人员进一步投资于工程时，将几乎没有可信度。或者更糟糕的是，当需要做出艰难的决定时，他们甚至不会被要求提供意见。其他领导者将没有背景来理解技术团队所要求的价值，或者对工程在那一刻如何运作的看法，他们将缺乏对未来可能是什么的共同愿景。作为技术领导者，只有定期与领导团队的其他成员互动，分享背景信息，并在此过程中参与对话，才能确保领导团队对工程如何帮助组织以及组织如何随着时间的推移而发展有共同的理解。

### Working With The CEO

每个 CTO CEO 关系都是不同的，尽管所有此类合作伙伴关系都有一些共同点，以及健康关系的一些关键先决条件。

#### Aligning Specific Objectives

首席执行官必须完全信任您领导技术团队实现业务目标的能力。建立这种信任意味着你需要能够与CEO进行良好的沟通，既要通过主动沟通，又要确保CEO总是有足够的背景来提出好的问题。

良好的沟通意味着要学会说商务语言，并避免在领导谈话中陷入技术术语。你想让CEO与你沟通，你说他们的语言越多（如果他们不是技术性的），你能从互动中得到的信息就越多，你们两个人相处得就越好。

#### Aligning Business Direction

您和首席执行官需要对业务方向有共同的理解，并能够进行建设性的甚至有争议的对话，以确保这种理解的深度。信任适用于整体业务方向和特定目标。

有很多方法可以建立这一点，但无论你采取什么方法，你都需要建立信任。参与共同的非工作活动，找到你们分享个人价值观的领域，并使用特定的工具和练习来建立这种信任（参见 Brene Brown 的 BRAVING Inventory，第 ctohb.com/braving 页）。

#### Aligning Culture And Values

与所有 C 级一样，CTO 和 CEO 应该在公司文化和价值观上保持高度一致。尤为重要的是，你要专注于在工程部门内部，以及在工程部门和公司其他部门之间建立积极的文化。技术团队通常是一个非常大的项目，如果不是初创公司预算中最大的一个项目的话。技术人员通常也是最具竞争力的招聘职位，这使得工程部门的招聘和不可避免的非自愿员工流动比其他部门更昂贵。

首席技术官和其他 C 级高管在文化和价值观上的高度一致性是确保技术团队感到受到尊重和融入公司的关键因素，这反过来又应该有助于留住人才。

### Delivering Bad News

与其他领导者或高管共事的一个一般建议是，不要回避向你的领导同事传达坏消息，尤其是首席执行官。由于你要对团队的表现负责，你可能会试图粉饰现实，宣传一切都很好。这种方法存在很多问题：

* 如果事情不顺利，意味着总是错过最后期限或质量低于预期，你的同事会知道这一点，并会想知道为什么你不承认这些失败并解释你将如何改进。现实与你如何表现现实之间的这种差异破坏了对你领导的信任。

* 有时，您需要为软件工程团队腾出时间进行非面向用户的工程作为投资，无论是在技术债务还是未来架构方面。你需要得到其他领导者的信任和可信度，这样其他人才会相信你并了解当时的投资回报率。

请参阅Jocko Willink和Leif Babin的*极端所有权：美国海军海豹突击队如何领导和获胜*的第1章的原则部分，以了解有关拥有失败的重要性的更多信息。

### Speaking the Language of Your Audience

技术主题通常非常微妙;细节决定成败。技术术语在帮助传达这种细微差别方面做得很好，因此当工程师解释技术主题时，他们经常使用其他部门成员无法理解的语言也就不足为奇了。我相信你已经目睹了过于热切的工程师试图用精力、激情和兴奋向非工程师解释他们的项目，结果却是茫然的目光，没有建立新的共识。作为技术领导者，您必须做得更好。

例如，如果你有一个主要的技术债务领域，你想在执行团队中倡导花整整一个月的时间重新构建这个代码领域，你需要以一种易于理解的方式传达你的理由。如果你在讨论延迟、RPC 调用、依赖注入和云服务提供商的首字母缩略词的对话中，你的 CEO 和 CFO 很可能几乎会立即将你排除在外。

另一方面，如果你围绕开发人员的生产力和团队士气来构建对话，并在未来六个月的团队速度的背景下解释债务偿还，你的论点将更有说服力。

### Technical Communication Best Practices

一些确保更成功的讨论和演示的一般技巧，尤其是在谈论技术时与非工程师进行讨论和演示：

预先建立共享语言/词汇。如果你需要使用任何普通高中生不理解的词，请确保你的听众已经知道它们，或者在开始解释之前清楚地定义它们。

使用相关的概念。技术挑战通常与其他技术挑战相提并论：在与非技术人员交谈时，这是行不通的。与其以每秒字节数来描述您的缓慢数据传输，不如将其与高速公路上的交通进行比较。

在此过程中确认理解。在解释过程中向听众提问。如果他们能在你面前说出妙语，那么你就知道你走在正确的轨道上。

不要因为你对技术语言的掌握而认为你在任何方面都是优越的，或者更糟糕的是，让你的听众因为缺乏知识而感到自卑。我不想对你来说太技术化，这是关闭观众的好方法。

一般来说，尽量保持你的解释尽可能简单明了。避免掉进兔子洞，这可能会分散注意力或以其他方式使观众失去兴趣。

## Hiring and Interviewing

作为技术领导者，有效招聘是影响最大的活动之一，也是最具挑战性的活动之一。您经常会发现自己试图在供应受限的市场中招聘人才，并与其他可能比您财力更雄厚的公司竞争。您的顶级候选人可能会收到其他竞争性的工作机会，这意味着您不仅需要对候选人进行资格认证，还需要让他们相信您的机会适合他们。

这样一来，招聘既是一种销售活动（候选人对您/您的公司进行资格认证），也是一个筛选过程（您/您的公司对候选人进行资格认证）。在定义团队的招聘流程时，请务必牢记这一点。

本书的这一部分按顺序涵盖了招聘和面试过程的各个部分，从员工人数计划到入职。

### Hire like a Startup

作为一家初创公司，您在招聘方面有几个关键优势，在此过程中利用这些优势以确保您能够吸引顶尖人才至关重要。一些功能可以为您提供优势：

* 你更小，这意味着你也应该比大型竞争对手更灵活、接触更频繁、招聘速度更快。

* 您可以出售一家极具吸引力的公司和个人成长轨迹。

* 您可以推销一种富有创造力和鼓舞人心的工作场所文化。

* 您可以推销成功的候选人将产生的影响。

* 您可以提供有意义的公司股权，从而能够分享公司成功的好处。

以下是利用这些优势的一些实用技巧：

* 为了快速行动，在发布职位描述之前，请培训并招募同事进行面试。在开始之前，确保每个人都了解日程安排流程、面试脚本和评分标准，以及如何使用申请人跟踪软件 （ATS） 阅读和留下反馈（参见寻找候选人，第 59 页）。

* 提前安排与每位候选人的所有面试。如果您的流程包括四次面试，请在开始时将所有四次面试都列入日历，最好在五个工作日内完成。如果你的团队很快就留下了他们的面试反馈（你应该坚持他们这样做），那么你可以提前通知任何未能通过的候选人，并取消任何待处理的日历邀请。另一种选择是，只有在候选人通过每一轮面试后才安排后续面试，每一步之间都会增加几天时间，从而轻松地将可能为期一周的过程变成三周或更长时间。

* 一个好的经验法则，尤其是在创业公司：没有人会太忙或太重要，以至于他们无法与候选人会面，如果他们这样做是有意义的，尤其是对于更高级的员工。如果一个强有力的候选人要求与你的首席执行官和首席运营官交谈，那么你应该安排与他们会面。

* 确保每个面试官都有一个独特的脚本或指南，涵盖不同的材料，或从不同角度的材料与其他面试。（有关这方面的更多详细信息，请参阅访谈最佳实践的“仅提出新问题”部分，第 63 页。

一如既往，天下没有免费的午餐，作为一家初创公司招聘的好处也伴随着权衡，主要是以风险的形式。候选人几乎肯定会问你关于你公司的产品市场契合度、手头现金或跑道、公司文化和工作/生活平衡的问题。我鼓励你坦率地与候选人谈论这些因素，与你的执行团队合作了解实际情况，并在被问到这些问题时得到很好的回答。

### Speed is Your Friend!

请记住，在招聘顶尖人才时，速度是您的朋友。如果你能在一周内让某人完成你的整个流程，你就会给你的创业公司带来一个重大优势，而大公司的流程通常需要几个月的时间才能做出决定。

### When To Hire: Headcount Planning

现金是一家年轻且尚未盈利的初创公司的命脉，因此，以新工程师的薪水形式承诺每年 100,000 多美元的经常性费用的决定不应掉以轻心。有几个关键因素会影响员工人数决策，其中最重要的是需求、优先级、时间和预算。

#### Role Need/Team Gap
决定招聘的第一步是确定团队中的差距。差距有几种形式。通常，在公司发展的早期阶段，这只是技能差距。例如，您的企业决定将移动应用程序作为您进入市场战略的关键要素，而您的创始团队以前从未在移动领域工作过。当然，随着时间的推移，他们可以学习并变得有效，但从短期和长期来看，聘请一位在移动设备上有经验并希望从事移动工作的高级工程师来构建和维护该项目会更有效率。

其他类型的差距包括资历差距（没有足够的高级经验来做出正确的决策，或者没有足够的初级人才来处理不太复杂的任务）、管理差距（一个经理负责太多人）或主题专业知识差距（团队中没有人对行业的某个领域有足够的了解来指导决策）。

雇用的另一个主要理由是增加团队的总带宽。这些类型的招聘应该与某种业务目标或产品路线图保持一致，这证明在给定时间引入新的永久团队成员是合理的。

#### Role Prioritization And Timing
一旦你发现了一个缺口，下一个要问的问题是什么时候需要填补这个缺口。考虑到获得优秀员工所需的准备时间，何时开始招聘流程是有意义的？

通常有尽快雇用的压力。试着抵御这种压力，因为这并不总是正确的答案。您雇用的每一个新人都增加了团队的复杂性和开销。假设差距的痛苦并不严重，如果你能让一个较小的团队再呆六个月并推迟招聘，这可能是一个好主意，因为它既降低了成本，又让你有更多时间为招聘建立案例。

团队的人数或招聘请求通常必须与其他团队的请求竞争，因此在整个公司开发一种通用语言来讨论招聘的紧迫性或重要性是很有用的。这不必非常复杂;它可能是一个 0-5 的排名系统，其中 0 代表迫切需要，而 5 代表招聘，这很好，但可以等待几个月或几个季度才能变得紧急。

#### Budgeting For New Hires
在一家无利可图的初创公司，你应该有一个财务模型，使支出与收入合理化，并大致预测你目前手头的现金在你需要另一轮融资之前能持续多长时间。大多数首席执行官和首席财务官都对这种模式有深刻而深入的理解;作为技术领导者，您几乎不需要花那么多时间在它上面。

但是，您必须清楚地了解您的部门对该模型的贡献，这主要以员工人数费用（当前和未来）的形式出现。该模型应以年化预算或费用运行率的形式提供一定程度的约束，以指导您的招聘时间。

### Hiring Goals and Objectives
就像设计软件系统一样，当你坐下来设计你的面试过程时，你应该首先考虑你的要求和目标。虽然每家公司都应该有自己的要求和观点，但以下是我在设计面试流程时考虑的一些事情：

**效率：** 雇用候选人需要多少时间和成本？

**成功率：** 被录用的候选人在工作中有多成功，他们在公司工作了多长时间？

**应聘者体验：** 应聘者在完成整个过程后是否会对贵公司给予高度评价，无论他们是否被录用？

**公平的机会：** 你是否确保每个人都有公平的机会被录用，并尽可能避免无意识的偏见？

**可扩展性：** 除了你之外，其他人能否运行这个过程，并像你一样有效/有相似的成功率？

#### Efficiency
对您的公司来说，招聘得好是一项昂贵的任务。这笔费用以实际美元为单位，无论是招聘人员、工作委员会列表还是招聘广告。它还需要时间，主要是员工花在进行面试上的时间。在设计面试流程时，请考虑每个步骤的意图是什么，您要过滤什么，以及完成过滤的最有效方法是什么。

减少或至少分散时间投资的一种方法是让其他团队成员参与招聘过程。根据给定面试的主题，您并不总是需要最高级的工程师在房间里。经过适当培训的招聘协调员可以像高级工程师或高管一样有效地进行电话筛选、文化面试或背景调查。

#### Success Rate
并非每次招聘都会成为贵公司的本垒打。有些人会被错误地升级，有些人不适合文化，有些人会在第一年被解雇或辞职。特别是当你扩大面试流程时，你需要衡量有多少招聘是成功的。作为技术领导者，这是为数不多的机会之一，您可以在其中计算清晰、一致和指示性的指标，因此请充分利用并确保您的流程是一流的。考虑跟踪招聘时间（从发布职位描述到新员工开始日期）、整体员工保留率、新员工流失（或降级）以及前两年晋升的新员工人数。

正如安迪·格罗夫（Andy Grove）在《高产出管理》一书中所讨论的那样，即使是世界级的面试过程也只有70%左右的成功率。从根本上说，招聘存在许多风险：你试图预测某人每周四十小时的表现，一周又一周，仅基于面试过程中收集的一些对话和数据点。

最好的领导者会跟踪他们的成功率，不怕承认招聘错误，并且会招聘缓慢，解雇速度快。

这是无法回避的：解雇一个在被雇用后不久就没有锻炼的新员工，这对每个人来说都是社交尴尬和不舒服的。但是，这对您的团队来说是负责任的事情。一些有助于为新员工提供透明度并帮助管理人员做出正确决策的做法包括实施正式的 90 天试用期或介绍期，并要求新员工/经理每 15 或 30 天签到一次，或使用合同雇用雇佣结构。

#### Candidate Experience
求职者体验是求职者在招聘过程中和之后对贵公司的感受。许多候选人会在申请或面试之前对您的公司进行尽职调查。他们可能会查看在线论坛和社交媒体，看看其他经历过您流程的候选人或员工对您有什么看法。

你不能总是控制人们对你的评价，但尽管如此，你还是希望提供一种候选人体验，使他们更有可能在网上阅读好东西，自己也有很好的体验，从而更倾向于继续你的面试并接受你的offer。

#### Equitable Opportunities
有一种说法是，人们倾向于雇用长得像自己的人。这通常是简单的面试评分方法的结果，这些方法仅仅依赖于面试官的直觉，而直觉往往受到无意识偏见的强烈影响。这种偏见可能会使其他种族、性别、民族等的候选人处于不利地位。

在设计面试流程时，您应该专注于基于与职位描述要求相一致的评分标准进行评估，而不仅仅是面试官的直觉。有关避免偏见的更多信息，请参阅《面试最佳实践》第 63 页中的“避免偏见”部分。



