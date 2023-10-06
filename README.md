Built on Vulkan-based graphics platform, it is being developed for my personal hobby and planned to be used for my graphics and parallel computing course projects. This semester, it is being used to complete assignments and experiments for the course DPA8190, and it is still being improved

- 资源管理
  组件模式，装饰器模式，名字叫法很多，和ue的类似，静态模型组件和蒙皮网格模型组件，这么设计是为了和ue更加贴近，更亲切。
  actor需要哪个组件，就生成哪个
  
- 命名规则

  f是结构，c是核心 类似u

###### Question

- Delegate 

  [Delegates and Lamba Functions in Unreal Engine | Unreal Engine 5.3 Documentation](https://docs.unrealengine.com/5.3/en-US/delegates-and-lamba-functions-in-unreal-engine/)

- WindowsMessageProcessing.cpp

- CoreMinimalObject: 

  - In it's derived class CFieldObject: what does "Field" refer to in its name? 

- CoreObject::Component derives 3 children : inputCompoent, fogComponet and TransformationComponent. 

  - Why does a component have a parent and list of children?

  - Is InputComponent only used for editorEngine?

- ![](NoteImage\Question01.png)

  Core	文件下应该是一些General的接口类，但是在这里重度依赖DX12的api，是不是很不科学？

###### Classes

![](NoteImage\CEngine.png)

![](NoteImage\CRenderingEngine.png)