#include<stdio.h>
#include<conio.h>
int main()
{
    int N, i;
    printf("Enter the value of N (limit): ");
    scanf("%d", &N);
    printf("\n");
    for(i=1; i<=N; i++)
    {
        if(i==N)
            printf("%d", i);
        else
            printf("%d,", i);
    }
    getch();
    return 0;
}









#include <stdio.h>

int main() {
    int n;

    // Input the value of 'n'
    printf("Enter the value of n: ");
    scanf("%d", &n);

    // Check if 'n' is even or odd, and adjust if needed
    if (n % 2 != 0) {
        n--; // Make 'n' even if it's odd
    }

    // Print the even number series
    printf("Even number series from 2 to %d: ", n);
    for (int i = 2; i <= n; i += 2) {
        printf("%d", i);
        if (i < n) {
            printf(", ");
        }
    }
    printf("\n");

    return 0;
}












#include <stdio.h>

int main() {
    int n;

    // Input the value of 'n'
    printf("Enter the value of n: ");
    scanf("%d", &n);

    // Check if 'n' is even or odd, and adjust if needed
    if (n % 2 == 0) {
        n--; // Make 'n' odd if it's even
    }

    // Print the odd number series
    printf("Odd number series from 1 to %d: ", n);
    for (int i = 1; i <= n; i += 2) {
        printf("%d", i);
        if (i < n) {
            printf(", ");
        }
    }
    printf("\n");

    return 0;
}













#include <stdio.h>

int main() {
    int n;

    // Input the value of 'n'
    printf("Enter the value of n: ");
    scanf("%d", &n);

    int a = 0, b = 1, c;

    // Print the Fibonacci series
    printf("Fibonacci series up to %d: %d, %d", n, a, b);

    c = a + b;
    while (c <= n) {
        printf(", %d", c);
        a = b;
        b = c;
        c = a + b;
    }

    printf("\n");

    return 0;
}











#include <stdio.h>

int main() {
    int n, sum = 0;

    // Input the value of 'n'
    printf("Enter the value of n: ");
    scanf("%d", &n);

    // Calculate the sum of the series
    for (int i = 1; i <= n; i++) {
        sum += i;
    }

    // Print the sum
    printf("Sum of the series 1 + 2 + 3 + ... + %d = %d\n", n, sum);

    return 0;
}











#include <stdio.h>

int main() {
    int n, sum = 0;

    // Input the value of 'n'
    printf("Enter the value of n: ");
    scanf("%d", &n);

    // Calculate the sum of even numbers from 2 to n
    for (int i = 2; i <= n; i += 2) {
        sum += i;
    }

    // Print the sum
    printf("Sum of even numbers from 2 to %d = %d\n", n, sum);

    return 0;
}










#include <stdio.h>

int main() {
    int n, sum = 0;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        if (i % 2 != 0) {  // Check if 'i' is odd
            sum += i;
        }
    }

    printf("The sum of the odd number series is: %d\n", sum);

    return 0;
}













#include <stdio.h>

int main() {
    int n, sum = 0;

    printf("Enter the value of N: ");
    scanf("%d", &n);

    int sign = 1;  // This variable keeps track of whether to add or subtract
    for (int i = 1; i <= n; i++) {
        sum += sign * i;  // Add or subtract i based on the sign
        sign *= -1;       // Toggle the sign for the next term
    }

    printf("The sum of the series is: %d\n", sum);

    return 0;
}












#include <stdio.h>

int main() {
    int n, sum = 0;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        sum += (i * 10 + 2);
    }

    printf("The sum of the series is: %d\n", sum);

    return 0;
}











#include <stdio.h>

int main() {
    int n, sum = 0;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        sum += (2 * i * i);
    }

    printf("The sum of the series is: %d\n", sum);

    return 0;
}












#include <stdio.h>

int main() {
    int n, sum = 0;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        sum += (i * 11);
    }

    printf("The sum of the series is: %d\n", sum);

    return 0;
}












#include <stdio.h>

int main() {
    int n, sum = 0;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i += 2) {
        sum += i * i;
    }

    printf("The sum of the squares of odd numbers is: %d\n", sum);

    return 0;
}










