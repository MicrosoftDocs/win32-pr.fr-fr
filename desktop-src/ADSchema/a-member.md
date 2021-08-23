---
title: Attribut de membre
description: Liste des utilisateurs qui appartiennent au groupe.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- Attribut de membre schéma Active Directory
- attribut de membre schéma Active Directory
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1efe13163946cb5be6ca83b5d0c7f964b8d6b1981ce45f79166af01bd62e6c9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705509"
---
# <a name="member-attribute"></a>Attribut de membre

Liste des utilisateurs qui appartiennent au groupe.



| Entrée | Valeur |
|-------------------|-------------------------------------------------------|
| CN                | Membre                                                |
| LDAP-Display-Name | member                                                |
| Taille              | \-                                                    |
| Mettre à jour le privilège  | Administrateur de domaine                                  |
| Fréquence des mises à jour  | Chaque fois qu’un utilisateur est ajouté à un groupe ou en est supprimé. |
| Attribute-Id      | 2.5.4.31                                              |
| System-ID-GUID    | bf9679c0-0de6-11d0-a285-00aa003049e2                  |
| Syntaxe            | [**Object(DS-DN)**](s-object-ds-dn.md)               |



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
|------------------------|-----------------------------------------------------------------------------------------|
| ID de lien                | 2                                                                                       |
| MAPI-Id                | 0x8009                                                                                  |
| System-Only            | Faux                                                                                   |
| Est de valeur unique       | Faux                                                                                   |
| Est indexé             | Faux                                                                                   |
| Dans le catalogue global      | Vrai                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000012                                                                              |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> [**Groupes de noms**](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Faux                                                                                                                                 |
| Est de valeur unique       | Faux                                                                                                                                 |
| Est indexé             | Faux                                                                                                                                 |
| Dans le catalogue global      | Vrai                                                                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> [**Groupes de noms**](c-groupofnames.md)<br/> [**Groupe MSMQ**](c-msmq-group.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|-------------------------------------|
| ID de lien                | 2                                   |
| MAPI-Id                | 0x8009                              |
| System-Only            | Faux                               |
| Est de valeur unique       | Faux                               |
| Est indexé             | Faux                               |
| Dans le catalogue global      | Vrai                                |
| Descripteur de sécurité NT | O :BAG : BAD : S :                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000012                          |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Faux                                                                                                                                 |
| Est de valeur unique       | Faux                                                                                                                                 |
| Est indexé             | Faux                                                                                                                                 |
| Dans le catalogue global      | Vrai                                                                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> [**Groupes de noms**](c-groupofnames.md)<br/> [**Groupe MSMQ**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Faux                                                                                                                                 |
| Est de valeur unique       | Faux                                                                                                                                 |
| Est indexé             | Faux                                                                                                                                 |
| Dans le catalogue global      | Vrai                                                                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> [**Groupes de noms**](c-groupofnames.md)<br/> [**Groupe MSMQ**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Faux                                                                                                                                 |
| Est de valeur unique       | Faux                                                                                                                                 |
| Est indexé             | Faux                                                                                                                                 |
| Dans le catalogue global      | Vrai                                                                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> [**Groupes de noms**](c-groupofnames.md)<br/> [**Groupe MSMQ**](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Faux                                                                                                                                 |
| Est de valeur unique       | Faux                                                                                                                                 |
| Est indexé             | Faux                                                                                                                                 |
| Dans le catalogue global      | Vrai                                                                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> [**Groupes de noms**](c-groupofnames.md)<br/> [**Groupe MSMQ**](c-msmq-group.md)<br/> |



 

 





