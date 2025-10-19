import java.util.Scanner;
public class MirrorCheck {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Concave length checking");
        System.out.print("Enter image distance v: ");
        double v = input.nextDouble();
        System.out.print("Enter object distance u: ");
        double u = input.nextDouble();
        u = -u;
        double f = 1 / ((1/v) + (1/u));
        System.out.printf("Focal length f = %.2f cm", f);
        System.out.println();
        if (f >= 21.0 && f <= 25.0) {
            System.out.println("Mirror is Acceptable");
        } else {
            System.out.println("Mirror is NOT acceptable");
        }
        input.close();
    }
}
