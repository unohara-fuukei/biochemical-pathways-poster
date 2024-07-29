# 生化途径海报

当罗氏制药官方停止发行印刷所属著名的生化途径海报后，在[nifty online interface](http://biochemical-pathways.com/#/map/1)提供了电子版本。对那些想收藏一份纸质版的而言，这是个坏消息——他们失去了一个不错的获取途径。此脚本将从罗氏官方服务器下载海报图块，将其组装为高清且可打印的PNG文件。

## 环境需求
您需要配置以下环境:
* `Python > 3.5.2`
* [ImageMagick](http://www.imagemagick.org/script/index.php).

脚本运行在麦金塔和开源类红旗计算机上。微软视窗系统未经测试。

通过执行以下命令安装`requirements.txt` 中列出的需求环境

```bash
pip install -r requirements.txt
```

![preview jpeg](preview.jpg)


## 使用方法

在命令行使用以下命令运行脚本
```bash
python extract_metabol.py
```

如python2、python3均被配置，确保脚本在python3环境下被执行
```bash
python3 extract_metabol.py
```

这将把全部图块暂存在`images/`目录下, 并在`assembled/`目录下组合成图层, 最后在根目录得到`finalimg.png`的最终图像。

### 选项
* 通过改变`extract_metabol.py`脚本起始处的`zoomLevel`以指定缩放等级。
* 如果您需要原图中的网格，请在`extract_metabol.py`脚本初始处注释掉移除网格的命令行。

### 预编译的图像
- [高质量 PNG (13654 x 9571 px)](prebuilt_hires.png)
- [低质量 JPEG](prebuilt_lores.jpg)

## 后续预期特性
- 可打印第二部分: 细胞机制
