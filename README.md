# LacreiSaudeVoluntariado
## Requirements:
    -Antes de começar, certifique-se de que o seu sistema atende aos requisitos mínimos para rodar o Android Studio. Abaixo estão os requisitos gerais para as principais plataformas:
	•	Windows:
	•	Windows 10 ou superior (64 bits)
	•	Mínimo de 8 GB de RAM (recomendado: 16 GB ou mais)
	•	4 GB de espaço livre no disco (recomendado: SSD)
	•	Resolução mínima de 1280 x 800
	•	Java Development Kit (JDK) incluído no Android Studio

## Installation Instructions:
    1.	Acesse o site oficial do Android Studio: https://developer.android.com/studio.
	2.	Clique no botão Download Android Studio.
	3.	Leia e aceite os termos de licença.
	4.	Baixe o instalador compatível com o seu sistema operacional.

## Configure o Android Virtual Device (AVD):
1.	Abra o AVD Manager:
	•	No Android Studio, clique em Tools > Device Manager (ou no ícone de dispositivo na barra de ferramentas superior).
2.	Crie um novo dispositivo virtual:
	•	Clique em Create Device.
	•	Escolha o tipo de dispositivo (por exemplo, Pixel 6, Tablet, etc.) e clique em Next.
	•	Selecione uma imagem do sistema (versão do Android) para o emulador:
	•	Se necessário, faça o download da versão desejada clicando em Download ao lado da imagem.
	•	Configure outras opções, como resolução e tamanho do disco, se necessário.
	•	Clique em Finish para salvar o dispositivo virtual.
3. Inicie o Emulador
	•	No Device Manager, localize o AVD que você criou.
	•	Clique no botão Play (ícone de triângulo verde) ao lado do dispositivo.
	•	O emulador será iniciado em uma janela separada.
4. Execute o Projeto no Emulador
	1.	No Android Studio, abra ou crie um projeto.
	2.	Certifique-se de que o AVD está iniciado e ativo.
	3.	Clique no botão Run (ícone de triângulo verde) na barra superior.
	4.	Escolha o emulador como o dispositivo de execução.
	5.	O aplicativo será instalado e executado no emulador.


# Documentação dos casos de teste:
## Validar cenários de teste da aplicação “Lacrei Saúde” usando vários tipos de teste, com linguagem Gherkin  
## CT01: Cadastro da pessoa usuária. 
### Cenário 1: Como usuário ainda não cadastrado, eu quero criar uma conta (fluxo principal). 
- Given: O usuario esta na tela de login 
- And: clica no botão "criar conta" 
- When: Quando ele preencher os campos com dados validos 
- And: aceita os termos de uso e confirma tem 18 anos o mais 
- And: clica em "Cadastrar" e mostra a tela informando o envio do link de verificação 
- Then: E possível verificar o link no email e acessar na tela principal para continuar o cadastro
  
#### Evidencias:  
https://github.com/user-attachments/assets/a23793ed-3db4-4e84-b5be-4a020b53face
### Cenário 2 : Como usuário ainda não cadastrado, eu quero criar uma conta mas uso dados invalidos (cenario negativo). 
- Given: O usuario esta na tela de login 
- And: clica no botão "criar conta" 
- When: Quando ele preencher os campos com dados inválidos  
- And: aceita os termos de uso e confirma tem 18 anos o mais 
- Then: mostra o campo com erro e não permite finalizar o cadastro
#### Evidencias:

### Cenário 3 : Como usuário ainda não cadastrado, eu quero criar uma conta com dados validos mas não aceito os termos (cenario alternativo). 
- Given: O usuario esta na tela de login 
- And: clica no botão "criar conta" 
- When : Quando ele preencher os campos com dados validos 
- And: não aceita os termos de uso e confirma tem 18 anos o mais 
- Then: mostra a mensagem de termos não aceitos e não permite finalizar o cadastro
#### Evidencias: 
https://github.com/user-attachments/assets/186c4c48-91c7-44b4-b661-c1c132988377

## CT02: Busca de um profissional de saúde. 
### Cenário 4 : Como usuário cadastrado, eu quero buscar e contatar um profesional (cenario principal). 
- Given: O usuario esta logado 
- When: preenche a barra de pesquisa professional com o valor "Medico Gay" e clica na lupa 
- And : valida informaçoes iniciais do professional  
- And: Solicita contato do professional via codigo SMS 
- And: preenche o código enviado  
- Then: mostra os contatos disponeis do profesional
#### Evidencias:
https://github.com/user-attachments/assets/c4216df9-2871-4cf4-8498-67dafbc20953

### Cenário 5 : Como usuário cadastrado , Eu quero buscar e contatar um profesional mas preencho codigo sms invalido (cenario negativo). 
- Given: O usuario esta logado 
- When: preenche a barra de pesquisa professional com o valor "Medico Gay" e clica na lupa 
- And: valida informaçoes iniciais do professional  
- And: Solcita contato do professional via codigo SMS 
- And: preenche o código com dados inválidos  
- Then: mostra a mensagem "Código incorreto"
#### Evidencias:
https://github.com/user-attachments/assets/85d7efc1-284c-4e69-b91a-36883903567f

## CT03: Edição de perfil da pessoa usuária. 
### Cenário 6 : Como usuário cadastrado , Eu quero editar meu contato principal (cenario principal). 
- Given: O usuario esta logado 
- When: clica no botão "editar dados" 
- And: seleciona "fluida" como identidade de gênero 
- Then: mostra a informação alterada
#### Evidencias:
https://github.com/user-attachments/assets/417d0efd-d79c-44fe-9408-03018140e6e9
https://github.com/user-attachments/assets/f1b78e0c-10f2-42f1-a62e-d3bfc7a37632

## CT04: Esquecer senha e resetar. 
## Cenário 7 : Como usuário cadastrado , Eu esqueci minha senha e quero recuperar (cenario principal). 
- Given: O usuario esta na tela de login 
- And: clica no opção "esqueci minha senha" 
- When: preencho o email valido e clico em "enviar link" 
<<<<<<< HEAD
- Then: e possível redefinir a senha via link enviado no email e acessar novamente na tela principal 

# Testes de acessibilidade:
### Cenário 1: Como usuário ainda não cadastrado, eu quero criar uma conta (fluxo principal). 
- Given: O usuario esta na tela de login 
- And: clica no botão "criar conta" 
- When: Quando ele preencher os campos com dados validos 
- And: aceita os termos de uso e confirma tem 18 anos o mais 
- And: clica em "Cadastrar" e mostra a tela informando o envio do link de verificação 
- Then: E possível verificar o link no email e acessar na tela principal para continuar o cadastro 
=======
- Then: e possível redefinir a senha via link enviado no email e acessar novamente na tela principal
#### Evidencias: 
https://github.com/user-attachments/assets/6d2e4fa0-d459-42e7-857e-6d0511a77179
>>>>>>> b3edcb845d65c151afee862649a14d2cadda7a58
