---
title: Description, attribut (schéma Active Directory)
description: Contient la description à afficher pour un objet. Cette valeur est limitée en tant que valeur à valeur unique pour la compatibilité descendante dans certains cas, mais elle est autorisée à plusieurs valeurs dans d’autres. Consultez la section Notes.
ms.assetid: 97dad871-5db0-4d1e-b931-1b053559f9c2
ms.tgt_platform: multiple
keywords:
- Attribut Description-schéma Active Directory
- Attribut Description-schéma Active Directory
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f53c344b026a89a3f579d1eb7fc7002a8a0410d28fd9b43d05882a4285eb73b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961727"
---
# <a name="description-attribute-ad-schema"></a>Description, attribut (schéma Active Directory)

Contient la description à afficher pour un objet. Cette valeur est limitée en tant que valeur à valeur unique pour la compatibilité descendante dans certains cas, mais elle est autorisée à plusieurs valeurs dans d’autres. Consultez la section Notes.



| Entrée | Valeur |
|-------------------|---------------------------------------------|
| CN                | Description                                 |
| LDAP-Display-Name | description                                 |
| Taille              | \-                                          |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.      |
| Fréquence des mises à jour  | Chaque fois que la description doit être modifiée.   |
| Attribute-Id      | 2.5.4.13                                    |
| System-ID-GUID    | bf967950-0de6-11d0-a285-00aa003049e2        |
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
|------------------------|------------------------------------------------------------------------------|
| ID de lien                | \-                                                                           |
| MAPI-Id                | 0x806F                                                                       |
| System-Only            | Faux                                                                        |
| Est de valeur unique       | Faux                                                                        |
| Est indexé             | Faux                                                                        |
| Dans le catalogue global      | Vrai                                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                 |
| Range-Lower            | 0                                                                            |
| Range-Upper            | 1 024                                                                         |
| Search-Flags           | 0x00000000                                                                   |
| System-Flags           | 0x00000010                                                                   |
| Classes utilisées dans        | [**Sam-domaine**](c-samdomain.md)<br/> [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                         |
| MAPI-Id                | 0x806F                                                                                                                                     |
| System-Only            | Faux                                                                                                                                      |
| Est de valeur unique       | Faux                                                                                                                                      |
| Est indexé             | Faux                                                                                                                                      |
| Dans le catalogue global      | Vrai                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                               |
| Range-Lower            | 0                                                                                                                                          |
| Range-Upper            | 1 024                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| Classes utilisées dans        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Retour au début**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | 0x806F                          |
| System-Only            | Faux                           |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 0                               |
| Range-Upper            | 1 024                            |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1 024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classes utilisées dans        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Retour au début**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**Réseau IP**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1 024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classes utilisées dans        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Retour au début**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**Réseau IP**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1 024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classes utilisées dans        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Retour au début**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**Réseau IP**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1 024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classes utilisées dans        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Retour au début**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**Réseau IP**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="remarks"></a>Remarques

L’attribut Description est implémenté en tant qu’attribut à valeurs multiples dans le schéma pour les cas où cela est autorisé. Pour un objet qui n’est pas une classe managée SAM, la description est à valeurs multiples. Pour un attribut qui est une classe managée SAM, l’attribut Description est à valeur unique. Les classes gérées SAM sont destinées à des éléments tels que les principaux de sécurité. par exemple, si vous avez, par exemple, un conteneur ou une classe de votre choix, le schéma vous permet d’utiliser plusieurs valeurs. Ce comportement de l’attribut Description est utilisé pour la compatibilité descendante avec les systèmes d’exploitation antérieurs, car l’attribut existait dans les API SAM avant l’existence d’AD.

 

 





