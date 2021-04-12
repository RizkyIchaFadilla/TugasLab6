# TugasLab6
package com.company;

public class Main
{

    public static void main(String[] args)
    {
	int JumlahMahasiswa = 8, JumlahJawaban = 10;
	char[][] jawabanMahasiswa = {
            {'A', 'B', 'A', 'C', 'C', 'D', 'E', 'E', 'A', 'D'}, {'D', 'B', 'A', 'B', 'C', 'A', 'E', 'E', 'A', 'D'},
            {'E', 'D', 'D', 'A', 'C', 'B', 'E', 'E', 'A', 'D'}, {'C', 'B', 'A', 'E', 'D', 'C', 'E', 'E', 'A', 'D'},
            {'A', 'B', 'D', 'C', 'C', 'D', 'E', 'E', 'A', 'D'}, {'B', 'B', 'E', 'C', 'C', 'D', 'E', 'E', 'A', 'D'},
            {'B', 'B', 'A', 'C', 'C', 'D', 'E', 'E', 'A', 'D'}, {'E', 'B', 'E', 'C', 'C', 'D', 'E', 'E', 'A', 'D'}
    };

	char[] kunciJawaban = {'D', 'B', 'D', 'C', 'C', 'D', 'A', 'E', 'A', 'D'};
	int[] result = new int[JumlahMahasiswa];

	for(int i=0; i<JumlahMahasiswa; i++)
    {
        int jawabanBenar = 0;
        for(int j=0; j<JumlahJawaban; j++)
        {
            if(jawabanMahasiswa[i][j] == kunciJawaban[j])
            {
                jawabanBenar++;
            }
        }
        result[i] = jawabanBenar;
    }

	    System.out.println("Hasil jawaban benar mahasiswa :");
	    for(int i=0; i<JumlahMahasiswa; ++i)
        {
            System.out.println("\nMahasiswa " + i + " Jumlah jawaban yang benar: " + result[i]);
        }
    }
}
