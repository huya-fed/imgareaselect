# imgareaselect


----------

> imgareaselect 是一个 允许用户使用简单、直观的点击、拖动界面图像选择矩形区域的jQuery插件。该插件可用于 web 应用程序中轻松实现图像裁剪功能，以及其他功能，如照片标记、 图像编辑功能，等等,Javascript部分主要依托于 jQuery。


## 使用imgareaselect这个插件：

	$(document).ready(function () {
	    $('img#photo').imgAreaSelect({
	        handles: true,
	        onSelectEnd: someFunction
	    });
	});

如果 jQuery 对象中有多个元素，将为所有元素启用该插件。imgAreaSelect也适用于非图像元素，以及任何块元素（例如，<div>有背景图片）； 您可以在 $(document).ready() 或 $(window).load() 事件处理程序初始化插件

## options参数

<table class="table table-bordered table-striped">
          <thead>
            <tr>
              <th style="width: 100px;">参数名</th>
              <th style="width: 80px;">数据类型</th>
              <th style="width: 100px;">默认值</th>
              <th>描述</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td> aspectRatio</td>
              <td>string</td>
              <td>&nbsp;</td>
              <td> 设定选取区域的显示比率，如：”4:3″</td>
            </tr>
            <tr>
              <td> autoHide</td>
              <td> boolean</td>
              <td>false</td>
              <td> 如果设置为true，当选择区域选择结束时消失；</td>
            </tr>
            <tr>
              <td> classPrefix</td>
              <td>string</td>
              <td>”imgareaselect” </td>
              <td> 这是一个字符串，表示插件样式的类名加前缀</td>
            </tr>
            <tr>
              <td> disable</td>
              <td>boolean</td>
              <td>&nbsp;</td>
              <td> 如果设置为true，禁用插件</td>
            </tr>
            <tr>
              <td> enable</td>
              <td>boolean</td>
              <td>&nbsp;</td>
              <td> 如果设置为true，插件被重新启用</td>
            </tr>
            <tr>
              <td> fadeSpeed</td>
              <td>boolean</td>
              <td>false</td>
              <td> 如果设置为大于零的数字，则用优美的淡入/淡出动画来显示图片，</td>
            </tr>
            <tr>
              <td> handles</td>
              <td>boolean</td>
              <td>false</td>
              <td> 如果设置为true，调整手柄则会显示在选择区域内，如果设置为”corners”，则只有角处理会显示调整手柄</td>
            </tr>
            <tr>
              <td> hide</td>
              <td>boolean</td>
              <td>&nbsp;</td>
              <td> 如果设置为true，选择范围是隐藏</td>
            </tr>
            <tr>
              <td> imageHeight</td>
              <td>number</td>
              <td>&nbsp;</td>
              <td> 图片的真实高度 (if scaled with the CSS width and height properties)</td>
            </tr>
            <tr>
              <td> imageWidth</td>
              <td>number</td>
              <td>&nbsp;</td>
              <td> 真实图片宽度 (if scaled with the CSS width and height properties)</td>
            </tr>
            <tr>
              <td> instance</td>
              <td>number</td>
              <td>&nbsp;</td>
              <td> 如果设置为true，imgAreaSelect() 调用返回一个imgAreaSelect绑定到的图像的实例，使您可以使用它的API方法</td>
            </tr>
            <tr>
              <td> keys</td>
              <td>boolean</td>
              <td>false</td>
              <td> 启用/禁用键盘支持，默认值为false</td>
            </tr>
            <tr>
              <td> maxHeight</td>
              <td>number</td>
              <td>&nbsp;</td>
              <td> 选取的最大高度（单位为像素）</td>
            </tr>
            <tr>
              <td> maxWidth</td>
              <td>number</td>
              <td>&nbsp;</td>
              <td> 选取的最大宽度（单位为像素）</td>
            </tr>
            <tr>
              <td> minHeight</td>
              <td>number</td>
              <td>&nbsp;</td>
              <td> 选取的最小高度（单位为像素）</td>
            </tr>
            <tr>
              <td> minWidth</td>
              <td>number</td>
              <td>&nbsp;</td>
              <td> 选取的最小宽度（单位为像素）</td>
            </tr>
            <tr>
              <td> movable</td>
              <td>boolean</td>
              <td>true</td>
              <td> 确定选取是否可以移动</td>
            </tr>
            <tr>
              <td> parent</td>
              <td>string</td>
              <td>“body”</td>
              <td> 一个jQuery对象或选择字符串，指定被追加到父元素，默认值为”body” </td>
            </tr>
            <tr>
              <td> persistent</td>
              <td>boolean</td>
              <td>false</td>
              <td> 如果设置为true，选择区以外的点击将不会启动一个新的选区（即用户将只能移动/调整现有的选择范围），默认值为false</td>
            </tr>
            <tr>
              <td> resizable</td>
              <td>boolean</td>
              <td> true</td>
              <td> 确定是否选择面积应可调整大小</td>
            </tr>
            <tr>
              <td> show</td>
              <td>boolean</td>
              <td>&nbsp;</td>
              <td> 如果设置为true，选区则会显示</td>
            </tr>
            <tr>
              <td> x1<br>
                y1 </td>
              <td>&nbsp;</td>
              <td>&nbsp;</td>
              <td> 最初选择区域的左上角坐标</td>
            </tr>
            <tr>
              <td> x2<br>
                y2 </td>
              <td>&nbsp;</td>
              <td>&nbsp;</td>
              <td> 最初选择区域的右上角坐标</td>
            </tr>
            <tr>
              <td> zIndex</td>
              <td>&nbsp;</td>
              <td>&nbsp;</td>
              <td> 插件元素的z-index值，正常情况下imgAreaSelect会自动分配，但有少数情况，有必要将其设置为制定值</td>
            </tr>
            <tr>
              <td> onInit</td>
              <td>function</td>
              <td>&nbsp;</td>
              <td> 插件初始化时的回调函数</td>
            </tr>
            <tr>
              <td> onSelectStart</td>
              <td>function</td>
              <td>&nbsp;</td>
              <td> 插件开始选择时的回调函数</td>
            </tr>
            <tr>
              <td> onSelectChange</td>
              <td>function</td>
              <td>&nbsp;</td>
              <td> 插件改变选区时的回调函数</td>
            </tr>
            <tr>
              <td> onSelectEnd</td>
              <td>function</td>
              <td>&nbsp;</td>
              <td>弹窗显示前的回调函数</td>
            </tr>
          </tbody>
        </table>


