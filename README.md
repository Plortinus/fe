# 前端技术方案积累

## 可视化

### HTML + CSS

### SVG

### Canvas

### WebGL

* Fragment Shaders（片段着色器）的入门指南 [The Book of Shaders](https://thebookofshaders.com/?lan=ch)


## Vue

### Vue大对象性能优化

处理大对象时，可以考虑以下解决方案来优化性能：

**1. 分页或虚拟滚动：**
如果可能的话，将大对象的数据进行分页处理，只在需要时加载当前页的数据。或者对于列表或表格等大型数据集合，可以使用虚拟滚动技术，只渲染可见区域的数据，而不是渲染整个列表。这样可以减少渲染和处理大量数据的负载，提高性能。

**2. 惰性加载：**
只在需要时加载大对象的部分数据，而不是一次性加载全部数据。根据用户的操作或视图的可见性，动态加载数据，避免不必要的性能开销。

**3. 数据分片：**
如果大对象包含多个属性或子对象，可以考虑将其拆分成多个较小的数据片段，只处理当前需要的数据。这样可以避免一次性处理整个大对象，减少内存占用和处理时间。

**4. 节流和防抖：**
当处理大对象时，特别是与用户输入或交互相关的情况下，可以使用节流（throttling）和防抖（debouncing）技术来控制触发事件的频率。这样可以减少不必要的计算和渲染次数，提高性能和响应速度。

**5. 缓存数据：**
如果大对象的数据是相对稳定的，可以考虑对数据进行缓存。通过缓存机制，可以避免重复的数据处理和计算，提高访问和操作数据的效率。

**6. 使用索引或哈希表：**
如果大对象需要频繁的搜索、筛选或访问特定属性的操作，可以考虑使用索引或哈希表等数据结构来加速这些操作。通过优化数据访问方式，可以减少搜索和筛选的复杂度，提高性能。

**7. 懒加载子组件：**
如果大对象包含了大量的子组件，可以考虑使用懒加载来延迟加载和渲染子组件。这样可以减少初始渲染的负载，只在需要时才渲染子组件。

**8. 内存管理：**
对于大对象，要注意及时释放不再需要的内存。在组件销毁时，清理相关的资源和引用，避免内存泄漏。

根据具体情况，可以选择适合你的解决方案，或者结合多种优化策略来处理大对象的性能问题。同时，根据应用的需求和数据量，进行性能测试和评估，确保满足应用程序的性能要求。
