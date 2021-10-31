# Lesson-8

How many days in a month

    int input;
    cout << "What month is it?Type the month in a number way. Example if its January type 1\n";
    cin >> input;
    switch (input)
    {
    case 1:
        cout << "January have 31 days.";
        break;
    case 2:
        cout << "February have 28/29 days.";
        break;
    case 3:
        cout << "March have 31 days.";
        break;
    case 4:
        cout << "April have 30 days.";
        break;
    case 5:
        cout << "May have 31 days.";
        break;
    case 6:
        cout << "June have 30 days.";
        break;
    case 7:
        cout << "July have 31 days.";
        break;
    case 8:
        cout << "August have 30 days.";
        break;
    case 9:
        cout << "September have 31 days.";
        break;
    case 10:
        cout << "October have 30 days.";
        break;
    case 11:
        cout << "November have 31 days.";
        break;
    case 12:
        cout << "December have 30 days.";
        break;
        }
   
 Gameplay
 
     #include <iostream>

    using namespace std;
    int main()
    {

        cout << "Would you like to continue? (Y/N): "; 
        char answer; 
        cin >> answer; 

          switch (answer)
          { 

          case 'Y':
          case 'y':
          {
            cout << "You selected yes";
            break;
          }

          case 'N':
          case 'n':
          {
            cout << "You selected no";
            break;
          }

          default: 
          {
            cout << "incorrect command";
          }

          }
        cin.get(); //keeps console window open in Visual Studio
        return 0;
      }

Fuel

    #include <iostream>
    using namespace std;
    int main()
    {
        cout << "Kindly enter how many litres you want to fill up your car\n";
        int lit;
        cin >> lit;
        if (lit != 0)
        {
            cout << "You have selected " << lit << " litres\n";
            cout << "Kindly select the fuel type you want for your car\n";
            cout << "Enter 'p' for Petrol\n 'd' for Diesel\n";
            char fuel;
            cin >> fuel;
            switch (fuel)
            {
            case 'P':
            case 'p':
            {

                cout << "You have selected Petrol for filling up your car\n "; 
                int c;
                c = lit * 0.8;
                cout << "\nThe price per litres is 0.8 now the total is " << c;
                break;
            }
            case 'd':
            case 'D':
            {
                cout << "You have selected Diesel for filling up your car ";
                int c;
                c = lit * 0.5;
                cout << "\nThe price per litres is 0.5 now the total is " << c;
                break;

                break;
            }

            default:
            {
                cout << "Incorrect command"; break;
            }
            }
        }
        else
        {
            cout << "Incorrect command\n ";
        }


    }

Temperature

     #include<iostream>
    using namespace std;
    int main()
    {
        int temp;
        cout << "temperature converter, please choose  1: celcius to fahrenheit 2: fahrenheit to celcius \n\n";
        cin >> temp;
        switch (temp)
        {
        case 1:
            int temp = (temp * 9 / 5) + 32;
            cout << "temperature is f =" << temp;
            break;
        case 2:
            int temp = (32 - 32) * 5 / 9;
            cout << "temperature is c =" << temp;
            break;
        default:
            cout << "invalid input";
            break;
        }
    }
    
 Name that shape
 
     int main()
    {
    int input;
    cout << "To know what shape it is, Type how many sides it has. Example if 4 sides then type 4\n";
    cin >> input;
    switch (input)
    {
    case 1:
      cout << "invalid" << endl;
      break;
    case 2:
      cout << "invalid" << endl;
      break;
    case 3:
      cout << "The shape is a triangle" << endl;
      break;
    case 4:
      cout << "The shape is a square." << endl;
      break;
    case 5:
      cout << "The shape is a pentagon" << endl;
      break;
    case 6:
      cout << "The shape is a hexagon" << endl;
      break;
    case 7:
      cout << "The shape is a heptagon" << endl;
      break;
    case 8:
      cout << "The shape is an octagon" << endl;
      break;
    case 9:
      cout << "The shape is a nonagon" << endl;
      break;
    case 10:
      cout << "The shape is a decagon" << endl;
      break;
    case 11:
      cout << "The shape is a hendecagon." << endl;
      break;
    case 12:
      cout << "The shape is a dodecagon." << endl;
      break;

    default:
    {
      cout << "Incorrect Input" << endl;
      break;
    }
    
Capital of France

    #include<iostream>
    using namespace std;
    int main()
      {
    char input;
    cout << "What is the capital of France?" << "Type R for Rome, Type P for Paris, type V for Venice" << endl;
    cin >> input;
    switch (input)
    {

    case 'P':
    case 'p':
    {
        cout << "Correct! The Capital of France is Paris" << endl;
        break;
    }


    case 'R':
    case 'r':
    case 'v':
    case 'V':
    {
        cout << "Incorrect. The Capital of France is Paris" << endl;
        break;
    }

    default:
    {
        cout << "Invalid Input" << endl;
    }
    
Grade

    #include <iostream>
    #include <exception>
    #include <string>

    using namespace std;
    int main()
    {




        cout << "Enter your full name" << endl;
        string name;
      // cin cannot read spaces, that is why we can use the getline code to read the input untill the next line
        getline(cin, name);


        cout << "\nEnter The Marks Between 0 To 100 to check your grade:";

        cout << "\nEnter The Mark: ";
        int marks;

        std::cin >> marks;
        //Using the cin.fail function (when user enters alphabet instead of numbers)
        if (std::cin.fail())
        {
            std::cin.clear();
            std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
            std::cout << "Incorrect command\n: ";
        }

        else if (marks > 100)

        {

            /* Marks greater than 100 */

            cout << "\nKindly input your Marks Between Limit\n";
        }

        else

        {

            switch (marks / 10)

            {

            case 10:

            case 9:
            case 8:

            {
                /* Marks between 80-100 */


                cout << name <<" Your Grade Is: A Excellent";


                break;
            }
            case 7:

            {    /* Marks between 70-79 */


                cout << name << " Your Grade Is: B Very Good";


                break;
            }
            case 6:
            {
                /* Marks between 60-69 */


                cout << name << " Your Grade Is: C Fair";

                break;
            }
            case 5:
            {
                /* Marks between 50-59 */

                cout << name << " Your Grade Is: D Need more practice";


                break;
            }
            case 4:
            {
                /* Marks between 40-49 */



                cout << name << " Your Grade Is: E Need more practice";



                break;
            }
            default:
            {
                /* Marks less than 40 */


                cout << name << " You Grade Is: F or Fail\n";


            }
            }
        }
    }
