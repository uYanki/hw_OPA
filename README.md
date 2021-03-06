# operational amplifier

---

运算放大器：https://www.bilibili.com/video/BV14E411i76t

* 主要观察输入端节点的电压相导致输出端的电压变化。

有源滤波器：https://www.bilibili.com/video/BV1vJ411G7hg?p=2

* 主要看不同频率的信号通过滤波器后的电压变化情况。
* 次要观察因输入信号电压偏大且经过放大器后的理论电压值大于运放电源电压范围而导致信号失真的情况。

---

①运放分析核心：运算放大器的同相输入端和反相输入端的电压相等。（虚短虚断）

②运放的电源：用来给输出端供电的，即输出端的电压范围在运放电源的电压范围内。

- 单电源供电：如 0v\~+3v；双电源供电：如 -12v\~+12v。
- 轨到轨(rail\-to\-rail)：输出端电压可接近、甚至达到电源电压。
- 电压跟随器：电压不变，电流放大。这里的电流不是来自于输入端，而是来自于运放电源。

③电压增益G：0dB -> 信号未放大；-3dB -> 0.707倍

④模拟滤波器：当输入信号的频率 $f=\frac{1}{2πRC}$，放大倍数 $A=\frac{V_{out}}{V_{in}}=0.707$ -> -3dB点。

https://www.bilibili.com/video/BV1ri4y1y7yG?spm_id_from=333.880.my_history.page.click

* 输入的信号是由多个不同频率的分量组成的（具体看傅里叶变换FFT）。

  因为每分量的频率不同，所以每个分量的所对应的增益也不一定相同。（具体看幅频特性曲线）

  \- 如将含有20Hz和50kHz的分量的信号通过低通滤波器，20Hz 的 A = 1，50kHz 的 A = 0.05，则 20Hz 的分量对应的电压不变，50kHz 的分量的电压被抑制，则输出部分的电压就降低了，因为少了 50kHz 分量的电压。

* 模拟滤波器是硬件上设计的滤波器，数字滤波器是软件上设计的滤波器



