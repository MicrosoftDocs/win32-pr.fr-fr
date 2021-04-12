---
title: Attribut options
description: Un champ de bits, où la signification des bits varie d’un objectClass à un objectClass. Peut se produire sur les objets inter-site-transport, NTDS-Connection, NTDS-DSA, NTDS-site-Settings et Site-Link.
ms.assetid: 07495cc1-1db0-4e0d-afbe-b21d2b50b6a1
ms.tgt_platform: multiple
keywords:
- Attribut options schéma Active Directory
- attribut options schéma Active Directory
topic_type:
- apiref
api_name:
- Options
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cdd970a805816e941c9eb017bf6b96302eef2b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479989"
---
# <a name="options-attribute"></a>Attribut options

Un champ de bits, où la signification des bits varie d’un objectClass à un objectClass. Peut se produire sur les objets inter-site-transport, NTDS-Connection, NTDS-DSA, NTDS-site-Settings et Site-Link.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | Options                              |
| LDAP-Display-Name | options                              |
| Taille              | 4 octets                              |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.307               |
| System-ID-GUID    | 19195a53-6da0-11d0-afd3-00c04fd930c9 |
| Syntaxe            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Faux                                                                                                                                                                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                   |
| Est indexé             | Faux                                                                                                                                                                                                                                                                  |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-site-paramètres**](c-ntdssitesettings.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Faux                                                                                                                                                                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                   |
| Est indexé             | Faux                                                                                                                                                                                                                                                                  |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-site-paramètres**](c-ntdssitesettings.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Faux                                                                                                                                                                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                   |
| Est indexé             | Faux                                                                                                                                                                                                                                                                  |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-site-paramètres**](c-ntdssitesettings.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Faux                                                                                                                                                                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                   |
| Est indexé             | Faux                                                                                                                                                                                                                                                                  |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-site-paramètres**](c-ntdssitesettings.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Faux                                                                                                                                                                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                   |
| Est indexé             | Faux                                                                                                                                                                                                                                                                  |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-site-paramètres**](c-ntdssitesettings.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Faux                                                                                                                                                                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                   |
| Est indexé             | Faux                                                                                                                                                                                                                                                                  |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-site-paramètres**](c-ntdssitesettings.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Faux                                                                                                                                                                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                   |
| Est indexé             | Faux                                                                                                                                                                                                                                                                  |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**NTDS-connexion**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-site-paramètres**](c-ntdssitesettings.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



 

 





