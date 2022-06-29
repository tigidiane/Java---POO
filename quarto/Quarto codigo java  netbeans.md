### Quarto 

package quarto;


public class Quarto {

    public static void main(String[] args) {
        Porta p1 = new Porta();
        p1.cor = "branca";
        p1.altura = 1.88f;
        p1.largura = 90;
        p1.posicao = "fechada";
        p1.fechadura = "destrancada";
        p1.status();
        
        p1.fecharPorta();
        
        p1.status();
        
        Cama c1 = new Cama();
        c1.tipo = "Box";
        c1.colchao = "Molas ensacadas";
        c1.cumprimento = 1.88f;
        c1.largura = 1.38f;
        c1.pillowtop = true;
        
        c1.status();
    }
    }

package quarto;

public class Cama {

       String tipo;
       String colchao;
       float largura;
       float cumprimento;
       boolean pillowtop;
       void status(){
       
       System.out.println("Cama");
       System.out.println("Tipo: " + this.tipo);
       System.out.println("Colchão " + this.colchao);
       System.out.println("Largura " + this.largura);
       System.out.println("Cumprimento " + this.cumprimento);
       
       if (this.pillowtop == true){
           System.out.println("Com Pillowtop");
       }else {
           System.out.println("Sem Pillowtop");
       }
       
       } 
       
       }
package quarto;

public class Porta { 

    String cor;
    int largura;
    float altura;
    String posicao;
    String fechadura;
//método status

    void status (){
        System.out.println("Porta do Quarto");
        System.out.println("Cor: " + this.cor);
        System.out.println("Altura: " + this.altura);
        System.out.println("Posição: " + this.posicao);
        System.out.println("Fechadura " + this.fechadura);
    }
​    //método abrir porta

       void abrirPorta(){ if("aberta".equals(this.posicao)){
            System.out.println("Impossível abrir a porta. Ela já está " 
                    + this.posicao + ".");
        }else if ("trancada".equals(this.fechadura)){
            System.out.println("Impossível abrir uma porta " 
                    + this.fechadura + ". Primeiro devemos destrancá-la.");
        }else {
            this.posicao = "aberta";
            System.out.println("Abrindo a porta...");
            System.out.println("Ok, porta " + this.posicao + ".");
        }
    }
​    //método fechar porta

        void fecharPorta(){
        if ("fechada".equals (this.posicao)){
            System.out.println("Impossível fechar a porta. Ela já está " 
                    + this.posicao + ".");
        }else {
            this.posicao = "fechada";
            System.out.println("Fechando a porta... ");
            System.out.println("Ok! A porta " + this.posicao + ".");
        }
    }
​    //método trancar a porta

        void trancarPorta(){
        if ("aberta".equals(this.posicao)){
            System.out.println("Impossível trancar uma porta " + this.posicao + "É necessário fechá-la");
        }else if("trancada".equals(this.fechadura)){
            System.out.println("Impossível trancar a porta " + "Ela já está " + this.fechadura);
        }else {
            this.fechadura = "trancada";
            System.out.println("Trancando a porta...");
            System.out.println("OK, a porta " + this.fechadura + ".");
        }
    }
​    //método destrancar Porta

        void destrancarPorta(){
        if ("aberta".equals(this.posicao)){
            System.out.println("Impossível trancar uma porta " + this.posicao + "É necessário fechá-la.");
        }else if("destrancada".equals (this.posicao)){
            System.out.println("Impossível destrancar a porta " + "Ela já está " + this.fechadura);
        }else {
            this.fechadura = "destrancada";
            System.out.println("Destrancando a porta...");
            System.out.println("Ok, porta " + this.fechadura + ".");
        }
        }
        }


​        