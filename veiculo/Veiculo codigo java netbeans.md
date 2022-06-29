### Veículo

package veiculo;

public class Veiculo {

    public static void main(String[] args) {
    Carro c1 = new Carro ("Ford", "Celta", 4, "verde", 100);
        
        System.out.println("=== veículos ===");
        System.out.println("Marca: " + c1.getMarca());
        System.out.println("Modelo: " + c1.getModelo());
        System.out.println("Portas: " + c1.getPortas()); 
        System.out.println("Cor: " + c1.getCor());
        System.out.println("Velocidade: " + c1.getVelocidade());
    }
    }

package veiculo;

public class Carro { 

    private String marca;
    private String modelo;
    private int portas;
    private String cor;
    private int velocidade;
    
    public Carro(String marca, String modelo, int portas, String cor, int velocidade) {
        this.marca = marca;
        this.modelo = modelo;
        this.portas = portas;
        this.cor = cor;
        this.velocidade = velocidade;
    }


    public String getMarca() {
        return marca;
    }
    
    public void setMarca(String marca) {
        this.marca = marca;
    }
    
    public String getModelo() {
        return modelo;
    }
    
    public void setModelo(String modelo) {
        this.modelo = modelo;
    }
    
    public int getPortas() {
        return portas;
    }
    
    public void setPortas(int portas) {
        this.portas = portas;
    }
    
    public String getCor() {
        return cor;
    }
    
    public void setCor(String cor) {
        this.cor = cor;
    }
      
    public int getVelocidade() {
        return velocidade;
    }
    
    public void setVelocidade(int velocidade) {
        this.velocidade = (int) velocidade;
    }
    }

