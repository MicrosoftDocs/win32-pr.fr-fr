---
description: Instructions relatives à l’utilisation de l’API du gestionnaire d’autorisations pour définir des autorisations en C++ en créant un magasin de stratégies d’autorisation.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Définition des autorisations en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc398d811f44b69dbde8d30f135fd4f30a552bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531229"
---
# <a name="defining-permissions-in-c"></a><span data-ttu-id="a741c-103">Définition des autorisations en C++</span><span class="sxs-lookup"><span data-stu-id="a741c-103">Defining Permissions in C++</span></span>

<span data-ttu-id="a741c-104">Dans le gestionnaire d’autorisations, vous définissez les utilisateurs qui ont accès aux ressources d’application en créant un magasin de stratégies d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="a741c-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="a741c-105">Pour plus d’informations sur la définition d’autorisations avec des listes de contrôle d’accès, consultez [définition d’autorisations avec des ACL en C++](defining-permissions-with-acls-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="a741c-105">For information about defining permissions with ACLs, see [Defining Permissions with ACLs in C++](defining-permissions-with-acls-in-c--.md).</span></span>

<span data-ttu-id="a741c-106">**Pour définir des autorisations d’accès**</span><span class="sxs-lookup"><span data-stu-id="a741c-106">**To define access permissions**</span></span>

1.  <span data-ttu-id="a741c-107">Créez le magasin dans lequel la stratégie d’autorisation est définie :</span><span class="sxs-lookup"><span data-stu-id="a741c-107">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="a741c-108">Création d’un objet du magasin de stratégies d’autorisation en C++</span><span class="sxs-lookup"><span data-stu-id="a741c-108">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  <span data-ttu-id="a741c-109">Créer une section dans le magasin de stratégies d’autorisation pour une application spécifique :</span><span class="sxs-lookup"><span data-stu-id="a741c-109">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="a741c-110">Création d’un objet d’application en C++</span><span class="sxs-lookup"><span data-stu-id="a741c-110">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)  
    </dl>
3.  <span data-ttu-id="a741c-111">Définissez les opérations que l’application implémente pour accéder aux ressources et les modifier :</span><span class="sxs-lookup"><span data-stu-id="a741c-111">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="a741c-112">Définition d’opérations en C++</span><span class="sxs-lookup"><span data-stu-id="a741c-112">Defining Operations in C++</span></span>](defining-operations-in-c--.md)  
    </dl>
4.  <span data-ttu-id="a741c-113">Regroupez les opérations en tâches de haut niveau que les utilisateurs souhaitent effectuer :</span><span class="sxs-lookup"><span data-stu-id="a741c-113">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="a741c-114">Regroupement d’opérations en tâches en C++</span><span class="sxs-lookup"><span data-stu-id="a741c-114">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  <span data-ttu-id="a741c-115">Définir des rôles composés de groupes de tâches :</span><span class="sxs-lookup"><span data-stu-id="a741c-115">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="a741c-116">Regroupement de tâches en rôles en C++</span><span class="sxs-lookup"><span data-stu-id="a741c-116">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)  
    </dl><span data-ttu-id="a741c-117">Un utilisateur affecté à un rôle a l’autorisation d’effectuer n’importe quelle tâche affectée à ce rôle.</span><span class="sxs-lookup"><span data-stu-id="a741c-117">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="a741c-118">Créer des scripts pour qualifier l’accès aux tâches au moment de l’exécution :</span><span class="sxs-lookup"><span data-stu-id="a741c-118">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="a741c-119">Accès éligible avec la logique métier en C++</span><span class="sxs-lookup"><span data-stu-id="a741c-119">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)  
    </dl><span data-ttu-id="a741c-120">Cette étape est facultative.</span><span class="sxs-lookup"><span data-stu-id="a741c-120">This step is optional.</span></span>
7.  <span data-ttu-id="a741c-121">Définir des groupes d’utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="a741c-121">Define groups of users:</span></span><dl>

[<span data-ttu-id="a741c-122">Définition de groupes d’utilisateurs en C++</span><span class="sxs-lookup"><span data-stu-id="a741c-122">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)  
    </dl><span data-ttu-id="a741c-123">Ces groupes peuvent ensuite être affectés à des rôles pour déterminer les tâches qu’ils peuvent effectuer.</span><span class="sxs-lookup"><span data-stu-id="a741c-123">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="a741c-124">Ajouter des utilisateurs à des groupes d’utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="a741c-124">Add users to user groups:</span></span><dl>

[<span data-ttu-id="a741c-125">Ajout d’utilisateurs à un groupe d’applications en C++</span><span class="sxs-lookup"><span data-stu-id="a741c-125">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



