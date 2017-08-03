# layer-node
layer笔记

http://www.layui.com/doc/modules/layer.html


使用方法

```html

<!---引入--->
<script src="layer/layer.js"></script>
<script>

layer.open({
  /**
  弹窗类型
  0:（信息框，默认）等同于layer.alert('酷毙了', {icon: 1});
  1:（页面层）等同于layer.tips(content, follow, options)
  2:（iframe层）
  3:（加载层）等同于layer.load(0);
  4:（tips层）
  */
  type: 0,
  title:'弹窗标题',
  content: '弹窗内容，content可传入的值是灵活多变的,随着type的不同而不同,详见官方文档',
  skin:'', //弹窗皮肤，默认为空，layer内置有两种layui-layer-lan  layui-layer-molv,还可以写自定义class名
  area:'',//弹窗宽高，默认auto，但当你只想定义宽度时，你可以area: '500px'，高度仍然是自适应的。当你宽高都要定义时，你可以area: ['500px', '300px']
  offset:'',//弹窗坐标默认垂直居中offset: ['100px', '50px']，详见官方文档
  icon:0,   //默认：-1（信息框）/0（加载层）,信息框默认不显示图标。当你想显示图标时，默认皮肤可以传入0-6如果是加载层，可以传入0-2
  btn: ['按钮一', '按钮二', '按钮三'],//默认值为'确认'，每个按钮都有点击后的回掉函数，详见官方文档
  btnAlign:'r',//按钮对齐方式，默认值为'r'居右，值可以是l r c
  closeBtn:'1',//关闭按钮样式 1/2
  shade:''//遮罩样式，默认是0.3透明度的黑色背景（'#000'）。如果你想定义别的颜色，可以shade: [0.8, '#393D49']；如果你不想显示遮罩，可以shade: 0
  shadeClose:'false'//是否点击遮罩关闭
  moveEnd: function(layero){//拖动完成后触发
  console.log("拖动完成");
  }
  tips:'',//tips方向和颜色
  success: function(layero, index){
   console.log(layero, index);
  },
});
layer.ready(callback)//页面加载后执行 
layer.msg('hello');//出现一下自动消失的那种
layer.confirm(content, options, yes, cancel) //询问框
layer.close(index) //关闭特定层
</script>
```
