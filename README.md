#Unity3D 事件总线#


----------


从EricFreeman那里fork来的,进行了许多改进,去掉了一些高级用法(对,我看不懂),增加了一些基础常用功能

功能(**添加**)包括:

1. 事件创建
2. 事件发送
3. **事件取消**
4. **监听者优先级**
5. **事件返回值**

**PS:本库不能用于多线程.推荐在Unity3D简单工程中使用**

**PS:本库不能用于多线程.推荐在Unity3D简单工程中使用**

**PS:本库不能用于多线程.推荐在Unity3D简单工程中使用**

# 使用方法: #

	using UnityEvent;

## 监听者部分: ##

**注册事件监听器**

**priority设置监听优先级**


     public static void Register<T>(this object obj,int priority=10)
	 public static void Register(object obj, Type listener, int priority=10)

**反注册事件监听器**

    public static void UnRegister<T>(this object obj)
	public static void UnRegister(object obj, Type listener)

## 事件发生在部分: ##

发送事件:

	public static void SendMessage<T>(object message)

##Ievent##

所有事件必须继承此类,提供了取消事件和返回值的功能

##IListener###

所有监听者必须实现的接口