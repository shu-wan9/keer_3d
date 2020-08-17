目录结构:
.\assets
.\js
index.html


函数列表:
KEER_Main.Init(canvasName, captureMode, assetPath);
初始化引擎
canvasName: Canvas的ID名
captureMode: true: 截图模式 false: 标准模式
assetPath: 存放戒指模型.json和.bin文件的路径

KEER_Main.Reset()
复位引擎，请在ngOnDestroy()函数里调用

KEER_Main.Load(headName, bodyName)
加载戒指
headname: 戒头名, 如A50
bodyname: 戒身名，如A6-D2.4

KEER_Main.Pause()
暂停渲染

KEER_Main.Resume()
恢复渲染

KEER_Main.ToggleRotation()
自动旋转

KEER_Main.IsAutoRotate()
返回是否正在自动旋转

KEER_Main.SetCameraAndShot(posIndex, fileName)
设置摄像机位置并截图
posIndex: 0 - 正面  1 - 侧面  2 - 45度角
fileName: 要保存的文件名

KEER_Main.start_load_cb
开始加载时的回调函数

KEER_Main.loaded_cb(head_success, body_success)
加载结束时的回调函数
head_success: 戒头是否加载成功
body_success: 戒臂是否加载成功
如:
   KEER_Main.loaded_cb = loaded;
   function loaded(head_success, body_success){
     KEER_Main.ToggleRotation();
   }
