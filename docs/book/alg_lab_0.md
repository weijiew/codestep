
> 这部分内容是在一些 OI/ACM 群里面的 ppt 摘录得，作者的出处已经不详，侵删。

比赛成绩=OI实力*比赛经验

是乘号不是加号！

拥有强大的比赛能力，在任何比赛都能获得不低的分数。

相反没有好的比赛能力，你的成绩将很不稳定，在OI现行制度下，极可能滚粗。

毫不夸张的说，我认识就有十数名选手因为比赛策略或者细节问题导致没有进队或者没有得到本该得到的名次。

某选手实力强劲，但是NOIP犯小错误，省选又犯小错误，最后没进省队，但是之后在NOI获得邀请赛AU。

某选手实力强劲(？)，但是APIO考试策略混乱不堪，最后成功获得92分。

某选手实力强劲，但是打错输入输出文件名，痛失第一名。

某选手实力强劲，但是看错题目浪费大量时间，最后卡线没有进队。

这些选手在比赛之后，都表示AC这题目本来是探囊取物的事情。但是最终还是失败了。

这样的例子数不胜数。

比赛只有一次，只能望着天空45度默默流泪。

OI，尤其是中国传统OI比赛，随机性很大，随机性来源有很多，主要是因为OI这个比赛的性质。

随机性的来源：

1.会做不一定写的出来

2.写出来感觉没问题但是很可能就写错了很小的地方然后爆0了，事后追悔莫及。

3.(数据可能是错的，有问题的，弱爆的)

4.题目是原题别人做过(这个别的竞赛也一样).

5.坑爹的题目，考你物理或者高等数学。

6.比赛场次非常少，一般是2场，一场失利就完蛋。

1->极强的代码能力，啥都能写。2->能对拍就对拍，不能对拍就认真仔细的写，不要出错。3->听天由命，看你人品。4->虽然这种天上掉馅饼的事情也有，但是指望这种东西不去认真学习显然是不靠谱的。5->不能多说。

6->不是我们能管的事情。

对拍非常重要。

特点：题目简单，数据也弱。

面对简单题，我们需要的是稳定的AC。

不要求速度，先认真的看完题目，然后从容解决傻逼题。

然后一般来说会有一道不是那么傻逼的题目，先确保其它的2道简单题没有问题，NOIP的题目往往可以简单的对拍，不需要花多少时间。

然后把时间都花在略难题上，争取得到自己能得的最高分。

注意使用特判法，不能确保100分做法正确性的时候最稳妥的做法是特判暴力的范围然后暴力范围用暴力，其他用100分做法，在C++中使用namespace很容易实现这个。

特点：题目有一定难度，无法全部做出。

易犯错误：考场看都没看，放过了本来应该是非常简单的题目。

在这种比赛中，正确的做题顺序非常重要，但是做题顺序来源于对题目的了解，而对题目的了解又需要花费你的时间，这两个方面各自牵制，并非独立。

我个人的做法是首先要抽出半小时看完所有题目并且随便想一想，然后对每题都可以标出使用你第一眼想到的做法能得多少分。

然后再每题花10分钟略微细致的分析加想一下。基本上不难的题目都可以做出，就算做不出也会有“这题不是很难”的感觉，并且标上目前这题你能得到的分数。那么根据之前对题目的了解，就可以决定做题的顺序了。

同时一个很推荐的方法是先尽快的把暴力都敲一下，这样既能对拍又能保证最低的分数，当然你的手速得快一点，不过暴力都写很久正解估计更写不出来了>_>。

90%的错误都是傻逼错误。

正确的写代码方式。

功能直接使用各自的模块。

写代码的时候集中注意力

变量名要有意义。

复制粘贴一段代码的时候，急于求成，没有根据上下文改对。

->复制粘贴的时候尽量注意，或者不复制粘贴使用独立的函数。

发现一个地方要改一下，这个地方可能影响很多其它的地方，没有考虑全，导致错误。

->突然发现要改一个地方的时候，好好想想这里会影响哪里。


浪费时间刷几千道水题毫无意义。

做真正有用的题目。

在一道坑爹题上浪费大量的时间是十分没有性价比的。

真正有效的训练在一年内就能成为很强的选手，而一味的磨蹭和颓废4，5年也就那样。

成功的路并不拥挤，因为大部分人都在颓废


做题的目的是学到新的东西以及锻炼代码能力，而不是盲目刷OJ的rank，那没有任何意义。

提高算法能力（想出做法的能力，分析问题的方法等等）

提高代码能力（写出正确的代码的能力）

提高调试能力（将错误的代码改对的能力）

对于省选到NOI来说

大部分由于做过类似的，不用想就能解决。

之后的大部分顺着题目进行一些简单的分析，就也能转化成做过的问题。

套模型。

学习更多的解题模型，可能具体也可能抽象，要多加思考。

TC 1000分 经常会有令人耳目一新的算法思路。并且Editorial由专家编写，注重解题的过程而不是罗列解法，当然由于难度较大自己做可能比较累，而且基本上是做不出来的吧大概<_<，所以推荐的方法是看看题目不要想太多不会做就看题解。就算自己做出来了也可以看一下题解的分析。这对提高算法能力非常有好处。

代码能力很大程度上取决于经验，你可能觉得这种可能需要大量的练习，但是其实也是有捷径的，那就是参考别人的代码。

最佳的方法是找一些可能比较难写的题目（APIO 2010 寻路， APIO 2011 kunai，CTSC 2011 杀菌计划挺多的），自己很可能写不出来，这时可以参考别人的代码，搞明白那些细节都是怎么处理的，

优秀的代码风格能够极大的提高代码能力。

如果是在TC/CF上刷题，可以经常参考Petr或者watashi的代码学习一下，他们的代码风格都很好。

分析问题的方法是什么？

不是凭运气猜出做法，而是根据一定的思路从容的得出解法。

做题说白了就是建模和解决模型的过程。做不出来可能有两个原因，一个是模型建错了，一个是对模型了解不够。前者说明分析没有到位，后者说明知识不够扎实。

对各种模型有清楚的了解，这样才能轻松的做题，真正的高手不一定智商很高，但是建模能力一定很强。

1.从简单的情况开始分析：经典方法，对原题没有思路，那么分析问题的简化版。

经典例子：找出字典序最小的解，那么我们先分析怎么找出一个解。

2.人的思维很大程度上跟关键字有关系，比如一个题目怎么想都不会，有人跟你说“容斥”，你可能瞬间就会做了。不妨列出对于这类问题已知的一些解决方法关键字，思考思考能否做。