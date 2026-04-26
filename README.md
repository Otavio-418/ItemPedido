<?php

class Produto {
    // No PHP 8.1+, usamos readonly para simular uma variável final (imutável)
    public readonly string $nome;

    public function __construct(string $nome) {
        $this->nome = $nome;
    }

    // Método final: subclasses não podem sobrescrever esta lógica
    public final function calcularPrecoVenda(float $markup, float $precoCompra): float {
        return $markup * $precoCompra;
    }
}