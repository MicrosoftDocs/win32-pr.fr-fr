---
description: Le Gestionnaire d’autorisations propose un cadre souple d’intégration du contrôle d’accès basé sur les rôles aux applications. Il permet aux administrateurs utilisant ces applications de proposer un accès par le biais de rôles utilisateur attribués associés à des fonctions.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Modèle du gestionnaire d’autorisations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20973b8b3e1b35780cc771c04302430b44352a112745842dcbdb66e92b948aad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784192"
---
# <a name="authorization-manager-model"></a>Modèle du gestionnaire d’autorisations

Le Gestionnaire d’autorisations propose un cadre souple d’intégration du contrôle d’accès basé sur les rôles aux applications. Il permet aux administrateurs utilisant ces applications de proposer un accès par le biais de rôles utilisateur attribués associés à des fonctions.

Les applications de Gestionnaire d'autorisations stockent la stratégie d'autorisation sous forme de magasins d'autorisations stockés dans les fichiers Active Directory ou XML, et appliquent cette stratégie au moment de l'exécution.

Les applications appellent ensuite une méthode de vérification d’accès au moment de l’exécution qui vérifie l’accès aux informations de stratégie dans le magasin d’autorisations.

La stratégie d’autorisation comprend les éléments suivants :

-   [Magasins de stratégies, applications et étendues](policy-stores--applications--and-scopes.md)
-   [Utilisateurs et groupes](users-and-groups.md)
-   [Opérations et tâches](operations-and-tasks.md)
-   [Rôles](roles.md)
-   [Règles métier](business-rules.md)
-   [Regroupements](collections.md)

 

 



