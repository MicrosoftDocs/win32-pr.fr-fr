---
title: RID-Previous-allocation-attribut pool
description: Contient le pool d’identificateurs relatifs (RID) à partir duquel un contrôleur de domaine est alloué.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory RID-Previous-allocation-pool Attribute
- Schéma AD de l’attribut rIDPreviousAllocationPool
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15438d55c9540ecca873395cc329058bc0773399
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844938"
---
# <a name="rid-previous-allocation-pool-attribute"></a>RID-Previous-allocation-attribut pool

L’attribut **RID-Previous-allocation-pool** contient le pool d’identificateurs relatifs (RID) à partir duquel un contrôleur de domaine est alloué. Cet attribut est une valeur de huit octets qui contient une paire d’entiers de 4 octets qui représentent les valeurs de début et de fin du pool RID. La valeur de départ est dans les quatre octets inférieurs et la valeur de fin se trouve dans les quatre octets supérieurs.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | RID-précédent-allocation-pool         |
| LDAP-Display-Name | rIDPreviousAllocationPool            |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.372               |
| System-ID-GUID    | 6617188a-8f3c-11d0-afda-00c04fd930c9 |
| Syntaxe            | [**Défini**](s-interval.md)       |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|----------------------------------------|
| ID de lien                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vrai                                   |
| Est de valeur unique       | Vrai                                   |
| Est indexé             | Faux                                  |
| Dans le catalogue global      | Faux                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Classes utilisées dans        | [**RID-définir**](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|----------------------------------------|
| ID de lien                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vrai                                   |
| Est de valeur unique       | Vrai                                   |
| Est indexé             | Faux                                  |
| Dans le catalogue global      | Faux                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Classes utilisées dans        | [**RID-définir**](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|----------------------------------------|
| ID de lien                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vrai                                   |
| Est de valeur unique       | Vrai                                   |
| Est indexé             | Faux                                  |
| Dans le catalogue global      | Faux                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Classes utilisées dans        | [**RID-définir**](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|----------------------------------------|
| ID de lien                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vrai                                   |
| Est de valeur unique       | Vrai                                   |
| Est indexé             | Faux                                  |
| Dans le catalogue global      | Faux                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Classes utilisées dans        | [**RID-définir**](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|----------------------------------------|
| ID de lien                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vrai                                   |
| Est de valeur unique       | Vrai                                   |
| Est indexé             | Faux                                  |
| Dans le catalogue global      | Faux                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Classes utilisées dans        | [**RID-définir**](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|----------------------------------------|
| ID de lien                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vrai                                   |
| Est de valeur unique       | Vrai                                   |
| Est indexé             | Faux                                  |
| Dans le catalogue global      | Faux                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Classes utilisées dans        | [**RID-définir**](c-ridset.md)<br/> |



 

 





