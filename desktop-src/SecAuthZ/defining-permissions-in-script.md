---
description: Instructions relatives à l’utilisation de l’API du gestionnaire d’autorisations pour définir des autorisations dans le script en créant un magasin de stratégies d’autorisation.
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: Définition des autorisations dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e16f377ffa669da0b686ac28783e9a370efec94d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952576"
---
# <a name="defining-permissions-in-script"></a><span data-ttu-id="35e7b-103">Définition des autorisations dans le script</span><span class="sxs-lookup"><span data-stu-id="35e7b-103">Defining Permissions in Script</span></span>

<span data-ttu-id="35e7b-104">Dans le gestionnaire d’autorisations, vous définissez les utilisateurs qui ont accès aux ressources d’application en créant un magasin de stratégies d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="35e7b-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="35e7b-105">**Pour définir des autorisations d’accès**</span><span class="sxs-lookup"><span data-stu-id="35e7b-105">**To define access permissions**</span></span>

1.  <span data-ttu-id="35e7b-106">Créez le magasin dans lequel la stratégie d’autorisation est définie :</span><span class="sxs-lookup"><span data-stu-id="35e7b-106">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="35e7b-107">Création d’un magasin de stratégies d’autorisation dans le script</span><span class="sxs-lookup"><span data-stu-id="35e7b-107">Creating an Authorization Policy Store in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  <span data-ttu-id="35e7b-108">Créer une section dans le magasin de stratégies d’autorisation pour une application spécifique :</span><span class="sxs-lookup"><span data-stu-id="35e7b-108">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="35e7b-109">Création d’un objet d’application dans un script</span><span class="sxs-lookup"><span data-stu-id="35e7b-109">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)  
    </dl>
3.  <span data-ttu-id="35e7b-110">Définissez les opérations que l’application implémente pour accéder aux ressources et les modifier :</span><span class="sxs-lookup"><span data-stu-id="35e7b-110">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="35e7b-111">Définition des opérations dans le script</span><span class="sxs-lookup"><span data-stu-id="35e7b-111">Defining Operations in Script</span></span>](defining-operations-in-script.md)  
    </dl>
4.  <span data-ttu-id="35e7b-112">Regroupez les opérations en tâches de haut niveau que les utilisateurs souhaitent effectuer :</span><span class="sxs-lookup"><span data-stu-id="35e7b-112">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="35e7b-113">Regroupement d’opérations en tâches dans un script</span><span class="sxs-lookup"><span data-stu-id="35e7b-113">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  <span data-ttu-id="35e7b-114">Définir des rôles composés de groupes de tâches :</span><span class="sxs-lookup"><span data-stu-id="35e7b-114">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="35e7b-115">Regroupement de tâches en rôles dans le script</span><span class="sxs-lookup"><span data-stu-id="35e7b-115">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)  
    </dl><span data-ttu-id="35e7b-116">Un utilisateur affecté à un rôle a l’autorisation d’effectuer n’importe quelle tâche affectée à ce rôle.</span><span class="sxs-lookup"><span data-stu-id="35e7b-116">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="35e7b-117">Créer des scripts pour qualifier l’accès aux tâches au moment de l’exécution :</span><span class="sxs-lookup"><span data-stu-id="35e7b-117">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="35e7b-118">Accès éligible avec la logique métier dans le script</span><span class="sxs-lookup"><span data-stu-id="35e7b-118">Qualifying Access with Business Logic in Script</span></span>](qualifying-access-with-business-logic-in-script.md)  
    </dl><span data-ttu-id="35e7b-119">Cette étape est facultative.</span><span class="sxs-lookup"><span data-stu-id="35e7b-119">This step is optional.</span></span>
7.  <span data-ttu-id="35e7b-120">Définir des groupes d’utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="35e7b-120">Define groups of users:</span></span><dl>

[<span data-ttu-id="35e7b-121">Définition de groupes d’utilisateurs dans le script</span><span class="sxs-lookup"><span data-stu-id="35e7b-121">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)  
    </dl><span data-ttu-id="35e7b-122">Ces groupes peuvent ensuite être affectés à des rôles pour déterminer les tâches qu’ils peuvent effectuer.</span><span class="sxs-lookup"><span data-stu-id="35e7b-122">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="35e7b-123">Ajouter des utilisateurs à des groupes d’utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="35e7b-123">Add users to user groups:</span></span><dl>

[<span data-ttu-id="35e7b-124">Ajout d’utilisateurs à un groupe d’applications dans le script</span><span class="sxs-lookup"><span data-stu-id="35e7b-124">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 



