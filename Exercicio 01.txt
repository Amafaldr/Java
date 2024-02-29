public class Aluno {

    private String nome;
    private int ra;
    private int faltas;

    public Aluno(String nome, int ra) {
        this.nome = nome;
        this.ra = ra;
        this.faltas = 0;
    }

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public int getRa() {
        return ra;
    }

    public void setRa(int ra) {
        this.ra = ra;
    }

    public int getFaltas() {
        return faltas;
    }

    public void registrarFalta() {
        faltas++;
    }

    @Override
    public String toString() {
        return "Aluno{" +
                "nome='" + nome + '\'' +
                ", ra=" + ra +
                ", faltas=" + faltas +
                '}';
    }
}

public class Main {

    public static void main(String[] args) {
        Aluno aluno = new Aluno("João Silva", 123456);

        System.out.println("Aluno antes de registrar falta: " + aluno);

        aluno.registrarFalta();

        System.out.println("Aluno depois de registrar falta: " + aluno);
    }
}
