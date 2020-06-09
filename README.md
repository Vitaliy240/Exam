1. 
#include <stdio.h> 

// определение структуры
struct student
{
    char name[30];
    int kurs;
    int age;
};
void main()
{
    // объявление массива на 10 структур
    struct student stud[10];
    int i, n;

    printf("Количество студентов:");
    // ввод n (число студентов)
    scanf("%d", &n);

    for(i=0;i<n;i++)
    {
        printf("Введите имя:");
        // ввод имени
        scanf("%s", stud[i].name);

        printf("Введите возраст:");
        // ввод возраста
        scanf("%d", &stud[i].age);

        printf("Введите номер курса:");
        // ввод номера курса
        scanf("%d", &stud[i].kurs);
    }

    // Вывод
    for(i=0;i<n;i++)
    {
        printf("Студент %s\n", stud[i].name);
        printf("Курс %d\n", stud[i].kurs);
        printf("Возраст %d\n", stud[i].age);
    }
}

2.  
#include <iostream>
#include <queue>  // подключили библиотеку queue
 
using namespace std;
 
int main() {
  setlocale(LC_ALL,"rus");
  queue <int> q;  // создали очередь q
  
  cout << "Пользователь, пожалуйста введите 7 чисел: " << endl;
 
  for (int h = 0; h < 7; h++) { 
    int a; 
    
    cin >> a;
      
    q.push(a);  // добавляем в очередь элементы
  }
  
  cout << endl;
  cout << "Самый первый элемент в очереди: " << q.front() << endl;  // выводим первый
                                                                   // элемент очереди
  q.pop();  // удаляем элемент из очереди
    
  cout << "Новый первый элемент (после удаления): " << q.front() << endl;
    
  if (!q.empty()) cout << "Очередь не пуста!";  // проверяем пуста ли очередь (нет)
    
  system("pause");
  return 0;
}

3.
#include <iostream>
#include <windows.h>
using namespace std;
 
int main()
{
    system("color 0a");
    setlocale(LC_ALL, "Rus");
    char str[100] = { 0 };
    cout << "Введите латиницу и кириллицу ";
    cin.getline(str, 100);
    OemToCharA(str, str);
    char x[] = "АБВГДЕЁЖЗИЙКЛМНОПРСТУФХЦЧШЩЬЫЪЭЮЯ";
    char x1[] = "абвгдеёжзиёклмнопрстуфхцчшщьыъэюя"; // Создал для дальнейшего использования
    for (int i = 0; i < strlen(str); i++)
    {
        if (str[i] >= 'А' && str[i] <= 'Я')
        {
            for (int j = 0; j < strlen(str);j++)
            {
                if (str[i] == x[j])
                {
                    *****          //Нужно присвоить str[i] число j
                };
                
            }
        }
 
    }
cout << str << endl;    
    system("pause");
    return 0;
}




4. ----




5. #include <iostream>
 
void ShowArray(int * arr, int n);
void InputArray(int * arr, int n);
void ModifyArray(int * arr, int n);
 
int main()
{
    setlocale(LC_ALL, "Russian");
    int size = 0;
 
    std::cout << "Ввод кол-ва элементов: ";
    std::cin >> size;
 
    if (size <= 0)
        return 0;
 
    int * arr = new int[size];
    
    InputArray(arr, size);
 
    std::cout << "\nИсходный массив: ";
    ShowArray(arr, size);
    ModifyArray(arr, size);
 
    std::cout << "\nМассив после обработки: ";
    ShowArray(arr, size);
 
    std::cout << std::endl;
    
    delete[] arr;
    return 0;
}
void ModifyArray(int * arr, int n)
{
    int temp = 0;
    for (int i = 0; i < (n / 2); i++)
    {
        temp = arr[n - i - 1];
        arr[n - i - 1] = arr[i];
        arr[i] = temp;
    }
}
 
void ShowArray(int * arr, int n)
{
    for (int i = 0; i < n; i++)
        std::cout << arr[i] << " ";
}
 
void InputArray(int * arr, int n)
{
    std::cout << "Ввод массива:" << std::endl;
    for (int i = 0; i < n; i++)
    {
        std::cout << "Ввод элемента № " << i + 1 << " = ";
        std::cin >> arr[i];
    }
}


