# Chapter02 开始学习C++

## 2.1

**题：** 编写一个C++程序，它显示您的姓名和地址。

**解：**

```Cpp
#include <iostream>

using namespace std;

int main()
{
    cout << "My name is WangShen." <<endl;
    cout << "My address is something that I can't tell you." <<endl;
    return 0;
}

```


## 2.2

**题：** 编写一个C++程序，它要求用户输入一个以 long 为单位的距离， 然后将它转换为码（yard，一long 等于 220 码）。
    
**解：**


```Cpp

#include <iostream>

using namespace std;

int main()
{
    int dis;
    cout << "Enter your distance: " << endl;
    cin >> dis ;
    int num = dis * 220;
    cout << "The " << dis <<" long is " << num <<" ma." << endl;
    return 0;
}

```

## 2.3

**题：** 编写一个C++程序，它使用 3 个用户定义的函数（包括main()），并生成下面的输出：

```bash

Three blind mice
Three blind mice
See how they run
See how they run

```
其中一个函数要调用两次，该函数生成前两行；另一个函数也被调用两次，并生成其余的输出。


**解：**


```Cpp

#include <iostream>

using namespace std;

void cout_func1();
void cout_func2();

int main()
{
    cout_func1();
    cout_func1();
    cout_func2();
    cout_func2();
    return 0;
}

void cout_func1()
{
    cout << "Three blind mice" << endl;
}

void cout_func2()
{
    cout << "See how they run" << endl;
}

```


## 2.4

**题：** 编写一个程序，让用户输入其年龄，然后显示该年龄包含多少个月，如下所示：

```bash
Enter your age: 29

```

**解：**

```Cpp
#include <iostream>

using namespace std;

int age_convert(int);

int main()
{
    int age;
    cout << "Enter your age: ";
    cin >> age;
    int month;
    month = age_convert(age);
    cout << "The age contains " << month <<" months." << endl;
}

int age_convert(int age)
{
    int month = age * 12;
    return month;
}

```


## 2.5

**题：** 编写一个程序，其中的main( )调用一个用户定义的函数（以摄氏温度值为参数，并返回相应的华氏温度值）。该程序按下面的格式要 求用户输入摄氏温度值，并显示结果：

```bash
Please enter a Celsius value: 20

20 degrees Celsius is 68 degrees Fahrenheit.

```

转换公式：华氏温度 = 1.8×摄氏温度 + 32.0


**解：**

```Cpp

#include <iostream>

using namespace std;

int degree_convert(int);

int main()
{
    int celsius_value,fahrenheit_value;
    cout << "Please enter a Celsius value: " << endl;
    cin >> celsius_value;
    fahrenheit_value = degree_convert(celsius_value);
    cout << celsius_value <<" degrees Celsius is " << fahrenheit_value << " degrees Fahrenheit.";
}

int degree_convert(int value)
{
    return value * 1.8 + 32.0;
}

```


## 2.6

**题：** 编写一个程序，其main( )调用一个用户定义的函数（以光年值为参数，并返回对应天文单位的值）。该程序按下面的格式要求用户输 入光年值，并显示结果：

```bash

Enter the number of light years: 4.2

4.2 light years = 265608 astromonical units.

```
天文单位是从地球到太阳的平均距离（约150000000公里或93000000英里），光年是光一年走的距离（约10万亿公里或6万亿英里）（除太阳外，最近的恒星大约离地球4.2光年）。请使用double类型，转换公式为：1光年=63240天文单位.


**解：**

```Cpp

#include <iostream>


double light_years2astromonical_unit(double light_years) {

    return light_years * 63240;
}


int main() {

    using namespace std;

    double light_years;
    cout << "nter the number of light years: ";
    cin >> light_years;

    cout << light_years 
         << " light years = " 
         << light_years2astromonical_unit(light_years)
         << " astromonical units." << endl;

    return 0;
}

```

## 2.7

**题：** 编写一个程序，要求用户输入小时数和分钟数。在 main() 函数中，将这两个值传递给一个void函数，后者以下面这样的格式显示这两个值：

```bash

Enter the number of hours: 9
Enter the number of minutes: 28

Time: 9:28

```

**解：**

```Cpp

#include <iostream>

using namespace std;

void time_maker(int,int);

int main()
{
    int time_hour,time_minute;
    cout << "Enter the number of hours: " << endl;
    cin >> time_hour;
    cout << "Enter the number of minutes: " << endl;
    cin >> time_minute;
    time_maker(time_hour,time_minute);
}

void time_maker(int hour,int minute)
{
    cout << "Time: ";
    cout << hour << ":" << minute;
}


```






