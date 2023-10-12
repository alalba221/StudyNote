- 资源管理
  组件模式，装饰器模式，名字叫法很多，和ue的类似，静态模型组件和蒙皮网格模型组件，这么设计是为了和ue更加贴近，更亲切。
  actor需要哪个组件，就生成哪个
- 命名规则

  f是结构，c是核心 类似u

###### DX12 vs. Vulkan

| DX12              | Vulkan     |
| ----------------- | ---------- |
| DXGIFactory       | Instance   |
| MianWindowsHandle | SurfaceKHR |
|                   |            |
|                   |            |
|                   |            |
|                   |            |
|                   |            |
|                   |            |
|                   |            |

###### Implementation

- CDirctXRenderingEngine 不再使用，只是用到CRenderEngine这一层， 里面的组件由Vulkan实现
- InitDirecrt3D()  函数不再使用，原函数里面的每一步转而都由RenderEgning里面的各个模块自己实现
- VulkanContext 参考[Piccolo/engine/source/runtime/function/render/include/render/vulkan_manager/vulkan_context.h at games104/homework02-rendering · BoomingTech/Piccolo (github.com)](https://github.com/BoomingTech/Piccolo/blob/games104/homework02-rendering/engine/source/runtime/function/render/include/render/vulkan_manager/vulkan_context.h)

###### Question

- Delegate

  [Delegates and Lamba Functions in Unreal Engine | Unreal Engine 5.3 Documentation](https://docs.unrealengine.com/5.3/en-US/delegates-and-lamba-functions-in-unreal-engine/)
- WindowsMessageProcessing.cpp
- CoreMinimalObject:

  - In it's derived class CFieldObject: what does "Field" refer to in its name?
- CoreObject::Component derives 3 children : inputCompoent, fogComponet and TransformationComponent.

  - Why does a component have a parent and list of children?
  - Is InputComponent only used for editorEngine?
- <img src="NoteImage\Question01.png" style="zoom:50%;" />

  Core	文件下应该是一些General的接口类，但是在这里重度依赖DX12的api，是不是很不科学？
  
- CRenderingEngine 按照命名规则属于核心(start with capital C),  目前代码中Fence,CMDlist 都是引擎中的CRenderingEngine 的member，但是如果要把这些Fence，cmdlist 这些每一个单独抽象一个class出来，他们是属于结构(F), 还是核心(C)?

###### Classes

- C

<img src="NoteImage\CCoreMinimalObject.png" width=600 />

<img src="NoteImage\CEngine.png" width=600 />

<img src="NoteImage\CRenderingEngine.png" width=600 />

- F

  <img src="NoteImage\IDirectDeviceInterfece.png" width=600 />
