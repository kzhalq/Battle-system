#include<iostream>//library
using namespace std;

void BattleSystem();
int MonsterGen();
int PlayerHealth = 50; //global variable

int main() {// starting pont of program
	int room = 1;
	char input = 'a';
	
	while (PlayerHealth >= 0 && input != 'q') { //game loop
		switch (room) {
		case 1:
			cout << "you're in room 1, you can go (s)outh" << endl;
			cin >> input;
			if (input == 's')
				room = 2;
			break;
		case 2:
			cout << "you're in room 2, you can go (n)orth" << endl;
			cin >> input;
			if (input == 'n')
				room = 1;
			else if (input == 'a')
				BattleSystem();
			    if (PlayerHealth <=0)
				break;
			break;
		}
	}
	if (PlayerHealth <= 0)
		cout << "GAME OVER!" << endl;
}

int MonsterGen() {
	int num = rand() % 100;
	if (num < 50) {
		cout << "a skeleton spawened!" << endl;
		return 1;
	}
	else {
		cout << "a spider appears and attacks!" << endl;
		return 2;
	}
}

void BattleSystem() {
	int MonsterType = MonsterGen();
	int MonsterHealth = 0; // default value, will be rewritten
	int MonsterAtk = 0;

	if (MonsterType == 1) //skeleton
		MonsterHealth = 40;
	else if (MonsterType == 2) { // spider
		MonsterHealth = 20;
	}

	while (MonsterHealth > 0 && PlayerHealth > 0) { // battle loop
		if (MonsterType == 1)
			MonsterAtk = rand() % 25; // can hit from 0-24
		else if (MonsterType == 2)
			MonsterAtk = rand() % 10 + 5; // can hit from 5 to 14
		cout << "the monster attacks you for " << MonsterAtk << "dmg!" << endl;

		PlayerHealth -= MonsterAtk;
		PlayerAtk = rand() % 11 + 20; //player hits for 20-30 dmg
		cout << "you attack the mosnter for " << PlayerAtk << "dmg!" << endl;
		cout << "the moster attacks you for 10 dmg!" << endl;
		PlayerHealth -= 10;
		cout << "you attack the monster for 10 dmg!" << endl;
		MonsterHealth= 10;
		system("pause");
		cout << "Your health is now " << PlayerHealth << ", and the moster's health is " << MonsterHealth << endl;

	}
}
