# Sistema de Celulares em C#

Este projeto consiste na implementação de um sistema de celulares em C# utilizando conceitos de orientação a objetos. O objetivo é criar uma abstração para diferentes marcas e modelos de celulares, permitindo um maior reuso de código e flexibilidade na adição de funcionalidades específicas.

## Classes

### `Smartphone` (Classe Abstrata)

- A classe abstrata `Smartphone` serve como modelo para celulares, contendo propriedades como `Marca` e `Modelo`.
- Métodos abstratos são definidos para ações comuns a todos os celulares, como `Ligar()`, `Desligar()`, `EnviarMensagem(string mensagem)`, `FazerChamada(string numero)`.

### `Nokia` e `Iphone` (Classes Derivadas de `Smartphone`)

- As classes `Nokia` e `Iphone` herdam da classe abstrata `Smartphone`.
- Cada uma dessas classes implementa os métodos abstratos de acordo com suas características específicas.

### `Reserva`

- A classe `Reserva` é responsável por modelar a reserva de suítes em um hotel.
- Utiliza a orientação a objetos para definir a relação entre hóspedes (`Pessoa`), suítes (`Suite`) e a reserva propriamente dita.

## Regras e Validações

- A classe `Smartphone` é abstrata, não permitindo instâncias diretas, servindo apenas como modelo.
- As classes `Nokia` e `Iphone` são classes filhas de `Smartphone`.
- O método `InstalarAplicativo` é sobrescrito nas classes `Nokia` e `Iphone`, já que ambos possuem maneiras diferentes de instalar um aplicativo.

## Como Utilizar

O programa contém um exemplo de utilização, criando instâncias de celulares Nokia e iPhone, realizando operações comuns, como ligar, enviar mensagens, fazer chamadas e instalar aplicativos.

```csharp
// Exemplo de criação de instância de Nokia
Nokia nokia = new Nokia
{
    Marca = "Nokia",
    Modelo = "3310"
};

// Exemplo de utilização dos métodos da classe Nokia
nokia.Ligar();
nokia.EnviarMensagem("Olá, como vai?");
nokia.FazerChamada("123456789");
nokia.InstalarAplicativo("WhatsApp");
nokia.Desligar();

// Exemplo de criação de instância de iPhone
Iphone iphone = new Iphone
{
    Marca = "Apple",
    Modelo = "iPhone 12"
};

// Exemplo de utilização dos métodos da classe iPhone
iphone.Ligar();
iphone.EnviarMensagem("Hello, how are you?");
iphone.FazerChamada("987654321");
iphone.InstalarAplicativo("Instagram");
iphone.Desligar();
