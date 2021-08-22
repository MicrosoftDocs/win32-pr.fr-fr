---
title: attribut ms-DS-Logon-Time-Sync-Interval
description: Cet attribut contrôle la granularité, en jours, à laquelle l’heure de la dernière ouverture de session d’un utilisateur ou d’un ordinateur, enregistrée dans l’attribut lastLogonTimestamp, est répliquée sur tous les contrôleurs de domaine d’un domaine.
ms.assetid: f1f9f1f8-df60-44b5-965d-631c4dd4ef84
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-Logon-Time-Sync-Interval
- Schéma Active Directory de l’attribut msDS-LogonTimeSyncInterval
topic_type:
- apiref
api_name:
- ms-DS-Logon-Time-Sync-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa27a1d6281eda7eea9f88a11c4ca6632422a1cfd9f0cb471aab513018c56150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118684633"
---
# <a name="ms-ds-logon-time-sync-interval-attribute"></a>attribut ms-DS-Logon-Time-Sync-Interval

Cet attribut contrôle la granularité, en jours, à laquelle l’heure de la dernière ouverture de session d’un utilisateur ou d’un ordinateur, enregistrée dans l’attribut lastLogonTimestamp, est répliquée sur tous les contrôleurs de domaine d’un domaine.



| Entrée | Valeur |
|-------------------|------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-Logon-Time-Sync-Interval                                                                             |
| LDAP-Display-Name | msDS-LogonTimeSyncInterval                                                                                 |
| Taille              | 4 octets                                                                                                    |
| Mettre à jour le privilège  | Administrateur de domaine                                                                                       |
| Fréquence des mises à jour  | Rarement, étant donné qu’il s’agit d’un paramètre de stratégie, il est mis à jour uniquement lorsqu’une modification de la stratégie à l’ensemble du domaine est souhaitée. |
| Attribute-Id      | 1.2.840.113556.1.4.1784                                                                                    |
| System-ID-GUID    | ad7940f8-e43a-4a42-83bc-d688e59ea605                                                                       |
| Syntaxe            | [**Énumération**](s-enumeration.md)                                                                       |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
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
| Dans le catalogue global      | Faux                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**Sam-domaine**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Faux                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**Sam-domaine**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Faux                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**Sam-domaine**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Faux                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**Sam-domaine**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Faux                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**Sam-domaine**](c-samdomain.md)<br/> |



 

 





