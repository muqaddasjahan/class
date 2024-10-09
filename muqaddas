import java.util.Scanner;

public class CinemaBookingSystem {
    public static void main(String[] args) {
        // Initialize a 5x5 cinema seating arrangement with seat names
        String[][] seats = new String[5][5];

        // Assign names to each seat
        for (int i = 0; i < seats.length; i++) {
            for (int j = 0; j < seats[i].length; j++) {
                seats[i][j] = "S" + (i * seats.length + (j + 1)); // Seat names like S1, S2, ..., S25
            }
        }

        Scanner scanner = new Scanner(System.in);
        boolean keepRunning = true;

        // Main loop for booking seats
        while (keepRunning) {
            // Display the seating arrangement
            System.out.println("Current Seating Arrangement:");
            displaySeats(seats);

            // Ask the user to input the seat name (e.g., S1, S2) or type 'exit' to quit
            System.out.print("Enter seat number (e.g., S1) or 'exit' to quit: ");
            String seatInput = scanner.next();

            // Check if the user wants to exit
            if (seatInput.equalsIgnoreCase("exit")) {
                keepRunning = false;
                break;
            }

            // Validate the seat input and book the seat
            boolean seatBooked = bookSeat(seats, seatInput);
            if (seatBooked) {
                System.out.println("Seat booked successfully!\n");
            }
        }

        System.out.println("Thank you for using the Cinema Booking System!");
    }

    // Method to display the seats
    public static void displaySeats(String[][] seats) {
        for (int i = 0; i < seats.length; i++) {
            for (int j = 0; j < seats[i].length; j++) {
                System.out.print(seats[i][j] + " "); // Print seat name or "Booked"
            }
            System.out.println();
        }
    }

    // Method to book a seat
    public static boolean bookSeat(String[][] seats, String seatName) {
        // Iterate through the 2D array to find the seat
        for (int i = 0; i < seats.length; i++) {
            for (int j = 0; j < seats[i].length; j++) {
                // Check if the seat name matches and is available
                if (seats[i][j].equals(seatName)) {
                    // If seat is not booked
                    if (!seats[i][j].equals("Booked")) {
                        seats[i][j] = "Booked"; // Mark seat as booked
                        return true; // Seat successfully booked
                    } else {
                        System.out.println("Sorry, that seat is already booked. Please choose another one.\n");
                        return false; // Seat already booked
                    }
                }
            }
        }
        // If the seatName doesn't exist in the array
        System.out.println("Invalid seat number. Please enter a valid seat name (e.g., S1).\n");
        return false;
    }
}
