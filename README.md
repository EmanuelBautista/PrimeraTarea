# PrimeraTarea
Aqui se encuentra mi primer proyecto

package figurasgeometricas;

abstract class Figura {
    public abstract double calcularArea();
}

class Cuadrado extends Figura {
    private double lado;
    
    public Cuadrado(double lado) {
        this.lado = lado;
    }
    
    @Override
    public double calcularArea() {
        return lado * lado;
    }
}

class Circulo extends Figura {
    private double radio;
    
    public Circulo(double radio) {
        this.radio = radio;
    }
    
    @Override
    public double calcularArea() {
        return Math.PI * radio * radio;
    }
}

public class FigurasGeometricas{
    public static void main(String[] args) {
        Figura cuadrado = new Cuadrado(5.0);
        Figura circulo = new Circulo(3.0);
        
        System.out.println("Área del cuadrado: " + cuadrado.calcularArea());
        System.out.println("Área del círculo: " + circulo.calcularArea());
    }
}
