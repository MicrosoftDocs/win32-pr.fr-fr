---
title: Attribut Last-Logon-timestamp
description: Il s’agit de l’heure de la dernière connexion de l’utilisateur au domaine.
ms.assetid: 6c94bccb-1e0a-421c-a00c-5f6e6389690f
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut Last-Logon-timestamp
- Schéma AD de l’attribut lastLogonTimestamp
topic_type:
- apiref
api_name:
- Last-Logon-Timestamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaea56a7456a46b7583633992f77e6fd836276151e6c9f6b792ba1abdd36b4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322149"
---
# <a name="last-logon-timestamp-attribute"></a>Attribut Last-Logon-timestamp

Il s’agit de l’heure de la dernière connexion de l’utilisateur au domaine. Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC). Chaque fois qu’un utilisateur ouvre une session, la valeur de cet attribut est lue à partir du DC. Si la valeur est plus ancienne \[ `current_time - msDS-LogonTimeSyncInterval` \] , la valeur est mise à jour. La mise à jour initiale après l’augmentation du niveau fonctionnel du domaine est calculée comme suit : 14 jours moins un pourcentage aléatoire de 5 jours.



| Entrée | Valeur |
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| CN                | Last-Logon-timestamp                                                                                                   |
| LDAP-Display-Name | lastLogonTimestamp                                                                                                     |
| Taille              | \-                                                                                                                     |
| Mettre à jour le privilège  | Cette valeur est définie par le système.                                                                                       |
| Fréquence des mises à jour  | Lorsque l’utilisateur ouvre une session et si cette valeur est antérieure à l’heure actuelle moins la valeur de msDS-LogonTimeSyncInterval. |
| Attribute-Id      | 1.2.840.113556.1.4.1696                                                                                                |
| System-ID-GUID    | c0e20a04-0e5a-4ff3-9482-5efeaecd7060                                                                                   |
| Syntaxe            | [**Défini**](s-interval.md)                                                                                         |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------|
| ID de lien                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Vrai                                                              |
| Est de valeur unique       | Vrai                                                              |
| Est indexé             | Faux                                                             |
| Dans le catalogue global      | Faux                                                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classes utilisées dans        | [**ms-DS-Bindable-objet**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



 

 





