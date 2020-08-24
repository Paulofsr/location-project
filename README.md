# location-project

Esse é o projeto *LOCATION-PROJECT". Para atender a demanda de pacotes enviado pelos dispositivos decifrá-los e disponibilizar os dados para consulta de localização.

Apresentado na Arquitetura inicial (imagem abaixo) um modelo MVP. Com dois microserviços simplificando suas funções:

* [ms-tcp-location](https://github.com/Paulofsr/ms-tcp-location): Através do protocolo TCP irá receber os Pacotes dos dispositivos.
* [ms-api-location](https://github.com/Paulofsr/ms-api-location): Através do protocolo HTTP irá receber do [ms-tcp-location](https://github.com/Paulofsr/ms-tcp-location) parte do pacote com os dados da situação do dispositivo e disponibilizará uma rota para consulta dos dados através do Número do dispositivo.


![Arquitetura 0.1](https://github.com/Paulofsr/location-project/blob/master/locatio-project.png?raw=true)

## Melhorias futuras

Com a inteção de melhorar a segurança, será implementado um controle de usuários e os dispositivos vinculados a ele. E um processo de autenticação usando o padrão JWT. 

Assim, ao consultar a localização do dispositivo ele irá, não somente, verificar a autenticação do Tokem como também se o usuário em questão tem permissão para consultar esse dados. Representado na imagem abaixo.


![Arquitetura 2.0](https://github.com/Paulofsr/location-project/blob/master/locatio-project-2.png?raw=true)