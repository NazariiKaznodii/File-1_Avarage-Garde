// College project
// Avarage grade

#include <iostream>
#include <iomanip>

using namespace std;

//Function prototype

double calcAvarage(int, int, int, int, int);
// 5 int scores 5 grades, but it also will work with only 1 int.
string determineGrade(int);

int main() {
	int score1, score2, score3, score4, score5;

	cout << "Entaer 5 test scores (one by one) to calc avarage; " << endl;
	cin >> score1;
	cout << "Grade: " << determineGrade(score1) << endl;

	cin >> score2;
	cout << "Grade: " << determineGrade(score2) << endl;

	cin >> score3;
	cout << "Grade: " << determineGrade(score3) << endl;

	cin >> score4;
	cout << "Grade: " << determineGrade(score4) << endl;

	cin >> score5;
	cout << "Grade: " << determineGrade(score5) << endl;

	double average = calcAvarage(score1, score2, score3, score4, score5);
	cout << "Average score: " << average << endl;
	cout << "Average Grade: " << determineGrade(average) << endl;

	return 0;
}

// Function to calculate the average
double calcAvarage(int score1, int score2, int score3, int score4, int score5) {
	return (score1 + score2 + score3 + score4 + score5) / 5;
}

// Function to determine the letter grade based on the score



string determineGrade(int score) {
	if (score >= 90 && score <= 100)
		return "A";
	else if (score >= 80 && score < 90)
		return "B";
	else if (score >= 70 && score < 80)
		return "C";
	else if (score >= 60 && score < 70)
		return "D";
	else
		return "F";

}
