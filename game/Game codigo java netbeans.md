##Game (código java - netbeans) 


Package jogoluta;

import java.util.Random;

public class Player implements Controles {
    private int energia;
    private String acerto;
    private int dano;
    Random random;
//construtor

    public Player() {
        this.energia = 100; //personagem com 100% de energia
        this.random = new Random();
    }
//getter e setter 

    public int getEnergia() {
        return energia;
    }
    
    public void setEnergia(int energia) {
        this.energia = energia;
    }
    
    public String getAcerto() {
        return acerto;
    }
    
    public void setAcerto(String acerto) {
        this.acerto = acerto;
    }
    
    public int getDano() {
        return dano;
    }
    
    public void setDano(int dano) {
        this.dano = dano;
    }

  //criar métodos

    @Override
    public void chute() {
        int chute = random.nextInt(10)+1;
        if (chute <= 3){
            this.setAcerto("Errou!");
            this.setDano(0);
        }else{
            this.setAcerto("Acertou!");
            this.setDano(random.nextInt(17)+8);
        }
    }
    
    @Override
    public void soco() {
        int soco = random.nextInt(10)+1;
        if (soco <= 3){
            this.setAcerto("Errou!");
            this.setDano(0);
        }else{
            this.setAcerto("Acertou!");
            this.setDano(random.nextInt(10)+1);
        }
    }
    
    @Override
    public void chute(int x) {
        int chute = random.nextInt(10)+1;
        if (chute <= 6){
            this.setAcerto("Errou!");
            this.setDano(0);
        }else{
            this.setAcerto("Acertou!");
            this.setDano(x / 2);
        }
    }
    
    @Override
    public void soco(int x) {
        int soco = random.nextInt(10)+1;
        if (soco <= 6){
            this.setAcerto("Errou!");
            this.setDano(0);
        }else{
            this.setAcerto("Acertou!");
            this.setDano(x / 3);
        }
    }
    }

   


package jogoluta;

public interface Controles {
    public abstract void chute();
    public abstract void chute(int x);
    public abstract void soco();
    public abstract void soco(int x);

}