---
title: Attribut Tombstone-Lifetime
description: Nombre de jours avant la suppression d’un objet supprimé des services d’annuaire.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Tombstone-Lifetime
- Schéma AD de l’attribut tombstoneLifetime
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c96d440b82f488e7968f787ae52d9f431350bee6050bd50b385f5751f51e76a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644949"
---
# <a name="tombstone-lifetime-attribute"></a>Attribut Tombstone-Lifetime

Nombre de jours avant la suppression d’un objet supprimé des services d’annuaire. Cela vous aide à supprimer des objets des serveurs répliqués et à empêcher les restaurations de réintroduire un objet supprimé. Cette valeur se trouve dans l’objet service d’annuaire de la carte réseau de configuration.



| Entrée | Valeur |
|-------------------|-----------------------------------------------------------|
| CN                | Tombstone-Lifetime                                        |
| LDAP-Display-Name | tombstoneLifetime                                         |
| Taille              | 4 octets. La valeur par défaut est de 60 jours quand aucune valeur n’est entrée. |
| Mettre à jour le privilège  | \-                                                        |
| Fréquence des mises à jour  | \-                                                        |
| Attribute-Id      | 1.2.840.113556.1.2.54                                     |
| System-ID-GUID    | 16c3a860-1273-11d0-a060-00aa006c33ed                      |
| Syntaxe            | [**Énumération**](s-enumeration.md)                      |



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
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Faux                                            |
| Est de valeur unique       | Vrai                                             |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Faux                                            |
| Est de valeur unique       | Vrai                                             |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Faux                                            |
| Est de valeur unique       | Vrai                                             |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Faux                                            |
| Est de valeur unique       | Vrai                                             |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Faux                                            |
| Est de valeur unique       | Vrai                                             |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Faux                                            |
| Est de valeur unique       | Vrai                                             |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Faux                                            |
| Est de valeur unique       | Vrai                                             |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



 

 





