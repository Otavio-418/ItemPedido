public class Produto {
    // Variável final: uma vez definida no construtor, não muda.
    private final String nome;

    public Produto(String nome) {
        this.nome = nome;
    }

    // Método final: impede que subclasses alterem a lógica de cálculo
    public final double calcularPrecoVenda(double markup, double precoCompra) {
        // Seguindo a fórmula solicitada: (markup * preco * compra)
        // Nota: Geralmente markup é um multiplicador sobre o custo.
        return markup * precoCompra;
    }

    public String getNome() {
        return nome;
    }
}
