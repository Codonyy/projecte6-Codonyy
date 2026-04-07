
# T06: Projecte Nexus — Implantació de PKI i Signatura Digital Corporativa

## Breu descripció

Implementació d’una **Infraestructura de Clau Pública (PKI)** per permetre la signatura digital corporativa dins l’empresa **Projecte Nexus**, garantint la integritat, autenticitat i no repudi dels documents interns.

---

## Introducció

Després d’assegurar la confidencialitat de les dades, Nexus necessita modernitzar la gestió documental substituint la signatura en paper per **signatures digitals corporatives**.

L’objectiu és crear una **Prova de Concepte (PoC)** que permeti:

- Emissió de certificats digitals interns
- Signatura oficial de documents PDF
- Validació de documents sense dependre de tercers

---

## Fase 1: Desplegament de la CA (Certificate Authority)

Instal·lació d’una Autoritat de Certificació en **Ubuntu Server**.

### Objectius

- Crear una CA corporativa pròpia
- Generar la clau arrel
- Preparar la infraestructura d’emissió de certificats

---

## Fase 2: Sol·licitud i Emissió de Certificats

Procés realitzat entre:

- **Administrador Nexus** (Servidor)
- **Treballador Nexus** (Client)

### Procés

1. Crear la sol·licitud de certificat (CSR)
2. Enviar la sol·licitud a la CA
3. Signar i emetre el certificat
4. Instal·lar:
   - Certificat arrel (CA)
   - Certificat client

---

## Fase 3: Signatura Digital i Verificació

Signatura d’un document PDF mitjançant certificat digital.

### Eina utilitzada

```
Adobe Acrobat Reader
```

### Verificacions

- Identitat del signant
- Integritat del document
- Validació del certificat

---

## Conceptes Clau

### Clau Pública

- Es comparteix amb altres usuaris
- Serveix per verificar signatures
- Forma part del certificat digital

### Clau Privada

- Només la té el propietari
- Serveix per signar documents
- No s’ha de compartir mai

---

## Lliurables

### Memòria tècnica (`memoria.md`)

Inclou:

- Instal·lació de la CA a Ubuntu Server
- Procediment de sol·licitud del certificat
- Creació del certificat client
- Instal·lació de la CA al client
- Instal·lació del certificat client
- Procés de signatura i verificació
- Explicació clau pública vs clau privada

---

### Evidència de la signatura

Incloure al repositori:

- PDF signat digitalment
- Certificat arrel de la CA:
