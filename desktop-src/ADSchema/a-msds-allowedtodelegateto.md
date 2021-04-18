---
title: attribut ms-DS-allowed-to-Delegate-to
description: Il s’agit d’un attribut sur les objets du compte de service (compte d’ordinateur ou d’utilisateur).
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory pour l’attribut ms-DS-allowed-to-Delegate-to
- Schéma Active Directory de l’attribut msDS-AllowedToDelegateTo
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9562442d20053848e48cd2b1d501e65611f7d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106519159"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a>attribut ms-DS-allowed-to-Delegate-to

Il s’agit d’un attribut sur les objets du compte de service (compte d’ordinateur ou d’utilisateur). Elle contient une liste de noms de principaux du service (SPN). Cet attribut est utilisé pour configurer un service afin qu’il puisse obtenir des tickets de service qui peuvent être utilisés pour la délégation avec restriction.



| Entrée | Valeur |
|-------------------|---------------------------------------------|
| CN                | ms-DS-autorisé-à-déléguer-à                |
| LDAP-Display-Name | msDS-AllowedToDelegateTo                    |
| Taille              | 0 à 64 Ko                                    |
| Mettre à jour le privilège  | \-                                          |
| Fréquence des mises à jour  | Rarement                                |
| Attribute-Id      | 1.2.840.113556.1.4.1787                     |
| System-ID-GUID    | 800d94d7-b7a1-42a1-b14d-7cae1423d07f        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------------|
| ID de lien                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Faux                                                              |
| Est de valeur unique       | Faux                                                              |
| Est indexé             | Faux                                                              |
| Dans le catalogue global      | Faux                                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------------|
| ID de lien                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Faux                                                              |
| Est de valeur unique       | Faux                                                              |
| Est indexé             | Faux                                                              |
| Dans le catalogue global      | Faux                                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------------|
| ID de lien                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Faux                                                              |
| Est de valeur unique       | Faux                                                              |
| Est indexé             | Faux                                                              |
| Dans le catalogue global      | Faux                                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------------|
| ID de lien                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Faux                                                              |
| Est de valeur unique       | Faux                                                              |
| Est indexé             | Faux                                                              |
| Dans le catalogue global      | Faux                                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------------|
| ID de lien                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Faux                                                              |
| Est de valeur unique       | Faux                                                              |
| Est indexé             | Faux                                                              |
| Dans le catalogue global      | Faux                                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





