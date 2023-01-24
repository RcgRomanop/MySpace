
# Improvment Points:

## ATF Scripts
--------------------------
- Separate Code between diferent repos. Definir responsáveis para cada um dos repos
confusão de branches
- Definir um padrão de escrita de nomes de variáveis/ações/elementos/nomes de cenarios.
- Definição de tabela de tags para contexto
- Add tags deprecated  and wip
- Avaliar a possibiliidade de ter um header genérico para o endpoint. Supostamnte Sim!
- Utilizar mais as variáveis para representar os valores fixos das validações, de modo a Não ter os valores Hardcoded.
- Personal test data (credenciais e valores)
- Ficheiro de env.data apenas precisa de incluir valores diferentes e só é necessário se houver valores diferentes
- Duplicação de código
- Remove unused code (paginas desnecessárias
- Remove random comments on the code
- Cenarios demasiado complexos (Telco. principalmente)
- Xpath instáveis
- Add yaml lint validation
- Pedir à equipa de desenvolvimento para definir id's para os elementos de UI

## CI/CD
------------------------
Add option to contain request/response on ws scenarios
Pq é que o processo de import dos dados para o azur esta comentado?

#Duvidas:
- Onde é que vejo os reports e as execuções dos testes?
- Como estão organizadas as regressões?
- Como é que é feito o delivery do nosso código?
- Como é que está a ser feito o versionamento do código?
- O que faz o modulo de javascript? É responsável pelo cleanup do testdata (Users)
- Preciso de uma lista de testes que estejam a falhar por motivos de atf/selenium
- Validar criação/cleanup test data?
- Validar inquérito sobre a possibilidade ou não de automatizar os cenários
- Validar se ha cenários que não estejam desenhados

# Product Owners: 
-----------------------------------------------------------
- Journy Designer-
- UFE -
- Core -
- CSM - ASDASDAS

# Repository improvements
-------------------------------------------------------------------

## UFE Tasks:
1. Create Ufe repository.
2. Adapt UFE pipeline.
3. Analyse test data needs
4. Resolve integration with:
	- "aux_foundation_oauth"
	- "core_uam_ext"
		- Create users
		- Add role/permissions
	- "core_user_access_management"
	- "core_timeline"
	- "core_uam"
	- "core_message"
	- "cms_jd_blueprint_actions"










