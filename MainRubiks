//Alexandre Nino
//Alexnino1234@hotmail.com

//Functional Rubik's Cube

#include<iostream>
#include<string>

using namespace std;
class Cube {
public:
	char Array[6][9];
	void FreshCube(char Array[6][9]);		//makes a cube with all the color in order
	void PrintCube(char Array[6][9]);		//Print all the sides to visualize
	void inputCube(char Array[6][9]);		//input individual colors
	void RotateSide(char Array[6][9],int side);		// Rotate face side
	void CounterRotateSide(char Array[6][9],int side);  // counter rotate a face
	void Right(char Array[6][9]);		// Right Turn ---- ALL THE FUNCTIONS following in the class ARE Rubiks Moves
	void RightInverse(char Array[6][9]); //Right "inverse" Turn
	void Left(char Array[6][9]);		//Left Turn
	void LeftInverse(char Array[6][9]); // Left "Inverse" Turn
	void Up(char Array[6][9]);
	void UpInverse(char Array[6][9]);
	void Down(char Array[6][9]);
	void DownInverse(char Array[6][9]);
	void Front(char Array[6][9]);
	void FrontInverse(char Array[6][9]);
	void Back(char Array[6][9]);
	void BackInverse(char Array[6][9]);
};
int main() {
	Cube RubiksCube;
	char Rubik[6][9];


	RubiksCube.FreshCube(Rubik);	//if you want to input your own values replace this line with RubiksCube.inputCube(Rubik);
	RubiksCube.PrintCube(Rubik);

	bool Quit = false;
	char answer = 'N';
	char move1;

	while (!Quit) {				// while loop made to enter multiple moves
		cout << "What move would you like to make?(L,LI,R,RI,U,UI..)\n";
		cin>>move1;
		move1 = toupper(move1);
		if (move1 == 'L') {
			RubiksCube.Left(Rubik);
		}
		else if(move1 == 'LI') {
			RubiksCube.LeftInverse(Rubik);
		}
		else if (move1 == 'R') {
			RubiksCube.Right(Rubik);
		}
		else if (move1 == 'RI') {
			RubiksCube.RightInverse(Rubik);
		}
		else if (move1 == 'B') {
			RubiksCube.Back(Rubik);
		}
		else if (move1 == 'BI') {
			RubiksCube.BackInverse(Rubik);
		}
		else if (move1 == 'D') {
			RubiksCube.Down(Rubik);
		}
		else if (move1 == 'DI') {
			RubiksCube.DownInverse(Rubik);
		}
		else if (move1 == 'F') {
			RubiksCube.Front(Rubik);
		}
		else if (move1 == 'FI') {
			RubiksCube.FrontInverse(Rubik);
		}
		else if (move1 == 'U') {
			RubiksCube.Up(Rubik);
		}
		else if (move1 == 'UI') {
			RubiksCube.UpInverse(Rubik);
		}
		else {
			cout << "Error: That is not an option\n";
		}

		
		
		RubiksCube.PrintCube(Rubik);
		cout << "Do you want to Quit? Y or N" << endl;  // quit option
		cin >> answer;

		answer = toupper(answer); 
		if (answer == 'Y')
			Quit = true;
	}



	

	system("Pause");
	return 0;
}

void Cube::FreshCube(char Array[6][9])  // This makes the fresh cube un-mixed, this is the main thingi used to test if all my move functions were working
{
	for (int i = 0; i < 6; i++)
		for (int j = 0; j < 9; j++)
			if (i == 0) {
				Array[i][j] = 'W';
			}
			else if (i == 1) {
				Array[i][j] = 'O';
			}
			else if (i == 2) {
				Array[i][j] = 'Y';
			}
			else if (i == 3) {
				Array[i][j] = 'R';
			}
			else if (i == 4) {
				Array[i][j] = 'B';
			}
			else if (i == 5) {
				Array[i][j] = 'G';
			}
}

