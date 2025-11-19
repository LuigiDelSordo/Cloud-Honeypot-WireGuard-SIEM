# Cloud-Honeypot-WireGuard-SIEM
![Topología de red](./foto1.jpeg)
## 🛡️ Proyecto ASIR – Infraestructura de Honeypots y SIEM en Oracle Cloud

Este proyecto recrea un entorno seguro orientado a ciberseguridad defensiva para analizar ataques reales de forma controlada mediante honeypots y un sistema SIEM.

## 🔧 Tecnologías utilizadas
- Oracle Cloud (VCN, Compute, Security Lists)
- Ubuntu Server
- Honeypots: *Cowrie (SSH)* y *DVWA (Web)*
- VPN *WireGuard* (modelo egress-only)
- *Elastic Stack (SIEM)* para análisis y correlación de eventos
- *Suricata* para IDS/IPS
- Proxmox / VirtualBox
- Bash scripting y firewalls

## 🏗️ Arquitectura
- Honeypots expuestos a Internet
- Salida controlada (egress-only) hacia servidor WireGuard
- VPN privada hacia SIEM sin acceso a Internet
- SIEM aislado en red interna
- Recolección y correlación de eventos desde honeypots

## 🎯 Objetivo del proyecto
- Analizar intentos de intrusión reales  
- Registrar eventos en un SIEM  
- Practicar segmentación de redes y endurecimiento del sistema  
- Simular una infraestructura corporativa segura en entorno Cloud

## 🚀 Cómo reproducir el proyecto (resumen)

1. Crear 3 instancias en Oracle Cloud (2 públicas y 1 privada).
2. Configurar reglas de seguridad (ingress/egress).
3. Instalar Cowrie y DVWA en los honeypots.
4. Configurar WireGuard como túnel hacia la red privada.
5. Enviar logs al SIEM (Elastic Stack).

## 📘 Lecciones aprendidas

- Configuración segura de redes en Oracle Cloud.
- Implementación de honeypots en producción controlada.
- Uso de WireGuard como canal seguro de logs.
- Correlación de eventos en un SIEM (Elastic).
- Segmentar infraestructura y aplicar hardening básico.
