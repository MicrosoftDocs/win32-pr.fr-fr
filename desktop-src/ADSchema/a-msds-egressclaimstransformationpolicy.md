---
title: attribut ms-DS-Sortss-claims-transformation-Policy
description: Il s’agit d’un lien vers un objet de stratégie de transformation de revendications pour les revendications de sortie (revendications quittant cette forêt) vers le domaine approuvé.
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de stratégie de sortie ms-DS-Sortss-claims-transformation-Policy
- Schéma Active Directory de l’attribut msDS-EgressClaimsTransformationPolicy
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3978944b6ae85fcc5fd33682abec7dd3fff0057
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943176"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a>attribut ms-DS-Sortss-claims-transformation-Policy

Il s’agit d’un lien vers un objet de stratégie de transformation de revendications pour les revendications de sortie (revendications quittant cette forêt) vers le domaine approuvé. Cela s’applique uniquement à une approbation inter-forêts entrante ou bidirectionnelle. Lorsque ce lien n’est pas présent, toutes les revendications sont autorisées à sortie en l’absence de.



| Entrée | Valeur |
|-------------------|-------------------------------------------|
| CN                | ms-DS-sortie-revendications-transformation-stratégie |
| LDAP-Display-Name | msDS-EgressClaimsTransformationPolicy     |
| Taille              | \-                                        |
| Mettre à jour le privilège  | \-                                        |
| Fréquence des mises à jour  | \-                                        |
| Attribute-Id      | 1.2.840.113556.1.4.2192                   |
| System-ID-GUID    | c137427e-9a73-b040-9190-1b095bb43288      |
| Syntaxe            | [**Object(DS-DN)**](s-object-ds-dn.md)   |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | 2192                                                 |
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



 

 





