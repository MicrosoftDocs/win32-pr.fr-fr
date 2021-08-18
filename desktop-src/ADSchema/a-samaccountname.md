---
title: SAM-Account-Name (attribut)
description: nom d’ouverture de session utilisé pour prendre en charge les clients et les serveurs exécutant des versions antérieures du système d’exploitation, par exemple Windows NT 4,0, Windows 95, Windows 98 et LAN Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut SAM-Account-Name
- Schéma AD de l’attribut sAMAccountName
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74aa558f63c2e1822f1435cdafd6290755b92b4d5e34c329d8472693f37185d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022227"
---
# <a name="sam-account-name-attribute"></a>SAM-Account-Name (attribut)

nom d’ouverture de session utilisé pour prendre en charge les clients et les serveurs exécutant des versions antérieures du système d’exploitation, par exemple Windows NT 4,0, Windows 95, Windows 98 et LAN Manager.

Cet attribut doit comporter 20 caractères ou moins pour prendre en charge les clients antérieurs, et ne peut pas contenir l’un des caractères suivants :

-   "/ \\ \[ \] : ; \| = , + \* ? < >



| Entrée | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| CN                | Nom de compte SAM                                                                         |
| LDAP-Display-Name | sAMAccountName                                                                           |
| Taille              | 20 caractères au maximum.                                                                   |
| Mettre à jour le privilège  | Administrateur de domaine                                                                     |
| Fréquence des mises à jour  | Cette valeur doit être affectée lorsque l’enregistrement de compte est créé et ne doit pas être modifié. |
| Attribute-Id      | 1.2.840.113556.1.4.221                                                                   |
| System-ID-GUID    | 3e0abfd0-126a-11d0-a060-00aa006c33ed                                                     |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                              |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Vrai                                                         |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Vrai                                                         |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Vrai                                                         |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Vrai                                                         |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Vrai                                                         |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Vrai                                                         |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



 

 





