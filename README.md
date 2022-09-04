# Двумерный Массив из Блоксхемы.

## для начала мы просим у пользователя ввести количество строк и столбцов используя код:
```
int m = InputNumbers(".........")
int n = InputNumbers(".........")
```

## Далее запрашиваем пользователя ввести диапозон чисел массива
```
int range = InputNumbers(".........")
```
## Далее создаем двумерный массив
```
int[,] array = new int[m,n];
```
### Пишем метод,который ,будет запрашивать пользовтеля ввести данные которые выше мы описали. 
```
int InputNumbers(string input)
{
    Console.Write(input);
    int output = Convert.ToInt32(Console.ReadLine());
    return output;
}
```
## создаем команду призыва войдовского метода
```
CreateArray(array);
WriteArray(array);
```
## пишем сам метод(войдовский метод)
```
void CreateArray(int[,] array)
{
    for (int i = 0; i < array.GetLength(0); i++)
    {
        for (int j = 0; j < array.GetLength(1); j++)
        {
            array[i, j] = new Random().Next(range);
        }
    }
}
```
## пишем войдовский метод,который будет выводить двумерный массив в консоль
```
void WriteArray(int[,] array)
{
    for (int i = 0; i < array.GetLength(0); i++)
    {
        for (int j = 0; j < array.GetLength(1); j++)
        {
            Console.Write(array[i, j] + " ");
        }
        Console.WriteLine();
    }
}
```