void Cube::PrintCube(char Array[6][9]) //This just helps visualize the cube 
{
	for (int i = 0; i < 3; i++) {
		for (int j = 0; j < 9; j++)
			if (j == 0 || j == 3 || j == 6) {
				cout << "      " << Array[i][j];
			}
			else if (j == 2 || j == 5 || j == 8)
				cout << " " << Array[i][j] << endl;
			else
				cout << " " << Array[i][j];
	}
	cout << Array[4][0] << " " << Array[4][1] << " " << Array[4][2] << "|"
		<< Array[3][0] << " " << Array[3][1] << " " << Array[3][2] << "|"
		<< Array[5][0] << " " << Array[5][1] << " " << Array[5][2] << endl;
	cout << Array[4][3] << " " << Array[4][4] << " " << Array[4][5] << "|"
		<< Array[3][3] << " " << Array[3][4] << " " << Array[3][5] << "|"
		<< Array[5][3] << " " << Array[5][4] << " " << Array[5][5] << endl;
	cout << Array[4][6] << " " << Array[4][7] << " " << Array[4][8] << "|"
		<< Array[3][6] << " " << Array[3][7] << " " << Array[3][8] << "|"
		<< Array[5][6] << " " << Array[5][7] << " " << Array[5][8] << endl;

	cout << "--------------------------" << endl;
}

void Cube::inputCube(char Array[6][9]) // This isnt used but an option if u want to mess with the code, its very annoying to input all the values
{
	cout << "Input Center White side\n";
		for (int i = 0; i < 9; i++) {
			cin >> Array[0][i];
		}
		cout << "Input Center Orange side\n";
		for (int i = 0; i < 9; i++) {
			cin >> Array[1][i];
		}
		cout << "Input Center Yellow side\n";
		for (int i = 0; i < 9; i++) {
			cin >> Array[2][i];
		}
		cout << "Input Center Red side\n";
		for (int i = 0; i < 9; i++) {
			cin >> Array[3][i];
		}
		cout << "Input Center Blue side\n";
		for (int i = 0; i < 9; i++) {
			cin >> Array[4][i];
		}
		cout << "Input Center Green side\n";
		for (int i = 0; i < 9; i++) {
			cin >> Array[5][i];
		}
}

void Cube::RotateSide(char Array[6][9],int side)	// Everything Below is just function to move the cube, lots of swaps and For-Loops going on.
{
	char temp, temp1;
	temp = Array[side][0];
	temp1 = Array[side][1];
	swap(Array[side][3], Array[side][1]);
	swap(Array[side][6], Array[side][0]);
	swap(Array[side][7], Array[side][3]);
	swap(Array[side][8], Array[side][6]);
	swap(Array[side][5], Array[side][7]);
	swap(Array[side][2], Array[side][8]);
	swap(temp, Array[side][2]);
	swap(temp1, Array[side][5]);
}

void Cube::CounterRotateSide(char Array[6][9],int side)
{
	char temp, temp1;
	temp = Array[side][8];
	temp1 = Array[side][5];
	swap(Array[side][7], Array[side][5]);
	swap(Array[side][6], Array[side][8]);
	swap(Array[side][3], Array[side][7]);
	swap(Array[side][0], Array[side][6]);
	swap(Array[side][2], Array[side][0]);
	swap(Array[side][1], Array[side][3]);
	swap(temp, Array[side][2]);
	swap(temp1, Array[side][1]);
}

void Cube::Right(char Array[6][9])
{
	for (int i = 2; i < 9; i = i + 3) {
		swap(Array[0][i], Array[1][i]);
	}
	for (int i = 2; i < 9; i = i + 3) {
		swap(Array[1][i], Array[2][i]);
	}
	for (int i = 2; i < 9; i = i + 3) {
		swap(Array[2][i], Array[3][i]);
	}
	
	RotateSide(Array,5);
}

void Cube::RightInverse(char Array[6][9])
{
	for (int i = 2; i < 9; i=i+3) {
		swap(Array[0][i], Array[3][i]);
	}
	for (int i = 2; i < 9; i=i + 3) {
		swap(Array[3][i], Array[2][i]);
	}
	for (int i = 2; i < 9; i=i + 3) {
		swap(Array[2][i], Array[1][i]);
	}
	CounterRotateSide(Array,5);
	}

