## TODO案例目标： 

**掌握Vue基础语法，强化 MVVM（数据驱动视图）思想**

## 功能实现：

### 没有待办事项

当没有待办事项，`.main`并且`.footer`应该被隐藏。

### 新待办事项

在应用程序顶部的输入中输入新的待办事项。加载页面时，应该将input元素聚焦，最好使用`autofocus`input属性。按下Enter键创建待办事项，将其添加到待办事项列表，然后清除输入。确保`.trim()`输入内容，然后在创建新的待办事项之前检查其是否为空。

### 全部标记为完成

此复选框将所有待办事项切换到与自身相同的状态。单击“清除完成”按钮后，请确保清除检查状态。当选中/取消选中待办事项时，也应更新“全部标记为已完成”复选框。例如。当所有待办事项都经过检查后，也应进行检查。

### 项目

待办事项具有三种可能的相互作用：

1. 单击复选框，通过更新待办事项的`completed`值并`completed`在其父项上切换类来将待办事项标记为已完成。``
2. ``通过在`.editing`类的切换上双击激活编辑模式``
3. 将鼠标悬停在待办事项上会显示“删除”按钮（`.destroy`）

### 编辑中

激活编辑模式后，它将隐藏其他控件，并提出一个包含待办事项标题的输入，该标题应突出显示（`.focus()`）。编辑内容应同时保存在模糊和输入上，并且`editing`应删除该类。确保`.trim()`输入正确，然后检查它是否为空。如果是空的，则应该销毁待办事项。如果在编辑过程中按了Escape键，则应保留编辑状态，并放弃所有更改。

### 计数器

以多种形式显示活动待办事项的数量。确保数字由``标签包裹。另外，还要确保变复数的`item`正确的字：`0 items`，`1 item`，`2 items`。示例：剩余**2**件

### 清除完成按钮

单击时删除已完成的待办事项。没有完整的待办事项时应隐藏

## 项目实现步骤：

**1：列表事项渲染**

- 有事项
- 无事项

**2：添加任务**

- 页面初始化时文本框获得焦点
- 敲回车事项添加到任务列表
- 不允许有非空数据
- 添加完成时清空文本框内容

**3.单个任务事项选中状态和样式**

**4.切换所有任务事项为 完成 或 未完成**

**5.删除任务事项**

**6.双击label进入编辑模式**

**7.进入编辑模式后**

- 编辑文本框自动获取焦点
- 在编辑文本框中敲回车失去焦点 和 失去焦点事件时取消标记
- 输入状态下按esc取消编辑

**8.清除所有已完成的任务**

