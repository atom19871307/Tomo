#include<iostream>
using namespace std;
int main()
{
	setlocale(LC_ALL, "Rus");
	int size;
	cout << "Введите размер массива: ";
	cin >> size;
	shared_ptr<int[]>array(new int[size]);
	for (int i = 0; i < size; i++)
	{
		*(array.get() + i) = i * i;
	}
	int sum = 0;
	for (int i = 0; i < size; i++)
	{
		sum = sum + array[i];
	}
	for (int i = 0; i < size; i++)
	{
		cout << "array[" << i << "]" << array[i] << endl;
	}
	cout << "Сумма элементов массива: " << sum << endl;
	return 0;
}
