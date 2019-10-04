# TarifaPedagioNFC
Uma companhia de concessão de rodovias te contratou para desenvolver um sistema automatizado para a cobrança de tarifa de seus pedágios. O sistema fará a cobrança via NFC de tal forma que o débito seja feito ao aproximar o aparelho celular de uma leitora. 

Para definir a tarifa corretamente, o sistema fará a leitura por imagem do veículo a fim de identificar qual é o seu tipo: carro, caminhão ou motocicleta. Em caso de carro ou caminhão, identificará se possui eixos extras.
 
Além da definição da tarifa a ser cobrada,  deve-se consultar um serviço externo para verificar se o veículo consta alguma ilegalidade. Caso haja alguma irregularidade, o sistema deve restringir o acesso.

Caso a leitura não seja bem sucedida, cobra-se o equivalente a um carro comum, sem eixos adicionais.

- Para motocicletas, cobra-se 5 reais
- Para veículos leves, cobra-se 10 reais e um adicional de 5 reais por eixo.
- Para veículos pesados, cobra-se 25 reais e um adicional de 15 reais por eixo.

Após a cobrança, o sistema deve emitir um comprovante de pagamento, no entanto, haverá a opção de escolha entre imprimir ou enviar por e-mail.

Considere o seguinte fluxo: 
- 1. O veículo se aproxima do pedágio;
- 2. O sistema efetua a leitura por imagens e exibe na tela a placa, o estado e o tipo de veículo;
- 3. O sistema consulta serviço para verificar irregularidades e exibe na tela o resultado;
- 4. O sistema calcula o valor a ser cobrado de tarifa e exibe na tela; 
- 5. O motorista aproxima o celular na leitora e faz o pagamento via NFC; 
- 6. O motorista escolhe o meio de emissão do comprovante. O sistema exibe na tela no formado: "*** Comprovante <IMPRESSO/EMAIL>. Veículo GHI123 - Moto . VALOR: XXX ***";

Implemente considerando que a leitura por imagens já está pronta e deve-se processar as seguintes entradas:
- Tipo: Caminhão, placa: "ABC123", estado: "SP", eixos adicionais: 4, comprovante: Papel;
- Tipo: Carro, placa: "DEF123", estado: "RJ", eixos adicionais: 1, Comprovante: Papel;
- Tipo: Carro, placa: "DEF123", estado:"RJ", eixos adicionais: 0, Comprovante: Papel;
- Tipo: Moto, placa: "GHI123", estado:"MG", eixos adicionais: 0), Comprovante: Papel; 
- Tipo: Não Identificado, placa: "JKL123", estado:"RS", Comprovante: Papel;
