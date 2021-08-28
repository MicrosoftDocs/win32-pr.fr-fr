---
title: Location (attribut)
description: Emplacement de l’utilisateur, tel qu’un numéro de bureau.
ms.assetid: 3ee97a61-6dce-4f41-b03a-a475706f3cbd
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut Location
- Schéma Active Directory de l’attribut Location
topic_type:
- apiref
api_name:
- Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7e8080ffa24c9b2a147e6e3ec76f586a92fba3456aa1f80d2875c1292940232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705769"
---
# <a name="location-attribute-ad-schema"></a>Emplacement, attribut (schéma Active Directory)

Emplacement de l’utilisateur, tel qu’un numéro de bureau.



| Entrée | Valeur |
|-------------------|---------------------------------------------|
| CN                | Emplacement                                    |
| LDAP-Display-Name | location                                    |
| Taille              | \-                                          |
| Mettre à jour le privilège  | \-                                          |
| Fréquence des mises à jour  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.222                      |
| System-ID-GUID    | 09dcb79f-165f-11d0-a064-00aa006c33ed        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                               |
| System-Only            | Faux                                                                                                                                                            |
| Est de valeur unique       | Vrai                                                                                                                                                             |
| Est indexé             | Vrai                                                                                                                                                             |
| Dans le catalogue global      | Vrai                                                                                                                                                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                |
| Range-Upper            | 1 024                                                                                                                                                             |
| Search-Flags           | 0x00000001                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                       |
| Classes utilisées dans        | [**Computer**](c-computer.md)<br/> [**File d’attente d’impression**](c-printqueue.md)<br/> [**Site**](c-site.md)<br/> [**Sous-réseau**](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Faux                                                                                                                                                                                              |
| Est de valeur unique       | Vrai                                                                                                                                                                                               |
| Est indexé             | Vrai                                                                                                                                                                                               |
| Dans le catalogue global      | Vrai                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1 024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classes utilisées dans        | [**Computer**](c-computer.md)<br/> [**File d’attente d’impression**](c-printqueue.md)<br/> [**divertissement**](c-room.md)<br/> [**Site**](c-site.md)<br/> [**Sous-réseau**](c-subnet.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------|
| ID de lien                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Faux                                                                   |
| Est de valeur unique       | Vrai                                                                    |
| Est indexé             | Vrai                                                                    |
| Dans le catalogue global      | Vrai                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                            |
| Range-Lower            | 0                                                                       |
| Range-Upper            | 1 024                                                                    |
| Search-Flags           | 0x00000001                                                              |
| System-Flags           | 0x00000010                                                              |
| Classes utilisées dans        | [**Site**](c-site.md)<br/> [**Sous-réseau**](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Faux                                                                                                                                                                                              |
| Est de valeur unique       | Vrai                                                                                                                                                                                               |
| Est indexé             | Vrai                                                                                                                                                                                               |
| Dans le catalogue global      | Vrai                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1 024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classes utilisées dans        | [**Computer**](c-computer.md)<br/> [**File d’attente d’impression**](c-printqueue.md)<br/> [**divertissement**](c-room.md)<br/> [**Site**](c-site.md)<br/> [**Sous-réseau**](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Faux                                                                                                                                                                                              |
| Est de valeur unique       | Vrai                                                                                                                                                                                               |
| Est indexé             | Vrai                                                                                                                                                                                               |
| Dans le catalogue global      | Vrai                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1 024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classes utilisées dans        | [**Computer**](c-computer.md)<br/> [**File d’attente d’impression**](c-printqueue.md)<br/> [**divertissement**](c-room.md)<br/> [**Site**](c-site.md)<br/> [**Sous-réseau**](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Faux                                                                                                                                                                                              |
| Est de valeur unique       | Vrai                                                                                                                                                                                               |
| Est indexé             | Vrai                                                                                                                                                                                               |
| Dans le catalogue global      | Vrai                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1 024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classes utilisées dans        | [**Computer**](c-computer.md)<br/> [**File d’attente d’impression**](c-printqueue.md)<br/> [**divertissement**](c-room.md)<br/> [**Site**](c-site.md)<br/> [**Sous-réseau**](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Faux                                                                                                                                                                                              |
| Est de valeur unique       | Vrai                                                                                                                                                                                               |
| Est indexé             | Vrai                                                                                                                                                                                               |
| Dans le catalogue global      | Vrai                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1 024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classes utilisées dans        | [**Computer**](c-computer.md)<br/> [**File d’attente d’impression**](c-printqueue.md)<br/> [**divertissement**](c-room.md)<br/> [**Site**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



 

 





