package javaz;

import java.util.Scanner;

public class WeatherApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int option;

        do {
            System.out.println("Options:");
            System.out.println("1. Get weather");
            System.out.println("2. Get Wind Speed");
            System.out.println("3. Get Pressure");
            System.out.println("0. Exit");
            System.out.print("Enter your choice: ");
            option = scanner.nextInt();
            scanner.nextLine(); // Consume the newline character left by nextInt()

            switch (option) {
                case 1:
                    getWeather(scanner);
                    break;
                case 2:
                    getWindSpeed(scanner);
                    break;
                case 3:
                    getPressure(scanner);
                    break;
                case 0:
                    System.out.println("Exiting the program.");
                    break;
                default:
                    System.out.println("Invalid option. Try again.");
            }
        } while (option != 0);

        scanner.close();
    }

    private static void getWeather(Scanner scanner) {
        System.out.print("Enter the date: ");
        String date = scanner.nextLine();
        // Call the API to get the weather data for the input date
        // Replace the following line with your API call and parsing logic
        double temperature = 25.0;
        System.out.println("Temperature for " + date + ": " + temperature + " °C");
    }

    private static void getWindSpeed(Scanner scanner) {
        System.out.print("Enter the date: ");
        String date = scanner.nextLine();
        // Call the API to get the wind speed data for the input date
        // Replace the following line with your API call and parsing logic
        double windSpeed = 12.5;
        System.out.println("Wind Speed for " + date + ": " + windSpeed + " m/s");
    }

    private static void getPressure(Scanner scanner) {
        System.out.print("Enter the date: ");
        String date = scanner.nextLine();
        // Call the API to get the pressure data for the input date
        // Replace the following line with your API call and parsing logic
        double pressure = 1013.25;
        System.out.println("Pressure for " + date + ": " + pressure + " hPa");
    }
    
}
