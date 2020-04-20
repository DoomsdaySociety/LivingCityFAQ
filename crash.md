[<- 返回](https://github.com/MrXiaoM/LivingCityFAQ/blob/master/JE.MD)  
# 崩溃日志解读  

如果你是学过Java的，我想你应该能一眼看得出来出现了什么问题并能找到解决方法  
可并不是人人都是程序员，所以才有这篇文章  
首先你需要知道崩溃日志的格式，本章节对新人不是很友好，请慎重阅读  
下面是一份完整的崩溃日志
```
---- Minecraft Crash Report ----

WARNING: coremods are present:
  CCLCorePlugin (CodeChickenLib-1.8-1.1.2.115-universal.jar)
  Main ([H一键快速兑换]AnonymTrade-2.4.0-mc1.8.9.jar)
  ShoulderPlugin ([越肩视角]ShoulderSurfing-1.8.8_1.8.9-1.1.jar)
  ForgePlugin ([皮肤显示]CustomSkinLoader_Forge-14.7.jar)
  Do not report to Forge! Remove FoamFixAPI (or replace with FoamFixAPI-Lawful) and try again. ([优化]foamfix-0.6.3-anarchy-1.8.x.jar)
Contact their authors BEFORE contacting forge

// Daisy, daisy...

Time: 20-4-13 下午4:28
Description: Rendering entity in world

java.lang.OutOfMemoryError: unable to create new native thread
	at java.lang.Thread.start0(Native Method)
	at java.lang.Thread.start(Unknown Source)
	at java.util.concurrent.ThreadPoolExecutor.addWorker(Unknown Source)
	at java.util.concurrent.ThreadPoolExecutor.execute(Unknown Source)
	at java.util.concurrent.AbstractExecutorService.submit(Unknown Source)
	at customskinloader.fake.FakeSkinManager.loadProfileTextures(FakeSkinManager.java:58)
	at net.minecraft.client.resources.SkinManager.func_152790_a(SourceFile)
	at net.minecraft.client.network.NetworkPlayerInfo.func_178841_j(SourceFile:105)
	at net.minecraft.client.network.NetworkPlayerInfo.func_178837_g(SourceFile:81)
	at net.minecraft.client.entity.AbstractClientPlayer.func_110306_p(AbstractClientPlayer.java:88)
	at net.minecraft.client.renderer.entity.RenderPlayer.func_110775_a(RenderPlayer.java:119)
	at net.minecraft.client.renderer.entity.RenderPlayer.func_110775_a(RenderPlayer.java:23)
	at net.minecraft.client.renderer.entity.Render.func_180548_c(Render.java:92)
	at net.minecraft.client.renderer.entity.RendererLivingEntity.func_77036_a(RendererLivingEntity.java:285)
	at net.minecraft.client.renderer.entity.RendererLivingEntity.func_76986_a(RendererLivingEntity.java:193)
	at net.minecraft.client.renderer.entity.RenderPlayer.func_76986_a(RenderPlayer.java:63)
	at net.minecraft.client.renderer.entity.RenderPlayer.func_76986_a(RenderPlayer.java:23)
	at net.minecraft.client.renderer.entity.RenderManager.func_147939_a(RenderManager.java:399)
	at net.minecraft.client.renderer.entity.RenderManager.func_147936_a(RenderManager.java:356)
	at net.minecraft.client.renderer.entity.RenderManager.func_147937_a(RenderManager.java:323)
	at net.minecraft.client.renderer.RenderGlobal.func_180446_a(RenderGlobal.java:837)
	at net.minecraft.client.renderer.EntityRenderer.func_175068_a(EntityRenderer.java:1751)
	at net.minecraft.client.renderer.EntityRenderer.func_78471_a(EntityRenderer.java:1580)
	at net.minecraft.client.renderer.EntityRenderer.func_181560_a(EntityRenderer.java:1370)
	at net.minecraft.client.Minecraft.func_71411_J(Minecraft.java:1051)
	at net.minecraft.client.Minecraft.func_99999_d(Minecraft.java:349)
	at net.minecraft.client.main.Main.main(SourceFile:124)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(Unknown Source)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(Unknown Source)
	at java.lang.reflect.Method.invoke(Unknown Source)
	at net.minecraft.launchwrapper.Launch.launch(Launch.java:135)
	at net.minecraft.launchwrapper.Launch.main(Launch.java:28)


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Stacktrace:
	at java.lang.Thread.start0(Native Method)
	at java.lang.Thread.start(Unknown Source)
	at java.util.concurrent.ThreadPoolExecutor.addWorker(Unknown Source)
	at java.util.concurrent.ThreadPoolExecutor.execute(Unknown Source)
	at java.util.concurrent.AbstractExecutorService.submit(Unknown Source)
	at customskinloader.fake.FakeSkinManager.loadProfileTextures(FakeSkinManager.java:58)
	at net.minecraft.client.resources.SkinManager.func_152790_a(SourceFile)
	at net.minecraft.client.network.NetworkPlayerInfo.func_178841_j(SourceFile:105)
	at net.minecraft.client.network.NetworkPlayerInfo.func_178837_g(SourceFile:81)
	at net.minecraft.client.entity.AbstractClientPlayer.func_110306_p(AbstractClientPlayer.java:88)
	at net.minecraft.client.renderer.entity.RenderPlayer.func_110775_a(RenderPlayer.java:119)
	at net.minecraft.client.renderer.entity.RenderPlayer.func_110775_a(RenderPlayer.java:23)
	at net.minecraft.client.renderer.entity.Render.func_180548_c(Render.java:92)
	at net.minecraft.client.renderer.entity.RendererLivingEntity.func_77036_a(RendererLivingEntity.java:285)
	at net.minecraft.client.renderer.entity.RendererLivingEntity.func_76986_a(RendererLivingEntity.java:193)
	at net.minecraft.client.renderer.entity.RenderPlayer.func_76986_a(RenderPlayer.java:63)
	at net.minecraft.client.renderer.entity.RenderPlayer.func_76986_a(RenderPlayer.java:23)

-- Entity being rendered --
Details:
	Entity Type: null (net.minecraft.client.entity.EntityOtherPlayerMP)
	Entity ID: 17685
	Entity Name: zi_yun
	Entity's Exact location: -423.25, 67.00, -942.66
	Entity's Block location: -424.00,67.00,-943.00 - World: (-424,67,-943), Chunk: (at 8,4,1 in -27,-59; contains blocks -432,0,-944 to -417,255,-929), Region: (-1,-2; contains chunks -32,-64 to -1,-33, blocks -512,0,-1024 to -1,255,-513)
	Entity's Momentum: 0.00, 0.00, 0.00
	Entity's Rider: ~~ERROR~~ NullPointerException: null
	Entity's Vehicle: ~~ERROR~~ NullPointerException: null

-- Renderer details --
Details:
	Assigned renderer: net.minecraft.client.renderer.entity.RenderPlayer@c0f417
	Location: -0.01,0.00,-0.01 - World: (-1,0,-1), Chunk: (at 15,0,15 in -1,-1; contains blocks -16,0,-16 to -1,255,-1), Region: (-1,-1; contains chunks -32,-32 to -1,-1, blocks -512,0,-512 to -1,255,-1)
	Rotation: 132.1875
	Delta: 0.8166046
Stacktrace:
	at net.minecraft.client.renderer.entity.RenderManager.func_147939_a(RenderManager.java:399)
	at net.minecraft.client.renderer.entity.RenderManager.func_147936_a(RenderManager.java:356)
	at net.minecraft.client.renderer.entity.RenderManager.func_147937_a(RenderManager.java:323)
	at net.minecraft.client.renderer.RenderGlobal.func_180446_a(RenderGlobal.java:837)
	at net.minecraft.client.renderer.EntityRenderer.func_175068_a(EntityRenderer.java:1751)
	at net.minecraft.client.renderer.EntityRenderer.func_78471_a(EntityRenderer.java:1580)

-- Affected level --
Details:
	Level name: MpServer
	All players: 10 total; [EntityPlayerSP['Chieh'/17392, l='MpServer', x=-423.24, y=67.00, z=-942.65], EntityOtherPlayerMP['zi_yun'/17685, l='MpServer', x=-423.25, y=67.00, z=-942.66], EntityOtherPlayerMP['R_Xing'/17692, l='MpServer', x=-423.25, y=67.00, z=-942.66], EntityOtherPlayerMP['§e[§b§l原版空岛§e]'/107, l='MpServer', x=-403.50, y=64.00, z=-935.44], EntityOtherPlayerMP['Herobrine'/102, l='MpServer', x=-432.34, y=65.00, z=-920.66], EntityOtherPlayerMP['§e[§6§l点券充值§e]'/104, l='MpServer', x=-418.56, y=67.00, z=-948.31], EntityOtherPlayerMP['§e[§d§l经典生存§e]'/80, l='MpServer', x=-406.56, y=64.00, z=-949.59], EntityOtherPlayerMP['§e[§a§l原版空岛§e]'/96, l='MpServer', x=-400.41, y=-62220813.75, z=-952.53], EntityOtherPlayerMP['§e[§3§l空岛战争§e]'/110, l='MpServer', x=-400.38, y=64.00, z=-952.50], EntityOtherPlayerMP['§e[§b§l钻石大陆§e]'/76, l='MpServer', x=-397.41, y=64.00, z=-935.47]]
	Chunk stats: MultiplayerChunkCache: 289, 289
	Level seed: 0
	Level generator: ID 01 - flat, ver 0. Features enabled: false
	Level generator options: 
	Level spawn location: -426.00,67.00,-945.00 - World: (-426,67,-945), Chunk: (at 6,4,15 in -27,-60; contains blocks -432,0,-960 to -417,255,-945), Region: (-1,-2; contains chunks -32,-64 to -1,-33, blocks -512,0,-1024 to -1,255,-513)
	Level time: 1830957815 game time, 712686004 day time
	Level dimension: 0
	Level storage version: 0x00000 - Unknown?
	Level weather: Rain time: 0 (now: true), thunder time: 0 (now: false)
	Level game mode: Game mode: survival (ID 0). Hardcore: false. Cheats: false
	Forced entities: 19 total; [EntityOtherPlayerMP['§e[§a§l原版空岛§e]'/96, l='MpServer', x=-400.41, y=-62220813.75, z=-952.53], EntityPlayerSP['Chieh'/17392, l='MpServer', x=-423.24, y=67.00, z=-942.65], EntityOtherPlayerMP['zi_yun'/17685, l='MpServer', x=-423.25, y=67.00, z=-942.66], EntityOtherPlayerMP['R_Xing'/17692, l='MpServer', x=-423.25, y=67.00, z=-942.66], EntityOtherPlayerMP['Herobrine'/102, l='MpServer', x=-432.34, y=65.00, z=-920.66], EntityOtherPlayerMP['§e[§b§l原版空岛§e]'/107, l='MpServer', x=-403.50, y=64.00, z=-935.44], EntityOtherPlayerMP['§e[§6§l点券充值§e]'/104, l='MpServer', x=-418.56, y=67.00, z=-948.31], EntityOtherPlayerMP['Herobrine'/102, l='MpServer', x=-432.34, y=65.00, z=-920.66], EntityOtherPlayerMP['§e[§6§l点券充值§e]'/104, l='MpServer', x=-418.56, y=67.00, z=-948.31], EntityOtherPlayerMP['§e[§b§l原版空岛§e]'/107, l='MpServer', x=-403.50, y=64.00, z=-935.44], EntityOtherPlayerMP['§e[§d§l经典生存§e]'/80, l='MpServer', x=-406.56, y=64.00, z=-949.59], EntityOtherPlayerMP['§e[§a§l原版空岛§e]'/96, l='MpServer', x=-400.41, y=-62220813.75, z=-952.53], EntityOtherPlayerMP['§e[§b§l钻石大陆§e]'/76, l='MpServer', x=-397.41, y=64.00, z=-935.47], EntityOtherPlayerMP['§e[§3§l空岛战争§e]'/110, l='MpServer', x=-400.38, y=64.00, z=-952.50], EntityOtherPlayerMP['§e[§3§l空岛战争§e]'/110, l='MpServer', x=-400.38, y=64.00, z=-952.50], EntityOtherPlayerMP['§e[§d§l经典生存§e]'/80, l='MpServer', x=-406.56, y=64.00, z=-949.59], EntityOtherPlayerMP['§e[§b§l钻石大陆§e]'/76, l='MpServer', x=-397.41, y=64.00, z=-935.47], EntityOtherPlayerMP['zi_yun'/17685, l='MpServer', x=-423.25, y=67.00, z=-942.66], EntityOtherPlayerMP['R_Xing'/17692, l='MpServer', x=-423.25, y=67.00, z=-942.66]]
	Retry entities: 0 total; []
	Server brand: exaCord (git:BungeeCord-Bootstrap:1.15-SNAPSHOT:aabf15c:256) <- PaperSpi
	Server type: Non-integrated multiplayer server
Stacktrace:
	at net.minecraft.client.multiplayer.WorldClient.func_72914_a(WorldClient.java:412)
	at net.minecraft.client.Minecraft.func_71396_d(Minecraft.java:2536)
	at net.minecraft.client.Minecraft.func_99999_d(Minecraft.java:370)
	at net.minecraft.client.main.Main.main(SourceFile:124)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(Unknown Source)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(Unknown Source)
	at java.lang.reflect.Method.invoke(Unknown Source)
	at net.minecraft.launchwrapper.Launch.launch(Launch.java:135)
	at net.minecraft.launchwrapper.Launch.main(Launch.java:28)

-- System Details --
Details:
	Minecraft Version: 1.8.9
	Operating System: Windows 10 (x86) version 10.0
	CPU: 4x Intel(R) Core(TM) i3-5005U CPU @ 2.00GHz
	Java Version: 1.8.0_121, Oracle Corporation
	Java VM Version: Java HotSpot(TM) Client VM (mixed mode), Oracle Corporation
	Memory: 288141240 bytes (274 MB) / 603979776 bytes (576 MB) up to 1073741824 bytes (1024 MB)
	JVM Flags: 12 total; -XX:+UnlockExperimentalVMOptions -XX:+UseG1GC -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=16M -XX:-UseAdaptiveSizePolicy -XX:-OmitStackTraceInFastThrow -Xmn128m -Xss1M -Xmx1024m -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump
	IntCache: cache: 0, tcache: 0, allocated: 13, tallocated: 95
	FML: MCP 9.19 Powered by Forge 11.15.1.2318 Optifine OptiFine_1.8.9_HD_U_I3 13 mods loaded, 13 mods active
	States: 'U' = Unloaded 'L' = Loaded 'C' = Constructed 'H' = Pre-initialized 'I' = Initialized 'J' = Post-initialized 'A' = Available 'D' = Disabled 'E' = Errored
	UCHIJA	mcp{9.19} [Minecraft Coder Pack] (minecraft.jar) 
	UCHIJA	FML{8.0.99.99} [Forge Mod Loader] (forge-1.8.9-11.15.1.2318-1.8.9.jar) 
	UCHIJA	Forge{11.15.1.2318} [Minecraft Forge] (forge-1.8.9-11.15.1.2318-1.8.9.jar) 
	UCHIJA	amft{2.4.0} [匿名者快速兑换模组] (minecraft.jar) 
	UCHIJA	foamfixcore{7.7.4} [FoamFixCore] (minecraft.jar) 
	UCHIJA	CustomMainMenu{2.0} [Custom Main Menu] ([主菜单]CustomMainMenu-2.0.jar) 
	UCHIJA	foamfix{@VERSION@} [FoamFix] ([优化]foamfix-0.6.3-anarchy-1.8.x.jar) 
	UCHIJA	journeymap{1.8.9-5.2.4} [JourneyMap] ([旅行地图]journeymap-1.8.9-5.2.4-unlimited.jar) 
	UCHIJA	customskinloader{14.7} [CustomSkinLoader] ([皮肤显示]CustomSkinLoader_Forge-14.7.jar) 
	UCHIJA	shouldersurfing{1.1} [Shoulder Surfing] ([越肩视角]ShoulderSurfing-1.8.8_1.8.9-1.1.jar) 
	UCHIJA	craftguide{1.7.1.0} [CraftGuide] (CraftGuide-1.7.1.0-forge[1.8.9].jar) 
	UCHIJA	oneclickcrafting{1.2.2} [One click crafting] (mcmap.cc-[一键合成MOD][1.8.9].jar) 
	UCHIJA	Neat{GRADLE:VERSION-GRADLE:BUILD} [Neat] (Neat 1.1-3.jar) 
	Loaded coremods (and transformers): 
CCLCorePlugin (CodeChickenLib-1.8-1.1.2.115-universal.jar)
  codechicken.lib.asm.ClassHeirachyManager
  codechicken.lib.asm.RenderHookTransformer
Main ([H一键快速兑换]AnonymTrade-2.4.0-mc1.8.9.jar)
  anonym.minecraft.mod.trade.ModTransformer
ShoulderPlugin ([越肩视角]ShoulderSurfing-1.8.8_1.8.9-1.1.jar)
  com.teamderpy.shouldersurfing.asm.ShoulderTransformations
ForgePlugin ([皮肤显示]CustomSkinLoader_Forge-14.7.jar)
  customskinloader.forge.TransformerManager
Do not report to Forge! Remove FoamFixAPI (or replace with FoamFixAPI-Lawful) and try again. ([优化]foamfix-0.6.3-anarchy-1.8.x.jar)
  pl.asie.foamfix.coremod.FoamFixTransformer
	GL info: ' Vendor: 'NVIDIA Corporation' Version: '4.6.0 NVIDIA 391.25' Renderer: 'GeForce 920M/PCIe/SSE2'
	Launched Version: HMCL 3.2.112
	LWJGL: 2.9.4
	OpenGL: GeForce 920M/PCIe/SSE2 GL version 4.6.0 NVIDIA 391.25, NVIDIA Corporation
	GL Caps: Using GL 1.3 multitexturing.
Using GL 1.3 texture combiners.
Using framebuffer objects because OpenGL 3.0 is supported and separate blending is supported.
Shaders are available because OpenGL 2.1 is supported.
VBOs are available because OpenGL 1.5 is supported.

	Using VBOs: No
	Is Modded: Definitely; Client brand changed to 'fml,forge'
	Type: Client (map_client.txt)
	Resource Packs: faithful64pack1.8.zip
	Current Language: 简体中文 (中国)
	Profiler Position: N/A (disabled)
	CPU: 4x Intel(R) Core(TM) i3-5005U CPU @ 2.00GHz
	OptiFine Version: OptiFine_1.8.9_HD_U_I3
	Render Distance Chunks: 15
	Mipmaps: 4
	Anisotropic Filtering: 1
	Antialiasing: 0
	Multitexture: false
	Shaders: null
	OpenGlVersion: 4.6.0 NVIDIA 391.25
	OpenGlRenderer: GeForce 920M/PCIe/SSE2
	OpenGlVendor: NVIDIA Corporation
	CpuCount: 4
```
如果你打开的崩溃日志格式不是这样的，请用 Notepad2 等文本编辑器打开，别nm用记事本  
我们从头开始解析崩溃日志的结构  
***
## 开头
在崩溃日志的开头，一般都会有这句话  
```
---- Minecraft Crash Report ----
```
这句话是用来证明这是mc的崩溃日志，不用管  
***
## FML的警告
紧接着，如果你有安装有 FML 的 mod，理应会有下面这段
```
WARNING: coremods are present:
  Mod的ID (Mod所在文件名.jar)
  ...
  ...
  Do not report to Forge! Remove 建议移除的Mod的ID (or replace with 建议替换成的Mod的ID) and try again. (建议移除的Mod的文件名.jar)
Contact their authors BEFORE contacting forge
```
文中的...是我省略了其他的mod，例子可以看上面完整的崩溃日志  
如果有出现最后一句 Do not report 之类的  
你可以试试删除它提到的mod，或者删除你所有的 FML Mod
***
## 貌似无意义的注释、时间和描述
```
// 注释

Time: 年-月-日 时:分
Description: 发生错误的描述
```
注释不用管，可能是随机生成的  
时间很明显，是崩溃时间  
发生错误的描述，好像是错误发生时mc在做什么  
***
## 正文:堆栈信息  
设计到程序的知识… 我会尽量地将语言通俗化的  
格式差不多是这样的  
```
发生异常的类名: 异常描述
  at 出错的方法位置
  at 出错的方法位置
  ...
```
这是mc告诉你，出了什么错，在哪个地方出了错  
**请记下“发生异常的类名”和“异常描述”，以后会用到**  
有时候还会伴随着一个或以上的:  
```
Caused by: 发生异常的类名: 异常描述
  at 出错的方法位置
  at 出错的方法位置
```
**这里的“发生异常的类名”和“异常描述”可能也同样重要**  

现在，举个例子，就拿上面的崩溃日志来说  
```
java.lang.OutOfMemoryError: unable to create new native thread
	at java.lang.Thread.start0(Native Method)
	at java.lang.Thread.start(Unknown Source)
	at java.util.concurrent.ThreadPoolExecutor.addWorker(Unknown Source)
	at java.util.concurrent.ThreadPoolExecutor.execute(Unknown Source)
	at java.util.concurrent.AbstractExecutorService.submit(Unknown Source)
	at customskinloader.fake.FakeSkinManager.loadProfileTextures(FakeSkinManager.java:58)
  ... 太多了，以下省略
```
此时，发生异常的类名就是 java.lang.OutOfMemoryError，异常描述就是unable to create new native thread  
异常描述是人能看得懂的语言，可以直接用百度翻译来翻译出来  
这里大致翻译出来的结果就是：无法创建新的本机进程  
最好还是先看发生异常的类名，你通常可以在百度查得到  
```
发生异常的类名 怎么办
```
就能查到相关结果，比如  
```
java.lang.OutOfMemoryError 怎么办
```
这里会列举出一些常见的问题和解决方法 (-即为空)
| 异常的类名 | 异常描述 | 出错位置包括的内容 | 解决方法 |
| ---- | ---- | ---- | ---- |
| java.lang.OutOfMemoryError | - | - | 运行内存过小，到启动器调大点 |
| org.lwjgl.LWJGLException | Pixel format not accelerated | - | 显卡驱动版本过低或未开启硬件加速，尝试升级显卡驱动或开启硬件加速。如果不行，只能换电脑或者将系统降级 |
| java.lang.NoSuchMethodError | - | - | 方法不存在，一般都是Mod的自身缺陷，或者mc自身的缺陷导致。看看出错的方法位置就知道是谁的锅了，看不懂可以找大佬帮忙看 |
| java.lang.NoClassDefFoundError | - | - | 同上，只不过是类不存在 |
| java.lang.NullPointerException | - | - | 同上，只不过是空指针错误 |
| java.lang.IndexOutOfBoundsException | - | - | 同上，只不过是索引超出界限 |
| java.io.FileNotFoundException | - | - | 文件不存在，可能是Mod的资源文件丢失 |  
  
解决个闪退还得当侦探，是不是觉得贼tm烦
***
## 杂项
在这一段下面的都是一堆乱七八糟的东西，看不懂别看  
```
A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------
```
在这一段下面全都是关于客户端和系统的信息
```
-- System Details --
Details:
```
比如 Minecraft Version (mc版本)  
Operating System (操作系统)  
等一大堆关于客户端和电脑配置的参数  
还有mod列表之类的，可能对你有用的信息
***
差不多就这了，有不懂的加我QQ 2431208142
<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>
你已经到达了世界的尽头  
![到底啦](https://s1.hdslb.com/bfs/seed/bplus-common/dynamic-assets/end.png)
