# Practika
package practika2;

import javax.swing.*;
import java.util.Scanner;
import java.util.ArrayList;


public class Main {
    //public static int nip;
    public static void main(String [] args){

        Scanner in = new Scanner(System.in);


        System.out.println("Введите количество типов товара для заполнения:");
        int n = in.nextInt();

        //ArrayList<Product> tovar = new ArrayList<Product>();
        Product[] tovar = new Product [n];

        for(int i = 0; i < n; i++) {

            int col;
            col = i +1;
            System.out.println("Введите информацию о товаре № " + col + "\n");
            //tovar.add(i, tovar.get());
            tovar[i] = new Product();
            System.out.println("Наименование : ");
            tovar[i].vvod1(tovar[i].name);
            System.out.println("Цена : ");
            tovar[i].vvod2(tovar[i].cost);
            System.out.println("Информаци о товаре : ");
            tovar[i].vvod3(tovar[i].info);
            System.out.println("Наличие доставки : ");
            tovar[i].vvod4(tovar[i].delivery);
            System.out.println("\n");
        }

        int m;
        System.out.println("Введите количество заказчиков для заполнения:");
        m = in.nextInt();
        Client[] zakazchik = new Client [m];

        for(int i = 0; i < m; i++) {

            zakazchik[i] = new Client();
            int col;
            col = i+1;
            System.out.println("Введите информацию о товаре № " + col + "\n");
            System.out.println("Наименование компании : ");
            zakazchik[i].zapolnenie1(zakazchik[i].name);
            System.out.println("Адрес : ");
            zakazchik[i].zapolnenie2(zakazchik[i].address);
            System.out.println("Телефон : ");
            zakazchik[i].zapolnenie3(zakazchik[i].telephone);
            System.out.println("Контактное лицо : ");
            zakazchik[i].zapolnenie4(zakazchik[i].FIO);
            System.out.println("\n");
        }

        for(int i = 0; i < n; i++){

            int col = i+1;
            System.out.println("Товар №"+ col);
            System.out.println("\n");
            System.out.println("Наименование : " + tovar[i].name + "\n");
            System.out.println("Цена : " + tovar[i].cost + "\n");
            System.out.println("Информация о товаре : " + tovar[i].info + "\n");
            System.out.println("Наличие доставки : " + tovar[i].delivery + "\n");
        }

        for(int i = 0; i < m; i++){

            int col = i+1;
            System.out.println("Заказчик №"+ col);
            System.out.println("\n");
            System.out.println("Наименование компании : " + zakazchik[i].name + "\n");
            System.out.println("Адрес : " + zakazchik[i].address + "\n");
            System.out.println("Телефон : " + zakazchik[i].telephone + "\n");
            System.out.println("Контактное лицо : " + zakazchik[i].FIO + "\n");
        }
    }
}


package practika2;

import java.util.Scanner;

public class Client {

    Scanner in = new Scanner(System.in);

    public String name;
    public String address;
    public int telephone;
    public String FIO;

    Client(String name, String address, int telephone, String FIO) {
        this.name = name;
        this.address = address;
        this.telephone = telephone;
        this.FIO = FIO;
    }

    Client() {
        name = "Nothing";
        address = "Nothing";
        telephone = 00000000;
        FIO = "Nothing";
    }


    public void zapolnenie1(String name) {
        this.name = in.nextLine();
    }
    public void zapolnenie2(String address) {
        this.address = in.nextLine();
    }
    public void zapolnenie3(int telephone) {
        this.telephone = in.nextInt();
    }
    public void zapolnenie4(String FIO) {
        this.FIO = in.nextLine();
    }
}


package practika2;

import java.util.Scanner;

public class Product {

    Scanner in = new Scanner(System.in);

    public static String name;
    public static int cost;
    public static String info;
    public boolean delivery;

    Product(String n, int c, String i, boolean d) {

        this.name = n;
        this.cost = c;
        this.info = i;
        this.delivery = d;
    }

    Product() {

        name = "nothing";
        cost = 0;
        info = "nothing";
        delivery = false;
    }


    public void vvod1(String name) {
        this.name = in.nextLine();
    }

    public void vvod2(int cost) {
        this.cost = in.nextInt();
    }

    public void vvod3(String info) {
        this.info = in.nextLine();
    }

    public void vvod4(boolean delivery) {
        this.delivery = in.nextBoolean();
    }
}

