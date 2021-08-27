---
title: attribut ms-FRS-Hub-Member
description: L’attribut ms-FRS-Hub-Member permet d’enregistrer les paramètres de topologie NTFRS par défaut.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory MS-FRS-Hub-Member Attribute
- Schéma Active Directory msFRS-Hub-Member Attribute
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2f2cc1014b081ac13183144fca34c2087539de0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885706"
---
# <a name="ms-frs-hub-member-attribute"></a>attribut ms-FRS-Hub-Member

L’attribut **MS-FRS-Hub-Member** permet d’enregistrer les paramètres de topologie NTFRS par défaut. Lorsqu’un membre FRS est ajouté ou supprimé à un jeu de réplicas, ces attributs sont désignés et des ajustements appropriés sont effectués sur les connexions entre le reste des membres FRS dans le jeu de réplicas.



| Entrée | Valeur |
|-------------------|--------------------------------------------------------------------|
| CN                | MS-FRS-Hub-Member                                                  |
| LDAP-Display-Name | msFRS-Hub-Member                                                   |
| Taille              | \-                                                                 |
| Mettre à jour le privilège  | Administrateur de domaine                                               |
| Fréquence des mises à jour  | Lors de la création du jeu de réplicas ou de la modification de la topologie par défaut. |
| Attribute-Id      | 1.2.840.113556.1.4.1693                                            |
| System-ID-GUID    | 5643ff81-35b6-4ca9-9512-baf0bd0a2772                               |
| Syntaxe            | [**Object(DS-DN)**](s-object-ds-dn.md)                            |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------|
| ID de lien                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Faux                                                     |
| Est de valeur unique       | Vrai                                                      |
| Est indexé             | Faux                                                     |
| Dans le catalogue global      | Faux                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes utilisées dans        | [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------|
| ID de lien                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Faux                                                     |
| Est de valeur unique       | Vrai                                                      |
| Est indexé             | Faux                                                     |
| Dans le catalogue global      | Faux                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes utilisées dans        | [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------|
| ID de lien                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Faux                                                     |
| Est de valeur unique       | Vrai                                                      |
| Est indexé             | Faux                                                     |
| Dans le catalogue global      | Faux                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes utilisées dans        | [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------|
| ID de lien                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Faux                                                     |
| Est de valeur unique       | Vrai                                                      |
| Est indexé             | Faux                                                     |
| Dans le catalogue global      | Faux                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes utilisées dans        | [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------|
| ID de lien                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Faux                                                     |
| Est de valeur unique       | Vrai                                                      |
| Est indexé             | Faux                                                     |
| Dans le catalogue global      | Faux                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes utilisées dans        | [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a>Remarques

Il s’agit du nom unique complet d’un objet de [**membre NTFRS**](c-ntfrsmember.md) . Le nom unique est au format « CN =*&lt; computerGuid &gt;*, CN = *<Dfs Link Name>* , CN = *<Dfs Root name>* , CN = volumes DFS, CN = service de réplication de fichiers, CN = System, DC =... »

 

 





