Вот пример кода на Kotlin для решения этой задачи:

fun main() {
    println("Введите номер билета (6 цифр):")
    val input = readLine()
    
    if (input != null && input.length == 6) {
        val firstHalf = input.substring(0, 3)
        val secondHalf = input.substring(3)
        
        val sumFirstHalf = firstHalf.map { it.toString().toInt() }.sum()
        val sumSecondHalf = secondHalf.map { it.toString().toInt() }.sum()
        
        if (sumFirstHalf == sumSecondHalf) {
            println("Билет счастливый!")
        } else {
            println("Билет не счастливый.")
        }
    } else {
        println("Некорректный ввод.")
    }
}


Скопируйте этот код в Intellij IDEA и запустите его. После этого вы сможете ввести номер билета и программа проверит, является ли он счастливым (сумма первых трех цифр равна сумме оставшихся трех цифр).
