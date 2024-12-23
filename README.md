# Desafio Carrefour #
# Testes Automatizados - API de Gerenciamento de Usuários #

Este repositório contém os testes automatizados para uma API de gerenciamento de usuarios (Listar Usuários, Cadastrar Usuario, Buscar Usuario por ID, Editar Usuario, Excluir Usuario)

### Requisitos:
- JMeter (versão 5.6.3)
- Java (versão 1.8.0_411-b09)

### Passos para executar os testes:
1. Clone este repositório:

2. 2. Abra o arquivo `JMT - Carrefour Challenge.jmx` no JMeter.
3. Execute os testes no JMeter e visualize os relatórios.

### Testes Executados
1. Os testes foram executados afim de garantir 100% de cobertura das API´s.
2. Destalhes sobre os Casos e Quantidades de Testes: 27 Testes Executados

> Retornos esperados conforme expectativas (Exemplo: 200, 201, 400 e 401);
		
> POST /login - Realizar login
(02 TESTES)
        Retorno 200 - Login com usuario valido OK!
					- Response - Login realizado com sucesso
				Retorno 401 - Login com usuario invalido
					- Response - E-mail e/ou senha invalidos
			********************************************************************************
> GET /usuarios - Listar usuários cadastrados (TRUE / FALSE / VAZIO )
(15 TESTES)
				Retorno 200 - Lista de Usuarios - STRINGS Vazias_ADM TRUE
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - STRINGS Vazias_ADM FALSE
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - STRINGS_ADM Vazias
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - ID Valido_ADM TRUE
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - ID Valido_ADM FALSE
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - ID Valido_ADM Vazio
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - NOME Valido_ADM TRUE
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - NOME Valido_ADM FALSE
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - NOME Valido_ADM Vazio
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - EMAIL Valido_ADM TRUE
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - EMAIL Valido_ADM FALSE
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - EMAIL Valido_ADM Vazio
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - PASSWORD Valido_ADM TRUE
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - PASSWORD Valido_ADM FALSE
					- Response Qtde X
				Retorno 200 - Lista de Usuarios - PASSWORD Valido_ADM Vazio
					- Response Qtde X
			********************************************************************************
> POST /usuarios - Cadastrar usuário
(02 TESTES)
        Retorno 201 - Cadastro com sucesso - NOVOS DADOS VALIDOS DE USUARIO (NOVO)
													 MESMOS DADOS DE USUARIO, EXCETO EMAIL (NOVO EMAIL)
				Retorno 400 - E-mail ja esta sendo usado - MESMOS DADOS DE USUARIO E EXCETO EMAIL
														   NOVOS DADOS VALIDOS, EXCETO EMAIL (MANTEM ANTIGO)
			********************************************************************************
> GET /usuarios/_ID} - Buscar usuário por ID
( 02 TESTES)
				Retorno 200 - Usuario Encontrado - ID Valido = 0uxuPY0cbmQhpEz1
					- Response Qtde = 1;
				Retorno 400 - Usuario Nao Encontrado - ID Invalido = 0uxuPY0cbmQhpEz
					- Response Qtde = 0 (Usuario Nao Encontrado)
			********************************************************************************
> DELETE /usuarios/{_ID} - Excluir usuário
( 02 TESTES)
				Retorno 200 - Registro Excluido com Sucesso - COM STRING _ID = NOVA, PEGA _ID DE NOVA CONSULTA _ID
					- Response = Registro Excluido com Sucesso				
				Retorno 200 - Nenhum Registro Excluido - COM STRING _ID = DO TESTE ANTERIOR
					- Response - Nenhum Registro Excluido			
			********************************************************************************
> PUT /usuarios/{_ID} - Editar usuário
(03 TESTES)
				Retorno 200 - Registro	Alterado com Sucesso - ID Valido = 2mikXbSZ3LJAJQEL , NOVOS DADOS VALIDOS DE USUARIO E EMAIL
															   ID = 2mikXbSZ3LJAJQEL , ALTERADO SOMENTE o CAMPO EMAIL para NOVO EMAIL ou EDICAO DE EMAIL
					- Response - Registro Alterado com Sucesso
				Retorno 201 - Cadastro realizado com sucesso - ID VALIDO, porem, com outras STRINGS ja existentes.
					- Response - Cadastro realizado com sucesso
				Retorno 400 - E-mail ja Cadastrado - COM STRING _ID = 2mikXbSZ3LJAJQEL , NOVOS DADOS VALIDOS DE USUARIO, EXCETO EMAIL (MANTEM ATUAL)
					- Response - Este email ja esta sendo usado
			 *********************************************************************************

### Resultados:
Os resultados podem ser encontrados nos arquivos `resultados.jtl` e nos gráficos gerados automaticamente no diretório `graphs`.

## Contribuição:
Sinta-se à vontade para sugerir melhorias ou fazer pull requests!
