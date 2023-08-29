# kahsolt-repo-index-tutorial

    A repo index of me @Kahsolt, also advices for coding newbies :)

----

### 如何写胶水代码 / 插件 / 再封装

⚪ 场景

- 我找到好几个有趣的项目，想把它们缝合在一起使用
- 我找到一个有趣的项目，它提供了插件API，我只要写个新插件就能实现想要的功能

⚪ 要点

- 尊重原项目设计思路，**不要** 直接改动原始代码，除非迫不得已 (如: 某些版本兼容性问题)
- 通过 **包装 (wrap)**、**继承 (inherit)**、**复制后修改 (copy & modify)** 来复用已有代码
- 设计一个抽象层，来统一化来自不同项目的可用组件

#### 胶水代码

点云视频数据处理

- https://github.com/Kahsolt/MPED-over-point-cloud-video

神经网络 - 对抗攻击:

- https://github.com/Kahsolt/adv-SAM
- https://github.com/Kahsolt/adv-patch-defense

神经网络 - 语音生成:

- https://github.com/Kahsolt/soft-vc-acoustic-models
- https://github.com/Kahsolt/soft-vc-acoustic-model-ablation-study
- https://github.com/Kahsolt/hubert-pitdyn

#### 插件

扩散模型 Web 应用:

- https://github.com/Kahsolt/stable-diffusion-webui-size-travel
- https://github.com/Kahsolt/stable-diffusion-webui-hires-fix-progressive
- https://github.com/Kahsolt/stable-diffusion-webui-vae-tile-infer
- https://github.com/Kahsolt/stable-diffusion-webui-prompt-travel
- https://github.com/Kahsolt/stable-diffusion-webui-vid2vid
- https://github.com/Kahsolt/modified-euler-samplers-for-sonar-diffusers
- https://github.com/Kahsolt/Cubemap-Tiling

#### 再封装

量子计算:

- https://github.com/Kahsolt/pyvqpanda


### 如何破坏性地就地魔改一个项目

⚪ 场景

- 我找到一个有趣的项目，需要替换其中大部分资源为我自己的才能用，我不关心这个项目以后的更新

⚪ 要点

- 从原仓库开 fork
- 如果你要把仓库完全专门化 (为某个目的特化，而让原项目失去通用性)，那你随便怎么改都行

#### 案例

- https://github.com/Kahsolt/hana-tap


### 如何从零开始写一个简单的项目

⚪ 场景

- 我面临一个全新的问题，没有基础代码，需要自己动手丰衣足食

⚪ 要点

- 模块化：2 ~ 4 个模块可以解决 90% 的问题
  - 独立性：模块只应依赖输入数据的形式和内容，而不应依赖别的模块的具体内部实现方式/特性
  - 通用性：模块可以直接搬到别的项目里，甚至开箱即用
  - 一致性：模块对外/对内 API **命名风格** 和 **语义层次** 大概一致
  - 非冗余性：每个模块功能性的交集应该尽可能少
    - 大块的 **数据常量/静态资源** 尤其不应当存在冗余
    - 否则这些功能应该被收集在一些工具模块 utils/constants 中

#### 案例

神经网络:

- https://github.com/Kahsolt/benchmark-pytorch-mmodel
- https://github.com/Kahsolt/nn-simple-tutorial
- https://github.com/Kahsolt/adversarial-prune
- https://github.com/Kahsolt/Neural-Classifier-Prototypes
- https://github.com/Kahsolt/textgenrnn-postmodern-philosophy

量子计算:

- https://github.com/Kahsolt/Tiny-Q

工具:

- https://github.com/Kahsolt/SQLBuilder
- https://github.com/Kahsolt/Akasha
- https://github.com/Kahsolt/IfYaml
- https://github.com/Kahsolt/dvcfg2oto
- https://github.com/Kahsolt/sodayo-mini

玩具:

- https://github.com/Kahsolt/a-puzzle-a-day-ext
- https://github.com/Kahsolt/img_to_wav
- https://github.com/Kahsolt/pic-dedup
- https://github.com/Kahsolt/TuringMachine
- https://github.com/Kahsolt/Istah


### 如何从零开始写一个综合性的项目

⚪ 要点

- 有一定的架构设计，但不要设计很多很大很通用，因为你写不完
- 先写一个简单的项目
  - 当某些模块变得臃肿时，再去 **分解** 它
  - 当某些模块功能不足时，再去 **扩展** 它
  - 当某些模块合理地发生了内在耦合/等位替换，再去 **合并/并置** 它们，或者为他们创建一个 抽象基类super_class / 管理器manager / 适配器adapter
- 学会让你的软件演化
  - 学会用 git tags 和 releases
  - 学会写 release note

#### 案例

Web 网站:

- https://github.com/Kahsolt/kahsolt.pythonanywhere.com

机器学习:

- https://github.com/Kahsolt/conv2d-kernels
- https://github.com/Kahsolt/water-quality-predict
- https://github.com/Kahsolt/Universal-Confusable-Perturbations

量子计算:

- https://github.com/Kahsolt/YouroQNet
- https://github.com/Kahsolt/Mindquantum-Hackathon-2023-VQE

----
by Armit
2023/08/29 
