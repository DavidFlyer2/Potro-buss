package potrobus;
import java.util.Scanner;
public class Potrobus {

    public static void main(String[] args) {
     Scanner entrada= new Scanner(System.in);
       datosRuta obj1 = new datosRuta();
       cosasOlvidadas obj2 = new cosasOlvidadas();
       tiempoLlegada obj3= new tiempoLlegada();
       int op;
       do{
       System.out.println("seleccione opcion a realizar");
        System.out.println("1=ver datos de la ruta");
         System.out.println("2= mostras objetos olvidados ");
          System.out.println("3=ver tiempo de llegada");
        int opc = entrada.nextInt();
       
       switch(opc){
           
           case 1:
             obj1.verDatos();
             break;
           case 2:   
            obj2.mostrarObjetosOlvidados();
           break;
           case 3:
               obj3.verTiempo();
               break;
       }
       System.out.println("regresar al menu oprima 1");
        op = entrada.nextInt();
         
       }while(op!=0);     
        
    }
    
}
