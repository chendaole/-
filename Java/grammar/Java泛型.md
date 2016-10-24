#Java泛型

#### extends
*用于限制 T 数据类型的范围

>\<T extends Number\> 表示 T 只接受 Number 及其子类，传入其他类型的数据会报错。这里的限定使用关键字 extends，后面可以是类也可以是接口。如果是类，只能有一个；但是接口可以有多个，并以“&”分隔，例如 \<T extends Interface1 & Interface2\>。

>这里的 extends 关键字已不再是继承的含义了，应该理解为 T 是继承自 Number 类的类型，或者 T 是实现了 XX 接口的类型。

    public <T extends Number> T getMax(T array[]){
        T max = null;
        for(T element : array){
            max = element.doubleValue() > max.doubleValue() ? element : max;
        }
        return max;
    }


###[References](http://www.weixueyuan.net/view/6323.html)
