---
title: Autre attribut-bien connu-Objects
description: Contient une liste de conteneurs par GUID et nom unique. Cela permet de récupérer un objet après qu’il a été déplacé en utilisant uniquement le GUID et le nom de domaine. Chaque fois que l’objet est déplacé, le système met automatiquement à jour le nom unique.
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory d’un autre attribut des objets bien connus
- Schéma AD de l’attribut otherWellKnownObjects
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c56d8ca4de5928e8109b2503b57d1afce5909df484e607392543e85cfa63118c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923989"
---
# <a name="other-well-known-objects-attribute"></a>Autre attribut-bien connu-Objects

Contient une liste de conteneurs par GUID et nom unique. Cela permet de récupérer un objet après qu’il a été déplacé en utilisant uniquement le GUID et le nom de domaine. Chaque fois que l’objet est déplacé, le système met automatiquement à jour le nom unique.



| Entrée | Valeur |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Autres objets bien connus                                                                                                                                                                                      |
| LDAP-Display-Name | otherWellKnownObjects                                                                                                                                                                                         |
| Taille              | Exemple de récupération du conteneur utilisateurs dans le domaine Microsoft : LDAP://(WKGUID = a9d1ca15768811d1aded00c04fd8d5cd, DC = Microsoft, DC = com). Remarque : les chevrons sont remplacés par des parenthèses pour éviter les conflits XML. |
| Mettre à jour le privilège  | Administrateur de schéma                                                                                                                                                                                          |
| Fréquence des mises à jour  | Chaque fois que l’objet est déplacé.                                                                                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1359                                                                                                                                                                                       |
| System-ID-GUID    | 1ea64e5d-ac0f-11d2-90df-00c04fd91ab1                                                                                                                                                                          |
| Syntaxe            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                               |



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
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



 

 





