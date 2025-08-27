# 📘 Mono-repo vs Multi-repo

## 🔹 O que é Mono-repo?
- **Mono-repo (repositório único)** significa que **todo o código da sua organização** (ou de um projeto maior) fica em **um único repositório Git**.

### ✅ Vantagens:
- Facilita a visibilidade: todo mundo enxerga tudo.
- Padronização de dependências e configs.
- Reuso de código sem precisar publicar pacotes.

### ⚠️ Desvantagens:
- Repositório muito pesado com o tempo.
- Builds e pipelines podem ficar mais lentos.
- Difícil separar permissões (ex: dar acesso só a parte do código).

---

## 🔹 O que é Multi-repo?
- **Multi-repo (múltiplos repositórios)** significa que **cada serviço/projeto fica em um repositório separado**.

### ✅ Vantagens:
- Repositórios menores e mais leves.
- Separação clara de responsabilidades.
- Times podem trabalhar de forma independente.

### ⚠️ Desvantagens:
- Pode gerar duplicação de código comum.
- Gestão de versões entre serviços pode ser mais complexa.
- Necessário configurar integração entre múltiplos repositórios.

---

## 🛠️ Comandos úteis no Multi-repo

Dentro do repositório principal você irá rodar os seguintes comandos.

- Para adicionar um módulo (Repositório)
```bash
git submodule add git@github.com:seu-org/user-service.git services/user-service
```
```bash
git add .
```
```bash
git commit -m ""
```
```bash
git push
```
- Para carregar os módulos dentro do multi-repo
```bash
git submodule update --init --recursive
```
- Para atualizar o multi-repo
```bash
git submodule update --remote
```
