#include <iostream>
#include <cmath>

using namespace std;

int main() {
    int choice;
    cout << "Виберіть номер завдання (17, 51, 54, 55, 58): ";
    cin >> choice;

    if (choice == 17) {
        double x, y;
        cout << "Введіть x та y: ";
        cin >> x >> y;

        // ОДЗ: x >= 0, y - sqrt(|x|) > 0, знаменник x + x^2 / 4 != 0
        if (x < 0 || (y - sqrt(abs(x))) <= 0 || (x + (pow(x, 2) / 4)) == 0) {
            cout << "Немає розв'язку" << endl;
        } else {
            double z = abs(log(y - sqrt(abs(x))) * (x - (y / (x + (pow(x, 2) / 4)))));
            cout << "Z = " << z << endl;
        }

    } else if (choice == 51) {
        double x;
        cout << "Введіть x: ";
        cin >> x;

        // ОДЗ: аргумент логарифма 2x - 4 > 0, знаменник x^2 - 1 != 0
        if ((2 * x - 4) <= 0 || (pow(x, 2) - 1) == 0) {
            cout << "Немає розв'язку" << endl;
        } else {
            // log3(t) = ln(t) / ln(3)
            double z = (log(2 * x - 4) / log(3)) / (pow(x, 2) - 1);
            cout << "Z = " << z << endl;
        }

    } else if (choice == 54) {
        double x;
        cout << "Введіть x: ";
        cin >> x;

        // ОДЗ: аргумент логарифма x^2 - 9 > 0, значення логарифма не дорівнює 0, знаменник != 0
        double log_val = log(pow(x, 2) - 9) / log(5);
        if ((pow(x, 2) - 9) <= 0 || log_val == 0) {
            cout << "Немає розв'язку" << endl;
        } else {
            double z = 1.0 / log_val;
            cout << "Z = " << z << endl;
        }

    } else if (choice == 55) {
        double x;
        cout << "Введіть x: ";
        cin >> x;

        // ОДЗ: 2x - 5 >= 0, знаменник x^2 + 4x - 5 != 0
        if ((2 * x - 5) < 0 || (pow(x, 2) + 4 * x - 5) == 0) {
            cout << "Немає розв'язку" << endl;
        } else {
            double z = sqrt(2 * x - 5) / (pow(x, 2) + 4 * x - 5);
            cout << "Z = " << z << endl;
        }

    } else if (choice == 58) {
        double x;
        cout << "Введіть x: ";
        cin >> x;

        // ОДЗ: підкореневий вираз x^2 - 4x + 3 > 0
        if ((pow(x, 2) - 4 * x + 3) <= 0) {
            cout << "Немає розв'язку" << endl;
        } else {
            double z = (x - 1) / sqrt(pow(x, 2) - 4 * x + 3);
            cout << "Z = " << z << endl;
        }

    } else {
        cout << "Невірний номер завдання!" << endl;
    }

    return 0;
}
