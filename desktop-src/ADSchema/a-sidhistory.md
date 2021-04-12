---
title: Attribut SID-History
description: Contient les SID précédents utilisés pour l’objet si l’objet a été déplacé à partir d’un autre domaine.
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut SID-History
- Schéma Active Directory de l’attribut sIDHistory
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16474a6463fc99e7ed2c1d2b1a2cdbf6ea9b6614
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479924"
---
# <a name="sid-history-attribute"></a>Attribut SID-History

Contient les SID précédents utilisés pour l’objet si l’objet a été déplacé à partir d’un autre domaine. Chaque fois qu’un objet est déplacé d’un domaine à un autre, un nouveau SID est créé et le nouveau SID devient l’objectSID. Le SID précédent est ajouté à la propriété sIDHistory.



| Entrée | Valeur |
|-------------------|------------------------------------------------|
| CN                | SID-History                                    |
| LDAP-Display-Name | sIDHistory                                     |
| Taille              | \-                                             |
| Mettre à jour le privilège  | Cette valeur est définie par le système.               |
| Fréquence des mises à jour  | Chaque fois que l’objet est déplacé vers un nouveau domaine. |
| Attribute-Id      | 1.2.840.113556.1.4.609                         |
| System-ID-GUID    | 17eb4278-d167-11d0-b002-0000f80367c1           |
| Syntaxe            | [**Chaîne (SID)**](s-string-sid.md)            |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Vrai                                                         |
| Est de valeur unique       | Faux                                                        |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Faux                                                        |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Faux                                                        |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Faux                                                        |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Faux                                                        |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Faux                                                        |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



 

 





