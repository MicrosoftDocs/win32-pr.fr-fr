---
title: Attribut Admin-Count
description: Indique qu’un objet donné a fait passer ses ACL à une valeur plus sécurisée par le système, car il était membre de l’un des groupes d’administration (directement ou transitivement).
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Admin-Count
- Schéma AD de l’attribut adminCount
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d652d53627643e1028ee73cc67678119c689e46d8f4ec289c92ca32127e098dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022847"
---
# <a name="admin-count-attribute"></a>Attribut Admin-Count

Indique qu’un objet donné a fait passer ses ACL à une valeur plus sécurisée par le système, car il était membre de l’un des groupes d’administration (directement ou transitivement).



| Entrée | Valeur |
|-------------------|-----------------------------------------------------|
| CN                | Admin-Count                                         |
| LDAP-Display-Name | adminCount                                          |
| Taille              | 4 octets                                             |
| Mettre à jour le privilège  | Cette valeur est définie par le système.                    |
| Fréquence des mises à jour  | Lorsqu’un objet est ajouté à un groupe d’administration. |
| Attribute-Id      | 1.2.840.113556.1.4.150                              |
| System-ID-GUID    | bf967918-0de6-11d0-a285-00aa003049e2                |
| Syntaxe            | [**Énumération**](s-enumeration.md)                |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------|
| ID de lien                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Faux                                                                 |
| Est de valeur unique       | Vrai                                                                  |
| Est indexé             | Faux                                                                 |
| Dans le catalogue global      | Faux                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------|
| ID de lien                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Faux                                                                 |
| Est de valeur unique       | Vrai                                                                  |
| Est indexé             | Faux                                                                 |
| Dans le catalogue global      | Faux                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------|
| ID de lien                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Faux                                                                 |
| Est de valeur unique       | Vrai                                                                  |
| Est indexé             | Faux                                                                 |
| Dans le catalogue global      | Faux                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------|
| ID de lien                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Faux                                                                 |
| Est de valeur unique       | Vrai                                                                  |
| Est indexé             | Faux                                                                 |
| Dans le catalogue global      | Faux                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------|
| ID de lien                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Faux                                                                 |
| Est de valeur unique       | Vrai                                                                  |
| Est indexé             | Faux                                                                 |
| Dans le catalogue global      | Faux                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------|
| ID de lien                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Faux                                                                 |
| Est de valeur unique       | Vrai                                                                  |
| Est indexé             | Faux                                                                 |
| Dans le catalogue global      | Faux                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> [**Utilisateur**](c-user.md)<br/> |



 

 





