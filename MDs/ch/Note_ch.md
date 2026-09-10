# RQ1 能力边界 能不能做
启发式评估


RQ1的组织方式：按“能力领域”分类，横着扫一遍

RQ1问的是：“一个能做doppelgänger研究的平台，应该具备哪些能力领域（C1头像、C2语音、C3动作……C5控制自主性……C9开发体验），这个SDK每个领域打几分？”——关心的是“权限” ：9个领域，一个都不能漏，每个领域给个分数。C5.4只是C5这个领域里的其中一个格，它的角色是回答：“控制自主性这个领域里，'约束不能被可靠执行'这个子问题，分数是多少？”


# RQ2  不同程度 会付出什么代价
技术性能评估

RQ2的组织方式：按“三个条件”分类，竖着比一比

RQ2问的是：“同一个SDK，换A/B/C彻底解决，在5个共同维度（成本延迟、可预测性、可复现性、+B唯一的约束可靠性）上，各自是什么代价？”——它介意“对比” ：A vs B vs C，谁在哪个维度上更贵、更划算。约束可靠性这45次试验的数据，这里的角色是：“帮B在这张A/B/C对比表里，填上它自己的那一格”。


# RQ3 开发者体验

使用情况评估


RQ0问的是"SDK适不适合作为研究平台"，而RQ2用"是否在光谱两端都撑得住、撑得住的代价是什么"来回答"适合到什么程度、适合哪一类研究"，这和RQ1回答的"支不支持哪些具体功能"是两个互补的角度，合在一起才是对RQ0完整的回答。



我继续复盘一下 目前我们的RQ123可以是可以 但是逻辑链断掉了
main RQ To what extent is the IVA SDK suitable as a research platform for controlled doppelgänger experiments in XR?

RQ1 What doppelganger-relevant capabilities does theSDK support, and where are its practical boundaries?
--> Outcome/contribution:
   - theoretical analysis of requirements
   - list of criteria, split by group with checklist √×

RQ2 What are the ????performance???? trade-offs of the constrained AI, full AI)
SDK across the human-AI autonomy spectrum (Woz, Outcome/contribution:Analysis by demonstration
Capabilities? Latency? Feasibility?

RQ1 What doppelganger-relevant capabilities does theSDK support, and where are its practical boundaries?--> Outcome/contribution:theoretical analysis of requirementslist of criteria, split by group with checklist
What do you demonstrate?
How does it relate to Doppelgangers?



RQ3 and how reliably can AI-driven behaviour
be
constrained to a defined persona?
-->0/C:
exemple persona --> constraintes derived from
persona
Empirical evaluation if AI respects constraints
(or how well and why not,...)


RQ4 What is the developer experience of using the SDK for this doppelganger research use case?
-->0/C:
someone's replicating a scenario (1--2 developers, dev-log, final artefact,...)
use-case: constrained AI? Full AI?