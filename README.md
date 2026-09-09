# comfyUi相关

## 基础整合包 (选一个):

**群里太阳大神做的**: sage 2.2+ cu133 + comfy3.2 : (推荐)
https://pan.quark.cn/s/1c89e061190c  (推荐,cu和sage比较新,对H3加速效果较好)


**闲兔**:
https://pan.quark.cn/s/18cb797c5b26 提取码：sJqm  (2080ti 会安装sage 1.x + cu130 )


**AI搅拌手ComfyUI管理大师:**
https://comfyit.cn/article/286


## 升级相关 (可选,选一个):
#### TE启动器:
链接: https://pan.quark.cn/s/228999e7c788 (可以用升级ComfyUI,太阳的整合包里已经有)

#### 闲兔启动器:

介绍: https://www.bilibili.com/video/BV1LqgK6BEz2
 安装包链接：https://pan.quark.cn/s/18cb797c5b26 提取码：sJqm  (作者也是2080ti)  


## 分块(2080必装)

20系列分块
有两个插件都是群里的星佬(胖大星)写的,记得github点星，unet也改了，帮助20系这种不支持bf16的优化量化

https://github.com/star7code/minimax-h3-fp16-exact-star7.git

https://github.com/star7code/minimax-h3-chunk-star7.git

参考工作流(https://github.com/gclinux/2080ti-ai/tree/main/workflow/H3)


## MinMax H3 基础模型 (22G推荐官方int8无剪枝,11G 推荐GGUF量化,需要NSFW推荐10eros):
**官方**:https://modelscope.cn/models/MiniMax/MiniMax-H3
整理网盘:https://pan.quark.cn/s/5794a96c46a6  (31G和 21G模型4选2)

**GGUF量化**:https://www.modelscope.cn/models/realrebelai/MiniMax-H3_GGUFs/files (进一步降低显存,11G的2080ti 可以尝试,22G的建议用官方int8模型)

**Kijai大神**W4A8版本及 VAE 的解码加速版本: https://huggingface.co/Kijai/MiniMax-H3-experimental/tree/main

网盘:https://pan.quark.cn/s/0bb19ad31d34


**红潮**NSFW版本: https://civitai.red/models/958009/redcraft-or-or-redmix-hybrid-a2a-beta1-lightning-8 (请勿在办公室打开)

**dasiwa** 解决浮夸表情版本: https://civitai.com/models/2877206/dasiwa-minimax-h3 搭配加速 https://pan.quark.cn/s/e5468a05559f, 网盘:https://pan.quark.cn/s/d3eab5cfde15

TenStrip的**10Eros**  混合版(F2V ,REFV 合并版本 带NSWF 带4步lora )https://huggingface.co/TenStrip/10Eros-Max/tree/main?not-for-all-audiences=true 


 **Singularity 微调版本(减少崩脸情况)**: https://www.bilibili.com/video/BV1sebn6rEcV 网盘:https://pan.quark.cn/s/6d17529b1181#/list/share 对比测试:https://www.bilibili.com/video/BV1rDbs6jE55 抱脸: https://huggingface.co/WarmBloodAban/Minimax-h3_Singularity 


### 声音修正

https://github.com/T8mars/comfyui-minimax-h3-audio-T8


## 加速(选一个)

#### 4步/8步lora:

##### 商汤(大家默认的官方加速)
商汤lightx2v: https://github.com/ModelTC/Minimax-H3-Turbo#model-specs

##### larryvr(推荐不油腻)
larryvrh  :https://huggingface.co/larryvrh/MiniMax-H3-Turbo-Lora/tree/main
最新V4版本(好用推荐):
网盘：https://pan.quark.cn/s/99b6139d96e2
需要用到特定加载器:
https://github.com/Larryvrh/ComfyUI-MiniMax-H3-Turbo 或者T8的lora加载器

##### 阿里巴巴
阿里巴巴8步lora:https://huggingface.co/alibaba-pai/MiniMax-H3-Acc-LoRAs


#### TE speed 跳步加速:
地址: https://pan.quark.cn/s/9c37b6c9a778
介绍: https://www.bilibili.com/video/BV1WYMR6mETN

#### sage 

 通过压缩主要活跃的注意力,从而减少内存搬运时候的工作量而提升速度.几乎不影响画质

请下载整合包,图灵架构官方不支持,群里大佬已经整合好.

如果你用官方的包,可以用:

:https://www.bilibili.com/video/BV1YSbz6VEzi/?spm_id_from=333.1391.0.0 专门补丁 

或者用群里星佬的插件:https://github.com/star7code/minimax-h3-chunk-star7.git (推荐,集合了多种加速和分块方案)

#### SolAttn 

这是一个Sage的替代品. 通过稀疏注意力机制,把画面非主要部分(例如虚化部分)工作量减少从而加快速度. 对画质有非常轻微影响.如果你没办法用SAGE,可以尝试.但安装也比较麻烦.

https://github.com/kijai/ComfyUI-SolAttn_triton




#### 加速集合
视频: https://www.bilibili.com/video/BV1Kjuo6wE6X/?spm_id_from=333.1387.homepage.video_card.click&vd_source=21da82be5ada7380d6171c0726234845
链接：https://pan.quark.cn/s/ade7543de75e?pwd=vMJQ



## 二次采样/小脸修复/高清超分

二次采样视频介绍:https://www.bilibili.com/video/BV1cq8w6DEfu节点: https://github.com/LBH-123-AI/Comfyui_Minimax_h3_latent_Upscaler 

低显存快速超分:https://github.com/ylchen333/ComfyUI-VOSR2



## 越狱:

越狱模型: https://huggingface.co/ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot/tree/main
 网盘: https://pan.quark.cn/s/6d7543c2cab7 提取码：VxeA 

或者 :

https://huggingface.co/linjian257/qwen3vl_32b_minimax_h3_int8_convrot_uncensored-by-linjian257

破限lora: https://huggingface.co/Serenak/chilloutmix/blob/main/MysticXXX_MMH3-V1.safetensors 建议用v1,因为它可以顺带可以去油腻,不破限时候也可以用. 也有V4你如果重点在破限可以试试https://huggingface.co/Serenak/chilloutmix/tree/main


## 提示词:

T8 : https://www.bilibili.com/video/BV19yhP62EtX
 ComfyUI-H3-VisionPromptor（本地提示词开源项目）： https://github.com/benjiyaya/ComfyUI-H3-VisionPromptor 
Json提示词skill下载链接：https://pan.quark.cn/s/ba8c92aea69d ,介绍:https://www.bilibili.com/video/BV1Pe8B6bEFL

## 导演台:

### 插件类导演台
国内Ai搅拌机大佬做的下载: https://github.com/AIMixer/ComfyUI_MiniMaxH3_Director (作者分享的网盘里有个200G的很多很乱的模型包,基本不用管,安装插件就好)

基于AI搅拌机导演台群里更改的低内存版本(内存低于32推荐,会写硬盘做缓存): https://github.com/fvdfggh/minimax-h3-director-performance-optimization (和上面的二选一)


闲兔导演台: https://www.bilibili.com/video/BV1Lk8a6fEfm (依赖很少,基本都是官方模型,但lora不能选文件,等更新比较好)


国外darksidewalker版本:  https://github.com/darksidewalker/ComfyUI-DaSiWa-Nodes (未测试)

孤海Goohai导演台 : https://github.com/goohai/Goohai-MiniMax-H3_Integration (依赖比较少)教程:https://www.bilibili.com/video/BV17f8y6iE6r/?spm_id_from=333.1387.homepage.video_card.click&vd_source=21da82be5ada7380d6171c0726234845

### 智能体类导演台:

Oh MY : https://github.com/TFboy1/oh-my-minimaxh3-director (来自群里小芋头,看到先去点个星,智能体会调用本地comfyui来生成视频)

## 显存管理

 https://gitee.com/windecay/ComfyUI-ReservedVRAM 




## 生图

### 人物资产
#### 人物多视角资产工作流:
实际上它 支持千问edit/F2K 自己换一下模型是可以的
介绍 : https://www.bilibili.com/video/BV1wYwMzDEvy
下载:https://pan.quark.cn/s/c330ea9212de

#### 4视图 F2K
介绍 : https://www.bilibili.com/video/BV1f8326tEuH
链接：https://pan.quark.cn/s/2558ed644f0f

#### 我比较推荐的lora

https://modelscope.cn/models/yan303145427/krea2-Cc-TM-GreatFigure F2K的魔鬼身材,能出大长腿
https://modelscope.cn/models/yan303145427/krea2-Cc-FY-portrait  让身材更加性感
https://modelscope.cn/models/yan303145427/krea2-Cc-FQWZ-ArtStyle 肢体美化,容易出小红气的pose

## 高清放大

###  Topaz Video AI (非comfyui)
https://www.qijishow.com/down/Topaz%20Video%20AI.html

https://www.423down.com/14531.html



## 大语言模型

两张22G 跑千问, 100+tps,有两个项目:
https://github.com/weicj/2080Ti-LLM-Toolbox
https://github.com/weicj/vLLM-2080Ti-Definitive


单卡GGUF 千问量化版,最高可到50tps,上下文还能拉到255k ,内存最好32G以上
https://huggingface.co/finex666/models
