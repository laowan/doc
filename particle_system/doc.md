# 粒子系统使用说明 #

## 编辑器 ##

![](particle_editor.png)

界面主要上下两部分组成，上面列出当前粒子系统的所有可配置的参数，当点击相应参数时，下面会出现对应控件，可以修改参数的值。

参数可分为四类：

- Particle System，系统参数
- Emitter，发射器参数
- Affector，影响器（效果器）参数
- Render，渲染参数

## 系统参数 ##

- Max particle：可同时存在的最大粒子数目

## 发射器 ##

粒子的初始大小、位置、颜色、速度、生存时间等参数，由发射器来决定，不同的发射器可以产生不同属性的粒子。  
目前已经实现的发射器有以下两个：

- Point
- Circle

发射器可配置的属性如下：

- Emission Rate：发射速率，每秒中发射的粒子个数
- Emit from：发射粒子的位置
- Angle：发射器的角度
- Radius：发射器的半径
- Velocity：粒子的速度
- Time to live：粒子的生存时间
- Scale：粒子的大小
- Start color：粒子的颜色

#### Point ####

圆锥体，Angle 和 Radius 如下图所示。
> 类似 Unity 中 [Shape module](https://docs.unity3d.com/Manual/PartSysShapeModule.html) 的 Cone。

![](point_emitter.png)

Point 类型的发射器发射粒子的位置（Emit from）有四种选择，分别为 Base、Base Shell、Volume、Volume Shell。

#### Circle ####

扇形，Angle 和 Radius 如下图所示。
> 类似 Unity 中 [Shape module](https://docs.unity3d.com/Manual/PartSysShapeModule.html) 的 Circle。

![](circle_emitter.png)

Circle 类型的发射器发射粒子的位置（Emit from）有四种选择，分别为 Base、Volume、Edge。

## 影响器（效果器） ##

当一个粒子诞生时，它的大小、颜色等参数都是固定的，如果想实现在粒子的生命周期中，大小、颜色等参数可动态改变，就要用到影响器的功能了。  
目前已实现的影响器有三个，可通过编辑器顶部的按钮创建，如下：

- Scale
- Color
- Animator

#### Scale ####

#### Color ####

#### Animator ####

## 渲染参数 ##

- Texture：可配置当前粒子使用的纹理图片   
  
> 1. 要求 png 格式
> 2. 只有当前 effect 文件夹中的图片才可以被选择（*.ofeffect 同级目录）
> 3. 建议图片长宽相同，如128*128

- Blend Mode：配置混合模式

