---
description: Les rôles ont deux objectifs différents dans le gestionnaire d’autorisations.
ms.assetid: 6d045ecb-432e-4ba6-b5d2-37db82ab1884
title: Rôles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65d140faa22c72d098c7a4ba2f13e952b2713f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863018"
---
# <a name="roles"></a><span data-ttu-id="3fad2-103">Rôles</span><span class="sxs-lookup"><span data-stu-id="3fad2-103">Roles</span></span>

<span data-ttu-id="3fad2-104">Les rôles ont deux objectifs différents dans le gestionnaire d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="3fad2-104">Roles serve two different purposes in Authorization Manager.</span></span> <span data-ttu-id="3fad2-105">Un rôle est un ensemble de tâches ou d’opérations auxquelles une catégorie d’utilisateurs a besoin d’accéder, et il s’agit également d’un ensemble d’utilisateurs et de groupes qui tiennent dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="3fad2-105">A role is a set of tasks or operations to which a category of users requires access, and it is also a set of users and groups that fit into that category.</span></span>

-   [<span data-ttu-id="3fad2-106">Rôles en tant qu’ensembles de tâches</span><span class="sxs-lookup"><span data-stu-id="3fad2-106">Roles as Sets of Tasks</span></span>](#roles-as-sets-of-tasks)
-   [<span data-ttu-id="3fad2-107">Rôles sous forme d’ensembles d’utilisateurs et de groupes</span><span class="sxs-lookup"><span data-stu-id="3fad2-107">Roles as Sets of Users and Groups</span></span>](#roles-as-sets-of-users-and-groups)
-   [<span data-ttu-id="3fad2-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3fad2-108">Related topics</span></span>](#related-topics)

## <a name="roles-as-sets-of-tasks"></a><span data-ttu-id="3fad2-109">Rôles en tant qu’ensembles de tâches</span><span class="sxs-lookup"><span data-stu-id="3fad2-109">Roles as Sets of Tasks</span></span>

<span data-ttu-id="3fad2-110">Une stratégie d’autorisation affecte des objets [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) à un objet [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) pour créer des ensembles de tâches.</span><span class="sxs-lookup"><span data-stu-id="3fad2-110">An authorization policy assigns [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) objects to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to create sets of tasks.</span></span> <span data-ttu-id="3fad2-111">Tous les utilisateurs et groupes attribués à cet objet **IAzRole** sont ensuite autorisés à accéder à toutes les opérations contenues par ces objets **IAzTask** .</span><span class="sxs-lookup"><span data-stu-id="3fad2-111">All users and groups assigned to that **IAzRole** object then have permission to access all operations contained by those **IAzTask** objects.</span></span>

<span data-ttu-id="3fad2-112">Étant donné qu’un objet [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) représente à la fois un ensemble de tâches et un ensemble d’utilisateurs et de groupes qui ont accès à ces tâches, le gestionnaire d’autorisations fournit un moyen de créer des définitions de rôles qui peuvent être attribuées à plusieurs objets **IAzRole** .</span><span class="sxs-lookup"><span data-stu-id="3fad2-112">Because an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object represents both a set of tasks and a set of users and groups that have access to those tasks, Authorization Manager provides a way to create role definitions that can be assigned to more than one **IAzRole** object.</span></span> <span data-ttu-id="3fad2-113">Un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) peut contenir d’autres objets **IAzTask** .</span><span class="sxs-lookup"><span data-stu-id="3fad2-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can contain other **IAzTask** objects.</span></span> <span data-ttu-id="3fad2-114">Vous pouvez ensuite utiliser cet objet **IAzTask** comme définition de rôle en l’affectant à un ou plusieurs objets **IAzRole** .</span><span class="sxs-lookup"><span data-stu-id="3fad2-114">You can then use that **IAzTask** object as a role definition by assigning it to one or more **IAzRole** objects.</span></span> <span data-ttu-id="3fad2-115">Affectez la valeur **true** à la propriété [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) de l’objet **IAzTask** pour que l’interface utilisateur du composant logiciel enfichable MMC du **Gestionnaire d’autorisations** affiche l’objet **IAzTask** en tant que rôle.</span><span class="sxs-lookup"><span data-stu-id="3fad2-115">Set the [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property of the **IAzTask** object to **TRUE** to cause the **Authorization Manager** MMC snap-in user interface to display the **IAzTask** object as a role.</span></span>

## <a name="roles-as-sets-of-users-and-groups"></a><span data-ttu-id="3fad2-116">Rôles sous forme d’ensembles d’utilisateurs et de groupes</span><span class="sxs-lookup"><span data-stu-id="3fad2-116">Roles as Sets of Users and Groups</span></span>

<span data-ttu-id="3fad2-117">Affectez des utilisateurs et des groupes à un objet [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) pour accorder à ces utilisateurs et groupes l’accès aux tâches assignées à cet objet **IAzRole** en appelant la méthode [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) ou [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) .</span><span class="sxs-lookup"><span data-stu-id="3fad2-117">Assign users and groups to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to grant those users and groups access to the tasks assigned to that **IAzRole** object by calling the [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) or [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) method.</span></span> <span data-ttu-id="3fad2-118">Assignez des groupes d’applications existants, représentés par les objets [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) , à un objet **IAzRole** en appelant la méthode [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) .</span><span class="sxs-lookup"><span data-stu-id="3fad2-118">Assign existing application groups, represented by [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) objects, to an **IAzRole** object by calling the [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) method.</span></span> <span data-ttu-id="3fad2-119">Tous les utilisateurs et groupes attribués à l’objet **IAzRole** ont accès aux tâches et aux opérations affectées à ce rôle.</span><span class="sxs-lookup"><span data-stu-id="3fad2-119">All users and groups assigned to the **IAzRole** object have access to the tasks and operations assigned to that role.</span></span> <span data-ttu-id="3fad2-120">Pour plus d’informations sur les groupes d’applications, voir [utilisateurs et groupes](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="3fad2-120">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fad2-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3fad2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fad2-122">Regroupement de tâches en rôles en C++</span><span class="sxs-lookup"><span data-stu-id="3fad2-122">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="3fad2-123">Définition de groupes d’utilisateurs en C++</span><span class="sxs-lookup"><span data-stu-id="3fad2-123">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> <dt>

[<span data-ttu-id="3fad2-124">Ajout d’utilisateurs à un groupe d’applications en C++</span><span class="sxs-lookup"><span data-stu-id="3fad2-124">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



