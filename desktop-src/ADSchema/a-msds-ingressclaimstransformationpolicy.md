---
title: ms-DS-entrée-revendications-transformation-stratégie (attribut)
description: Il s’agit d’un lien vers un objet de stratégie de transformation de revendications pour les revendications entrantes (revendications entrantes dans cette forêt) à partir du domaine approuvé.
ms.assetid: 67f87782-85ed-41bb-a60d-f6c11fcda80e
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs ms-DS-entrée-revendications-transformation-stratégie
- Schéma Active Directory de l’attribut msDS-IngressClaimsTransformationPolicy
topic_type:
- apiref
api_name:
- ms-DS-Ingress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50e3c187a4cb3b2a465257b408a1f5603c756ba
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519850"
---
# <a name="ms-ds-ingress-claims-transformation-policy-attribute"></a>ms-DS-entrée-revendications-transformation-stratégie (attribut)

Il s’agit d’un lien vers un objet de stratégie de transformation de revendications pour les revendications entrantes (revendications entrantes dans cette forêt) à partir du domaine approuvé. Cela s’applique uniquement à une approbation inter-forêts sortante ou bidirectionnelle. Si ce lien est absent, toutes les revendications entrantes sont supprimées.



| Entrée | Valeur |
|-------------------|--------------------------------------------|
| CN                | ms-DS-entrée-revendications-transformation-stratégie |
| LDAP-Display-Name | msDS-IngressClaimsTransformationPolicy     |
| Taille              | \-                                         |
| Mettre à jour le privilège  | \-                                         |
| Fréquence des mises à jour  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.2191                    |
| System-ID-GUID    | 86284c08-0c6e-1540-8b15-75147d23d20d       |
| Syntaxe            | [**Object(DS-DN)**](s-object-ds-dn.md)    |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | 2190                                                 |
| MAPI-Id                | \-                                                   |
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Faux                                                |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> |



 

 





