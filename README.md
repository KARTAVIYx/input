#include <fstream> 
#include <iostream> 
#include <fstream> 
#include <string>   
#include <vector> 
#include <cstdlib>
#include <cmath>
using namespace std;


struct Lesson {
    string name;
    int grade;
};

struct Student {
    int age;
    string name;
    Lesson lessons[2]; //у каждого ученика есть 2 урока
};

int main() {
    setlocale(0, "ru");
    // создаем студента
    Student student_1;
    student_1.age = 20;
    student_1.name = "Mark";
    student_1.lessons[0] = { "Math", 90 };
    student_1.lessons[1] = { "Physics", 85 };

    cout << "Student_1: " << student_1.age << " " << student_1.name << "\n";
    for (int i = 0; i < 2; ++i) {
        std::cout << "урок: " << student_1.lessons[i].name << ", оценка: " << student_1.lessons[i].grade << "\n";
    }

    // Создание структуры для точки
    struct Point {
        int x;
        int y;
    };

    // Создайте два точечных объекта a и b
    Point a = { 1, 2 };
    Point b = { 4, 6 };

    // Вычислить расстояние между точками
    double distance = sqrt(pow(b.x - a.x, 2) + pow(b.y - a.y, 2));
    cout << "Distance between points a and b: " << distance << "\n";

    // Дополнительные примеры структур
    struct Anthill {
        // Свойства муравейника
    };

    struct Car {
        // Свойства автомобиля
    };

    struct Marker {
        // Свойства маркера
    };

    struct ResidentialComplex {
        // Недвижимость жилого комплекса
    };

    //Создание структуры для ученика с оценками
    struct StudentInfo {
        std::string firstName;
        std::string lastName;
        int studentID;
        int mathGrade;
        int physicsGrade;
        int englishGrade;
        double averageGrade;
    };

    // Инициализировать одного учащегося
    StudentInfo student1 = { "John", "Doe", 12345, 85, 88, 92, 0 }; // Предполагая, что оценки превышают 100

    //Меню для взаимодействия с пользователем
    int choice;

    do {
        cout << "\nMenu:\n";
        cout << "1. Добавьте информацию о новом студенте\n";
        cout << "2. Показать информацию обо всех студентах\n";
        cout << "3. Выход\n";
        cout << "Введите свой выбор: ";
        cin >> choice;

        if (choice == 1) {
            // Добавьте информацию о новом студенте
            string firstName, lastName;
            int studentID, mathGrade, physicsGrade, englishGrade;

            cout << "Введите имя: ";
            cin >> firstName;
            cout << "Введите фамилию: ";
            cin >> lastName;
            cout << "Введите студенческий билет: ";
            cin >> studentID;
            cout << "Введите оценку по математике: ";
            cin >> mathGrade;
            cout << "Поступить в класс физики: ";
            cin >> physicsGrade;
            cout << "Введите оценку по английскому языку: ";
            cin >> englishGrade;

            StudentInfo newStudent = { firstName, lastName, studentID, mathGrade, physicsGrade, englishGrade, 0 };
            // Рассчитать среднюю оценку
            newStudent.averageGrade = (mathGrade + physicsGrade + englishGrade) / 3.0;
        }
        else if (choice == 2) {
            // Показать информацию обо всех студентах
            // учащихся может быть несколько, они могут быть сохранены в векторе или массиве
        }

    } while (choice != 3);

    return 0;
}
