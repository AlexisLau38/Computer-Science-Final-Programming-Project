```java
//NAME: Alexis Lau
import java.util.Scanner;
public class FinalProgrammingProject {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        //Greeting (1 Mark)
        System.out.println("Welcome to the G1 Test: Road Rules.");
        //Display of menu (3 Marks)
        String a = "a. Write a G1 Test";
        String b = "b. Login as admin";
        System.out.println(a + "\n" + b);
        System.out.print("Type a or b to choose option: ");
        String chosen_option = sc.nextLine();
        if (chosen_option.equals("a")) {
            //Part A Questions
            // We use an array because in Part A there are many different questions, and we can store multiple different questions within a single name in order to access it efficiently and more conveniently.
            String[] PartA = {
                    "To get your vehicle out of a skid, you should first:",
                    "When may you lend your driver's license?",
                    "What must a driver do before entering a highway from a private road or driveway?",
                    "Never change lanes in traffic without:",
                    "When the driver of another vehicle is about to overtake and pass your vehicle, you must:",
                    "When you are deciding whether or not to make a U-turn, your first consideration should be to check:",
                    "Is it more dangerous to drive at the maximum speed limit at night than during daytime as:",
                    "You should under all conditions drive at a speed which will allow you to:",
                    "As a G2 driver, your blood alcohol level must not be over:",
                    "Unless otherwise posted, the maximum speed limit allowed in cities, towns, villages, and built-up areas is:"
            };
            String[] PartAChoices = {
                    "A. Steer straight ahead.\nB. Steer in the opposite direction of the skid.\nC. Steer in the direction you want to go.\nD. Apply brakes hard.",
                    "A. In emergencies.\nB. To a person learning to drive.\nC. It is not permitted.\nD. For identification purposes.",
                    "A. Enter or cross the highway as quickly as possible.\nB. Yield right of way to all vehicles approaching on the highway.\nC. Sound horn and proceed with caution.\nD. Give hand signal then take right of way.",
                    "A. Looking in the rear view mirror only.\nB. Giving proper signal and looking to make sure the move can be made safely.\nC. Blowing your horn and looking to the rear.\nD. Decreasing speed and giving correct signal.",
                    "A. Speed up so that passing is not necessary.\nB. Move to the left to prevent passing.\nC. Signal to the other driver not to pass.\nD. Move to the right and allow such vehicle to pass.",
                    "A. Traffic regulations.\nB. Presence of trees, fire hydrants or poles near the curb.\nC. Turning radius of your car.\nD. Height of curb.",
                    "A. Your reaction time is slower at night.\nB. You cannot see as far ahead at night.\nC. Some drivers unlawfully drive with parking lights only.\nD. The roadways are more apt to be slippery at night.",
                    "A. Stop within 150 meters (500 feet)\nB. Stop within 90 meters (300 feet)\nC. Stop within 60 meters (200 feet)\nD. Stop within a safe distance.",
                    "A. 0.04\nB. 0.07\nC. 0.09\nD. 0.00",
                    "A. 50 km/h\nB. 40 km/h\nC. 60 km/h\nD. 55 km/h"
            };
            String[] PartAAnswers = {
                    "C","C","B","B","D","A","B","D","D","A"
            };
            int score = 0/6;
            int questionsLeft = PartA.length;
            System.out.println("G1 Drivers Test: ");
            //In the following phrase, we create a loop for each of the remaining questions.
            for (int p = questionsLeft; p >= 4; p--) {
                //In order to generate random questions, we use the Math.random method where we multiply the Math.random() by p in order to make the number of random numbers larger.
                int q = (int) (Math.random() * p);
                System.out.println("\n" + PartA[q]);
                System.out.println(PartAChoices[q]);
                //Now, we must check whether the user's answer is inputted so we use a while loop.
                while (true) {
                    System.out.print("Enter A, B, C, or D: ");
                    String userAnswer = sc.nextLine().toUpperCase();
                    if (userAnswer.equals(PartAAnswers[q])) {
                        System.out.println("Correct.");
                        score = score + 1;
                    }
                    else {
                        System.out.println("Incorrect.");
                    }
                    //Now we will check if they passed the first section by checking if they scored 4 or more.
                    if (score < 4) {
                        //Now we have Part B Questions:
                        String[] PartB = {
                                "When passing a cyclist, leave at least __ distance between your vehicle and the cyclist.",
                                "If you are approaching an intersection with a non-operating signal, you should:",
                                "What do the two solid yellow lines mean on the road?",
                                "Why must drivers use signals when turning?",
                                "What lane of traffic should drivers use when they intend to make a right-hand turn?",
                                "Which driver has right-of-way in a roundabout?",
                                "If a signal light changes from green to amber as a driver approaches an intersection, what should the driver do?",
                                "When it is safe to do so, passing other vehicles on the right side...",
                                "How many meters in both directions must drivers be able to see in order to make a legal U-turn?",
                                "When driving with headlights on, in what situations are drivers required to use low beam headlights?"
                        };
                        String[] PartBChoices = {
                                "A. 1 meter.\nB. 2 meters.\nC. 3 meters.\nD. 1.5 meters.",
                                "A. Treat it as a four way stop.\nB. Continue going straight.\nC. Make an abrupt stop.\nD. Slow down the speed of your vehicle.",
                                "A. You are not allowed to pass the solid double yellow lines whichever way you are driving.\nB. You can cross the lines whichever way you are driving.\nC. You can cross the lines if you are driving North.\nD. You can cross the lines if you plan to turn left ahead.",
                                "A. To notify pedestrians of their intention.\nB. To notify drivers behind them of their intention.\nC. To notify oncoming traffic of their intention.\nD. ALl of the above.",
                                "A. The lane closest to the left side of the road.\nB. The lane approaching from the left.\nC. The lane closest to the center line of the road.\nD. The lane closest to the right of the road.",
                                "A. A driver turning right into the roundabout.\nB. A driver turning left into the roundabout.\nC. A driver already in the roundabout.\nD. A driver approaching the roundabout.",
                                "A. Speed up to clear the intersection as quickly as possible.\nB. Stop. If the stop cannot be made safely, proceed with caution.\nC. Maintain current speed and continue through intersection.\nD. Sound the horn to warn pedestrians and other drivers that the vehicle will travel through the intersection.",
                                "A. Is permitted when the street or highway has two or more lanes for traffic in the direction the vehicle is traveling.\nB. Is not permitted under any circumstance.\nC. Is permitted at any time on any street or highway.\nD. Is permitted provided it is possible to do so by driving on the shoulder of the road.",
                                "A. 100 meters.\nB. 150 meters.\nC. 50 meters.\nD. 250 meters.",
                                "A. Within 300 meters of an oncoming vehicle.\nB. Within 150 meters of an oncoming vehicle.\nC. Within 50 meters of an oncoming vehicle.\nD. Within 250 meters of an oncoming vehicle."
                        };
                        String[] PartBAnswers = {
                                "A","A","A","D","D","C","B","A","B","B"
                        };
                        //Now we will do the same checking process as Part A.
                        int scoreB = 0/6;
                        int questionsLeftForB = PartB.length;
                        for (int x = questionsLeft; x >= 4; x--) {
                            //In order to generate random questions, we use the Math.random method where we multiply the Math.random() by p in order to make the number of random numbers larger.
                            int z = (int) (Math.random() * x);
                            System.out.println("\n" + PartB[z]);
                            System.out.println(PartBChoices[z]);
                            //Now, we must check whether the user's answer is inputted so we use a while loop.
                            while (true) {
                                System.out.print("Enter A, B, C, or D: ");
                                String userAnswerB = sc.nextLine().toUpperCase();
                                if (userAnswerB.equals(PartBAnswers[z])) {
                                    System.out.println("Correct.");
                                    scoreB = scoreB + 1;
                                }
                                else {
                                    System.out.println("Incorrect.");
                                }
                                //Now we will check if they passed the last section by checking if they scored 4 or more.
                                if (score < 4) {
                                    System.out.println("\nYour final score is " + (score + scoreB) + "/12");
                                }
                                if (score + scoreB >= 8) {
                                    System.out.print("You passed!");
                                }
                                else {
                                    System.out.print("You failed.");
                                }
                                }
                                }
                    }
                    else {
                        System.out.print("You can no longer pass because you scored lower than 4/6 in Part A.");
                    }
                    //This part removes each used question.
                    PartA[q] = PartA[p-1];
                    PartAChoices[q] = PartAChoices[p-1];
                    PartAAnswers[q] = PartAAnswers[p-1];
                }
            }

        }
        else {
            for (int i = 0; i < 10000; i++) {
                System.out.print("Enter password: ");
                String userAnswerToPassword = sc.nextLine();
                String correctAnswerToPassword = "HelloWorld123";
                if (userAnswerToPassword.equals(correctAnswerToPassword)) {
                    System.out.println("You are now logged in as admin.");
                    break;
                }
                else {
                    System.out.println("Password is incorrect. Try again: ");
                }
            }

        }
    }
}
```