#include <stdio.h>

int main() {
    int n, sum = 0;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        sum += i * i * i;
    }

    printf("The sum of the cubes of the first %d numbers is: %d\n", n, sum);

    return 0;
}










#include <stdio.h>

int main() {
    int n;
    unsigned long long factorial = 1;

    printf("Enter a positive integer: ");
    scanf("%d", &n);

    if (n < 0) {
        printf("Factorial is not defined for negative numbers.\n");
    } else {
        for (int i = 1; i <= n; i++) {
            factorial *= i;
        }
        printf("Factorial of %d is: %llu\n", n, factorial);
    }

    return 0;
}













#include <stdio.h>
#include <math.h>

int main() {
    int number, originalNumber, remainder, result = 0, n = 0;

    printf("Enter an integer: ");
    scanf("%d", &number);

    originalNumber = number;

    // Count the number of digits in the number
    while (originalNumber != 0) {
        originalNumber /= 10;
        n++;
    }

    originalNumber = number;

    // Calculate the result using the sum of the nth powers of its digits
    while (originalNumber != 0) {
        remainder = originalNumber % 10;
        result += pow(remainder, n);
        originalNumber /= 10;
    }

    if (result == number) {
        printf("%d is an Armstrong number.\n", number);
    } else {
        printf("%d is not an Armstrong number.\n", number);
    }

    return 0;
}












#include <stdio.h>

int main() {
    int n, num;
    double sum = 0.0;

    printf("Enter the number of values: ");
    scanf("%d", &n);

    printf("Enter %d numbers:\n", n);

    for (int i = 1; i <= n; i++) {
        printf("Enter number %d: ", i);
        scanf("%d", &num);
        sum += num;
    }

    double average = sum / n;

    printf("Sum of the %d numbers is: %.2f\n", n, sum);
    printf("Average of the %d numbers is: %.2f\n", n, average);

    return 0;
}











#include <stdio.h>

int main() {
    int number;

    printf("Enter an integer: ");
    scanf("%d", &number);

    printf("Digits of %d are: ", number);

    int temp = number;
    int digit;
    int isNegative = 0;

    if (temp < 0) {
        isNegative = 1;
        temp = -temp;  // Convert negative number to positive for processing
    }

    // Extract and print digits
    while (temp > 0) {
        digit = temp % 10;
        printf("%d ", digit);
        temp /= 10;
    }

    if (isNegative) {
        printf("(Note: The number was negative)");
    }

    printf("\n");

    return 0;
}













#include <stdio.h>

int main() {
    int number;

    printf("Enter an integer: ");
    scanf("%d", &number);

    int temp = number;
    int digit;
    int sum = 0;

    // Calculate the sum of digits
    while (temp != 0) {
        digit = temp % 10;
        sum += digit;
        temp /= 10;
    }

    printf("Sum of the digits of %d is: %d\n", number, sum);

    return 0;
}











#include <stdio.h>

int main() {
    int number;

    printf("Enter an integer: ");
    scanf("%d", &number);

    int temp = number;
    int reversedNumber = 0;
    int digit;

    // Reverse the digits
    while (temp != 0) {
        digit = temp % 10;
        reversedNumber = reversedNumber * 10 + digit;
        temp /= 10;
    }

    printf("Reversed number: %d\n", reversedNumber);

    return 0;
}















#include <stdio.h>

int main() {
    int num;

    printf("Enter an integer: ");
    scanf("%d", &num);

    if (num % 2 == 0) {
        printf("%d is even.\n", num);
    } else {
        printf("%d is odd.\n", num);
    }

    return 0;
}











#include <stdio.h>

int main() {
    int num;

    printf("Enter an integer: ");
    scanf("%d", &num);

    if (num % 2 == 0) {
        printf("%d is even.\n", num);
    } else {
        printf("%d is odd.\n", num);
    }

    return 0;
}













#include <stdio.h>

int main() {
    int a, b, temp;

    printf("Enter two integers:\n");
    scanf("%d %d", &a, &b);

    temp = a;
    a = b;
    b = temp;

    printf("After swapping:\n");
    printf("a = %d\n", a);
    printf("b = %d\n", b);

    return 0;
}












