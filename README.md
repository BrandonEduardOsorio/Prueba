import java.util.*;

public class Automóvil {
    String marca;
    int modelo;
    int motor;

    enum TipoCombustible {
        GASOLINA, BIOETANOL, DIESEL, BIODISESEL, GAS_NATURAL
    }

    TipoCombustible tipoCombustible;

    enum TipoAutomóvil {
        CIUDAD, SUBCOMPACTO, COMPACTO, FAMILIAR, EJECUTIVO, SUV
    }

    TipoAutomóvil tipoAutomóvil;

    int númeroPuertas;
    int cantidadAsientos;
    int velocidadMáxima;

    enum TipoColor {
        BLANCO, NEGRO, ROJO, NARANJA, AMARILLO, VERDE, AZUL, VIOLETA
    }

    TipoColor color;
    int velocidadActual = 0;

    Automóvil(String marca, int modelo, int motor, TipoCombustible tipoCombustible, TipoAutomóvil tipoAutomóvil, int númeroPuertas, int cantidadAsientos, int velocidadMáxima, TipoColor color) {
        this.marca = marca;
        this.modelo = modelo;
        this.motor = motor;
        this.tipoCombustible = tipoCombustible;
        this.tipoAutomóvil = tipoAutomóvil;
        this.númeroPuertas = númeroPuertas;
        this.cantidadAsientos = cantidadAsientos;
        this.velocidadMáxima = velocidadMáxima;
        this.color = color;
    }

    // ... (resto de métodos)

    public static void main(String args[]) {
        try (Scanner scanner = new Scanner(System.in)) {
            System.out.print("Ingrese la marca del automóvil: ");
            String marca = scanner.nextLine(); // Leemos la marca del automóvil
            
            // Resto de entradas del usuario
            // ...
            
            Automóvil auto1 = new Automóvil(marca, 2018, 3, TipoCombustible.DIESEL, TipoAutomóvil.EJECUTIVO, 5, 6, 250, TipoColor.NEGRO);
            auto1.imprimir();
            auto1.setVelocidadActual(100);
            System.out.println("Velocidad actual = " + auto1.getVelocidadActual()); // Usamos el método getVelocidadActual()
            auto1.acelerar(20);
            System.out.println("Velocidad actual = " + auto1.getVelocidadActual());
            auto1.desacelerar(50);
            System.out.println("Velocidad actual = " + auto1.getVelocidadActual());
            auto1.frenar();
            System.out.println("Velocidad actual = " + auto1.getVelocidadActual());
            auto1.desacelerar(20);
        }
    }

    private void frenar() {
    }

    private void desacelerar(int i) {
    }

    private void acelerar(int i) {
    }

    private String getVelocidadActual() {
        return null;
    }

    private void setVelocidadActual(int i) {
    }

    private void imprimir() {
    }
}

