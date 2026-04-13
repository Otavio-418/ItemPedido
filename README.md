# ItemPedido
<?php
declare(strict_types=1);

final class ItemPedido {

    private Produto $produto;
    private int $quantidade;

    public function __construct(Produto $produto, int $quantidade) {
        $this->produto = $produto;
        $this->quantidade = $quantidade;
    }

    public function setProduto(Produto $produto): void {
        $this->produto = $produto;
    }

    public function getProduto(): Produto {
        return $this->produto;
    }

    public function setQuantidade(int $quantidade): void {
        $this->quantidade = $quantidade;
    }

    public function getQuantidade(): int {
        return $this->quantidade;
    }

    // Calcula o valor total do item
    public function getSubtotal(): float {
        return $this->produto->getPreco() * $this->quantidade;
    }
}