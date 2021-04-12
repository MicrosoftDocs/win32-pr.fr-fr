---
description: Le Gestionnaire d’autorisations propose un cadre souple d’intégration du contrôle d’accès basé sur les rôles aux applications. Il permet aux administrateurs utilisant ces applications de proposer un accès par le biais de rôles utilisateur attribués associés à des fonctions.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Modèle du gestionnaire d’autorisations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3455c9577f24b260bd02f947d0af99ec85570bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321221"
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

 

 



