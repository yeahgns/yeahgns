## Olá, eu sou o Guilherme 👋

**SRE & SysAdmin | Specialty in VoIP**

Engenheiro focado em **infraestrutura, automação, segurança e confiabilidade de sistemas de telefonia (PBX/VoIP)**. Minha atuação vai desde o gerenciamento de redes e virtualização (Proxmox/Linux) até o desenvolvimento de ferramentas internas e automações que transformam a experiência do cliente final.

---

### 💡 O que eu faço no dia a dia

- **Infraestrutura como Código & Automação:** Orquestração e gerenciamento de frotas de VMs (Proxmox + Ansible) para provisionamento e deploys contínuos sem downtime.
- **Confiabilidade & Observabilidade (SRE):** Implantação e manutenção de métricas de saúde de infraestrutura e serviços (Zabbix, Prometheus, Webhooks).
- **Segurança em Camada de Rede:** Hardening de servidores Linux, controle de acesso e mitigação proativa de ataques em ambientes expostos à internet.
- **Engenharia de Software de Apoio:** Desenvolvimento de ferramentas e relatórios customizados para resolver dores reais de negócio e usabilidade no ecossistema de PBX (Asterisk/Issabel).

---

### 🚀 Principais Projetos (até o momento)

#### 🛡️ [SIP Shield](https://github.com/yeahgns/sip-shield)
> **Proteção plug-and-play em camada de rede para servidores PBX (Issabel/Asterisk).**
- **O problema:** Servidores VoIP públicos sofrem ataques brutais de SIP scanning constantemente; ferramentas de aplicação (Fail2ban) só reagem *após* as tentativas.
- **A solução:** Firewall inteligente via `iptables`/`ipset` que bloqueia tráfego fora do país de destino em nível de pacote (GeoIP), fecha portas de gerenciamento para `localhost` e exporta métricas estruturadas (Prometheus/JSON) com instalador idempotente para automação via Ansible.

#### 📊 [Issabel CDR Report v2](https://github.com/yeahgns/issabel-cdr-report-v2)
> **Relatório de CDR reescrito para transformar registros crus de telefonia em métricas humanas.**
- **O problema:** O relatório nativo do Issabel gera dezenas de linhas poluídas para uma única ligação (tentativas por ramal, filas, etc.), confundindo os clientes.
- **A solução:** Interface construída sem dependências que agrupa o histórico por `linkedid`, calcula tempo real de espera (descontando URA) e mapeia chamadas perdidas sem retorno. Todo esse desenvolvimento buscou a praticidade para os clientes de enxergar o que realmente precisam.

#### 🎧 [Issabel Call Center Plus](https://github.com/yeahgns/issabel-callcenter-v2)
> **Um painel de call center que mostra, num relance, o que está acontecendo na operação.**
- **O problema:** Supervisores precisam saber na hora quem está atendendo, quem está em pausa e se tem cliente esperando. No Issabel nativo, essa visão é difícil de montar e não funciona bem numa TV da operação.
- **A solução:** Um painel em tempo real que mostra a situação de cada agente, o tamanho das filas (com alerta quando o cliente espera demais) e o andamento das campanhas de saída. Pode ser deixado em tela cheia numa TV, respeita as permissões de cada usuário e é instalado sem mexer no que já existe no Call Center.

---
