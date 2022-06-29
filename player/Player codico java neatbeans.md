### Player

package player;

public class Player {


    public static void main(String[] args) {
        Controles c1 = new Controles();
        
       c1.status(); // posicao inicial
       c1.power();
       c1.playPause();
       c1.stop();
       c1.next();
       c1.prev();
    
    }
    }

package player;

public class Controles implements Tela{
    private boolean ligado;
    private boolean tocando;
    private int musica;
    private String lista [];
//método construtor

    public Controles() {
        this.ligado = false;
        this.tocando = false;
        this.musica = 1;
    }
//métodos getter e setter
​    

    public String[] getLista() {
        return lista;
    }
    
    public void setLista(String[] lista) {
        this.lista = lista;
    }
    
    public boolean isLigado() {
        return ligado;
    }
    
    public void setLigado(boolean ligado) {
        this.ligado = ligado;
    }
    
    public boolean isTocando() {
        return tocando;
    }
    
    public void setTocando(boolean tocando) {
        this.tocando = tocando;
    }
    
    public int getMusica() {
        return musica;
    }
    
    public void setMusica(int musica) {
        this.musica = musica;
    }
//sobreposição de métodos
​    

    @Override
    public void power() {
        System.out.println("Apertando o Power:");
        if (this.ligado == false){
            this.setLigado (true);
            System.out.println("Player Ligado.");
        }else{
            this.setLigado (false);
            System.out.println("Player desligado.");
        }
    }
    
    @Override
    public void playPause() {
        System.out.println("Apertando Play/Pause:");
        if(this.ligado == false){
            System.out.println("Nada aconteceu." + "O player está desligado.");
        }else{
            if (this.tocando == false){
                this.setTocando(true);
                System.out.println("O player " + " está tocando a música " + this.getMusica());
            }else{
                this.setTocando (false);
                System.out.println("O player" + "está pausado.");
            }
        }
    }
    
    @Override
    public void stop() {
        System.out.println("Apertando Stop");
        if (this.ligado == false){
        System.out.println("Nada aconteceu " + "O player está desligado");
    }else{
        if (this.tocando == true){
            this.setTocando (false);
            System.out.println("Player Parado.");
            }else{
            System.out.println("O player já está parado.");
            }
        }
    }
    
    @Override
    public void next() {
        System.out.println("Apertando o botão de avançar:");
        if (this.ligado == false){
        System.out.println("Nada Aconteceu. " + "O player está desligado.");
    }else{
            this.setMusica (this.getMusica() + 1);
        System.out.println("O player está tocando " + "a música " + this.getMusica());
        }
    }
    
    @Override
    public void prev() {
        System.out.println("Apertando o botão Voltar ");
        if (this.ligado == false){
            System.out.println("Nada aconteceu " + "O player não retornou.");
        }else{
            this.setMusica (this.getMusica() - 1);
            System.out.println("O player volta " + " a música " + this.getMusica()
            );
        }
    }
//método próprio

    public void status (){
        //verifica se está ligado
        if (this.ligado == true){
            System.out.println("O player " + " está ligado");
        }else {
            System.out.println("O player" + "está desligado!");
        }
//verifica se está tocando

        if (this.tocando == true){
            System.out.println("O player " + " está tocando a música" + this.getMusica());
        }else{
    }
    }
    }
    

package player;

public interface Tela {
    public abstract void power();
    public abstract void playPause();
    public abstract void stop();
    public abstract void next();
    public abstract void prev();
    }
