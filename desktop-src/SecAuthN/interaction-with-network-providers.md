---
description: Explique les interactions entre Winlogon et les fournisseurs de réseau.
ms.assetid: 09d0b5ce-e2ac-40d7-bc35-272c5f831788
title: Interaction avec les fournisseurs de réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d3eeadb7a9f4d8137e1d9b1ef7ff2430910cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011278"
---
# <a name="interaction-with-network-providers"></a>Interaction avec les fournisseurs de réseau

Vous pouvez configurer un système pour qu’il prenne en charge zéro, un ou plusieurs fournisseurs réseau. Chacun de ces fournisseurs de réseau peut spécifier qu’il nécessite un traitement d’authentification interactive spécial. Cette fonctionnalité permet aux réseaux installés de collecter des informations d’identification et d’authentification spécifiques à chaque réseau, tout en les autorisant à les collecter pendant une ouverture de session normale et sous l’parapluie sécurisé du [*contexte*](../secgloss/c-gly.md) et du Bureau de [*Winlogon*](../secgloss/w-gly.md) .

Winlogon appelle les fournisseurs réseau dans un certain nombre de cas. Après une ouverture de session réussie, Winlogon appelle les fournisseurs de réseau afin qu’ils puissent collecter les [*informations d’identification*](../secgloss/c-gly.md) et authentifier l’utilisateur pour son réseau. Winlogon appelle également des fournisseurs réseau lorsque les utilisateurs modifient leur mot de passe. Cela permet à chaque utilisateur de conserver un seul mot de passe à utiliser sur tous les réseaux.

La structure d’informations de [**\_ \_ notification \_ wlx MPR**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) est utilisée pour fournir des informations d’identification et d’authentification dans les fonctions Gina appropriées. Cette structure comprend les membres suivants.



| Membre             | Description                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **pszUserName**    | Nom de compte de l’utilisateur connecté.                                                                                                                                                      |
| **pszDomain**      | Nom de domaine de l’utilisateur connecté. Tous les modèles d’authentification ne disposent pas d’un concept de domaine (ou de son équivalent). ce membre peut donc avoir la **valeur null**.                                              |
| **pszPassword**    | Lorsque l’utilisateur a donné un mot de passe en texte clair lors de l’authentification, il permet à d’autres fournisseurs de réseau d’utiliser le même mot de passe (pour obtenir une ouverture de session unique) sans inviter l’utilisateur.    |
| **pszOldPassword** | Après une modification de mot de passe, en fournissant le mot de passe d’origine ici et le nouveau mot de passe dans le membre **pszPassword** , permet aux fournisseurs de réseau de mettre à niveau leur mot de passe sans inviter l’utilisateur. |



 

Une [*Gina*](../secgloss/g-gly.md) n’a pas besoin de fournir ces informations aux fournisseurs réseau. Si un pointeur **null** est passé au lieu d’un pointeur de structure valide, les fournisseurs de réseau invitent l’utilisateur à fournir des informations.

 

 
