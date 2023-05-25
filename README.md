# Cigarrera
exa Final
Model
package cigarro;



        
    public class Cigarro {
    private final int cantidadHojas;
    private final int tiempoPicado;
    private final int aroma;
    private final int azucar;
    private final int nicotina;

    public Cigarro(int cantidadHojas, int tiempoPicado, int aroma, int azucar, int nicotina) {
        this.cantidadHojas = cantidadHojas;
        this.tiempoPicado = tiempoPicado;
        this.aroma = aroma;
        this.azucar = azucar;
        this.nicotina = nicotina;
    }

    public void realizarPicado() {
        System.out.println("Arrancando la máquina");
        for (int i = 0; i < tiempoPicado; i++) {
            System.out.println("Picado y desvenado " + i);
        }
    }

    public int obtenerCantidadCigarrillos() {
        return cantidadHojas + aroma + azucar + nicotina;
    }

    public int obtenerTotalCajetillas() {
        int totalCigarrillos = obtenerCantidadCigarrillos();
        int cajetillas;
        int cigarrillosExcedentes;

        if (totalCigarrillos % 2 == 0) {
            cajetillas = totalCigarrillos / 14;
            cigarrillosExcedentes = totalCigarrillos % 14;
        } else {
            cajetillas = totalCigarrillos / 20;
            cigarrillosExcedentes = totalCigarrillos % 20;
        }

        System.out.println("Total de cajetillas: " + cajetillas);
        System.out.println("Cigarrillos excedentes: " + cigarrillosExcedentes);

        return cajetillas;
    }

    public static void main(String[] args) {
      
        Cigarro calculator = new Cigarro(95, 14, 6, 22, 5);

        
        System.out.println("Cantidad de hojas: " + calculator.cantidadHojas);
        System.out.println("Tiempo de picado: " + calculator.tiempoPicado);
        System.out.println("Aroma: " + calculator.aroma);
        System.out.println("Azúcar: " + calculator.azucar);
        System.out.println("Nicotina: " + calculator.nicotina);

        // Realizar el picado de las hojas
        calculator.realizarPicado();

        // Obtener la cantidad de cigarrillos
        int cantidadCigarrillos = calculator.obtenerCantidadCigarrillos();
        System.out.println("Cantidad de cigarrillos: " + cantidadCigarrillos);

        // Obtener el total de cajetillas y cigarrillos excedentes
        int totalCajetillas = calculator.obtenerTotalCajetillas();
    }
}

Model
metodo
package Models;

import java.util.logging.Logger;


public class Principal {

   String cantidadHojas;
   String tiempoPicado;
   String aroma;
   String azucar;
   String nicotina;

    public Principal() {
    }

    public Principal(String cantidadHojas, String tiempoPicado, String aroma, String azucar, String nicotina) {
        this.cantidadHojas = cantidadHojas;
        this.tiempoPicado = tiempoPicado;
        this.aroma = aroma;
        this.azucar = azucar;
        this.nicotina = nicotina;
    }
    private static final Logger LOG = Logger.getLogger(Principal.class.getName());

    public void setCantidadHojas(String cantidadHojas) {
        this.cantidadHojas = cantidadHojas;
    }

    public void setTiempoPicado(String tiempoPicado) {
        this.tiempoPicado = tiempoPicado;
    }

    public void setAroma(String aroma) {
        this.aroma = aroma;
    }

    public void setAzucar(String azucar) {
        this.azucar = azucar;
    }

    public void setNicotina(String nicotina) {
        this.nicotina = nicotina;
    }

    @Override
    public String toString() {
        return "Principal{" + "cantidadHojas=" + cantidadHojas + ", tiempoPicado=" + tiempoPicado + ", aroma=" + aroma + ", azucar=" + azucar + ", nicotina=" + nicotina + '}';
    }
   
    }
