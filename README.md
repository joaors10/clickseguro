<<<<<<< HEAD
# clickseguro
Aplicação simples para testes automatizados de segurança com OWASP ZAP
=======
# ClickSeguro (versão sem Docker)

Projeto para a atividade de DevSecOps – Testes de Segurança Automatizados (FIAP).
Aplicação estática com vulnerabilidades propositalmente simples (XSS reflexivo) para serem detectadas pelo OWASP ZAP.

## Como usar localmente
1. Extraia os arquivos e, na pasta do projeto, execute:
   ```bash
   python3 -m http.server 8080
   ```
2. Acesse: http://localhost:8080

## Observação sobre o workflow
O arquivo `.github/workflows/zap.yml` demonstra como rodar o ZAP no GitHub Actions sem usar Docker na aplicação:
- Baixa e inicia o ZAP em modo daemon no runner
- Sobe um servidor local (python http.server)
- Executa varredura e gera `zap_report.html`
- Falha o job se houver vulnerabilidades com severidade High ou Critical
>>>>>>> 177bb33 (first commit)
