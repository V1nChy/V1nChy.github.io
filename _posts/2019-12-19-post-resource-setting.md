---
layout: post
title:  "��Դ��������"
date:   2019-12-19
excerpt: "��Ŀ��ģ�͡�������Ƶ��Դ�������÷�����¼"
tag:
- mmorpg
- ����
comments: false
---
## ��Ҫ

��Ȼ�����ֻ��ڴ��ձ鶼�ǳ����ˣ�����Ϊ��Ŀ��Ҫ�����еͶ˻�����ios�ڴ�Ƚ�С�����Զ��ڴ��Ż�������Ҫ��С��΢�Ľ��С�����Ŀ�У���Բ�ͬ��ƽ̨������Դ�����ʱ�����˲��컯���ã����������¼�¼��

## ģ��

* `meshCompression`��ѹ����Խ��ģ���ļ�ԽС������ģ������Ϊ`Low`������������������Ч��ģ����Ϊ`Hight`��
* `Read/Write Enable`������Ҫ����ʱ�޸�ģ�͵�ͳһ**�ر�**�����ǵ���ģ����Ҫ���о�̬��������Ҫ������
* `Optimize Mesh`��**����**��������GPU���ܡ�
* `Normals`������Ҫ������Ϣ������Ϊ`None`����Сģ�ʹ�С��
* `Optimize Game Objects`��**����**������¶��Hierarchy���ӽڵ��Ƴ���
* `Anim. Compression`��ʹ��`Optimal`,���`Keyframe Reduction`��ʡԼ50%��С��
* `Import Lights`����Ŀ�в�����Ҫ��**�ر�**��
* `Index Format`��Mesh Index buffer �Ĵ�С����Ŀ��ʹ��`16bit`(���65535������)

## ����

* `Read/Write Enable`������Ҫ����ʱ��ȡͼƬ������Ϣ��**����**������������һ�����ڴ����ġ�
* `Generate Mip Maps`���������3Dģ����ͼ������ã��������Լ33%���ڴ濪����Mipmaps��ҪΪԶ����������ɽ�Ϊ������С��ͼ��������Ⱦ���µĻ�����ʧ����UI��ͼ������ȫ�ò���������Ŀ��ȫ���ر��ˡ�
* `Max Size`��ͳһ��Ϊ**2048**��
* `Format`��
   * `Android`��͸����ͼ`ETC2_RBGA8`����͸����ͼ`ETC2_RGB`����������ͼ`RGBA 16`��
   * `IOS`��ui��ͼ`ASTC_RGBA_6x6`��͸����ͼ`PVRTC_RGBA4`����͸����ͼ`PVRTC_RGB4`,��������ͼ**RGBA 16**
* `Compression Quality`������ͼ���������������Ʒ��Խ������ͼԽ��

## ��Ƶ

* `Force To Mono`�����á�
* `Load Type`��ʹ��`Compressed In Memory`,�߲��߽�ѹ��
* `Compression Format`��ʹ��`Vorbis`��ѹ���Ƚϸߡ�

## ����

[Unity�����Ż� �C ����ƪ](https://wuzhiwei.net/unity-settings-optimization/)  

[unity��ͼ��ʽ](https://blog.csdn.net/studyinroom/article/details/90479419)  

## ��Ŀ��ַ

github��ַ��[�����༭��](https://github.com/V1nChy/Game-Scene-Editor)