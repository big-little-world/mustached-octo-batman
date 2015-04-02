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
	int a,b, t;
	cout << "n=";
	cin >> n;
	int *c = new int [n];
	for (t = 0; t < n; t++)
		cin >> c[t];
	cout << "\n";
	for (t = 0; t < n; t++) cout << c[t] << ' ';
	
	for (a = 1; a < n; a++)
		for (b = n - 1; b >= a; b--){
			if (c[b - 1] > c[b]){
				t = c[b - 1];
				c[b - 1] = c[b];
				c[b] = t;
			}
		}

	cout << "\n"<<"Massiv posle sortirovki:" << "\n";
	for (t = 0; t < n; t++)
		cout << c[t] << ' ';
		system("Pause");
	return 0;
}
	
