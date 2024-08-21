```cpp
#include <iostream>
#include <iomanip>
using namespace std;
const double pi = 3.14159;
class areacalculator
{
public:
	virtual double calculate() = 0;
	double m_Num1;
	double m_Num2;
};
class rectangle :public areacalculator
{
public:
	virtual double calculate()
	{
		return m_Num1 * m_Num2;
	}
};
class square :public areacalculator
{
public:
	virtual double calculate()
	{

	}
};
class triangle :public areacalculator
{
public:
	virtual double calculate()
	{

	}
};
class circle :public areacalculator
{
public:
	virtual double calculate()
	{

	}
};
void dowork()
{
	areacalculator* abc;
	int choice;
	double Num1, Num2;
	cout << "请选择需要计算的图形形状：\n";
	cout << "1、长方形\n";
	cout << "2、正方形\n";
	cout << "3、圆形\n";
	cout << "4、三角形\n";
	cin >> choice;
	switch (choice)
	{
	case 1:
		cout << "请输入长\n";
		cin >> Num1;
		cout << "请输入宽\n";
		cin >> Num2;
		abc = new rectangle;
		abc->m_Num1 = Num1;
		abc->m_Num2 = Num2;
		cout << "长为" << Num1 << "厘米，宽为" << Num2 << "厘米的长方形的面积为";
		cout << fixed << setprecision(3) << abc->calculate() << "平方厘米" << endl;
		delete abc;
		break;
	case 2:
	
		break;
	case 3:
		
		break;
	case 4:
		
		break;
	default:
		cout << "输入错误，请重新输入";
		break;
	}
	system("pause");
	system("cls");
}
int main()
{
	while (1) 
	{
		cout << "欢迎使用面积计算器\n";
		dowork();
	}
	system("pause");
	return 0;
}
```