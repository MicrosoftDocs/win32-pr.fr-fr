---
description: Windows prend en charge un ensemble de fonctions qui créent une liste de contrôle d’accès (ACL) ou modifient les entrées de contrôle d’accès (ACE) dans une ACL existante.
ms.assetid: 71301aab-1040-4f61-855f-2b891c8b6077
title: Création ou modification d’une liste de contrôle d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0deb72bcd1a1c805dd8524027601952dda0eac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863246"
---
# <a name="creating-or-modifying-an-acl"></a>Création ou modification d’une liste de contrôle d’accès

Windows prend en charge un ensemble de fonctions qui créent une [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) ou modifient les entrées de contrôle d' [*accès*](/windows/desktop/SecGloss/a-gly) (ACE) dans une ACL existante.

La fonction [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) crée une liste de contrôle d’accès. **SetEntriesInAcl** peut spécifier un ensemble complet d’ACE pour la liste de contrôle d’accès (ACL), ou il peut fusionner une ou plusieurs nouvelles entrées de contrôle d’accès avec les ACE d’une liste ACL existante. La fonction **SetEntriesInAcl** utilise un tableau de structures d' [**\_ accès explicites**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) pour spécifier les informations relatives aux nouvelles entrées du nouveau. Chaque structure d' **\_ accès explicite** contient des informations qui décrivent une seule entrée de contrôle d’accès. Ces informations incluent les droits d’accès, le type d’entrée du contrôle d’accès, les indicateurs qui contrôlent l’héritage ACE et une structure de [**tiers de confiance**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) qui identifie le tiers de confiance.

**Pour ajouter une nouvelle entrée du contrôle d’accès à une liste ACL existante**

1.  Utilisez la fonction [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) ou [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) pour récupérer la liste DACL ou SACL existante à partir du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)d’un objet.
2.  Pour chaque nouvelle entrée du contrôle d’accès, appelez la fonction [**BuildExplicitAccessWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildexplicitaccesswithnamea) pour remplir une structure d' [**\_ accès explicite**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) avec les informations qui décrivent l’entrée du contrôle d’accès.
3.  Appelez [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla), en spécifiant l’ACL existante et un tableau de structures d' [**\_ accès explicites**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) pour les nouvelles entrées du contrôle d’accès. La fonction **SetEntriesInAcl** alloue et initialise la liste de contrôle d’accès et ses ACE.
4.  Appelez la fonction [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) ou [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) pour attacher la nouvelle liste de contrôle d’accès au descripteur de sécurité de l’objet.

Si l’appelant spécifie une liste de contrôle d’accès (ACL) existante, [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) fusionne les nouvelles informations ACE avec les ACE existantes dans la liste de contrôle d’accès. Prenons le cas, par exemple, dans lequel la liste de contrôle d’accès existante accorde l’accès à un tiers de confiance spécifié et une structure d' [**\_ accès explicite**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) refuse l’accès au même tiers de confiance. Dans ce cas, **SetEntriesInAcl** ajoute une nouvelle entrée de contrôle d’accès refusée pour le tiers de confiance, supprime ou modifie l’ACE access-allowed pour le tiers de confiance.

Pour obtenir un exemple de code qui fusionne une nouvelle entrée du contrôle d’accès dans une liste ACL existante, consultez [modification des ACL d’un objet en C++](modifying-the-acls-of-an-object-in-c--.md).

 

 
