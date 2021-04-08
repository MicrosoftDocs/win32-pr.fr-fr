---
title: attribut ms-DS-Trust-forêt-Trust-info
description: Contient les informations d’approbation de forêt (objet BLOB binaire) utilisées par le système pour un objet Trusted-Domain.
ms.assetid: 60944ff6-d2b1-4f53-8557-7d79a7d9df51
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut ms-DS-Trust-forêt-Trust-info
- Schéma Active Directory de l’attribut msDS-TrustForestTrustInfo
topic_type:
- apiref
api_name:
- ms-DS-Trust-Forest-Trust-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e259abaeae4d99b80b8ff6a390901f1c9f51e6a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744677"
---
# <a name="ms-ds-trust-forest-trust-info-attribute"></a>attribut ms-DS-Trust-forêt-Trust-info

Contient les informations d’approbation de forêt (objet BLOB binaire) utilisées par le système pour un objet Trusted-Domain.



| Entrée | Valeur |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-Trust-forêt-Trust-info                                                                                      |
| LDAP-Display-Name | msDS-TrustForestTrustInfo                                                                                          |
| Taille              | \-                                                                                                                 |
| Mettre à jour le privilège  | \-                                                                                                                 |
| Fréquence des mises à jour  | Uniquement lorsque la relation d’approbation entre les forêts change. Cela peut se produire si la topologie d’une forêt approuvée change. |
| Attribute-Id      | 1.2.840.113556.1.4.1702                                                                                            |
| System-ID-GUID    | 29cc866e-49d3-4969-942e-1dbc0925d183                                                                               |
| Syntaxe            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                              |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
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
| Dans le catalogue global      | Vrai                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Vrai                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Vrai                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Vrai                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Vrai                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> |



 

 





