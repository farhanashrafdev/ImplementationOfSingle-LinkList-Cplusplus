/*
Write C++ program to give implementation of singly linked list and should have the following
functionality.
-InsertFirst ( ? )
-InsertLast ( ? )
-InsertSpecific ( ? )
-DisplayList ( ? )
-DisplaySize ( ? )
-DeleteFirst ( ? )
-DeleteLast ( ? )
-DeleteSpecific( ? )
*/

#include<iostream>
#include<string>
using namespace std;
struct List {
	int data; List* next;
};
List* head = NULL;
List* tail = NULL;
int count = 0, listnumber = 0;
void InsertFirst();
void InsertLast();
int InsertSpecific();
void DisplayList();
void DisplaySize();
void DeleteFirst();
void DeleteLast();
void DeleteSpecific();
int main() {
	int choice = 0; bool in, run = true; int tterminate = 0;
	do {
		do {
			system("cls");
			cout << "Please Select any of the followings: " << endl;
			cout << "1 for Insert at First " << endl;
			cout << "2 for Insert at Last " << endl;
			cout << "3 for Insert at Specific " << endl;
			cout << "4 for Display  List " << endl;
			cout << "5 for Display Size " << endl;
			cout << "6 for Delete First(" << endl;
			cout << "7 for Delete Last " << endl;
			cout << "8 for Delete Specific " << endl;
			cin >> choice;
			if (choice < 1 || choice>8)
			{
				cout << " invalid choice enter again";
				in = true;
			}
			else in = false;
			system("cls");
		} while (in);

		switch (choice)
		{
		case 1:	 InsertFirst(); break;
		case 2:  InsertLast(); break;
		case 3:  InsertSpecific(); break;
		case 4:   DisplayList(); break;
		case 5:	  DisplaySize();	break;
		case 6:  DeleteFirst(); break;
		case 7:  DeleteLast(); break;
		case 8:  DeleteSpecific() ; break;
		}


		cout << endl;
		cout << "Do you want to perform another function?: (Enter 0 for yes)(any number for not): "; cin >> tterminate;
		if (tterminate == 0)
			run = true;
		else run = false;




	} while (run);
	return 0;
}
void InsertFirst() {


	if (head == NULL)
	{
		List* temp = new List;
		cout << "Enter the data: "; cin >> temp->data; temp->next = NULL;
		head = temp;
		tail = temp;
		cout << "Value is Entered Sucessfully ";
		listnumber++;
	}
	else if (head != NULL) {
		List* temp = new List;
		cout << "Enter the data: "; cin >> temp->data;
		temp->next = head;
		head = temp;
		cout << "Value is entered sucessfuly ";
		listnumber++;
	}


}
void InsertLast() {

	if (tail == NULL)
	{
		List* temp = new List;
		cout << "Enter the data: "; cin >> temp->data; temp->next = NULL;
		tail = temp;
		head = temp;
		cout << "List is inserted Sucessfully " << endl;
		listnumber++;
	}
	else if (tail != NULL) {
		List* temp = new List;
		tail->next = temp;
		tail = temp;
		cout << "Enter value: "; cin >> tail->data;
		tail->next = NULL;
		cout << "Value is inserted sucessfuly " << endl;
		listnumber++;
	}
}
int InsertSpecific() {
	int n = listnumber;
	cout << "the total number of lists are:  " << listnumber << endl;
	do {
		cout << "Enter after which list you want to insert the list: "; cin >> n;
		if (n > listnumber) { cout << "please select the correct value max is: " << listnumber; system("cls"); }
	} while (n > listnumber);

	List* temp = new List;
	int count;
	temp = head;
	count = 1;
	for (int i = 1; i < n-1; i++)
	{

		temp = temp->next;
		count = i;
	}
	List* temp1 = new List;
	temp1->next = temp->next;//3rd
	cout << "Enter value to inserted at " << count + 1 << endl;
	cin >> temp1->data;
	temp->next = temp1;
	listnumber++;

	return 0;
}
void DisplayList() {
	if (head == NULL && listnumber == 0) cout << "Linklist is empty: ";
	List* temp = new List;
	temp = head;
	for (int i = 1; i <= listnumber; i++)
	{
		cout << "The value of List " << i << " is: " << temp->data << endl;
		temp = temp->next;
	}
	temp = NULL;
	delete temp;

}
void DisplaySize() {
	cout << "The total number of lists are: " << listnumber << endl;

}
void DeleteFirst() {
	if (head == NULL && listnumber == 0) cout << "Linklist is empty: ";
	List* temp = new List;
	temp = head;
	head = head->next;
	temp->next = NULL;
	temp->data = 0;
	delete temp;
	listnumber--;
}
void DeleteLast() {
	if (head == NULL&&listnumber==0) cout << "Linklist is empty: ";
	List* temp = new List;
	temp = head;
	for (int i = 1; i < listnumber; i++)
	{
		temp = temp->next;
	}
	if (temp->next == NULL)
		delete temp;
	else cout << "Wronge node it was....";
	cout << "total number of nodes are: " << listnumber << endl;
listnumber--;
cout << "Deleted the last one now the total nodes are " << listnumber << endl;

}
void DeleteSpecific() {
	if (head == NULL && listnumber == 0) cout << "Linklist is empty: ";

	List* temp = new List; int n;
	temp = head; List* tempr;
	cout << "The total number of nodes are:" << listnumber << endl;
	do {
		cout << "Enter which not you want to delete: "; cin >> n;
		if (n > listnumber || n < 0)cout << "Please enter correct node max are " << listnumber << endl;
	} while (n > listnumber || n < 0);
	for (int i = 1; i < n - 1; i++)
		temp = temp->next;

	tempr=temp->next;
	temp->next = temp->next->next;
	delete tempr;
	listnumber--;
}
