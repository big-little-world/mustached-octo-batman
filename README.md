# mustached-octo-batman
/*
Реализовать алгоритм сортировки пузырьком:
входные данные:
N-количество элементов для сортировки;
а1, а2, а2,...,аN;
выходные данные:
b1, b2, b3,..., bN;(b1<b2<b3<...<b4N)

ai-unsigned char
Lab УЦ8-41
Прохоров М.В
*/
#include <iostream>
#include <cstdlib>
using namespace std;
int main()
{
	
	int n;
	int b,c, t;
	cout << "n=";
	cin >> n;
	int *a = new int [n];
	for (t = 0; t < n; t++)
		cin >> a[t];
	cout << "\n";
	for (t = 0; t < n; t++) cout << a[t] << ' ';
	
	for (b = 1; b < n; b++)
		for (c = n - 1; c >= b; c--){
			if (a[c - 1] > a[c]){
				t = a[c - 1];
				a[c - 1] = a[c];
				a[c] = t;
			}
		}

	cout << "\n"<<"Array after sortirovka:" << "\n";
	for (t = 0; t < n; t++)
		cout << a[t] << ' ';
		system("Pause");
	return 0;
}
