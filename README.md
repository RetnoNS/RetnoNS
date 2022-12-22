# Ujian Akhir Semester 
<br>Mata Kuliah 	: Dasar Pemrogrman
<br>Nama		: Retno Nissa Salsabillah
<br>NIM		: 1227050114	
<br>Jurusan		: [Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## Deskripsi Umum
Program  ini dibuat untuk memenuhi Ujian Akhir Semester Mata Kuliah Dasar Pemrograman.
Dibawah ini terdapat dua program. Didalam program ini terdapat fungsi array dan pengulangan for. 
Program yang pertama menginputkan nilai baris dan kolom lalu hasil nilai baris dan kolom ini dibalik dari kolom menjadi baris.
Program yang kedua untuk mencari nilai yang ddapat dibagi 3, 5, dan 7 dari hasil inputan untuk baris dan kolom.

## Source Code
```
#include <iostream>
using namespace std;

int main (){
	
	//Data Diri
	cout << " --------------------------------------"<<endl;
	cout << " Nama  : Retno Nissa Salsabillah"<<endl;
	cout << " NIM   : 1227050114"<<endl;
	cout << " Kelas : IF-C"<<endl;
	cout << " --------------------------------------"<<endl;
	
	//Soal 1 Input Jumlah baris dan kolom,kemudian dibalik.
	int brs, klm, input [25][25], muncul [25][25];
	
	cout <<endl;
	cout << " Jumlah Baris : ";
	cin >> brs;
	cout << " Jumlah Kolom : ";
	cin >> klm;
	
	//Pengulangan Input Nilai
	cout <<endl;
	cout << " Masukan Angka : "<<endl;
	for (int i=1; i<=brs; i++){
		for (int j=1; j<=klm; j++){
			cin >> input [i][j];
		}
	}
	
	for (int p=1; p<=brs; p++){
		for (int q=1; q<=klm; q++){
			muncul[q][p] = input[p][q];
		}
	}
	
	//Memunculkan Nilai Baris dan Kolom
	cout<<endl;
	cout << " Hasil Inputan Asli :"<<endl;
	for (int r=1; r<=klm; r++){
		for (int s=1; s<=brs; s++){
			cout <<" "<<muncul [r][s]<<"\t";
		}
		cout<<endl;
	}
	
	//Memunculkan Nilai Kebalikannya
	cout<<endl;
	cout << " Hasil Inputan Kebalikannya :"<<endl;
	for (int r=1; r<=brs; r++){
		for (int s=1; s<=klm; s++){
			cout <<" "<<muncul [s][r]<<"\t";
		}
		cout<<endl;
	}
	
	//Soal 2 Buat pada array 2 dimensi angka-angka yang habis dibagi 3,5,7
	cout<<endl;
	cout << " Angka Yang Habis Dibagi 3, 5, 7 adalah : "<<endl;
	for (int r=1; r<=brs; r++){
		for (int s=1; s<=klm; s++){
			if (muncul [s][r] %3 == 0 && muncul [s][r] %5 == 0 && muncul [s][r] %7 == 0) {
				cout <<"habis dibagi 3, 5 dan 7 : " << muncul[s][r]<<" " << endl;
			}
			else if (muncul [s][r] %5 == 0 && muncul [s][r] %7 == 0){
				cout <<"habis dibagi 5 dan 7 : " << muncul[s][r]<<" " << endl;
			}  
			else if (muncul [s][r] %7 == 0){
				cout <<"habis dibagi 7 : " << muncul[s][r]<<" " << endl;
			}
		}
	}
}
```
## Output
	
<br> --------------------------------------
 <br>Nama  : Retno Nissa Salsabillah
 <br>NIM   : 1227050114
 <br>Kelas : IF-C
 <br>--------------------------------------

 <br> Baris : 2
 <br>Jumlah Kolom : 2

 <br>Masukan Angka :	
<br>105	
<br>35	
<br>7
<br>420
	
 <br>Hasil Inputan Asli :
<br>105  		7
 <br>35     		420

 <br>Hasil Inputan Kebalikannya :
 <br>105     		35
 <br>7       		420
	
 <br>Angka Yang Habis Dibagi 3, 5, 7 adalah :
<br>habis dibagi 3, 5 dan 7 : 105
<br>habis dibagi 5 dan 7 : 35
<br>habis dibagi 7 : 7
<br>habis dibagi 3, 5 dan 7 : 420
