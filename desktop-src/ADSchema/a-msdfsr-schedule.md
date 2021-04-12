---
title: MS-DFSR-attribut Schedule
description: Contient la planification de réplication pour le service de réplication système de fichiers DFS (DFS).
ms.assetid: 6dfcce16-44a4-4f7a-93ba-0c0d50605682
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de planification MS-DFSR
- msDFSR-schéma AD d’attribut de planification
topic_type:
- apiref
api_name:
- ms-DFSR-Schedule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118ab92c656899d8275f0ff63ae43b412cf9742e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480132"
---
# <a name="ms-dfsr-schedule-attribute"></a>MS-DFSR-attribut Schedule

Contient la planification de réplication pour le service de réplication système de fichiers DFS (DFS).



| Entrée | Valeur |
|-------------------|-------------------------------------------------------|
| CN                | MS-DFSR-planification                                      |
| LDAP-Display-Name | msDFSR-planification                                       |
| Taille              | \-                                                    |
| Mettre à jour le privilège  | \-                                                    |
| Fréquence des mises à jour  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.6.13.3.14                            |
| System-ID-GUID    | 4699f15f-a71f-48e2-9ff5-5897c0759205                  |
| Syntaxe            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | Faux                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                          |
| Range-Lower            | 336                                                                                                                                   |
| Range-Upper            | 336                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Classes utilisées dans        | [**MS-DFSR-le groupe**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-connexion**](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | Faux                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                          |
| Range-Lower            | 336                                                                                                                                   |
| Range-Upper            | 336                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Classes utilisées dans        | [**MS-DFSR-le groupe**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-connexion**](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | Faux                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                          |
| Range-Lower            | 336                                                                                                                                   |
| Range-Upper            | 336                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Classes utilisées dans        | [**MS-DFSR-le groupe**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-connexion**](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | Faux                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                          |
| Range-Lower            | 336                                                                                                                                   |
| Range-Upper            | 336                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Classes utilisées dans        | [**MS-DFSR-le groupe**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-connexion**](c-msdfsr-connection.md)<br/> |



## <a name="remarks"></a>Notes

L’attribut fait partie de la prise en charge du service de réplication système de fichiers DFS (DFS).

 

 





