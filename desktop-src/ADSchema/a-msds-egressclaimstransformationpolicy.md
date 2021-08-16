---
title: attribut ms-DS-Egress-claims-Transformation-Policy
description: Il s’agit d’un lien vers un objet de stratégie de transformation de revendications pour les revendications de sortie (revendications quittant cette forêt) vers le domaine approuvé.
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- schéma AD des attributs ms-DS-Egress-claims-Transformation-Policy
- Schéma Active Directory de l’attribut msDS-EgressClaimsTransformationPolicy
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99ec71308c0ebc17942b3400d8ddd9e87ff88ea29d4f21e93047c3aa80f77128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118014652"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a>attribut ms-DS-Egress-claims-Transformation-Policy

Il s’agit d’un lien vers un objet de stratégie de transformation de revendications pour les revendications de sortie (revendications quittant cette forêt) vers le domaine approuvé. Cela s’applique uniquement à une approbation inter-forêts entrante ou bidirectionnelle. Lorsque ce lien n’est pas présent, toutes les revendications sont autorisées à sortie en l’absence de.



| Entrée | Valeur |
|-------------------|-------------------------------------------|
| CN                | ms-DS-Egress-revendications-Transformation-stratégie |
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



 

 





