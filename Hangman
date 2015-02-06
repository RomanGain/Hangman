#include <iostream>
#include <string.h>
#include <cstdlib>

using namespace std;

void ScreenStars(int f)
{
	for (int i = 0; i<f; i++)
	{
		cout << "* ";
	}
}

void stars(int f, char *b)
{
	for (int i = 0; i<f; i++)
	{
		b[i] = '*';
	}
}

void change(char *x, char *b, char a, int f)
{
	int i = 0;
	while (i<f)
	{
		if (x[i] == a){
			b[i] = x[i];
		}
		cout << b[i] << " ";
		i++;
	}
}

int count(char *b, char a, int f)
{
	int i = 0, j = 0;
	while (i<f)
	{
		if (b[i] == a){
			j++;
		}
		i++;
	}
	return j;
}

void EndingGame(int z)
{
	if (z == 6)
		{
			cout << "\nYou loose! Game over" << endl;
			cout << "\t \t \t \t               _______         " << endl;
			cout << "\t \t \t \t                |   |          " << endl;
			cout << "\t \t \t \t                |  \\O/        " << endl;
			cout << "\t \t \t \t                |   |          " << endl;
			cout << "\t \t \t \t                |  / \\        " << endl;
			cout << "\t \t \t \t                |              " << endl;
			cout << "\t \t \t \t               ----            " << endl;
		}
	else
		{
			cout << "Congratulations! You win!" << endl;
			cout << "\t \t \t \t                   \\O/        " << endl;
			cout << "\t \t \t \t                    |          " << endl;
			cout << "\t \t \t \t                   / \\        " << endl;
		}
}

void HangAndEnterWord(char *x1, char *x2, char *x3, char *x4, char *x5)
{
	cout << "\nPlease enter the letter..." << endl;
	cout << "\t \t \t \t               _______         " << endl;
	cout << "\t \t \t \t                |   |          " << endl;
	cout << "\t \t \t \t                |   " << x1 << "     " << endl;
	cout << "\t \t \t \t                |  " << x3 << x2 << x4 << "            " << endl;
	cout << "\t \t \t \t                |  " << x5 << "      " << endl;
	cout << "\t \t \t \t                |              " << endl;
	cout << "\t \t \t \t               ----            " << endl;
}



int main(int argc, char** argv)
{
	int z = 0, y = 0, j;
	char *x1 = " ", *x2 = " ", *x3 = " ", *x4 = " ", *x5 = " ";
	char x[30], b[30], a;

	cout << " 1 Player " << "\nPlease enter the word..." << endl;
	cin >> x;
	system("cls");
	int f = strlen(x);
	ScreenStars(f);
	stars(f,b);

	cout << "\n 2 Player " << endl;

	do{
		HangAndEnterWord(x1, x2, x3, x4, x5);
		cin >> a;
		system("cls");
		change(x, b, a, f);

		if (count(b, a, f) > 0)
			{
				cout << "\nGood! Keep going!" << endl;
				y += count(b, a, f);
			}
		else
			{
				z++;
				cout << "\nSorry! This word doesn't have a  \"" << a << "\" letter" << endl;
				switch (z)
				{
					case 1:
						{
							x1 = "O";
							break;
						}
					case 2:
						{
							x2 = "|";
							break;
						}
					case 3:
						{
							x3 = "\\";
							break;
						}
					case 4:
						{
							x4 = "/";
							break;
						}
					case 5:
						{
							x5 = "/";
							break;
						}
				}
			}
	} while (z != 6 && f - y >0);

	system("cls");
	EndingGame(z);
	system("pause");
	return 0;
}
