# (Apunte) Curso de Ethereum para Developers

## Capitulo 1: ¿Qué es Ethereum?

### ¿Qué es Ehereum?
Ethereum es una plataforma para ejecutar contratos inteligentes (smart contracts) a través de una Máquina Virutal que aplica los cambios al sistema. Ethereum es una "Open Blockchain" que utiliza una cadena de bloques para sincronizar y guardar los cambios que ocurren al estado del sistema, y utiliza una criptomoneda llamada Ether (ETC) para medir y restringir los costos de Ejecución

* Es una plataforma para ejecutar contratos inteligentes a través de una maquina virtual (Ethereum Virtual Machine - EVM)
* Utiliza una cadena de bloques para sincronizar y guardar los cambios en el sistema
* Utiliza una criptomoneda (Ether - ETH) para gestionar los costos de transacción dentro del ecosistema
* En la ruta de desarrollo de Ethereum podemos encontrar 4 etapas:
    * Frontier (2015)
    * Homestead (2016)
    * Metropolis (2017)
    * Serenity (Ethereum 2.0) - La etapa actual del ecosistema
        * Transición de PoW a PoS
        * Beacon Chain
        * PoS Validators
        * Shard Chains
* Ethereum es Turing Completo en busca de ejecutar cualquier programa desde cualquier parte del mundo

### Ethereum vs. Bitcoin
Ethereum: Turing Completo | La moneda cumple una función para un objetivo más amplio. \
Bitcoin: Turing Incompleto | Limitado a ser un sistema monetario superseguro.


## Capitulo 2: Componentes de Ethereum
### Red P2P
Esta red hace referencia a un mecanismo de transferencia de igual a igual o persona a persona, sobre la cual no existe ningún ente central y de lo contrario se maneja la información de manera descentralizada y segura.
### Algoritmo de consenso
Ethereum al igual que Bitcoin poseen un mecanismo de consenso basado en una prueba de trabajo o Proof of Work (PoW), presentada en sus inicios por Satoshi Nakamoto el creador de Bitcoin. De esta manera Satoshi logro pactar un acuerdo o un consenso entre los nodos, para decidir cual nodo es el encargado de generar un nuevo bloque y actualizar la blockchain, ya que no existe un ente central.
### Ether
Es la moneda propia de Ethereum, esta corre sobre la primera capa de la blockchain de Ethereum haciendola su moneda principal. El verdadero objetivo de esta moneda es servir como herramienta para poder construir la red de aplicaciones descentralizadas que corren dentro de Ethereum.
###  Ethereum Virtual Machine
La maquina virtual de Ethereum es la principal encargada de leer y ejecutar la logica de los contratos inteligentes o Smart Contracts escritos en el lenguaje Solidity, para que la red blockchain pueda incluir e interpretar esta lógica. Cada uno de los nodos en su interior poseen esta maquina virtual.
### Algoritmo criptográfico de seguridad (Ethash)
Es el algoritmo encargado de cifrar la información manejada en la blockchain de Ethereum. Los mineros utilizan este algoritmo para poder crear nuevos bloques.
### Clientes (Geth, Parity)
Estos clientes son paquetes que instalas en tu computador para poder correr un nodo dentro de este y poder conectarte a la red blockchain de Ethereum.

### Conceptos Relevantes
* **Clientes/Nodos:** Los clientes son los encargados de empaquetar el sistema sobre el cual se puede ejecutar un nodo en la red BlockChain. Cuando instalas en tu computador este cliente, automáticamente te conviertes en un nodo participante en la red de Ethereum.
* **Wallets:** Las wallets o billeteras son aplicaciones que nos permiten administrar nuestras cuentas de Ethereum o de cualquier otra red, para poder interactuar con otras personas que también sean parte de esta red. Además de poder controlar nuestros fondos y activos.
* **Smart Contracts:** Son los programas que nos permiten comunicarnos con la blockchain a partir de ciertas condiciones especificadas dentro de el contrato inteligente. Estos contratos se ejecutan dentro de la EVM para ser analizados y posteriormente implementados en la blockchain.
* **Web3:** Es una nueva web descentralizada sobre la cual no necesariamente va a existir un ente central, si no que de lo contrario, al ser una red descentralizada o P2P vamos a hacer nosotros mismos los usuarios los encargados tomar decisiones autónomas sin necesidad de recurrir o de pedir información a un ente central.


## Capitulo 3: La moneda ETH y el GAS
Una nota importante es que el gas NO es ether. Esta concepción tradicional nos lleva a creer que, por ejemplo, si $ETH tiene un precio mayor, entonces los costos de la red también. Sin embargo, son dos conceptos que NO están directamente vinculados. \
Entonces, ¿cómo funciona? El gas es sólo eso: gas, y se mide en unidades de gas. Sin embargo, se paga en $ETH. \

Piensa en esto como si tú fueras en automóvil de tu casa a tu trabajo. La cantidad de trabajo no cambia porque la ruta es la misma sin importar la cantidad de veces que la recorras. Es decir el mismo recorrido siempre consume la misma gasolina, pero, ¿qué pasa si la gasolina escasea? El precio por unidad de gas sube. En el contexto de Ethereum, lo que escasea es el blockspace, es decir, hay una cantidad finita de gas que puede aceptar un bloque (sumando el gas de todas las transacciones de dicho bloque)

### ¿Qué son las unidades de gas?
Las unidades de gas son una representación de esfuerzo computacional. Cuando compilamos código de Solidity a ejecutable de la EVM, el listado de códigos de operación implicará un coste en gas que está definido por una tabla de operadores. Es decir, de la misma forma que tu automóvil. Una llamada a una función de un contrato inteligente va a costar siempre la misma cantidad de gas. Lo que cambia es lo demandado que está ese gas en ese momento. 


## Capitulo 4: Etapas de desarrollo y actualizaciones programadas

### Actualizaciones
![imagen](https://user-images.githubusercontent.com/19738553/217055227-27345553-37f4-4a86-93ad-a3f5051ac08a.png)


## Capitulo 5: ¿Qué es la criptografía asimétrica?

### Funciones Hash
Las funciones hash son funciones que permiten llevar un contenido del dominio al rango de la función en tiempo polinomial. No obstante, invertir el hash es matemáticamente muy complejo y no viable. Es un método de integridad de la información.

### Firma Digital
La firma digital es un proceso criptográfico derivado de la criptografía asimétrica que utiliza la llave privada de un usuario para codificar un mensaje.
Debido a las características de la criptografía asimétrica. Codificar un mensaje con la llave privada permite que con el contenido original, se puede derivar la llave pública. Este es un mecanismo que no es utilizado para ocultar información, pero para asegurar autoría, es decir, si yo soy capaz de derivar la llave pública con el mensaje y la firma, entonces FORZOSAMENTE el dueño de la llave privada codificó ese mensaje, lo cuál es una garantía NO REPUDIABLE de autoría. \
En la blockchain, las transacciones no sólo son hasheadas, si no que son comprobadas como mensajes con autoría a través de la firma digital. La forma en la que se usan en conjunto es que el hash de la transacción es firmado por la llave privada que acredita la transacción.

### Otros
* **Criptografía Fuerte:** Es un tipo de criptografia que nadie puede romper, si uno no tiene la Llave para descifrar dicho mensaje, no existe poder humano o computacional para descifrar dicho mensaje.
* **Criptografía Asimétrica:** Tambien denominada "Llave publica"  \
![imagen](https://user-images.githubusercontent.com/19738553/217056443-ee480979-510b-4fba-95a0-a23c6959c6d9.png)
