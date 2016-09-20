package pertemuan4;

import java.util.ArrayList;
import java.util.Scanner;

class Mahasiswa{
    String nama;
    double nilai;
    public Mahasiswa(String nama, double nilai){
        this.nama = nama;
        this.nilai = nilai;
    }
}

public class Pertemuan4 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        
        ArrayList<Mahasiswa> kelompok = new ArrayList<Mahasiswa>();
        int pilihan = 0;
        do{
            System.out.println("1. Push, 2. Pop, 3. View, 4. Quit");
            Scanner in = new Scanner(System.in);
            pilihan = in.nextInt();
            switch(pilihan){
                case 1: //push
                    System.out.print("Nama: ");
                    String nama = new Scanner(System.in).nextLine();
                    System.out.print("Nilai: ");
                    double nilai = in.nextDouble();
                    kelompok.add(new Mahasiswa(nama, nilai));
                    break;
                case 2: //pop
                    if(kelompok.size()>0){
                        Mahasiswa mhs = kelompok.get(0);
                        kelompok.remove(0);
                        System.out.println("Popped " +mhs.nama+" "+mhs.nilai);
                    }
                    break;
                case 3: //view
                    for(int i=0; i<kelompok.size(); i++){
                        Mahasiswa mhs = kelompok.get(i);
                        System.out.println(i+" "+mhs.nama+" "+mhs.nilai);
                    }
                    break;
            }
        }while(pilihan < 4);
    }


         }
      
