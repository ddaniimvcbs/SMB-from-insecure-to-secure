# samba-security-lab
🇪🇸 Laboratorio SMB: permisos en Samba y Linux, mínimo privilegio y análisis ofensivo de configuraciones inseguras y escalada de privilegios. 🇬🇧 SMB lab: Samba and Linux permissions, least privilege, offensive analysis of insecure configurations and privilege escalation.


# SMB: From Insecure to Secure

Laboratorio práctico de seguridad en SMB/Samba, construido desde cero para
aprender pentesting, hardening y purple teaming de forma aplicada. El
objetivo no es solo atacar o solo defender: es entender el mismo protocolo
desde los dos lados, documentando cada paso con evidencia real capturada
en mi propio entorno de pruebas.

## Objetivo del proyecto

- Montar un servidor Samba correctamente endurecido, y documentar por qué
  cada opción de configuración importa.
- Montar un segundo servidor deliberadamente mal configurado, explotarlo,
  y documentar cómo se detecta y cómo se corrige cada fallo.
- Entender el protocolo SMB y su autenticación (NTLM) a nivel de paquete,
  no solo de teoría.
- Automatizar parte del proceso de auditoría con herramientas propias en
  Python.

Este proyecto es también mi forma de aprender Python aplicado a
ciberseguridad: cada script nace de una necesidad real del laboratorio,
no de un ejercicio aislado.

## Estado actual

🚧 En desarrollo activo. Este repositorio se actualiza de forma continua
conforme avanzo en cada fase.

## Estructura del repositorio

- `scripts/` — Herramientas en Python para auditoría SMB (enumeración,
  validación de objetivos, generación de reportes).
- `docs/` — Documentación técnica: configuración de servidores, análisis
  de protocolo, misconfiguraciones y su explotación/corrección.

## Hoja de ruta

- [x] Script de auditoría SMB (validación de entrada, manejo de errores,
      timeout y reintento, detección de hallazgos críticos)
- [x] Servidor Samba endurecido (SMB3 mínimo, firma y cifrado
      obligatorios, sin sesiones anónimas)
- [x] Análisis del protocolo NTLM con capturas propias (Wireshark):
      negociación, desafío, respuesta y verificación
- [ ] Servidor Samba deliberadamente vulnerable (misconfiguraciones
      controladas: permisos abiertos, acceso anónimo, SMB1, etc.)
- [ ] Explotación documentada de cada misconfiguración
- [ ] Detección: qué rastro deja cada ataque en los logs
- [ ] Corrección de cada vulnerabilidad, con validación posterior
- [ ] Escalada de privilegios en Linux a partir de malas configuraciones
      (permisos, SUID)

## Entorno de pruebas

Todo el contenido de este repositorio se ha generado y probado
exclusivamente en un laboratorio propio y aislado (máquinas virtuales
bajo mi control). Ninguna técnica mostrada aquí se ha aplicado contra
sistemas de terceros sin autorización.

## Motivación

Este proyecto forma parte de mi aprendizaje autodidacta en pentesting y
programación. Documento tanto los aciertos como los errores del proceso,
porque creo que el camino para llegar a una solución importa tanto como
la solución misma.
