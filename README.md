# GelismisHesapMakinesi
www.patika.dev
-----------------------


import java.util.Scanner;

public class GelismisHesapMakinesi {
	
	static int sum(int a,int b) {
		int result = a+b;
		System.out.println("Toplam: " + result);
		return result;
	}
	static int minus(int a,int b) {
		int result = a - b;
		System.out.println("Çıkarma: " +result);
		return result;
	}
	static int times(int a, int b) {
		int result = a * b;
		System.out.println("Çarpma: " + result);
		return result;
	}
	static int divided(int a, int b) {
		if(b==0) {
			System.out.println("İkinci sayi 0 olamaz ");
			return 0;
		}
		int result = a/b;
		System.out.println("Bölüm: " +result);
		return result;
	}
	static int power(int a, int b){
		int result =1;
		for(int i=1; i<=b; i++) {
			result *= a;
		}
		
		System.out.println("Üslü sayi: " +result);
		return result;
	}
	static int fak(int a) {
		int result = 1;
	    for (int i = 1; i <= a; i++) {
	        result *= i;
	    }
	    return result;
	}
	static int mod(int a,int b) {
		int result = a%b;
		System.out.println("Mod alma: " +result);
		return result;
	}
	static void calc(int a,int b) {
		System.out.println("Çevresi: " + (2*(a+b)));
		System.out.println("Alanı: " + (a*b) );
	}
	
	public static void main(String[] args) {
		
        Scanner scan = new Scanner(System.in);
        int select;
        String menu = "1- Toplama İşlemi\n"
                + "2- Çıkarma İşlemi\n"
                + "3- Çarpma İşlemi\n"
                + "4- Bölme işlemi\n"
                + "5- Üslü Sayı Hesaplama\n"
                + "6- Faktoriyel Hesaplama\n"
                + "7- Mod Alma\n"
                + "8- Dikdörtgen Alan ve Çevre Hesabı\n"
                + "0- Çıkış Yap";
        
        while(true) {
        	System.out.println(menu);
        	System.out.println("Bir işlem seçiniz: ");
        	select = scan.nextInt();
        	if(select==0) {
        		break;
        	}
        	if(select==6) {
        		System.out.println("Bir sayi giriniz");
        	}
        	if(select !=6) {
        		System.out.println("İki sayi giriniz");
        	}
        	if(select> 8) {
        		System.out.println("Geçersiz işlem girdiniz!");
        	}
        	
        	int a = scan.nextInt();
        	int b = scan.nextInt();	
        	switch(select) {
        	case 1:
        		sum(a,b);
        		break;
        	case 2:
        		minus(a,b);
        		break;
        	case 3:
        		times(a,b);
        		break;
        	case 4:
        		divided(a,b);
        		break;
        	case 5:
        		power(a,b);
        		break;
        	case 6:
        	    System.out.println("Faktöriyel: " + fak(a));
        	    break;
        	case 7:
        		mod(a,b);
        		break;
        	case 8:
        		calc(a,b);
        		break;
        	default:	
        		System.out.println("Geçersiz işlem girdiniz ");
        	}
        }
        System.out.println("Güle güle");
        	
        
        }
	}
