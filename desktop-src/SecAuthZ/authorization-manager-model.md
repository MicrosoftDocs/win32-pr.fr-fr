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
# <a name="authorization-manager-model"></a><span data-ttu-id="7b7e2-104">Modèle du gestionnaire d’autorisations</span><span class="sxs-lookup"><span data-stu-id="7b7e2-104">Authorization Manager Model</span></span>

<span data-ttu-id="7b7e2-105">Le Gestionnaire d’autorisations propose un cadre souple d’intégration du contrôle d’accès basé sur les rôles aux applications.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-105">Authorization Manager provides a flexible framework for integrating role-based access control into applications.</span></span> <span data-ttu-id="7b7e2-106">Il permet aux administrateurs utilisant ces applications de proposer un accès par le biais de rôles utilisateur attribués associés à des fonctions.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-106">It enables administrators who use those applications to provide access through assigned user roles that relate to job functions.</span></span>

<span data-ttu-id="7b7e2-107">Les applications de Gestionnaire d'autorisations stockent la stratégie d'autorisation sous forme de magasins d'autorisations stockés dans les fichiers Active Directory ou XML, et appliquent cette stratégie au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-107">Authorization Manager applications store authorization policy in the form of authorization stores that are stored in Active Directory or XML files and apply authorization policy at run time.</span></span>

<span data-ttu-id="7b7e2-108">Les applications appellent ensuite une méthode de vérification d’accès au moment de l’exécution qui vérifie l’accès aux informations de stratégie dans le magasin d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-108">Applications then call a run-time access check method that checks access against the policy information in the authorization store.</span></span>

<span data-ttu-id="7b7e2-109">La stratégie d’autorisation comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7b7e2-109">Authorization policy includes the following parts:</span></span>

-   [<span data-ttu-id="7b7e2-110">Magasins de stratégies, applications et étendues</span><span class="sxs-lookup"><span data-stu-id="7b7e2-110">Policy Stores, Applications, and Scopes</span></span>](policy-stores--applications--and-scopes.md)
-   [<span data-ttu-id="7b7e2-111">Utilisateurs et groupes</span><span class="sxs-lookup"><span data-stu-id="7b7e2-111">Users and Groups</span></span>](users-and-groups.md)
-   [<span data-ttu-id="7b7e2-112">Opérations et tâches</span><span class="sxs-lookup"><span data-stu-id="7b7e2-112">Operations and Tasks</span></span>](operations-and-tasks.md)
-   [<span data-ttu-id="7b7e2-113">Rôles</span><span class="sxs-lookup"><span data-stu-id="7b7e2-113">Roles</span></span>](roles.md)
-   [<span data-ttu-id="7b7e2-114">Règles métier</span><span class="sxs-lookup"><span data-stu-id="7b7e2-114">Business Rules</span></span>](business-rules.md)
-   [<span data-ttu-id="7b7e2-115">Regroupements</span><span class="sxs-lookup"><span data-stu-id="7b7e2-115">Collections</span></span>](collections.md)

 

 



