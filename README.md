package com.byaj;



import java.util.Arrays;
import java.util.ArrayList;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> products = new ArrayList<String>();
        ArrayList<Double> prices = new ArrayList<Double>();
        ArrayList<String> purchases = new ArrayList<String>();
        ArrayList<Double> purchaseprices = new ArrayList<Double>();
        products.add("Bison Sweater");
        prices.add(55.99);
        products.add("Bison Tee");
        prices.add(14.99);
        products.add("Bison Hoodie");
        prices.add(23.99);
        products.add("Bison Bumpersticker");
        prices.add(4.99);

        String decision;
        Scanner input = new Scanner(System.in);
        String item;
        double sum = 0.0;
        int index = -1;
        do {
            System.out.println("What item did you buy? if you did not buy anything enter no:  ");
            item = input.nextLine();
            purchases.add(item);
            for (int i = 0; i < products.size(); i++) {
                if (item.equals(products.get(i))) {
                    index = i;
                }
            }
            purchaseprices.add(prices.get(index));
        } while (!item.equalsIgnoreCase("no"));


        for (int i = 0; i < purchases.size() - 1; i++) {
            System.out.println("Items that I purchased: " + purchases.get(i));
            sum += purchaseprices.get(i);
        }

        System.out.println("Total Spent: " + sum);

    }

}