void Cube::Left(char Array[6][9])
{
	
	for (int i = 0; i < 7; i = i + 3) {
		swap(Array[0][i], Array[3][i]);
	}
	for (int i = 0; i < 7; i = i + 3) {
		swap(Array[3][i], Array[2][i]);
	}
	for (int i = 0; i < 7; i = i + 3) {
		swap(Array[2][i], Array[1][i]);
	}

	RotateSide(Array, 4);
}

void Cube::LeftInverse(char Array[6][9])
{
	
	for (int i = 0; i < 7; i = i + 3) {
		swap(Array[0][i], Array[1][i]);
	}
	for (int i = 0; i < 7; i = i + 3) {
		swap(Array[1][i], Array[2][i]);
	}
	for (int i = 0; i < 7; i = i + 3) {
		swap(Array[2][i], Array[3][i]);
	}
	CounterRotateSide(Array, 4);
}

void Cube::Up(char Array[6][9])
{
	for (int i = 0; i < 3; i++) {
		swap(Array[0][i], Array[5][i]);
	}
	for (int i = 0; i < 3; i++) {
		swap(Array[5][i], Array[2][i]);
	}
	for (int i = 0; i < 3; i++) {
		swap(Array[2][i], Array[4][i]);
	}
	RotateSide(Array, 3);
}
void Cube::UpInverse(char Array[6][9])
{
	for (int i = 0; i < 3; i++) {
		swap(Array[0][i], Array[4][i]);
	}
	for (int i = 0; i < 3; i++) {
		swap(Array[4][i], Array[2][i]);
	}
	for (int i = 0; i < 3; i++) {
		swap(Array[2][i], Array[5][i]);
	}
	CounterRotateSide(Array, 3);
}

void Cube::Down(char Array[6][9])
{
	for (int i = 6; i < 9; i++) {
		swap(Array[0][i], Array[4][i]);
	}
	for (int i = 6; i < 9; i++) {
		swap(Array[4][i], Array[2][i]);
	}
	for (int i = 6; i < 9; i++) {
		swap(Array[2][i], Array[5][i]);
	}
	RotateSide(Array, 1);
}
void Cube::DownInverse(char Array[6][9])
{
	for (int i = 6; i < 9; i++) {
		swap(Array[0][i], Array[5][i]);
	}
	for (int i = 6; i < 9; i++) {
		swap(Array[5][i], Array[2][i]);
	}
	for (int i = 6; i < 9; i++) {
		swap(Array[2][i], Array[4][i]);
	}
	CounterRotateSide(Array, 1);
}

void Cube::Front(char Array[6][9])
{
	RotateSide(Array, 0);
	for (int i = 6; i < 9; i++) {
		swap(Array[3][i],Array[4][i]);
	}
	for (int i = 6; i < 9; i++) {
		swap(Array[4][i], Array[1][i]);
	}
	for (int i = 6; i < 9; i++) {
		swap(Array[1][i], Array[5][i]);
	}
}

void Cube::FrontInverse(char Array[6][9])
{
	CounterRotateSide(Array, 0);
	for (int i = 6; i < 9; i++) {
		swap(Array[3][i], Array[5][i]);
	}
	for (int i = 6; i < 9; i++) {
		swap(Array[5][i], Array[1][i]);
	}
	for (int i = 6; i < 9; i++) {
		swap(Array[1][i], Array[4][i]);
	}
}

void Cube::BackInverse(char Array[6][9])
{
	CounterRotateSide(Array, 2);
	for (int i = 0; i < 3; i++) {
		swap(Array[3][i], Array[4][i]);
	}
	for (int i = 0; i < 3; i++) {
		swap(Array[4][i], Array[1][i]);
	}
	for (int i = 0; i < 3; i++) {
		swap(Array[1][i], Array[5][i]);
	}
}

void Cube::Back(char Array[6][9])
{
	RotateSide(Array, 2);
	for (int i = 0; i < 3; i++) {
		swap(Array[3][i], Array[5][i]);
	}
	for (int i = 0; i < 3; i++) {
		swap(Array[5][i], Array[1][i]);
	}
	for (int i = 0; i < 3; i++) {
		swap(Array[1][i], Array[4][i]);
	}

}
