---
title: Attribut Entry-TTL
description: Cet attribut opérationnel est géré par le serveur et semble être présent dans chaque entrée dynamique.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut Entry-TTL
- Schéma AD de l’attribut entryTTL
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcd3e06304824ba51431b00b6a5b90d24d7719194dd84974470a101d5f6a1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961558"
---
# <a name="entry-ttl-attribute"></a>Attribut Entry-TTL

Cet attribut opérationnel est géré par le serveur et semble être présent dans chaque entrée dynamique. L’attribut n’est pas présent lorsque l’entrée ne contient pas la classe d’objet dynamicObject. La valeur de cet attribut est le temps, en secondes, pendant lequel l’entrée continuera d’exister avant d’apparaître dans le répertoire. En l’absence d’opérations d’actualisation, il est garanti que les valeurs retournées en lisant l’attribut dans deux recherches successives sont sans importance. La plus petite valeur autorisée est 0, ce qui indique que l’entrée peut disparaître sans avertissement. L’attribut est marqué non-MODIFICATION par l’utilisateur, car il ne peut être modifié qu’à l’aide de l’opération d’actualisation.



| Entrée | Valeur |
|-------------------|---------------------------------------------|
| CN                | TTL d’entrée                                   |
| LDAP-Display-Name | entryTTL                                    |
| Taille              | 4 octets. Maximum = 1 an, valeur par défaut = 1 jour. |
| Mettre à jour le privilège  | \-                                          |
| Fréquence des mises à jour  | \-                                          |
| Attribute-Id      | 1.3.6.1.4.1.1466.101.119.3                  |
| System-ID-GUID    | d213decc-d81a-4384-AAC2-dcfcfd631cf8        |
| Syntaxe            | [**Énumération**](s-enumeration.md)        |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Faux                                                |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classes utilisées dans        | [**Objet dynamique**](c-dynamicobject.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Faux                                                |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classes utilisées dans        | [**Objet dynamique**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Faux                                                |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classes utilisées dans        | [**Objet dynamique**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Faux                                                |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classes utilisées dans        | [**Objet dynamique**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Faux                                                |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classes utilisées dans        | [**Objet dynamique**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Faux                                                |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classes utilisées dans        | [**Objet dynamique**](c-dynamicobject.md)<br/> |



 

 