## Callback 函数

回调函数 （参见onInit、 onSelectStart、 onSelectChange 和 onSelectEnd 参数） 传递两个参数。第一个参数是插件所附加到的图像的引用，第二参数是一个对象，表示当前选定内容。对象有六个属性：

<table class="table table-bordered table-striped">
  <thead>
    <tr>
      <th width="179">属性</th>
      <th width="679">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td> x1<br>
        y1 </td>
      <td>所选区域的左上角的坐标</td>
    </tr>
    <tr>
      <td> x2<br>
        y2 </td>
      <td> 选定区域右下角的坐标</td>
    </tr>
    <tr>
      <td> width</td>
      <td>选择宽度</td>
    </tr>
    <tr>
      <td> height</td>
      <td>选择高度</td>
    </tr>
  </tbody>
</table>

下面是一个示例将选择结束后执行的回调函数

	$('img#photo').imgAreaSelect({
	    onSelectEnd: function (img, selection) {
	        alert('width: ' + selection.width + '; height: ' + selection.height);
	    }
	});

## 键盘支持

如果keys 参数设置为 true，选择区域可以使用键盘移动/调整。默认情况下，使用下面的键

<table class="table table-bordered table-striped">
  <thead>
    <tr>
      <th width="23%">属性</th>
      <th width="77%">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>方向键</td>
      <td>将选区移动 10 个像素</td>
    </tr>
    <tr>
      <td> Shift&nbsp;+ 方向键</td>
      <td>将选区移动 1个像素</td>
    </tr>
    <tr>
      <td> Ctrl&nbsp;+&nbsp;方向键</td>
      <td>将选择区域调整 10 个像素的大小</td>
    </tr>
    <tr>
      <td> Shift&nbsp;+&nbsp;Ctrl&nbsp;+ 方向键</td>
      <td>将选择区域调整 1 个像素的大小</td>
    </tr>
  </tbody>
</table>

您可以通过将键值对设置一个对象覆盖上面的默认键值的绑定。该对象可能有以下属性

<table class="table table-bordered table-striped">
  <thead>
    <tr>
      <th width="13%">属性</th>
      <th width="87%">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td> arrows</td>
      <td>定义方向键的行为</td>
    </tr>
    <tr>
      <td> shift &nbsp;</td>
      <td>定义 Shift 键的行为</td>
    </tr>
    <tr>
      <td> ctrl &nbsp;</td>
      <td>定义 Ctrl 键的行为</td>
    </tr>
    <tr>
      <td> alt</td>
      <td>定义 Alt 键的行为</td>
    </tr>
  </tbody>
</table>


