# 粒子系统使用说明 #
***
## 编辑器 ##

![](https://github.com/laowan/doc/blob/master/particle_system/particle_editor.png)

![](particle_editor.png)

界面主要上下两部分组成，上面列出当前粒子系统的所有可配置的参数，当点击相应参数时，下面会出现对应参数的设置控件，可以修改参数的值。

参数可分为四类：

- Particle System，系统参数
- Emitter，发射器参数
- Affector，影响器（效果器）参数
- Render，渲染参数

## 系统参数 ##

- Max particle：最大粒子数目


## 发射器 ##

- Emission Rate
- Emit from
- Angle
- Radius
- Velocity
- Time to live
- Scale
- Start color

## 影响器（效果器） ##

当一个粒子诞生时，它的大小、颜色等参数都是固定的，如果想实现在粒子的生命周期中，大小、颜色等参数可动态改变，就要用到影响器的功能了。目前已实现的影响器有以下三个：

- Scale
- Color
- Animator

## 渲染参数　##

- Texture
- Blend Mode