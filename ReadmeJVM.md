public class JvmComprehension { 

    public static void main(String[] args) { 
        int i = 1;                      // 1 Создаем примитивную переменную значение которой храниться на Stack.
        Object o = new Object();        // 2 Создаеться новый объект в куче и что бы к нему обратиться в Steck создаем ссылку "о".
        Integer ii = 2;                 // 3 Создаем ссылочную переменную.
        printAll(o, i, ii);             // 4 Обращаемся к методу. Создаеться новый фрейм в Stack. (Новый метод новый фрейм).
        System.out.println("finished"); // 7
    }

    private static void printAll(Object o, int i, Integer ii) {
        Integer uselessVar = 700;                   // 5 Создаем ссылочную переменную значение которой во фрейм printALL (видна только в пределах метода).
        System.out.println(o.toString() + i + ii);  // 6 Создаеться фрэйм для этого метода. Вызываеться метод toString который преобразовывает переменную "о" в строкое значение. Происходит конкатенация с переменными "i" и "ii" которые java преобразует в строковые значения самостоятельно.
    }
}