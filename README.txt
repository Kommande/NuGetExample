1. Собрать проект
2. Создать папку для локального NuGet репозитория.
3. Открыть консоль перейти в папку с проектом(там где .csproj файл)
4. Выполнить nuget pack -IncludeReferencedProjects -properties Configuration=Debug
5. Выполнить nuget add NuGetExample.1.0.0.nupkg -source <путь из пункта 2>
6. Созадать консольный проект Test(Консольное приложение .Net Framework)
7. Пкм по проекту-> управление пакетами NuGet->параметры(Шестеренка в правой верхней части окна)->добавить новый источник пакетов через кнопку "+".
8. Изменить поле источник на папку из пунка 2->ок.
9. Перейти во вкладку Обзор-> установить пакет
10. Заменить код фалйа program.cs на этот
using System;
using NuGetExample;
namespace Test
{
    class Program
    {
        static void Main(string[] args)
        {
            var value = MyMath.Square(10);

            Console.WriteLine(value);
            Console.Read();
        }
    
    }
}
11. Запустить

