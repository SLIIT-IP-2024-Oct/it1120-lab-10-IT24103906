import java.util.Scanner;

class IT24103906 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the mark: ");
        int mark = scanner.nextInt();

        assert (mark >= 0 && mark <= 100) : "Invalid Mark";
        System.out.println("Mark is Validated");

        char grade;
        if (mark >= 75) {
            grade = 'A';
        } else if (mark >= 60) {
            grade = 'B';
        } else if (mark >= 50) {
            grade = 'C';
        } else if (mark >= 40) {
            grade = 'D';
        } else {
            grade = 'F';
        }
 
        assert (isGradeCorrect(mark, grade)) : "Incorrect Grade Assigned";
        System.out.println("Grade: " + grade);
    }

    private static boolean isGradeCorrect(int mark, char grade) {
        switch (grade) {
            case 'A':
                return mark >= 75;
            case 'B':
                return mark >= 60 && mark < 75;
            case 'C':
                return mark >= 50 && mark < 60;
            case 'D':
                return mark >= 40 && mark < 50;
            case 'F':
                return mark < 40;
            default:
                return false;
        }
    }
}
