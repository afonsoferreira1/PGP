# PGP

Passo a passo sugerido

O trabalho tem duas etapas, e a Etapa 1 alimenta a Etapa 2. Esta é uma ordem prática, que deixa as decisões que condicionam o resto para o início.

Passo 0: Organizar o grupo (primeira semana)
Criar um repositório partilhado (Git) e uma pasta comum para os documentos.
Escolher uma ferramenta de diagramas partilhada (draw.io, Lucidchart, PlantUML, etc.).
Ler o enunciado todos juntos e anotar dúvidas para o docente.
Decidir a stack (a MEAN é a sugerida; se escolherem outra, a pesquisa começa já na Etapa 1).
Etapa 1: Desenho inicial (até 6 de novembro)
Passo 1: Perceber o problema
Listar os atores: utilizador, gestor da loja e serviços externos (pagamentos, mapas/geocodificação).
Agrupar as 29 user stories por área: conta e perfil, catálogo e pesquisa, coleção, listas, pedidos de versões, loja e compra, gestão e estatísticas.
Passo 2: Diagrama de casos de uso
Um caso de uso por funcionalidade (ou por grupo de user stories).
Ligar os serviços externos aos casos de uso que os usam (por exemplo, pagamento e mapa do perfil).
Usar include e extend onde fizer sentido.
Passo 3: Diagrama de classes ou entidade-associação

É o artefacto mais exigente, por isso convém fazê-lo com calma:

Identificar as entidades: Artista (solista/grupo), Álbum, Canção, Faixa, Suporte, Versão do álbum, Utilizador, Coleção, Lista, Pedido, Notificação, Carrinho, Fatura e linhas de fatura.
Definir atributos, tipos e identificadores (MBID, ISRC, ISNI, EAN-13, username).
Definir associações e multiplicidades (por exemplo, canção para faixas, grupo para membros).
Registar as restrições RI-01 a RI-30 e acrescentar as que faltam (RI-31, ...), como identificadores únicos e estados do pedido.
Se não couber numa página A4, fazer um diagrama de topo sem atributos, com grupos de classes a cores, e um diagrama detalhado por grupo.
Passo 4: Diagramas de atividades (ou BPMN)

Escolher os fluxos mais ricos, por exemplo:

Compra: pesquisar, ver álbum, carrinho, pagamento externo, resultado, atualizar stock, coleção e fatura.
Pedido de nova versão: utilizador submete, gestor analisa, aceita ou recusa, notificação.
Registo de álbum pelo gestor.
Passo 5: Esboços da interface (wireframes)
Focar nas funcionalidades complexas: página do álbum com versões e stock, carrinho e pagamento, coleção com ordenação, dashboard de estatísticas com mapa.
Pensar logo no mobile (RNF-04, responsive).
Passo 6: Pesquisa de serviços externos
Pagamentos: comparar, por exemplo, Stripe, PayPal e MB WAY/SIBS (modo sandbox).
Mapas e geocodificação: Leaflet com OpenStreetMap e Nominatim, comparado com Google Maps.
Para cada escolha, apresentar uma lista de vantagens e a comparação com um concorrente (custo, documentação, facilidade, modo de testes).
Passo 7: Relatório e entrega
Juntar tudo no relatório, rever a consistência entre diagramas (os nomes das entidades devem coincidir) e preparar a apresentação.
Entregar o ZIP PGP-2627-GXX-E1.ZIP no Moodle.
Etapa 2: Planeamento (até 4 de dezembro)
Passo 8: Equipa e papéis
Atribuir papéis: gestor de projeto (que também é parcialmente product owner), frontend, backend, base de dados, arquiteto, segurança e redes, testes com utilizadores, etc.
Considerar as competências e a disponibilidade de cada pessoa.
Passo 9: Ferramentas e software
Separar o que é ferramenta de desenvolvimento (editor, Git, CI/CD, Swagger) do que é software necessário para a aplicação funcionar (Node, MongoDB, etc.).
Para cada item, indicar o propósito e o link da documentação.
Passo 10: Esforço disponível
Contar as semanas do semestre, descontando avaliações e feriados, e as horas por pessoa. Isto dá o limite máximo de esforço.
Passo 11: Story points (planning poker)
Fazer uma sessão com todo o grupo, estimando as 29 user stories com uma escala (Fibonacci). Escolher uma história de referência e discutir as divergências.
Passo 12: Montar o product backlog
Além das user stories, incluir tarefas como configuração do ambiente, CI/CD, deploy, testes, testes de usabilidade (SUS), segurança, backups, proteção de dados e as atividades de redes.
Decompor as tarefas grandes para estimar melhor. O total não pode exceder o esforço disponível.
Passo 13: Distribuir pelos 3 sprints
O product owner ordena por prioridade e dependências (conta e login primeiro, catálogo antes de coleção, carrinho antes de pagamento).
Equilibrar o esforço dos sprints e deixar folga.
Passo 14: Mapa de Gantt
Tarefas, durações, sprints assinalados, dependências e pessoas atribuídas.
Tabela com o esforço total por pessoa.
Passo 15: Gestão de risco
Tabela de riscos com probabilidade, impacto, mitigação, monitorização e plano de contingência (por exemplo, atraso na integração de pagamentos, falta de disponibilidade, limites das APIs gratuitas).
Passo 16: API REST em OpenAPI
No editor Swagger, definir endpoints por recurso (/artists, /albums, /users, /cart, etc.), formatos de pedido e resposta e códigos HTTP.
Seguir boas práticas REST (RNF-09) e guardar num ficheiro .yaml.
Passo 17: Relatório final e entrega
Rever a coerência com a Etapa 1 e entregar PGP-2627-GXX-E2.ZIP.
Dicas
Façam revisões cruzadas entre membros para detetar incoerências.
Mantenham uma lista única de nomes (glossário) para as entidades.
Preparem a apresentação com antecedência, porque todos os elementos têm de estar presentes e saber responder sobre todo o trabalho.
