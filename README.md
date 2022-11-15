# House-of-the-Dragon 龙之家族
Three basic guidelines were raised for a systematic redesignation of Arduino, ESP32, and rp2040 Rasp-Pico, etc. <i>Drogon, Rhaegal, and Viserion</i> were named for them, yes after Queen Danny's three dragons. These three suggestions also mention a quick connector and PCB designation layout for open hardware.

May every creative idea fly freely with wings of unified and convenient development board. And may every maker fly as a dragonraider. May the electronic  creative activities more green and sustainable for earth and human society.

![这是图片](https://github.com/ange1026/House-of-the-Dragon/blob/main/Background%20Medium.jpg "")

<br />
<br />
<br />


## HouYi Shooting Suns  后羿射日

In the past ten years, the development board of the maker circle has been releasing new models every year, and the corresponding supporting function expansion boards are also flooding. The resulting flood of e-waste is a problem that no responsible maker can ignore. How to start from ourselves and reduce the generation of e-waste, I have three solutions. First, it uses the Wang interface to unify the IO interface of the expansion board. This project introduces the second solution: taking the Houyi/Hybrid layout as an example to unify several common development boards.

创客圈近十年来开发板每年都在出新款，相应的配套功能扩展板也在泛滥。由此带来的电子垃圾泛滥，是任何一位有责任心的创客都不能忽视的问题。如何从自身做起，减少电子垃圾的产生，我有三个方案。其一，是用王氏接口统一扩展板的IO接口。本文介绍第二个方案：以Houyi/Hybrid布局为例，统一若干款常见开发板。

![后羿](https://gss0.baidu.com/-4o3dSag_xI4khGko9WTAnF6hhy/zhidao/pic/item/2e2eb9389b504fc2b1489155e8dde71190ef6d4e.jpg "后羿射日")

The birth of Arduino around 2010 promoted the innovation and creation of electronic technology in many disciplines such as art and biology, and a series of functional expansion boards followed Arduino's pin layout, although the layout itself was a serendipitous event, and some people thought it was unsatisfactory. This phenomenon shows that the layout of the development board is currently inheriting history, neither long (enough for full compliance) nor short enough (to abandon), and has not been carefully studied to effectively standardize. Especially when I designed the Bagua keyboard, I was particularly impressed by the non-standard of different main control boards and firmware. For example, the Raspberry Pico's USB interface and metal contacts for power input are themselves a distinctive design of the Raspberry Pi, which is convenient for flying wires to connect to external power sources or USB devices. But once it needs to be made into a keyboard, it needs to solder additional metal spring probes to maintain the connection, and the price of spring probes is still high. So I moved them to the position of the unified pin header, which is also handled on the Raspberry Pi 40pin, but not necessarily on other development boards. More importantly, when the Bagua keyboard (the keyboard with the Bagua is listed as the matrix), I found that if I need to try other main controls, the PCB layout needs to be adjusted more, and this phenomenon is more widespread in the design of development boards for various main controls: obviously similar functions, such as realizing the control of a small RC car, or a greenhouse with controllable temperature and humidity, but because of the replacement of better performance or specific purpose chips, it is necessary to redesign the main control board, together with the redesigned expansion board. And these fixed-interface function shields are mostly idle after the tech competition. What a waste! This is a crime! To know that although the main body of the chip currently comes from the most widely distributed silicon element on the earth, how many processes, electricity, and water resources are required for the whole process from gravel to chip, and the large number of heavy metals contained in silicon-based chips also need to be recycled, and then there are also PCB boards in the manufacturing and recycling process There are also pollution and waste problems. So, if advertise yourself as a maker, at a time when environmental problems are so prominent, can you stop turning a blind eye to these old problems? Could we do better within our innovation activities, such as reducing all kinds of e-waste from the side before other green approaches such as carbon-based chips are mature?

2010年前后Arduino的诞生，促进了电子技术在艺术、生物等多个学科领域的创新创造，一系列功能扩展板都沿袭了Arduino的针脚布局方式，尽管这个布局的产生本身是个偶然事件，并且有部分人认为其不尽如人意。这个现象说明开发板的布局目前是沿袭不短不长的历史，并未经过仔细研究以有效规范的。特别在我设计[八卦键盘](https://oshwhub.com/torah/xing-huo-ji-hua-ba-gua-jian-pan-by-sudo-wang-yq)时，对于不同主控板和固件的不规范感触特别深刻。例如，树莓派Pico的usb接口和电源输入的金属触点，本身是树莓派很有特色的设计，方便飞线连接外部电源或USB设备。但是一旦需要将它制作成键盘，就需要焊接额外的金属弹簧探头来维持连接，而目前弹簧探头的价格还是较高的。所以我将它们移到统一排针的位置上去，这在树莓派40pin上也是如此处理的，但是其他开发板则未必。更主要的是，当设计好八卦键盘（以八卦配列为矩阵的键盘）后，我发现如需尝试其他主控，则PCB布线需要调整的地方较多，这个现象在各种主控的开发板设计上更加泛滥：明明是相似的功能，比如实现了一个小车的控制，一个温湿度可控的温室，但却要因为更换了性能更好或特定用途的芯片，就需要重新设计主控板，连带着重新设计扩展板，而这些固定接口的功能扩展板大多数时候在比赛结束后就闲置了。这是浪费啊！这是犯罪！要知道芯片的主体目前虽然来自地球上最广泛分布的硅元素，但其从沙砾到芯片的全过程需要多少工序、电力和水资源啊，而且硅基芯片所包含的大量重金属，也需要多大的代价进行回收，然后还有PCB板在制造和回收过程中同样存在着污染和浪费问题。所以，请自我标榜为创客各位，在环境问题如此突出的当下，能不能不要再对这些老问题熟视无睹，而是在碳基芯片等其他绿色途径还未成熟前，就从身边做起，减少创新活动中产生的各种电子垃圾呢？

![扩展板太多](https://github.com/Torah/House-of-the-Dragon/blob/main/too-many-shields.jpg "too many shield become elec-trash")

Based on the above considerations, I designed the Wang interface at first, then took the Raspberry Pico as an example to propose the Houyi/Hybrid layout to unify several commonly-used development boards. The original Raspberry Pico layout diagram shown in Figure 1(a), the official Raspberry Pico main control board has 9 grounded GND pin pads. I don't quite know the role of redundant 9 pins, or I don't think that GND pins that need so much redundancy have any special use, especially when I need to use the main control chip of some common-used development boards, such as ESP32, 32u4, etc. also follow the similar pin layout of Raspberry Pico, I will find that ESP32 chips can use more IO pins than Pico, and even Pico fails to lead all available pins (such as 23, 25 pins) to the pin header, instead, it appears in the form of metal contacts on the back. So my suggestion is to introduce a set of design specifications (the Wang's Initiative to Standardize Board Design), as shown in Figure 1(b):
1. No more than 8 ground pins need to be shot down from the origianl position of the 9 ground pins and replaced with available IO pins;
2. Follow Pico's plate size, and retain the position of Vin, 3V3, Rst (Run);
3. The 2nd and 3rd pins from top to bottom on the right side are USB Data+ and USB Data- signal pins, respectively.

正是基于上述考虑，我首先设计了[王氏接口](https://oshwhub.com/torah/wu-zhen-jie-kou-yi-tong-jiang-hu-xing-huo-ji-hua)，接着以树莓派Pico为例，提出Houyi/Hybrid布局方式，来统一几款常见的开发板。如图1(a)的原版树莓派Pico布局图所示，官方的树莓派Pico主控板是有9个接地GND引脚焊盘的。我不太清楚冗余9个脚的作用，或者我本人不认为需要这么多冗余的GND脚有很大的作用，特别是我需要将一些常见开发板的主控芯片，如ESP32、32u4等也沿用树莓派Pico类似的引脚布局时，会发现ESP32芯片可以使用的IO引脚比Pico更多，并且即使是Pico，也未能将所有可用引脚（如23、25脚）都引到排针脚上，而是以背面金属触点的方式出现。所以我的建议是引入一套设计规范（《规范开发板设计的王氏倡议》），如图1（b）所示：

1.削减9个接地脚中不超过8个的位置，代替以可用的IO引脚；

2.沿袭Pico的板型尺寸，并保留Vin、3V3、Rst(Run)的位置；

3.右侧自上而下第2、3脚分别为USB Data+和USB Data-信号脚。

![后羿布局](https://github.com/Torah/House-of-the-Dragon/blob/main/HouYi-Layout.png "HouYi/Hybrid Layout")

The idea to remove eight and remain one in article 1st coincided with the ancient Chinese myth of HouYi shooting the Suns, and the design specifications were to be used to modify many development boards including ESP32 and 32u4. Therefore, I named it Houyi/Hybrid board layout. Of course, as long as other chips are suitable, they will also be added to the Houyi/Hybrid board design list, and the corresponding function expansion board is expected to be compatible with multiple main control boards at the same time, thereby greatly reducing the waste of resources in the innovation process, especially the expenditure of makers' wallets. Because the number of available IO pins of the chip is different, my current recommendation is to remove eight and remain one, but leave specifically which GND open to be choosen, based on usage habits and convenience. And when the available IO pins are not enough to fill the eight positions, it is recommended that the surplus pin pads hang in the air.

因为第1条去八留一的思想，和中国古代神话后羿(HouYi)射日的巧合，并且该倡议的设计规范是要用于改造包括ESP32、32u4等一众开发板的，所以我命名为Houyi/Hybrid板型布局。当然，其他芯片只要合适，也会陆续加入Houyi/Hybrid的板型设计中来，相应的功能扩展板，就有望同时兼容多款主控板，从而大量减少创新过程中的资源浪费，特别是创客们钱包的支出。因为芯片的可用IO脚数参差不齐，所以我目前的建议是去八留一，但留的一个GND具体留哪一个有待使用中进一步观察使用方便和习惯，并且当可用IO脚不足以填补去的八个位置时，建议富余的针脚焊盘悬空。


<br />
<br />
<br />


## The Dragon Has Three Heads 龙有三个头

Through the above transformation, I made a Bagua keyboard that can be compatible with multiple main control boards, and via introducing the Wang interface, I made the corresponding Pico expansion board. Because I first proposed the Houyi/Hybrid board layout and made the related control board, I own the naming rights to them. Daenerys Targaryen is a famous wheel breaker whose behavior is similar to that of the HouYi, or Qin Shi Huang. So I'd like to name the main control board of the ESP32, rp2040 and 32u4 chips currently redesigned with the Houyi/Hybrid layout after Queen Danny's three dragons, Drogon, Rhaegal and Viserion. And the main control board of other chips that appear later when using the Houyi/Hybrid layout can also be named by its first producer after dragons within “House of the Dragon” or “Dance of the Dragons”. Of course, considering that the footprint size of some chips is really too big to suit Houyi/Hybrid board layout, after the emergence of more suitable board design specifications for them in the future, as long as the Houyi/Hybrid plate type idea is used to unify the pin header, it can also be named after a very large dragon in the history of Westeros, such as Balerion, Vhagar, etc. Of course, if George R.R.Martin grandpa or other creators of "Ice and Fire" oppose on this, I can also name the boards after hybrid rice, hybrid fruits, etc. May every creative idea fly freely with wings of unified and convenient development board. And may every maker fly as a dragonraider.

通过以上改造，我制作了能够兼容多款主控板的[八卦键盘](https://www.bilibili.com/video/BV1se4y1n7bn/)，并且通过引入[王氏接口](https://www.bilibili.com/video/BV1Ea411V7x3/)，制作了相应的Pico扩展板。因为我首先提出Houyi/Hybrid板型布局并制作相关主控板，我拥有了它们的命名权。丹妮莉丝.坦格利安是著名的历史车轮打破者，其行为和Houyi/Hybrid板型布局的提出有相似之处，所以我将目前采用Houyi/Hybrid板型重新设计的ESP32、rp2040和32u4芯片的主控板以丹尼女王的三条龙的名字卓耿、雷戈和韦赛利昂命名。并且以后出现的其他芯片的采用Houyi/Hybrid板型的主控板，也可以由其首先制作者以《龙之家族》等龙的名字命名。当然，考虑到某些芯片的封装尺寸实在太大，不能采用Houyi/Hybrid板型，在将来有更适合它们的板型设计规范出现后，只要采用Houyi/Hybrid板型思想统一排针接口的，也可以以维斯特洛大陆历史上体型很大的龙，如贝勒里恩、瓦格哈尔等名字命名。当然如果马丁老爷子等《冰火》相关主创人员对此有意见，我也可以考虑用杂交水稻、杂交水果等的名字命名它们。愿每一个创意都能乘统一而方便的各型开发板自由飞翔。愿每一位创客都能御风而行。

![龙有三个头](https://bkimg.cdn.bcebos.com/pic/bf096b63f6246b60a3c60c13e5f81a4c500fa289 "坦格利安族徽")

But the transformation did not stop in this direction. In addition to my two suggestions for the Wang interface and the Houyi layout, I give the 3rd suggestion: the dragon has three heads.
It's not enough that the different main control boards of Drogon, Rhaegal, and Viserion can perfectly replace each other. In the original "Ice and Fire" prophecy that "the dragon has three heads", the dragon is a monster with three heads, exactly the same as the pattern on the Targaryen family crest. So different motherboards like Drogon, Rhaegal, and Viserion are expected to alternate with each other more easily.

但是改造并未在这个方向上停止。除了我提出的王氏接口、后羿板型这两条建议以外，我还有第三个建议：龙有三个头。
仅仅卓耿、雷戈和韦赛利昂不同的主控板可以完美替换彼此还不够。在《冰火》原著里“龙有三个头”的预言里，龙是长着三个脑袋的怪物，也就是坦格利安家族族徽上的图案。所以卓耿、雷戈和韦赛利昂这样不同的主控板还应该能更方便地彼此替换才更加完美。

![龙有三个头](https://github.com/Torah/House-of-the-Dragon/blob/main/the-Dragon-has-three-heads.jpg "龙有三个头")

PCB half-holes are commonly found in wireless communication modules such as Bluetooth, because half-holes have the advantage of wetting and tension for pad adsorption of solder. In recent years, it has also appeared more and more on some development boards, such as the Raspberry Pico development board. However, with the rise in chip prices in recent years, the price of modules has also risen, and the cost of modules soldered to the test base plate in the development stage is also precious. If it can be recycled, it is more environmentally friendly for the high-energy-consuming chip industry. However, the development board, including Raspberry Pico, is currently using the way of soldering pin row and function expansion base plate plugging, which will not only increase the trouble of welding pin row and female header, but also completely do not effectively use the convenience that stamp half hole may bring in, expecially when you want to recycle them and then install it on other functional boards. You need desoldering, which is time-consuming, laborious and resource-consuming. Therefore, I am inspired by the structure of fixtures such as chip burners, gives full play to the particularity of the half-hole structure of stamps, design a non-destructive connection structure, and elastically connect the half-hole PCB module represented by Raspberry Pico, so as to realize the connection and non-connection state can be reversed at any time, and the process of soldering and desoldering is not required during the state switching process, and resources and time are greatly saved.

PCB半孔常见于蓝牙等无线通讯模块，因为半孔对于焊盘吸附焊锡有浸润和张力方面的优势。近年来也越来越多地出现在一些开发板上，例如树莓Pico开发板。但是随着近年芯片涨价潮，模块的价格也水涨船高，在开发阶段焊接在测试底板上的模块成本上也是珍贵的，如果能回收对于高能耗的芯片行业来说，也是对环境更加友好的。但是包括树莓Pico在内的开发板，目前都是采用焊接排针的方式和功能扩展底板插接，这样不仅会增加焊接排针、排母的麻烦，完全没有有效利用邮票半孔可能带来的便捷，而且这样焊接了排针的树莓Pico开发板如果想回收再贴装在其他功能板上，就需要拆焊，费时、费事、费资源。因而本发明人从芯片烧录器等治具结构上获得启发，充分发挥邮票半孔结构的特殊性，设计了非破坏性的连接结构，对树莓Pico为代表的半孔PCB模块进行弹性连接，从而实现连接和非连接状态的随时可逆，状态切换过程中无需焊接和拆焊的过程，资源和时间都得到极大的节约。

所以我的建议是，在功能扩展板设计时，不仅采用王氏接口方便传感器、执行器的连接，采用Houyi/Hybrid板型，使得多种主控板可方便替换升级，同时还要充分利用邮票孔和半孔针的连接关系，使得主控板和功能扩展板之间的连接关系可逆、省时、节约资源。以上就是我关于开发板设计的三条规范的建议，也是我对于环境友好型可持续创新的贡献，我在[八卦键盘](https://www.bilibili.com/video/BV1x8411x7FG/)中的设计制作实践中，也是按照这样的指导思想去努力实现“道”所倡导的天人合一的状态的。
