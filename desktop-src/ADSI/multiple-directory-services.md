---
title: Plusieurs services d’annuaire
description: L’un des défis de l’utilisation d’un environnement informatique distribué consiste à identifier et à localiser des ressources telles que des utilisateurs, des groupes, des files d’attente à l’impression et des documents.
ms.assetid: 66929290-b830-4768-a2ae-604d1a9de5c4
ms.tgt_platform: multiple
keywords:
- ADSI des services d’annuaire multiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc2e174fc1b07564f1cca6c12093a289a0c865a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309246"
---
# <a name="multiple-directory-services"></a><span data-ttu-id="e7e33-104">Plusieurs services d’annuaire</span><span class="sxs-lookup"><span data-stu-id="e7e33-104">Multiple Directory Services</span></span>

<span data-ttu-id="e7e33-105">L’un des défis de l’utilisation d’un environnement informatique distribué consiste à identifier et à localiser des ressources telles que des utilisateurs, des groupes, des files d’attente à l’impression et des documents.</span><span class="sxs-lookup"><span data-stu-id="e7e33-105">One challenge of working within a distributed computing environment is identifying and locating resources such as users, groups, print queues, and documents.</span></span> <span data-ttu-id="e7e33-106">Un service d’annuaire fait partie d’un environnement informatique distribué qui fournit un moyen de localiser et d’identifier les utilisateurs et les ressources disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="e7e33-106">A directory service is the part of a distributed computing environment that provides a way to locate and identify the users and resources available in the system.</span></span> <span data-ttu-id="e7e33-107">Un service d’annuaire est semblable à un annuaire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="e7e33-107">A directory service is like a phone directory.</span></span> <span data-ttu-id="e7e33-108">En fonction du nom d’une personne ou d’une ressource, il fournit les données nécessaires pour accéder à la personne ou à la ressource.</span><span class="sxs-lookup"><span data-stu-id="e7e33-108">Given a name for a person or a resource, it provides the data necessary to access that person or resource.</span></span> <span data-ttu-id="e7e33-109">Vous n’avez pas besoin de commencer par lier des données pour accéder à une ressource sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="e7e33-109">You do not have to start with binding data to access a resource on the network.</span></span>

<span data-ttu-id="e7e33-110">La plupart des entreprises disposent déjà de nombreux répertoires différents en place.</span><span class="sxs-lookup"><span data-stu-id="e7e33-110">Most enterprises already have many different directories in place.</span></span> <span data-ttu-id="e7e33-111">Par exemple, les systèmes d’exploitation réseau, les systèmes de messagerie électronique et les produits de groupware possèdent tous leurs propres répertoires.</span><span class="sxs-lookup"><span data-stu-id="e7e33-111">For example, network operating systems, electronic mail systems, and "groupware" products all have their own directories.</span></span> <span data-ttu-id="e7e33-112">De nombreux problèmes surviennent quand une seule entreprise déploie plusieurs annuaires.</span><span class="sxs-lookup"><span data-stu-id="e7e33-112">Many issues arise when a single enterprise deploys multiple directories.</span></span> <span data-ttu-id="e7e33-113">Ces problèmes incluent notamment la convivialité, la cohérence des données, le coût de développement et le coût de support, entre autres.</span><span class="sxs-lookup"><span data-stu-id="e7e33-113">These issues include usability, data consistency, development cost, and support cost, among others.</span></span>

<span data-ttu-id="e7e33-114">Ces problèmes sont résolus dans ADSI, car il existe un ensemble unique et cohérent d’interfaces qui peuvent être utilisées pour gérer et utiliser n’importe quel service d’annuaire ayant un fournisseur ADSI.</span><span class="sxs-lookup"><span data-stu-id="e7e33-114">These issues are addressed in ADSI, in that there is provided a single, consistent, open set of interfaces that can be used for managing and using any directory service that has an ADSI provider.</span></span>

 

 