#include <stdio.h>

int main() {
    int a, b;

    printf("Enter two integers:\n");
    scanf("%d %d", &a, &b);

    a = a + b;
    b = a - b;
    a = a - b;

    printf("After swapping:\n");
    printf("a = %d\n", a);
    printf("b = %d\n", b);

    return 0;
}













#include <stdio.h>

int main() {
    int a, b, c;

    printf("Enter three integers:\n");
    scanf("%d %d %d", &a, &b, &c);

    int temp = a;
    a = b;
    b = c;
    c = temp;

    printf("After swapping:\n");
    printf("a = %d\n", a);
    printf("b = %d\n", b);
    printf("c = %d\n", c);

    return 0;
}














#include <stdio.h>

int main() {
    int a, b;

    printf("Enter two integers:\n");
    scanf("%d %d", &a, &b);

    if (a > b) {
        printf("%d is the biggest.\n", a);
    } else {
        printf("%d is the biggest.\n", b);
    }

    return 0;
}













#include <stdio.h>

int main() {
    int n, num, max;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    printf("Enter %d integers:\n", n);
    scanf("%d", &max);

    for (int i = 1; i < n; i++) {
        scanf("%d", &num);
        if (num > max) {
            max = num;
        }
    }

    printf("The biggest number is: %d\n", max);

    return 0;
}














#include <stdio.h>
#include <math.h>

int main() {
    double x, term, sum = 0.0;
    int n;

    printf("Enter the value of x in radians: ");
    scanf("%lf", &x);

    printf("Enter the number of terms (n): ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        term = pow(x, 2 * i - 1) / tgamma(2 * i);
        if (i % 2 == 0) {
            term *= -1; // Alternate terms have a negative sign
        }
        sum += term;
    }

    printf("sin(%lf) = %lf\n", x, sum);

    return 0;
}















#include <stdio.h>
#include <math.h>

int main() {
    double x, term, sum = 1.0;
    int n;

    printf("Enter the value of x in radians: ");
    scanf("%lf", &x);

    printf("Enter the number of terms (n): ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        term = pow(x, 2 * i) / tgamma(2 * i);
        if (i % 2 != 0) {
            term *= -1; // Alternate terms have a negative sign
        }
        sum += term;
    }

    printf("cos(%lf) = %lf\n", x, sum);

    return 0;
}













#include <stdio.h>
#include <math.h>

int main() {
    double x, term, sum = 1.0;
    int n;

    printf("Enter the value of x: ");
    scanf("%lf", &x);

    printf("Enter the number of terms (n): ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        term = pow(x, i) / tgamma(i + 1);
        sum += term;
    }

    printf("e^(%lf) = %lf\n", x, sum);

    return 0;
}














#include <stdio.h>

int main() {
    int n, search, found = 0;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int array[n];

    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &array[i]);
    }

    printf("Enter the element to search for: ");
    scanf("%d", &search);

    for (int i = 0; i < n; i++) {
        if (array[i] == search) {
            printf("Element found at index %d.\n", i);
            found = 1;
            break;
        }
    }

    if (!found) {
        printf("Element not found in the array.\n");
    }

    return 0;
}











#include <stdio.h>

int main() {
    double usage, bill;

    printf("Enter the cubic feet of water used: ");
    scanf("%lf", &usage);

    if (usage <= 1000) {
        bill = 15.00;
    } else if (usage <= 2000) {
        bill = 15.00 + 0.0175 * (usage - 1000);
    } else if (usage <= 3000) {
        bill = 15.00 + 0.0175 * 1000 + 0.02 * (usage - 2000);
    } else {
        bill = 15.00 + 0.0175 * 1000 + 0.02 * 1000 + 70.00;
    }

    printf("Water bill: $%.2lf\n", bill);

    return 0;
}








#include <stdio.h>

