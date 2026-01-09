# Esquema de flujo de conexión entre cliente y servidor FTP 

## Canal de control
* Común a ambos modos
* Se establece al inicio de la conexión.
* Permanece abierto durante toda la sesión.
* Transporta comandos FTP.
┌─────────────┐          TCP 21          ┌─────────────┐
│ Cliente FTP │ ───────────────────────▶ │ Servidor FTP│
│             │ ◀─────────────────────── │             │
└─────────────┘   comandos / respuestas  └─────────────┘

## Modo activo
* Canal de control:
┌─────────────┐          TCP 21          ┌─────────────┐
│ Cliente FTP │ ───────────────────────▶ │ Servidor FTP│
└─────────────┘                          └─────────────┘

* Canal de datos:
┌─────────────┐          TCP 20          ┌─────────────┐
│ Cliente FTP │ ◀─────────────────────── │ Servidor FTP│
└─────────────┘                          └─────────────┘

## Modo pasivo
* Canal de control:
┌─────────────┐          TCP 21           ┌─────────────┐
│ Cliente FTP │ ───────────────────────▶ │ Servidor FTP│
└─────────────┘                          └─────────────┘

* Canal de datos:
┌─────────────┐     TCP puerto pasivo    ┌─────────────┐
│ Cliente FTP │ ───────────────────────▶ │ Servidor FTP│
└─────────────┘                          └─────────────┘
