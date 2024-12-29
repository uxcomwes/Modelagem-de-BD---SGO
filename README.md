Nesse esquema conceitual, foi dada a seguinte narrativa: 

Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica
Clientes levam veículos à oficina mecânica para serem consertados ou para passarem por revisões  periódicas
Cada veículo é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega.
A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra
O valor de cada peça também irá compor a OSO cliente autoriza a execução dos serviços
A mesma equipe avalia e executa os serviços
Os mecânicos possuem código, nome, endereço e especialidade
Cada OS possui: n°, data de emissão, um valor, status e uma data para conclusão dos trabalhos.

Com base na especificações acima, foi feita a seguinte modelagem: 

Entidades criadas: Cliente, Veiculo, Equipe de Mecânicos, Ordem de Serviço, Tabela de Mão de Obra e Peças.
Relacionamentos: A entidade cliente foi diretamente relacionada a entidade veiculo através do tipo 1:n, pois um cliente pode ter mais de um veículo. Entretanto, o veículo foi relacionado a apenas uma equipe de mecânicos(1:1), tornando-a responsável pelo mesmo.
A equipe de mecânicos foi relacionada a Ordem de serviço que foi gerada após analisar o caso do veículos (1:n) e a Ordem de Serviço foi relacionada ao cliente, dando origem a entidade "Autorização - Execução do Serviço". A mesma foi relacionada com a equipe de mecânicos, que depende da autorização do cliente para executar o serviço.
A entidade "Ordem de Serviço" também possui duas entidades atreladas ao seu funcionamento, sendo elas: Tabela de Mão de Obra e Peças, que é o que compõe o valor final do serviço prestado. 
