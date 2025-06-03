# Appsec-aulas

# Desenvolvimento Seguro de Software

## Introdução
O desenvolvimento seguro visa criar aplicações protegidas contra ameaças e vulnerabilidades. Nesta aula, abordaremos conceitos essenciais para garantir um código mais seguro.

---

## 1. Processo de Desenvolvimento Seguro
### Princípios de Códigos Seguros
- **Validação de entrada**: Impedir ataques como SQL Injection e Buffer Overflow.
- **Privilégio mínimo**: Reduzir permissões ao necessário para evitar acessos indevidos.
- **Defesa em profundidade**: Uso de múltiplas camadas de proteção.

### Mecanismos de Defesa
- Firewalls e antivírus
- Monitoramento contínuo e auditorias de segurança
- Aplicação de patches e updates periódicos

---

## 2. Ameaças e Riscos
### Tipos de ameaças:
- **Ataques de injeção** (SQL, XSS)
- **Buffer Overflow**
- **Exposição de dados sensíveis**
- **Ransomware**

### Mitigação de riscos:
- Implementação de controles de acesso
- Segurança na comunicação (TLS, HTTPS)
- Análise estática e dinâmica do código

---

## 3. Software e Controles
- **Controle de acesso baseado em função (RBAC)**
- **Logs e auditoria**
- **Uso de bibliotecas seguras e testadas**

---

## 4. Código Seguro em C
### Práticas recomendadas:
```c
// Exemplo de uso seguro de strings em C
#include <stdio.h>
#include <string.h>

int main() {
    char buffer[50];
    strncpy(buffer, "Texto seguro", sizeof(buffer) - 1);
    buffer[sizeof(buffer) - 1] = '\0'; // Evita overflow
    printf("%s\n", buffer);
    return 0;
}
