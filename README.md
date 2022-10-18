# cuddly
/****************************************************************
/ @author: Teisi Makhala
/ @purpose: ATM APP
/ @date: October 2022
/ @contact: teisilydia@gmail.com
/****************************************************************/

#include <iostream>
using namespace std;

//Creating an ATM App
void showMenu()
{
	cout << "***************** MENU *********************" << endl;
	cout << "          1. Balance " << endl;
	cout << "          2. Deposit " << endl;
	cout << "          3. Withdraw" << endl;
	cout << "          4. Exit" << endl;
	cout << "*******************************************" << endl;
	
}
int main()
{
	double balance = 154.33,deposited,withdraw;
	int option;
	do{
	    showMenu();
	    cout <<"Enter the option " ;
	    cin >> option;
	    system("cls");
	    
        switch(option){
	    case 1: cout << "Balance is M" << balance << endl; break;
	    case 2: cout << "Please enter amount:M";
	            cin >> deposited;
	            balance +=deposited;
	        break;
        case 3: cout << "Please enter amount:M" ;
                cin >> withdraw;
                if (withdraw<=balance)
            	    balance -= withdraw;
			
			    else
				    cout <<"Not enough balance." << endl;
			break;
		}
		}while(option!=4);
	
	system("pause>0");
				
}
