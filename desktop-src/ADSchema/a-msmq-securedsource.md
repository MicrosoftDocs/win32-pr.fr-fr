---
title: MSMQ-Secured-attribut source
description: Dans le cadre d’un objet MSMQ, il est défini en appelant l’API MQCreateQueue ou MQSetProperties. Il détermine si MSMQ accepte uniquement les messages provenant d’une source sécurisée (https, par exemple) pour cette file d’attente.
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de source sécurisé MSMQ-
- Schéma AD d’attribut MSMQ-SecuredSource
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dd005cedcd650aa0604a85e78a46d10f1e01b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519769"
---
# <a name="msmq-secured-source-attribute"></a>MSMQ-Secured-attribut source

Dans le cadre d’un objet MSMQ, il est défini en appelant l’API MQCreateQueue ou MQSetProperties. Il détermine si MSMQ accepte uniquement les messages provenant d’une source sécurisée (https, par exemple) pour cette file d’attente.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | MSMQ-sécurisé-source                  |
| LDAP-Display-Name | MSMQ-SecuredSource                   |
| Taille              | 4 octets                              |
| Mettre à jour le privilège  | Propriétaire de la file d’attente.                     |
| Fréquence des mises à jour  | Lorsqu’une file d’attente est créée.             |
| Attribute-Id      | 1.2.840.113556.1.4.1713              |
| System-ID-GUID    | 8bf0221b-7a06-4d63-91f0-1499941813d3 |
| Syntaxe            | [**Boolean**](s-boolean.md)         |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Vrai                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**MSMQ-file d’attente**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Vrai                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**MSMQ-file d’attente**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Vrai                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**MSMQ-file d’attente**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Vrai                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**MSMQ-file d’attente**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Vrai                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**MSMQ-file d’attente**](c-msmqqueue.md)<br/> |



 

 





