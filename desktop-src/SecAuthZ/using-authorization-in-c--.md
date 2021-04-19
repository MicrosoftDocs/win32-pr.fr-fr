---
description: Utilisez l’API du gestionnaire d’autorisations pour contrôler l’accès aux ressources de l’application.
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: Utilisation de l’autorisation en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6771d16748d3c04680b545a83e382fa3d5ce78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523318"
---
# <a name="using-authorization-in-c"></a><span data-ttu-id="604fd-103">Utilisation de l’autorisation en C++</span><span class="sxs-lookup"><span data-stu-id="604fd-103">Using Authorization in C++</span></span>

<span data-ttu-id="604fd-104">Vous pouvez utiliser l’API du gestionnaire d’autorisations pour contrôler l’accès aux ressources de l’application.</span><span class="sxs-lookup"><span data-stu-id="604fd-104">You can use the Authorization Manager API to control access to application resources.</span></span>

<span data-ttu-id="604fd-105">Si vous disposez d’une solution de contrôle d’accès existante basée sur des [*listes de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) et que vous souhaitez éviter de convertir cette solution pour utiliser le gestionnaire d’autorisations, vous pouvez continuer à utiliser les listes de contrôle d’accès pour contrôler l’accès aux ressources.</span><span class="sxs-lookup"><span data-stu-id="604fd-105">If you have an existing access control solution based on [*access control lists*](/windows/desktop/SecGloss/a-gly) (ACLs) and want to avoid converting this solution to use Authorization Manager, you can continue to use ACLs to control access to resources.</span></span> <span data-ttu-id="604fd-106">Pour plus d’informations sur le contrôle de l’accès aux ressources à l’aide de listes de contrôle d’accès, consultez [définition d’autorisations avec des ACL en c++](defining-permissions-with-acls-in-c--.md), [établissement d’un contexte client à partir d’un SID en c++](establishing-a-client-context-from-a-sid-in-c--.md)et [vérification de l’accès client avec des ACL en c++](verifying-client-access-with-acls-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="604fd-106">For information about controlling access to resources using ACLs, see [Defining Permissions with ACLs in C++](defining-permissions-with-acls-in-c--.md), [Establishing a Client Context from a SID in C++](establishing-a-client-context-from-a-sid-in-c--.md), and [Verifying Client Access with ACLs in C++](verifying-client-access-with-acls-in-c--.md).</span></span>

> [!Note]  
> <span data-ttu-id="604fd-107">Pour les grandes entreprises, il existe un compromis entre la surcharge administrative et les performances.</span><span class="sxs-lookup"><span data-stu-id="604fd-107">For large enterprises, there is a trade-off between administrative overhead and performance.</span></span> <span data-ttu-id="604fd-108">À mesure que le nombre de ressources et d’utilisateurs sécurisés augmente, l’administration des ACL devient plus complexe.</span><span class="sxs-lookup"><span data-stu-id="604fd-108">As the number of secured resources and users increases, the administration of ACLs becomes more complicated.</span></span> <span data-ttu-id="604fd-109">Les performances ne sont pas affectées, car toutes les informations requises sur les droits d’accès sont distribuées aux ressources sécurisées.</span><span class="sxs-lookup"><span data-stu-id="604fd-109">Performance is not affected because all required information about access rights is distributed to the secured resources.</span></span> <span data-ttu-id="604fd-110">Les performances du gestionnaire d’autorisations sont affectées par la mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="604fd-110">The performance of Authorization Manager is affected by scaling.</span></span>

 

<span data-ttu-id="604fd-111">Pour plus d’informations sur les autres tâches d’autorisation, consultez [prise en charge des tâches pour l’autorisation en C++](supporting-tasks-for-authorization-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="604fd-111">For information about other authorization tasks, see [Supporting Tasks for Authorization in C++](supporting-tasks-for-authorization-in-c--.md).</span></span>



| <span data-ttu-id="604fd-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="604fd-112">Topic</span></span>                                                                                                                | <span data-ttu-id="604fd-113">Description</span><span class="sxs-lookup"><span data-stu-id="604fd-113">Description</span></span>                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="604fd-114">Définition des autorisations en C++</span><span class="sxs-lookup"><span data-stu-id="604fd-114">Defining Permissions in C++</span></span>](defining-permissions-in-c--.md)                                                       | <span data-ttu-id="604fd-115">Définissez les utilisateurs qui ont accès aux ressources d’application en créant un magasin de stratégies d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="604fd-115">Define which users have access to which application resources by creating an authorization policy store.</span></span> |
| [<span data-ttu-id="604fd-116">Vérification de l’accès client à une ressource demandée en C++</span><span class="sxs-lookup"><span data-stu-id="604fd-116">Verifying Client Access to a Requested Resource in C++</span></span>](verifying-client-access-to-a-requested-resource-in-c--.md) | <span data-ttu-id="604fd-117">Vérifiez si le client a accès à une ou plusieurs opérations.</span><span class="sxs-lookup"><span data-stu-id="604fd-117">Check whether the client has access to one or more operations.</span></span>                                           |
| [<span data-ttu-id="604fd-118">Délégation de la définition des autorisations en C++</span><span class="sxs-lookup"><span data-stu-id="604fd-118">Delegating the Defining of Permissions in C++</span></span>](delegating-the-defining-of-permissions-in-c--.md)                   | <span data-ttu-id="604fd-119">Déléguez l’administration des magasins de stratégies d’autorisation stockés dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="604fd-119">Delegate the administration of authorization policy stores that are stored in Active Directory.</span></span>          |



 

 

 
