package practica1proceso;

import java.util.Scanner;

public class Practica1Proceso {
   
    public static void main(String[] args) {
        
       int matriza[][],matrizb[][],fil,col,x,y,matrizf[][];
       
      Scanner entrada = new Scanner(System.in);
      System.out.printf("ingrse numero de filas:");
      fil=entrada.nextInt();
      System.out.printf("ingrse numero de columnas:");
      col=entrada.nextInt();
      
      if(fil==col){
      matriza = new int [fil][col];
      
      System.out.println("digite los numeros de la primera  matriz ");//pedir la matriz a
      for(x=0;x<fil;x++){
           for(y=0;y<col;y++){
               System.out.print("["+x+"]["+y+"]=");
               matriza[x][y] = entrada.nextInt();
           }
      }
      
      matrizb = new int [fil][col];
      
      System.out.println("digite los numeros de la segunda  matriz ");//pedir la matriz b
      for(x=0;x<fil;x++){
           for(y=0;y<col;y++){
               System.out.print("["+x+"]["+y+"]=");
               matrizb[x][y] = entrada.nextInt();
           }
      }

      for(x=0;x<fil;x++){//imprimir la matriz a 
           for(y=0;y<col;y++){
               System.out.print(matriza[x][y]);
           }
           System.out.println("");  
           }
      
      System.out.println("*");//un espacio para que no se vean juntas 
      
      for(x=0;x<fil;x++){//imprimir la matriz b
           for(y=0;y<col;y++){
               System.out.print(matrizb[x][y]);
           }
           System.out.println("");
              
           }
      matrizf = new int [fil][col];
      for(x=0;x<fil;x++){//multtiplicacion de  las matrices
           for(y=0;y<col;y++){
               matrizf[x][y] = matriza[x][y] * matrizb[x][y];
           }
           System.out.println("");
              
           }
       System.out.println("el resulatdo es");//imprimir el resultado
        for(x=0;x<fil;x++){//imprimir el resultdo
           for(y=0;y<col;y++){
               System.out.print(matrizf[x][y]);
           }
           System.out.println("");
              
           }  
        
        
      }
      else{
           System.out.println("no se puede realizar la operacion");
      }
    }
    
}
