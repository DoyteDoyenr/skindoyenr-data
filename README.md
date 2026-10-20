# skindoyenr-data

Base de conhecimento que o [SkinDoyenr](https://github.com/DoyteDoyenr) usa para sugerir runas e itens contra o time inimigo.

- `knowledge.json` — perfis dos campeões (tipo de dano, cura, escudos, controle de grupo, escalonamento, com a habilidade de origem), e o que cada item e runa responde.
- `schema/knowledge.schema.json` — o formato (JSON Schema 2020-12).

O app baixa `knowledge.json` daqui a cada 6 horas e só troca a cópia local quando `dataVersion` é maior. Sem internet, usa a cópia que vem no instalador.

Para publicar uma atualização: edite `knowledge/profiles/` no projeto do app, rode `bun run build-knowledge` (valida contra o schema e sobe o `dataVersion`) e envie o conteúdo de `knowledge/dist/` para este repositório.
