Unity3D 事件总线
======================
从别人那fork来的代码,其实实现很简单,然而懒人的我并不想写.
# 使用方法: #

## 监听者部分: ##

注册事件监听器(在start函数中调用):
     EventAggregator.Register<BaseEvent>(this);
反注册事件监听器(在OnDestroy函数中调用):
    EventAggregator.UnRegister<BaseEvent>(this);

## 事件发生在部分: ##

发送事件:
	 EventAggregator.SendMessage<BaseEvent>(new BaseEvent());

BaseEvent是我做的一个事件基类,其他事件类必须派生此类才行.