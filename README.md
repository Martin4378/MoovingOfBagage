# MoovingOfBagage

import java.util.Scanner;

public class P46_MoovingOfBagage {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        int w = Integer.parseInt(scanner.nextLine());
        int l = Integer.parseInt(scanner.nextLine());
        int h = Integer.parseInt(scanner.nextLine());

        int roomVolume = w * l * h;
        int boxesVolume = 0;

        while (boxesVolume <= roomVolume) {

            String command = scanner.nextLine();

            if (command.equalsIgnoreCase("done")) {
                break;
            }

            int currentBoxesCount = Integer.parseInt(command);
            boxesVolume += currentBoxesCount;


        }

        int volumeDifference = roomVolume - boxesVolume;

        if (volumeDifference >= 0) {
            System.out.printf("%d Cubic meters left.%n", volumeDifference);
        } else {
            System.out.printf("No more free space! You need %d Cubic meters more.%n", Math.abs(volumeDifference));
        }
    }

}
