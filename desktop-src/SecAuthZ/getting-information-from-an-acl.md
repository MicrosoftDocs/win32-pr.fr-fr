---
description: Plusieurs fonctions sont fournies pour récupérer les informations de contrôle d’accès à partir d’une liste de contrôle d’accès (ACL).
ms.assetid: a0839c49-09e9-4407-8702-051b88ef2231
title: Obtention d’informations à partir d’une liste de contrôle d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5ef90d40058efd19790829f92c37a976359cbc61601d72fa2fee4cc4a93ec7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913671"
---
# <a name="getting-information-from-an-acl"></a>Obtention d’informations à partir d’une liste de contrôle d’accès

Plusieurs fonctions sont fournies pour récupérer les informations de contrôle d’accès à partir d’une [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL). Celles-ci incluent des fonctions permettant de déterminer les droits d’accès qu’une liste de contrôle d’accès accorde ou audite à un [tiers de confiance](trustees.md)spécifié. D’autres fonctions vous permettent d’extraire des informations sur les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) d’une liste de contrôle d’accès.

La fonction [**GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) récupère un tableau de structures [**d' \_ accès explicites**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) qui décrivent les ACE dans une liste de contrôle d’accès. Cela peut être utile lors de la copie d’informations ACE d’une liste de contrôle d’accès à une autre. Par exemple, un appel à **GetExplicitEntriesFromAcl** pour obtenir des informations sur les ACE dans une ACL peut être suivi en passant les structures d' **\_ accès explicites** retournées dans un appel à la fonction [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) pour créer des ACE équivalentes dans une nouvelle liste de contrôle d’accès.

La fonction [**GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) vous permet de déterminer les droits d’accès effectifs qu’une liste DACL accorde à un tiers de confiance spécifié. Les droits d’accès effectifs du tiers de confiance sont les droits d’accès qu’un DACL accorde au tiers de confiance ou à tous les groupes dont le tiers de confiance est membre. **GetEffectiveRightsFromAcl** vérifie tous les ACE access-allowed et Access-denied dans la liste DACL spécifiée.

**Utilisez les étapes suivantes pour déterminer les droits d’accès d’un tiers de confiance à un objet.**

1.  Appelez la fonction [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) ou [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) pour obtenir un pointeur vers la liste DACL d’un objet.
2.  Appelez la fonction [**GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) pour récupérer les droits d’accès que la liste DACL accorde à un tiers de confiance spécifié.

La fonction [**GetAuditedPermissionsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getauditedpermissionsfromacla) vous permet de vérifier une liste SACL pour déterminer les droits d’accès audités pour un tiers de confiance spécifié ou pour tous les groupes dont le tiers de confiance est membre. Les droits d’audit indiquent les types de tentatives d’accès qui obligent le système à générer un enregistrement d’audit dans le journal des événements de sécurité. La fonction retourne deux [*masques d’accès*](/windows/desktop/SecGloss/a-gly): l’un contenant les droits d’accès surveillés pour les échecs de tentatives d’accès et l’autre contenant les droits d’accès surveillés pour un accès réussi. **GetAuditedPermissionsFromAcl** vérifie toutes les entrées de contrôle d’intégrité système dans une liste SACL.

 

 
