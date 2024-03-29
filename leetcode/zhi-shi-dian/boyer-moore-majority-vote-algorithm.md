# Boyer–Moore majority vote algorithm

> **博耶-摩尔多数投票算法**（英语：Boyer–Moore majority vote algorithm）,中文常作多数投票算法、摩尔投票算法等，是一种用来**寻找一组元素中占多数元素的常数空间级**[**时间复杂度**](https://zh.wikipedia.org/wiki/%E6%97%B6%E9%97%B4%E5%A4%8D%E6%9D%82%E5%BA%A6)**算法**。

该算法在其局部变量中存储一个数组元素和一个计数器，计数器初始化为 0。然后对数组进行遍历操作，在遍历到元素 x 的时候：如果计数器为 0，则算法将 x 存储到数组元素变量，并将计数器设置为 1。 否则，它将 x 与存储的元素进行比较，然后递增计数器（如果它们相等）或递减计数器（不相等）。 在此过程结束时，如果数组中存在占多数的元素，则它将是存储的数组元素变量的值。

算法可以用[伪代码](https://zh.wikipedia.org/wiki/%E4%BC%AA%E4%BB%A3%E7%A0%81)如下表示：

> 初始化元素m并给计数器i赋初值_i_ = 0
>
> 对于输入队列中每一个元素x：
>
> &#x20;   若_i_ = 0, 那么 _m_ = _x_ and _i_ = 1
>
> &#x20;   否则若_m_ = _x_, 那么 _i_ = _i_ + 1
>
> &#x20;   否则 _i_ = _i_ − 1
>
> 返回 m

即便输入序列没有多数元素，这一算法也会返回一个序列元素。然而如果能够进行第二轮遍历，检验返回元素的出现次数，就能判断返回元素是否为多数元素。因此算法需要两次遍历，亚线性空间算法无法通过一次遍历就得出输入中是否存在多数元素。[\[3\]](https://zh.wikipedia.org/wiki/%E5%A4%9A%E6%95%B0%E6%8A%95%E7%A5%A8%E7%AE%97%E6%B3%95#cite\_note-3)



参考：[多数投票算法](https://zh.wikipedia.org/wiki/%E5%A4%9A%E6%95%B0%E6%8A%95%E7%A5%A8%E7%AE%97%E6%B3%95)
