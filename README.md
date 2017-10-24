# TV-Subscription

#include <iostream>

using namespace std;

int main()

{
    char choice1, choice2;
    double account, code, prechannels, connections, fee;

    cout<<"Enter R or r if you are residential or B or b for business"<<endl;
    cin>>choice1;
    cout<<"Please enter account number"<<endl;
    cin>>account;
    cout<<"Please enter your customer code"<<endl;
    cin>>code;
    cout<<""<<endl;
    cout<<"Do you have any premium channels? Y or y for YES or N or n for NO"<<endl;
    cin>>choice2;

    if (choice2=='Y'||choice2=='y')
    {
        cout<<"How many premium channels do you have\n"<<endl;
        cin>>prechannels;
    }

    else if (choice2=='N' || choice2=='n')
        cout<<"No Premium Channels\n"<<endl;



    if (choice1=='B' || choice1=='b')
    {
        cout<<"How many connections do you have?\n"<<endl;
        cin>>connections;
    }


    if (connections<=10)
    {
        fee=75;
    }

    else 
    {
        fee=connections+75;
    }


    if (choice1=='R'||choice1=='r')
    {
        cout<<"Bill processing fee:     $"<<4.50<<endl;
        cout<<"Basic service fee:       $"<<20.50<<endl;
        cout<<"Premium channels:        $"<<7.50*prechannels<<endl;
        cout<<"Total is:                $"<<4.50+20.50+prechannels*7.50<<endl;
    }

    else if (choice1=='B' || choice1=='b')
    {

        cout<<"Bill processing fee:     $"<<15.00<<endl;
        cout<<"Basic service fee:       $"<<fee<<endl;
        cout<<"Premium channels fee:    $"<<prechannels*50<<endl;
        cout<<"Total is:                $"<<15.00+fee+prechannels*50.00<<endl;
    }
    return 0;
    }

