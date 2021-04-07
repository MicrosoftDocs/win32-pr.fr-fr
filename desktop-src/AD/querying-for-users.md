---
title: Interrogation des utilisateurs
description: Pour rechercher un utilisateur, la requête doit contenir l’expression de recherche \ 0034 ;( (utilisateur objectClass) (objectCategory person)) \ 0034 ;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- utilisateurs Active Directory, interrogation pour les utilisateurs
- Active Directory, utiliser, utilisateurs, interroger des utilisateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39037ff805dab753aae066d1f6611432b28ea73c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724460"
---
# <a name="querying-for-users"></a><span data-ttu-id="20c25-105">Interrogation des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="20c25-105">Querying for Users</span></span>

<span data-ttu-id="20c25-106">Pour rechercher un utilisateur, la requête doit contenir l’expression de recherche « (& (objectClass = user) (objectCategory = person)) ».</span><span class="sxs-lookup"><span data-stu-id="20c25-106">To query for a user, the query must contain the search expression "(&(objectClass=user)(objectCategory=person))".</span></span>

<span data-ttu-id="20c25-107">Étant donné que la classe Computer est une sous-classe de l’utilisateur, une requête contenant uniquement (objectClass = user) retourne des objets User et Computer.</span><span class="sxs-lookup"><span data-stu-id="20c25-107">Because the computer class is a subclass of user, a query containing only (objectClass=user) would return user objects and computer objects.</span></span> <span data-ttu-id="20c25-108">En outre, la catégorie d’objet de l’objet utilisateur est personne (pas utilisateur); par conséquent, l’expression (objectCategory = user) ne retourne aucun utilisateur.</span><span class="sxs-lookup"><span data-stu-id="20c25-108">Also, the object category of the user object is person (not user); therefore, the expression (objectCategory=user) does not return any users.</span></span> <span data-ttu-id="20c25-109">Si vous utilisez l’expression (objectCategory = person), la requête retourne les objets User et contact.</span><span class="sxs-lookup"><span data-stu-id="20c25-109">If you use the expression (objectCategory=person), the query returns user objects and contact objects.</span></span>

<span data-ttu-id="20c25-110">Les utilisateurs peuvent être placés dans n’importe quel conteneur ou unité d’organisation d’un domaine, ainsi que la racine du domaine.</span><span class="sxs-lookup"><span data-stu-id="20c25-110">Users can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="20c25-111">Cela signifie que les utilisateurs peuvent se trouver à de nombreux emplacements dans la hiérarchie de répertoires.</span><span class="sxs-lookup"><span data-stu-id="20c25-111">This means that users can be in numerous locations in the directory hierarchy.</span></span> <span data-ttu-id="20c25-112">Vous pouvez effectuer une recherche détaillée « (objectCategory = user) » pour rechercher tous les utilisateurs dans un conteneur, une unité d’organisation, un domaine, une arborescence de domaine ou une forêt, en fonction de l’objet auquel le pointeur [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) que vous utilisez est lié.</span><span class="sxs-lookup"><span data-stu-id="20c25-112">You can perform a deep search for "(objectCategory=user)" to find all users in a container, organizational unit, domain, domain tree, or forest—depending on the object that the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer you are using is bound to.</span></span>

 

 