每个属性可以设置为像素 (≥ 1） 的选择区域,当特定键被按下时应该移动/调整大小数，或者"resize"字符串，指示密钥应该切换到调整大小模式的字符串。示例：

	$('img#example').imgAreaSelect({
	    keys: { arrows: 15, ctrl: 5, shift: 'resize' }
	});

使用这些设置，按箭头键仅将选择区域通过移动 15 像素，按 Ctrl 键将移动修改区域大小为 5 个像素，按住 shift 键将切换到调整大小。

如果有多个imgAreaSelect实例的页面有初始化的键选项,在任何时刻只有一实例可以控制键盘。默认情况下，任何用户操作 (选择区调整大小或移动） 或 reinvocation 插件实例上的 imgAreaSelect() 方法使键盘控制一个。



## API 方法
为了简化扩展插件，并将它与其他 web 应用程序的组件集成提供了几个 API 方法。

为了使用这些方法，您需要插件的对象实例。若要获取之一，调用 imgAreaSelect() 方法， 将instance选项设置为 true；

	var ias = $('#photo').imgAreaSelect({ instance: true });

现在，您可以使用此对象调用公共方法。例如，要设置的预定义的选择区域

	ias.setSelection(50, 50, 150, 200, true);
	ias.setOptions({ show: true });
	ias.update();

请注意，您应该只有在该实例完全初始化后使用，即在 onInit 回调函数，或已触发后随时 onInit。

可使用以下方法:


<table class="table table-bordered table-striped">
  <thead>
    <tr>
      <th width="15%">方法名</th>
      <th width="85%">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td> getOptions </td>
      <td> getOptions()
        <p>获取当参数</p>
        <p><strong>返回:</strong><br>
      一个对象，包含当前使用中的参数</p></td>
    </tr>
    <tr>
      <td>   setOptions   &nbsp;</td>
      <td> setOptions(newOptions)
        <p>设置参数</p>
        <p><strong>参数:</strong><br>
      <strong>newOptions</strong>&nbsp;– 新的参数对象</p></td>
    </tr>
    <tr>
      <td>   getSelection   &nbsp;</td>
      <td> getSelection([noScale])
        <p>获取当前所选内容</p>
        <p><strong>参数:</strong><br>
        <strong>noScale</strong>&nbsp;(optional) – 如果设置为 true，缩放不会应用于返回的选择</p>
        <p><strong>返回:</strong><br>
      选择对象</p></td>
    </tr>
    <tr>
      <td> setSelection </td>
      <td> setSelection(x1, y1, x2, y2, [noScale])
        <p>设置当前所选内容</p>
        <p><strong>参数:</strong><br>
          <strong>x1</strong>&nbsp;– 选择区域的左上角顶部 X 坐标<br>
          <strong>y1</strong>&nbsp;– 选择区域的左上角的 Y 坐标<br>
          <strong>x2</strong>&nbsp;– 选择区域的右下角的 x 坐标<br>
          <strong>y2</strong>&nbsp;– 选择区域右下角的 Y 坐标<br>
        <strong>noScale</strong>&nbsp;(optional) – 如果设置为 true，缩放不会应用于新的选择</p>
          <div class="alert alert-info">
                      <strong>注意：</strong> 此方法仅插件实例中设置选定内容的内部表示形式， 它不会更新可视化界面。 如果您想要显示的新选择，可以在setSelection() 后调用 update() 。 还要确保 theshow 选项被设置为 true。.
                    </div>
      </td>
    </tr>
    <tr>
      <td> cancelSelection </td>
      <td> cancelSelection()
        <p>取消当前选定内容</p>
      <div class="alert alert-info"> <strong>注意：</strong> 此方法隐藏选择/外部区域。因此没有必要调用 update() （作为反对 tosetSelection())。</div></td>
    </tr>
    <tr>
      <td> update </td>
      <td> update([resetKeyPress])
        <p>更新插件元素</p>
        <p><strong>参数:</strong><br>
      <strong>resetKeyPress</strong>&nbsp;(optional) – 如果设置为 false，此实例 keypress 事件处理程序没有激活</p></td>
    </tr>
  </tbody>
</table>


## 预览

	function preview(img, selection) {
	    var scaleX = 100 / (selection.width || 1);
	    var scaleY = 100 / (selection.height || 1);
	  
	    $('#ferret + div > img').css({
	        width: Math.round(scaleX * 400) + 'px',
	        height: Math.round(scaleY * 300) + 'px',
	        marginLeft: '-' + Math.round(scaleX * selection.x1) + 'px',
	        marginTop: '-' + Math.round(scaleY * selection.y1) + 'px'
	    });
	}
	
	$(document).ready(function () {
	    $('<div><img src="ferret.jpg" style="position: relative;" /><div>')
	        .css({
	            float: 'left',
	            position: 'relative',
	            overflow: 'hidden',
	            width: '100px',
	            height: '100px'
	        })
	        .insertAfter($('#ferret'));
	
	    $('#ferret').imgAreaSelect({ aspectRatio: '1:1', onSelectChange: preview });
	});



## 参考

http://www.css88.com/EasyTools/javascript/jQueryPlugin/imgAreaSelect/index.html

