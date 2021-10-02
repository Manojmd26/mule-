	#include<fstream.h>
	#include<conio.h>
	#include<dos.h>
	
	void main( )
	{		
	 char filename[20] , data[80];
	 clrscr();

	 cout << "Enter filename" << endl;
	 cin >> filename;

	 ifstream fp ( filename );
	 if( fp.fail( ))
	 cout << "Sorry file not found/Invalid path" << endl;
	 else
	 {
		do
		{	
		 fp.getline( data , 80 );
		 cout << data << endl;
		 delay(100);
		}
		while( ! fp.eof() );
		fp.close();
	}

	}
			 
		 

	
	
	
