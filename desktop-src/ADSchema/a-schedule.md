---
title: Attribut de planification
description: Objet BLOB de planification tel que défini par le service de travail Windows NT. Utilisé par la réplication.
ms.assetid: 5eb6409d-3fb5-4368-8b7f-ce19567b7260
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de planification
- Schéma AD de l’attribut de planification
topic_type:
- apiref
api_name:
- Schedule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b65ff20b9eaba0c8429f5fec164e44a3e4b842e82bfddcca61461f6832f55d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022217"
---
# <a name="schedule-attribute"></a>Attribut de planification

Objet BLOB de planification tel que défini par le service de travail Windows NT. Utilisé par la réplication.



| Entrée | Valeur |
|-------------------|-------------------------------------------------------|
| CN                | Planifier                                              |
| LDAP-Display-Name | schedule                                              |
| Taille              | \-                                                    |
| Mettre à jour le privilège  | \-                                                    |
| Fréquence des mises à jour  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.211                                |
| System-ID-GUID    | dd712224-10e4-11d0-a05f-00aa006c33ed                  |
| Syntaxe            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Faux                                                                                                                                                                                                                                                                            |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                             |
| Est indexé             | Faux                                                                                                                                                                                                                                                                            |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-Site-Paramètres**](c-ntdssitesettings.md)<br/> [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-abonné**](c-ntfrssubscriber.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Faux                                                                                                                                                                                                                                                                            |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                             |
| Est indexé             | Faux                                                                                                                                                                                                                                                                            |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-Site-Paramètres**](c-ntdssitesettings.md)<br/> [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-abonné**](c-ntfrssubscriber.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                            |
| MAPI-Id                | \-                                                                                                                                                            |
| System-Only            | Faux                                                                                                                                                         |
| Est de valeur unique       | Vrai                                                                                                                                                          |
| Est indexé             | Faux                                                                                                                                                         |
| Dans le catalogue global      | Faux                                                                                                                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                  |
| Range-Lower            | \-                                                                                                                                                            |
| Range-Upper            | \-                                                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                                                    |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-Site-Paramètres**](c-ntdssitesettings.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Faux                                                                                                                                                                                                                                                                            |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                             |
| Est indexé             | Faux                                                                                                                                                                                                                                                                            |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-Site-Paramètres**](c-ntdssitesettings.md)<br/> [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-abonné**](c-ntfrssubscriber.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Faux                                                                                                                                                                                                                                                                            |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                             |
| Est indexé             | Faux                                                                                                                                                                                                                                                                            |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-Site-Paramètres**](c-ntdssitesettings.md)<br/> [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-abonné**](c-ntfrssubscriber.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Faux                                                                                                                                                                                                                                                                            |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                             |
| Est indexé             | Faux                                                                                                                                                                                                                                                                            |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-Site-Paramètres**](c-ntdssitesettings.md)<br/> [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-abonné**](c-ntfrssubscriber.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Faux                                                                                                                                                                                                                                                                            |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                             |
| Est indexé             | Faux                                                                                                                                                                                                                                                                            |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-Site-Paramètres**](c-ntdssitesettings.md)<br/> [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-abonné**](c-ntfrssubscriber.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



 

 





