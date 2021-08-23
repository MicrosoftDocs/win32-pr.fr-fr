---
title: Attribut Given-Name
description: Contient le nom donné (prénom) de l’utilisateur.
ms.assetid: acffe751-9911-4e80-8a26-351a21a6385e
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Given-Name
- Schéma AD de l’attribut givenName
topic_type:
- apiref
api_name:
- Given-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ee788506d098123888a9389d9256dd4203cae463cf008723e99e8180750d591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706059"
---
# <a name="given-name-attribute"></a>Attribut Given-Name

Contient le nom donné (prénom) de l’utilisateur.



| Entrée | Valeur |
|-------------------|---------------------------------------------|
| CN                | Given-Name                                  |
| LDAP-Display-Name | givenName                                   |
| Taille              | \-                                          |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.      |
| Fréquence des mises à jour  | Lors de la création de l’enregistrement de l’utilisateur.          |
| Attribute-Id      | 2.5.4.42                                    |
| System-ID-GUID    | f0f8ff8e-1191-11d0-a060-00aa006c33ed        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------------|
| ID de lien                | \-                                                                 |
| MAPI-Id                | 0x3A06                                                             |
| System-Only            | Faux                                                              |
| Est de valeur unique       | Vrai                                                               |
| Est indexé             | Vrai                                                               |
| Dans le catalogue global      | Vrai                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000005                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Faux                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                   |
| Est indexé             | Vrai                                                                                                                   |
| Dans le catalogue global      | Vrai                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Faux                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                   |
| Est indexé             | Vrai                                                                                                                   |
| Dans le catalogue global      | Vrai                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Faux                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                   |
| Est indexé             | Vrai                                                                                                                   |
| Dans le catalogue global      | Vrai                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Faux                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                   |
| Est indexé             | Vrai                                                                                                                   |
| Dans le catalogue global      | Vrai                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Faux                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                   |
| Est indexé             | Vrai                                                                                                                   |
| Dans le catalogue global      | Vrai                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





