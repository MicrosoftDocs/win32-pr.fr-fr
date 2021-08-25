---
title: Attribut Repl-Interval
description: Attribut des objets Site-Link qui définit l’intervalle, en minutes, entre les cycles de réplication entre les sites de la liste de sites.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Repl-Interval
- Schéma AD de l’attribut replInterval
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb5cd02d3458684f6d70cff84435c7809fcd4c912befd65373a264f961cefd72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837439"
---
# <a name="repl-interval-attribute"></a>Attribut Repl-Interval

Attribut des objets Site-Link qui définit l’intervalle, en minutes, entre les cycles de réplication entre les sites de la liste de sites. Doit être un multiple de 15 minutes (granularité de la réplication des services de domaine intersites), un minimum de 15 minutes et un maximum de 10 080 minutes (une semaine).



| Entrée | Valeur |
|-------------------|------------------------------------------------|
| CN                | Repl-Interval                                  |
| LDAP-Display-Name | replInterval                                   |
| Taille              | 4 octets                                        |
| Mettre à jour le privilège  | Administrateur d’entreprise                       |
| Fréquence des mises à jour  | Lorsque l’intervalle de réplication doit être modifié. |
| Attribute-Id      | 1.2.840.113556.1.4.1336                        |
| System-ID-GUID    | 45ba9d1a-56fa-11d2-90d0-00c04fd91ab1           |
| Syntaxe            | [**Énumération**](s-enumeration.md)           |



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
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Faux                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                       |
| Est indexé             | Faux                                                                                                      |
| Dans le catalogue global      | Faux                                                                                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Faux                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                       |
| Est indexé             | Faux                                                                                                      |
| Dans le catalogue global      | Faux                                                                                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Faux                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                       |
| Est indexé             | Faux                                                                                                      |
| Dans le catalogue global      | Faux                                                                                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Faux                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                       |
| Est indexé             | Faux                                                                                                      |
| Dans le catalogue global      | Faux                                                                                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Faux                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                       |
| Est indexé             | Faux                                                                                                      |
| Dans le catalogue global      | Faux                                                                                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Faux                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                       |
| Est indexé             | Faux                                                                                                      |
| Dans le catalogue global      | Faux                                                                                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Faux                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                       |
| Est indexé             | Faux                                                                                                      |
| Dans le catalogue global      | Faux                                                                                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes utilisées dans        | [**Transport inter-sites**](c-intersitetransport.md)<br/> [**Lien de site**](c-sitelink.md)<br/> |



 

 





