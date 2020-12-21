# Overloading_Template_Functions
Program that displays Overloading Template Functions that swap variables and Arrays


     #include <iostream>
     #include <string>
     using std::cout;
     using std::endl;
     using std::string;





    template <typename T>
    void swap(T &a, T &b)		//Function that Swaps the ints and strings from main
    {
    	T temporaryVar = a;
		a = b;
		b = temporaryVar;
	
		cout << "a: " << a << "\tb:" << b << "\n";
    }


    template <typename T>
    
    
    void swap(T a[], T b[], int size)		//Function that Swaps Arrays from main
    {
    	for (int i = 0; i < size; i++)
		{
			T temporaryVar = a[i];
			a[i] = b[i];
			b[i] = temporaryVar;
		}
    }


    int main()
    {
		int a = 15;
		int b = 25;

		string first = "Rat";
		string second = "Taco";

		swap (a, b);		//Swap ints
		swap (first, second);	//Swap strings
		cout << "\na: " << a << "\tb:" << b << "\n";		//cout ints after swap
		cout << "\na: " << first << "\tb: " << second << endl;	//cout strings after swap
	
	
		//Swapping Arrays
	
		int nines[] = {9,9,9,99};
		int ones[] = {1,1,1,11};
		const int SIZE = 4;
	
		
		for (int i = 0; i < SIZE; i++)		//couts arrays before swap
		{
			cout << nines[i] << "\t" << ones[i] << "\t";
		}
		cout << endl;
		
		swap(nines, ones, SIZE);
		
	
		
		for (int i = 0; i < SIZE; i++)		//couts Arrays after swap
		{
			cout << nines[i] << "\t" << ones[i] << "\t";
		}
		cout << endl;
	 
      return 0;

    }