int main() {
    int original, sum, check_digit, new_number;
    
    printf("Enter a four-digit number: ");
    scanf("%d", &original);

    sum = (original / 1000) + ((original / 100) % 10) + ((original / 10) % 10) + (original % 10);
    check_digit = (sum % 2 == 0) ? 0 : 1;

    new_number = original * 10 + check_digit;

    printf("Original number: %d\n", original);
    printf("New number: %d\n", new_number);

    return 0;
}











#include <stdio.h>

int main() {
    int original, sum, check_digit, new_number;
    
    printf("Enter a four-digit number: ");
    scanf("%d", &original);

    sum = (original / 1000) + ((original / 100) % 10) + ((original / 10) % 10) + (original % 10);
    check_digit = (sum % 2 == 0) ? 0 : 1;#include <stdio.h>

int main() {
    int age;
    double charge;

    printf("Enter the age of the person: ");
    scanf("%d", &age);

    if (age > 55) {
        charge = 10.00;
    } else if (age >= 21) {
        charge = 15.00;
    } else if (age >= 13) {
        charge = 10.00;
    } else if (age >= 3) {
        charge = 5.00;
    } else {
        charge = 0.00;
    }

    printf("Ticket charge: $%.2lf\n", charge);

    return 0;
}














#include <stdio.h>

int main() {
    int num_people, age;
    double base_price, total_price;
    char business_trip;

    printf("Enter the number of people: ");
    scanf("%d", &num_people);

    if (num_people == 2) {
        base_price = 85.00;
    } else if (num_people == 3) {
        base_price = 90.00;
    } else if (num_people == 4) {
        base_price = 95.00;
    } else {
        printf("Enter the base price: ");
        scanf("%lf", &base_price);
    }

    printf("Is the customer on a business trip? (Y/N): ");
    scanf(" %c", &business_trip);

    printf("Enter the customer's age: ");
    scanf("%d", &age);

    if (business_trip == 'Y') {
        total_price = base_price * 0.8;
    } else if (age > 60) {
        total_price = base_price * 0.85;
    } else {
        total_price = base_price;
    }

    printf("Total cost of the room: $%.2lf\n", total_price);

    return 0;
}
















#include <stdio.h>

int main() {
    int num_courses, i;
    char grades[100];
    double total_points = 0, total_units = 0;

    printf("Enter the number of courses: ");
    scanf("%d", &num_courses);

    for (i = 0; i < num_courses; i++) {
        char grade;
        int units;

        printf("Enter grade for course %d: ", i + 1);
        scanf(" %c", &grade);

        printf("Enter units for course %d: ", i + 1);
        scanf("%d", &units);

        switch (grade) {
            case 'A':
                total_points += 4.0 * units;
                break;
            case 'B':
                total_points += 3.0 * units;
                break;
            case 'C':
                total_points += 2.0 * units;
                break;
            case 'D':
                total_points += 1.0 * units;
                break;
            case 'F':
                total_points += 0.0 * units;
                break;
            default:
                printf("Invalid grade entered!\n");
                i--; // To re-enter data for this course
        }

        total_units += units;
    }

    double gpa = total_points / total_units;
    printf("GPA: %.2lf\n", gpa);

    return 0;
}














#include <stdio.h>

int main() {
    int num_students, i;
    int total_A = 0, total_B = 0, total_C = 0, total_D = 0, total_F = 0;

    printf("Enter the number of students: ");
    scanf("%d", &num_students);

    for (i = 0; i < num_students; i++) {
        int student_number, grade;
        char letter_grade;

        printf("Enter student number for student %d: ", i + 1);
        scanf("%d", &student_number);

        printf("Enter grade for student %d: ", i + 1);
        scanf("%d", &grade);

        if (grade >= 90) {
            letter_grade = 'A';
            total_A++;
        } else if (grade >= 78) {
            letter_grade = 'B';
            total_B++;
        } else if (grade >= 65) {
            letter_grade = 'C';
            total_C++;
        } else if (grade >= 50) {
            letter_grade = 'D';
            total_D++;
        } else {
            letter_grade = 'F';
            total_F++;
        }

        printf("Student %d: Number: %d, Grade: %d, Letter Grade: %c\n", i + 1, student_number, grade, letter_grade);
    }

    printf("Total A: %d, Total B: %d, Total C: %d, Total D: %d, Total F: %d\n", total_A, total_B, total_C, total_D, total_F);

    return 0;
}














#include <stdio.h>

int main() {
    double car_price, accessory_price = 0, sales_tax, total_cost;
    int num_accessories, i;

    printf("Enter the initial price of the car: ");
    scanf("%lf", &car_price);

    printf("Enter the number of accessories (0 to 10): ");
    scanf("%d", &num_accessories);

    for (i = 0; i < num_accessories; i++) {
        double accessory_price_i;
        printf("Enter the price of accessory %d: ", i + 1);
        scanf("%lf", &accessory_price_i);
        accessory_price += accessory_price_i;
    }

    printf("Enter the sales tax percentage: ");
    scanf("%lf", &sales_tax);

    total_cost = car_price + accessory_price + (car_price + accessory_price) * sales_tax / 100;

    printf("Total cost of the car: $%.2lf\n", total_cost);

    return 0;
}













#include <stdio.h>

int main() {
    double original_price, sale_price, discount = 0.10;
    int day;

    printf("Enter the original price of the item: ");
    scanf("%lf", &original_price);

    sale_price = original_price;

    for (day = 1; day <= 5; day++) {
        printf("Day %d: Sale price: $%.2lf\n", day, sale_price);
        sale_price -= sale_price * discount;
    }

    return 0;
}











#include <stdio.h>

int main() {
    double loan_amount = 3000.00;
    double monthly_payment = 85.00;
    double interest_rate = 0.01; // 1% per month
    double balance = loan_amount;
    int months = 0;

    printf("Month\tPrincipal\tInterest\tBalance\n");

    while (balance > 0) {
        double interest = balance * interest_rate;
        double principal = monthly_payment - interest;

        if (principal > balance) {
            principal = balance;
            monthly_payment = principal + interest;
        }

        balance -= principal;

        printf("%d\t%.2lf\t\t%.2lf\t\t%.2lf\n", months + 1, principal, interest, balance);

        months++;
    }

    printf("It takes %d months to pay off the loan.\n", months);

    return 0;
}













#include <stdio.h>

int main() {
    int fillups = 6;
    double total_miles = 0.0, total_gallons = 0.0;

    for (int i = 1; i <= fillups; i++) {
        double miles, gallons;
        printf("Fillup %d\n", i);
        printf("Enter miles driven: ");
        scanf("%lf", &miles);
        printf("Enter gallons of gas: ");
        scanf("%lf", &gallons);

        total_miles += miles;
        total_gallons += gallons;
    }

    double average_mpg = total_miles / total_gallons;

    printf("Average miles per gallon: %.2lf\n", average_mpg);

    return 0;
}











#include <stdio.h>

int main() {
    int num_courses;
    double total_points = 0, total_units = 0;

    printf("Enter the number of courses: ");
    scanf("%d", &num_courses);

    for (int i = 1; i <= num_courses; i++) {
        char grade;
        int units;

        printf("Enter grade for course %d (A/B/C/D/F): ", i);
        scanf(" %c", &grade);

        units = 3; // Assuming all courses are 3 units

        switch (grade) {
            case 'A':
                total_points += 4.0 * units;
                break;
            case 'B':
                total_points += 3.0 * units;
                break;
            case 'C':
                total_points += 2.0 * units;
                break;
            case 'D':
                total_points += 1.0 * units;
                break;
            case 'F':
                total_points += 0.0 * units;
                break;
            default:
                printf("Invalid grade entered!\n");
                i--; // To re-enter data for this course
        }

        total_units += units;
    }

    double gpa = total_points / total_units;
    printf("GPA: %.2lf\n", gpa);

    return 0;
}













#include <stdio.h>

int main() {
    int class_size = 35;
    int scores[class_size], highest_score = 0;
    char grades[class_size];

    printf("Enter scores for %d students:\n", class_size);

    for (int i = 0; i < class_size; i++) {
        printf("Enter score for student %d: ", i + 1);
        scanf("%d", &scores[i]);
        
        if (scores[i] > highest_score) {
            highest_score = scores[i];
        }
    }

    for (int i = 0; i < class_size; i++) {
        if (scores[i] >= highest_score - 2) {
            grades[i] = 'A';
        } else if (scores[i] >= highest_score - 4) {
            grades[i] = 'B';
        } else if (scores[i] >= highest_score - 6) {
            grades[i] = 'C';
        } else if (scores[i] >= highest_score - 8) {
            grades[i] = 'D';
        } else {
            grades[i] = 'F';
        }

        printf("Student %d: Score: %d, Grade: %c\n", i + 1, scores[i], grades[i]);
    }

    printf("Highest score: %d\n", highest_score);

    return 0;
}










#include <stdio.h>

int main() {
    int hours_per_day = 24;
    int min_employees = 3;
    int employees_per_customer = 1;
    int customers[14][24]; // Assuming customers[day][hour]

    // Assume you have the customer data filled in the array

    // Calculate the average customers per hour over 14 days
    int total_customers = 0;
    for (int day = 0; day < 14; day++) {
        for (int hour = 0; hour < 24; hour++) {
            total_customers += customers[day][hour];
        }
    }
    double avg_customers_per_hour = (double) total_customers / (14 * hours_per_day);

    // Calculate the required employees per hour
    int required_employees[24];
    for (int hour = 0; hour < 24; hour++) {
        required_employees[hour] = min_employees + (avg_customers_per_hour / 20);
    }

    // Output the required employees per hour
    for (int hour = 0; hour < 24; hour++) {
        printf("Hour %d: %d employees\n", hour, required_employees[hour]);
    }

    return 0;
}












#include <stdio.h>

int main() {
    int num_salespeople = 10;
    int days_per_week = 7;
    int days_off = 2;

    double sales[10][7]; // Assuming sales[salesperson][day]

    // Assume you have the sales data filled in the array

    double total_weekly_sales = 0;
    for (int salesperson = 0; salesperson < num_salespeople; salesperson++) {
        double weekly_sales = 0;
        for (int day = 0; day < days_per_week; day++) {
            weekly_sales += sales[salesperson][day];
        }
        total_weekly_sales += weekly_sales;

        double avg_sales_per_day = (weekly_sales * 1.0) / (days_per_week - days_off);
        printf("Salesperson %d: Avg sales per day: %.2lf\n", salesperson + 1, avg_sales_per_day);
    }

    double avg_sales_per_week = total_weekly_sales / (num_salespeople * (days_per_week - days_off));
    printf("Total Avg Sales per Week: %.2lf\n", avg_sales_per_week);

    return 0;
}











Algorithm:
1. Create a 2D array to store test grades (students x tests).
2. Loop through each student and each test:
   a. Read and store the test grade.
3. Read the student number and test number.
4. Display the grade for the given student and test.

Pseudocode:
Initialize 2D array grades[25][4]  // 25 students, 4 tests

For student = 1 to 25
    For test = 1 to 4
        Display "Enter test grade for student ", student, " and test ", test
        Read grades[student][test]
    End For
End For

Display "Enter student number: "
Read studentNumber
Display "Enter test number: "
Read testNumber

Display "Grade for student ", studentNumber, " and test ", testNumber, ": ", grades[studentNumber][testNumber]












Algorithm:
1. Create parallel arrays for student names and test scores.
2. Read student's name.
3. Sequentially search for the name in the names array.
4. If found, print the name and corresponding test scores.

Pseudocode:
Initialize arrays studentNames[25], testScores[25][4]  // 25 students, 4 tests

For student = 1 to 25
    Display "Enter student name for student ", student
    Read studentNames[student]
    For test = 1 to 4
        Display "Enter test score for ", studentNames[student], " and test ", test
        Read testScores[student][test]
    End For
End For

Display "Enter student's name: "
Read searchName

Found = false
For student = 1 to 25
    If searchName equals studentNames[student]
        Display "Student: ", studentNames[student]
        Display "Test scores: "
        For test = 1 to 4
            Display testScores[student][test], " "
        End For
        Found = true
        Exit Loop
    End If
End For

If Found is false
    Display "Student not found."














Algorithm:
1. Initialize arrays for wages, departments, gender, age.
2. Read data for all employees.
3. Loop through departments and calculate:
   a. Total wages of men and women in each department.
   b. Total number of employees in each department.
   c. Total age of men and women in each department.
4. Calculate average age and average wage per department and gender.

Pseudocode:
Initialize arrays wages[12], departments[12], gender[12], age[12]

For employee = 1 to 95
    Read wage, department, gender, age
    Add wage to wages[department]
    Increment department count in departments array
    If gender equals "male"
        Add age to age[department] for men
    Else
        Add age to age[department] for women
End For

For department = 1 to 12
    Calculate average wage for department
    Calculate average age for department for men and women
    Display department, average wage, average age for men, average age for women
End For












Algorithm:
1. Initialize arrays age[95], gender[95], maritalStatus[95], major[95], salary[95].
2. Read data for all alumni.
3. Loop through data and calculate average salary for specific conditions.

Pseudocode:
Initialize arrays age[95], gender[95], maritalStatus[95], major[95], salary[95]

For alumnus = 1 to 95
    Read age, gender, maritalStatus, major, salary
End For

Display "Enter a set of conditions (age, gender, marital status, major): "
Read condition1, condition2, condition3, condition4

totalSalary = 0
numAlumni = 0
For alumnus = 1 to 95
    If age[alumnus] equals condition1 and gender[alumnus] equals condition2 and maritalStatus[alumnus] equals condition3 and major[alumnus] equals condition4
        totalSalary += salary[alumnus]
        numAlumni++
    End If
End For

If numAlumni > 0
    averageSalary = totalSalary / numAlumni
    Display "Average salary for given conditions: ", averageSalary
Else
    Display "No alumni found for given conditions."













#include <stdio.h>

int main() {
    int num_students = 1200;
    int class_levels[5] = {0}; // Undergrad levels (0-3) and graduate level (4)
    int major_count[7] = {0}; // Count of students per major
    int class_major_count[5][7] = {0}; // Count of students per class level per major

    // Assume you have the student data with class levels and majors

    for (int i = 0; i < num_students; i++) {
        int class_level, major;

        // Assume you input the class level and major for each student
        // class_level ranges from 0 to 4 (0-3 for undergrad and 4 for grad)
        // major ranges from 0 to 6 (7 different majors)

        class_levels[class_level]++;
        major_count[major]++;
        class_major_count[class_level][major]++;
    }

    // Output class level distribution
    for (int i = 0; i < 5; i++) {
        printf("Class Level %d: %d students\n", i, class_levels[i]);
    }

    // Output major distribution
    for (int i = 0; i < 7; i++) {
        printf("Major %d: %d students\n", i, major_count[i]);
    }

    // Output class level per major distribution
    for (int i = 0; i < 5; i++) {
        for (int j = 0; j < 7; j++) {
            printf("Class Level %d, Major %d: %d students\n", i, j, class_major_count[i][j]);
        }
    }

    return 0;
}














#include <stdio.h>

int main() {
    int num_days = 14;
    double wind_speeds[14]; // Assume you have the wind speed data for each day

    // Assume you have filled in the wind speed data for each day

    double total_wind_speed = 0;
    double highest_speed = wind_speeds[0];
    double lowest_speed = wind_speeds[0];

    for (int i = 0; i < num_days; i++) {
        total_wind_speed += wind_speeds[i];
        if (wind_speeds[i] > highest_speed) {
            highest_speed = wind_speeds[i];
        }
        if (wind_speeds[i] < lowest_speed) {
            lowest_speed = wind_speeds[i];
        }
    }

    double average_speed = total_wind_speed / num_days;

    printf("Average Wind Speed over 2 weeks: %.2lf\n", average_speed);
    printf("Highest Wind Speed: %.2lf\n", highest_speed);
    printf("Lowest Wind Speed: %.2lf\n", lowest_speed);

    for (int i = 0; i < num_days; i++) {
        double speed_difference = highest_speed - wind_speeds[i];
        printf("Day %d: Difference from Highest: %.2lf\n", i + 1, speed_difference);
    }

    return 0;
}
