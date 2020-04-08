# Desafio Conceito ReactJS

Nestapa etapa, mostramos que entendemos na prática os conceitos básicos sobre reactJS e seus pilares:

- Componentes
- Propriedade
- Estado & Imutabilidade

O desafio consiste em adicionarmos novos repositórios à nossa coleção partindo de uma API construída em NodeJS.

Método de adicionar repositório:
Apenas um texto estático seguido de um Date.Now() para que capturemos o timestamp atual para termos certeza que os repositórios que estão
sendo adicionados, não estão sendo repetidos.

#markdown

async function handleAddRepository() {
    const response = await api.post("repositories", {
      title: `Novo Repositório ${Date.now()}`,
    });

    setRepositories([...repositories, response.data]);
  }
