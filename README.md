# gestaodeforces
Sistema de Gestão de STP

Descrição

O Sistema de Gestão de STP foi desenvolvido com o objetivo de padronizar, registrar e rastrear intervenções temporárias realizadas em sistemas de automação industrial.

Durante o desenvolvimento do projeto, foi criado o conceito de STP (Supressão Temporária de Proteção), utilizado para representar alterações temporárias aplicadas em Controladores Lógicos Programáveis (PLCs), tais como:

Forces ON/OFF;
Instruções AFI (Always False Instruction);
Desabilitação temporária de lógicas;
Outras alterações temporárias realizadas durante manutenção, testes ou diagnóstico.

O sistema surgiu devido à inexistência de um processo padronizado para registro dessas intervenções, que normalmente eram anotadas manualmente em relatórios de turno e, em muitos casos, não eram registradas.

Problema Identificado

Antes da implantação do sistema:

O registro dos forces dependia da lembrança do técnico;
Não existia rastreabilidade centralizada;
Havia risco operacional devido à permanência de alterações temporárias nos PLCs;
Não existia histórico estruturado para auditorias e consultas.
Solução Desenvolvida

O Sistema de Gestão de STP permite:

✅ Registrar todas as intervenções temporárias realizadas nos PLCs;

✅ Consultar rapidamente intervenções em aberto ou finalizadas;

✅ Filtrar registros por equipamento, local, tipo e estado;

✅ Manter histórico completo das alterações realizadas;

✅ Exportar dados para planilhas Excel;

✅ Realizar backup e importação de registros;

✅ Gerenciar cadastros auxiliares (equipamentos, locais, tipos, solicitantes, executantes e diretorias).

Funcionalidades
  Autenticação
Login de utilizadores;
Controle de acesso por utilizador.
  Gestão de Forces
Cadastro de novas STPs;
Edição de informações;
Encerramento de intervenções;
Consulta e pesquisa avançada.
  Cadastros Auxiliares
Equipamentos;
Locais;
Autômatos;
Tipos;
Solicitantes;
Executantes;
Diretorias.
  Relatórios
Exportação para Excel;
Backup dos registros;
Importação de dados.

Arquitetura Futura

Atualmente o sistema opera através do cadastro manual obrigatório de todas as intervenções realizadas durante o turno.

Está prevista uma segunda fase de desenvolvimento com integração automática ao AssetCentre.

Fluxo previsto

PLC → AssetCentre → Log de Modificações → Banco de Dados → Sistema de Gestão de STP → Tratamento Técnico

Nesta arquitetura, todas as alterações realizadas nos PLCs serão identificadas automaticamente pelo AssetCentre e disponibilizadas para análise e tratamento pela equipe técnica.

Levantamento Inicial Realizado

Durante o estudo foram analisados quatro PLCs industriais.

Resultados encontrados:

Item	Quantidade
Branches em branco	148
Forces ON/OFF	36
Linhas desabilitadas (AFI)	152

Como melhoria de padronização, os branches em branco passaram a ser substituídos pelos bits:

ALW_ON (sempre verdadeiro);
ALW_OFF (sempre falso).
Tecnologias Utilizadas
Python
SQLite
Flet
Git
GitHub

(Atualize esta lista conforme as tecnologias efetivamente utilizadas no projeto.)

Capturas de Tela
Tela de Login

Sistema de autenticação para acesso dos utilizadores.

Cadastro de STP

Registro completo das intervenções temporárias realizadas nos PLCs.

Consulta e Pesquisa

Consulta avançada com filtros e exportação de resultados.

Cadastros Auxiliares

Gestão de equipamentos, locais, autômatos e demais entidades do sistema.

Benefícios Obtidos
Aumento da rastreabilidade operacional;
Redução da dependência de registros manuais;
Padronização das intervenções temporárias;
Melhoria na segurança operacional;
Disponibilidade de histórico para auditorias.
Autor

Tiago Diniz

Engenharia de Software | Automação Industrial | SCADA | OT Systems

Licença

Este projeto foi desenvolvido para fins acadêmicos e de melhoria contínua dos processos industriais.
