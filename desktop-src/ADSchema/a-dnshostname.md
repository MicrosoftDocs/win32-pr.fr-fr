---
title: Attribut DNS-Host-Name
description: Nom de l’ordinateur enregistré dans DNS.
ms.assetid: ba655adb-cb70-47f2-820f-c5b0749d3e70
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut DNS-Host-Name
- Schéma AD de l’attribut dNSHostName
topic_type:
- apiref
api_name:
- DNS-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7580a58e5d3042633a9dd665354bc883b4fdb87c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519489"
---
# <a name="dns-host-name-attribute"></a>Attribut DNS-Host-Name

Nom de l’ordinateur enregistré dans DNS.



| Entrée | Valeur |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Nom d’hôte DNS                                                               |
| LDAP-Display-Name | dNSHostName                                                                 |
| Taille              | Chaque segment peut avoir 63 caractères. La longueur totale peut être de 255 caractères. |
| Mettre à jour le privilège  | Administrateur de domaine                                                        |
| Fréquence des mises à jour  | Lorsque l’ordinateur est nommé.                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.619                                                      |
| System-ID-GUID    | 72e39547-7b18-11d1-adef-00c04fd8d5cd                                        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                 |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Faux                                                                                                                                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                       |
| Est indexé             | Faux                                                                                                                                                                                                                      |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2 048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classes utilisées dans        | [**Autorité de certification**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**Infrastructure à clé publique-service d’inscription**](c-pkienrollmentservice.md)<br/> [**Serveur**](c-server.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Faux                                                                                                                                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                       |
| Est indexé             | Faux                                                                                                                                                                                                                      |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2 048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classes utilisées dans        | [**Autorité de certification**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**Infrastructure à clé publique-service d’inscription**](c-pkienrollmentservice.md)<br/> [**Serveur**](c-server.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|---------------------------------------|
| ID de lien                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Faux                                 |
| Est de valeur unique       | Vrai                                  |
| Est indexé             | Faux                                 |
| Dans le catalogue global      | Vrai                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                          |
| Range-Lower            | 0                                     |
| Range-Upper            | 2 048                                  |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes utilisées dans        | [**Serveur**](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Faux                                                                                                                                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                       |
| Est indexé             | Faux                                                                                                                                                                                                                      |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2 048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classes utilisées dans        | [**Autorité de certification**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**Infrastructure à clé publique-service d’inscription**](c-pkienrollmentservice.md)<br/> [**Serveur**](c-server.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Faux                                                                                                                                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                       |
| Est indexé             | Faux                                                                                                                                                                                                                      |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2 048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classes utilisées dans        | [**Autorité de certification**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**Infrastructure à clé publique-service d’inscription**](c-pkienrollmentservice.md)<br/> [**Serveur**](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Faux                                                                                                                                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                       |
| Est indexé             | Faux                                                                                                                                                                                                                      |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2 048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classes utilisées dans        | [**Autorité de certification**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**Infrastructure à clé publique-service d’inscription**](c-pkienrollmentservice.md)<br/> [**Serveur**](c-server.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Faux                                                                                                                                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                       |
| Est indexé             | Faux                                                                                                                                                                                                                      |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2 048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classes utilisées dans        | [**Autorité de certification**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**Infrastructure à clé publique-service d’inscription**](c-pkienrollmentservice.md)<br/> [**Serveurs**](c-server.md)<br/> |



 

 





