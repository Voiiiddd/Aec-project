#include <iostream>
#include <string>
#include <cctype>
using namespace std;


string checkStrength(const string &password)
{
bool hasUpper = false, hasLower = false, hasDigit = false, hasSpecial = false;
int length = password.length();


for (char ch : password)
{
if (isupper(ch)) hasUpper = true;
else if (islower(ch)) hasLower = true;
else if (isdigit(ch)) hasDigit = true;
else hasSpecial = true;
}


if (length >= 8 && hasUpper && hasLower && hasDigit && hasSpecial)
return "Strong";
else if (length >= 6 && hasLower && hasDigit)
return "Medium";
else
return "Weak";
}


int main()
{
string password;


cout << "Enter your password: ";
cin >> password;


string strength = checkStrength(password);


cout << "\nPassword Strength: " << strength << endl;


if (strength == "Weak")
{
cout << "Suggestions:\n";
cout << "- Increase password length\n";
cout << "- Add numbers and special characters\n";
}
else if (strength == "Medium")
{
cout << "Suggestions:\n";
cout << "- Add uppercase letters\n";
cout << "- Add special characters\n";
}
else
{
cout << "Your password is secure." << endl;
}


return 0;
}
