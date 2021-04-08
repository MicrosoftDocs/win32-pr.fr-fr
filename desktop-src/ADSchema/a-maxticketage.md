---
title: Attribut Max-ticket-Age
description: Cet attribut détermine la durée maximale, en heures, pendant laquelle le ticket TGT (Ticket-Granting Ticket) d’un utilisateur peut être utilisé dans le cadre de l’authentification Kerberos.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Max-ticket-Age
- Schéma AD de l’attribut maxTicketAge
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d68bca2f8dd87d37be7215e26f549424cd32b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744348"
---
# <a name="max-ticket-age-attribute"></a>Attribut Max-ticket-Age

Cet attribut détermine la durée maximale, en heures, pendant laquelle le ticket TGT (Ticket-Granting Ticket) d’un utilisateur peut être utilisé dans le cadre de l’authentification Kerberos. Lorsque le ticket TGT d’un utilisateur expire, un nouveau doit être demandé ou le ticket existant doit être renouvelé. Par défaut, ce paramètre est défini sur 10 heures dans l’objet de stratégie de groupe de domaine par défaut.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | Max-ticket-Age                       |
| LDAP-Display-Name | maxTicketAge                         |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.77                |
| System-ID-GUID    | bf9679be-0de6-11d0-a285-00aa003049e2 |
| Syntaxe            | [**Défini**](s-interval.md)       |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|----------------------------------------------------|
| ID de lien                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Faux                                              |
| Est de valeur unique       | Vrai                                               |
| Est indexé             | Faux                                              |
| Dans le catalogue global      | Faux                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|----------------------------------------------------|
| ID de lien                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Faux                                              |
| Est de valeur unique       | Vrai                                               |
| Est indexé             | Faux                                              |
| Dans le catalogue global      | Faux                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------|
| ID de lien                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Faux                                              |
| Est de valeur unique       | Vrai                                               |
| Est indexé             | Faux                                              |
| Dans le catalogue global      | Faux                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|----------------------------------------------------|
| ID de lien                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Faux                                              |
| Est de valeur unique       | Vrai                                               |
| Est indexé             | Faux                                              |
| Dans le catalogue global      | Faux                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------|
| ID de lien                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Faux                                              |
| Est de valeur unique       | Vrai                                               |
| Est indexé             | Faux                                              |
| Dans le catalogue global      | Faux                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|----------------------------------------------------|
| ID de lien                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Faux                                              |
| Est de valeur unique       | Vrai                                               |
| Est indexé             | Faux                                              |
| Dans le catalogue global      | Faux                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> |



 

 





