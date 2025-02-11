#include <iostream>
#include <cstdlib>  // Для std::rand та std::srand
#include <ctime>    // Для std::time (для ініціалізації генератора випадкових чисел)

int rand(int low, int high) {
    // Генерація випадкового числа в межах [low, high]
    return low + std::rand() % (high - low + 1);
}

int main() {
    // Ініціалізація генератора випадкових чисел
    std::srand(static_cast<unsigned int>(std::time(0)));

    int low = 5, high = 20;

    // Виведення кількох випадкових чисел у діапазоні [low, high]
    for (int i = 0; i < 10; i++) {
        std::cout << rand(low, high) << std::endl;
    }

    return 0;
}
