---
title: Fonctions de groupe
description: Un groupe global contient des comptes d’utilisateurs d’un domaine qui sont regroupés sous un nom de compte de groupe.
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7696755cd5f5cbe75de11d386cb238fa3bd5d35d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382508"
---
# <a name="group-functions"></a><span data-ttu-id="064fa-103">Fonctions de groupe</span><span class="sxs-lookup"><span data-stu-id="064fa-103">Group Functions</span></span>

<span data-ttu-id="064fa-104">Un *groupe global* contient des comptes d’utilisateurs d’un domaine qui sont regroupés sous un nom de compte de groupe.</span><span class="sxs-lookup"><span data-stu-id="064fa-104">A *global group* contains user accounts from one domain that are grouped together under one group account name.</span></span> <span data-ttu-id="064fa-105">Un groupe global peut contenir uniquement des membres (utilisateurs) du domaine dans lequel le groupe global est créé ; il ne peut pas contenir de groupes locaux.</span><span class="sxs-lookup"><span data-stu-id="064fa-105">A global group can contain only members (users) from the domain where the global group is created; it cannot contain local groups.</span></span> <span data-ttu-id="064fa-106">Un groupe global est disponible dans son propre domaine et dans n’importe quel domaine d’approbation.</span><span class="sxs-lookup"><span data-stu-id="064fa-106">A global group is available within its own domain and within any trusting domain.</span></span>

<span data-ttu-id="064fa-107">Les fonctions de groupe d’administration de réseau contrôlent les groupes globaux.</span><span class="sxs-lookup"><span data-stu-id="064fa-107">The network management group functions control global groups.</span></span> <span data-ttu-id="064fa-108">Les fonctions de groupe sont répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="064fa-108">The group functions are listed following.</span></span>



| <span data-ttu-id="064fa-109">Fonction</span><span class="sxs-lookup"><span data-stu-id="064fa-109">Function</span></span>                                     | <span data-ttu-id="064fa-110">Description</span><span class="sxs-lookup"><span data-stu-id="064fa-110">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="064fa-111">**NetGroupAdd**</span><span class="sxs-lookup"><span data-stu-id="064fa-111">**NetGroupAdd**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | <span data-ttu-id="064fa-112">Crée un groupe global.</span><span class="sxs-lookup"><span data-stu-id="064fa-112">Creates a global group.</span></span>                                                           |
| [<span data-ttu-id="064fa-113">**NetGroupAddUser**</span><span class="sxs-lookup"><span data-stu-id="064fa-113">**NetGroupAddUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | <span data-ttu-id="064fa-114">Ajoute un utilisateur à un groupe global existant.</span><span class="sxs-lookup"><span data-stu-id="064fa-114">Adds one user to an existing global group.</span></span>                                        |
| [<span data-ttu-id="064fa-115">**NetGroupDel**</span><span class="sxs-lookup"><span data-stu-id="064fa-115">**NetGroupDel**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | <span data-ttu-id="064fa-116">Supprime un groupe global, que le groupe ait ou non des membres.</span><span class="sxs-lookup"><span data-stu-id="064fa-116">Removes a global group whether or not the group has any members.</span></span>                  |
| [<span data-ttu-id="064fa-117">**NetGroupDelUser**</span><span class="sxs-lookup"><span data-stu-id="064fa-117">**NetGroupDelUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | <span data-ttu-id="064fa-118">Supprime un nom d’utilisateur d’un groupe global.</span><span class="sxs-lookup"><span data-stu-id="064fa-118">Removes one user name from a global group.</span></span>                                        |
| [<span data-ttu-id="064fa-119">**NetGroupEnum**</span><span class="sxs-lookup"><span data-stu-id="064fa-119">**NetGroupEnum**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | <span data-ttu-id="064fa-120">Répertorie tous les groupes globaux sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="064fa-120">Lists all global groups on a server.</span></span>                                              |
| [<span data-ttu-id="064fa-121">**NetGroupGetInfo**</span><span class="sxs-lookup"><span data-stu-id="064fa-121">**NetGroupGetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | <span data-ttu-id="064fa-122">Retourne des informations sur un groupe global particulier.</span><span class="sxs-lookup"><span data-stu-id="064fa-122">Returns information about a particular global group.</span></span>                              |
| [<span data-ttu-id="064fa-123">**NetGroupGetUsers**</span><span class="sxs-lookup"><span data-stu-id="064fa-123">**NetGroupGetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | <span data-ttu-id="064fa-124">Répertorie tous les membres d’un groupe global particulier.</span><span class="sxs-lookup"><span data-stu-id="064fa-124">Lists all members of a particular global group.</span></span>                                   |
| [<span data-ttu-id="064fa-125">**NetGroupSetInfo**</span><span class="sxs-lookup"><span data-stu-id="064fa-125">**NetGroupSetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | <span data-ttu-id="064fa-126">Définit des informations générales sur un groupe global.</span><span class="sxs-lookup"><span data-stu-id="064fa-126">Sets general information about a global group.</span></span>                                    |
| [<span data-ttu-id="064fa-127">**NetGroupSetUsers**</span><span class="sxs-lookup"><span data-stu-id="064fa-127">**NetGroupSetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | <span data-ttu-id="064fa-128">Attribue des membres à un nouveau groupe global ; remplace les membres d’un groupe existant.</span><span class="sxs-lookup"><span data-stu-id="064fa-128">Assigns members to a new global group; replaces the members of an existing group.</span></span> |



 

<span data-ttu-id="064fa-129">Quand vous appelez la fonction [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) pour créer un groupe global, vous devez fournir un nom de groupe.</span><span class="sxs-lookup"><span data-stu-id="064fa-129">When you call the [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) function to create a global group, you must supply a group name.</span></span> <span data-ttu-id="064fa-130">Au départ, un nouveau groupe n’a aucun membre.</span><span class="sxs-lookup"><span data-stu-id="064fa-130">Initially, a new group has no members.</span></span>

<span data-ttu-id="064fa-131">Les comptes d’utilisateurs appartiennent automatiquement aux utilisateurs du domaine de groupe global spécial.</span><span class="sxs-lookup"><span data-stu-id="064fa-131">User accounts automatically belong to the special global group Domain Users.</span></span> <span data-ttu-id="064fa-132">L’appartenance à ce groupe est indirectement contrôlée par les fonctions [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)et [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="064fa-132">Membership in this group is indirectly controlled by the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), and [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) functions.</span></span>

<span data-ttu-id="064fa-133">Les informations de compte de groupe global sont disponibles aux niveaux suivants :</span><span class="sxs-lookup"><span data-stu-id="064fa-133">Global group account information is available at the following levels:</span></span>

-   [<span data-ttu-id="064fa-134">**Infos de groupe \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="064fa-134">**GROUP\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [<span data-ttu-id="064fa-135">**\_Infos sur le groupe \_ 1**</span><span class="sxs-lookup"><span data-stu-id="064fa-135">**GROUP\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [<span data-ttu-id="064fa-136">**\_Informations sur le groupe \_ 2**</span><span class="sxs-lookup"><span data-stu-id="064fa-136">**GROUP\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [<span data-ttu-id="064fa-137">**\_Infos sur le groupe \_ 3**</span><span class="sxs-lookup"><span data-stu-id="064fa-137">**GROUP\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [<span data-ttu-id="064fa-138">**\_Informations sur le groupe \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="064fa-138">**GROUP\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [<span data-ttu-id="064fa-139">**\_Informations sur le groupe \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="064fa-139">**GROUP\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

<span data-ttu-id="064fa-140">Les niveaux 1002 et 1005 sont valides uniquement pour la fonction [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) .</span><span class="sxs-lookup"><span data-stu-id="064fa-140">The 1002 and 1005 levels are valid only for the [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) function.</span></span>

<span data-ttu-id="064fa-141">Les informations des membres du groupe global sont disponibles au niveau des informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="064fa-141">Global group member information is available at the following information level:</span></span>

-   [<span data-ttu-id="064fa-142">**\_Informations sur les utilisateurs du groupe \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="064fa-142">**GROUP\_USERS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

<span data-ttu-id="064fa-143">Pour plus d’informations, consultez fonctions de [groupe local](local-group-functions.md)de gestion de réseau.</span><span class="sxs-lookup"><span data-stu-id="064fa-143">For more information, see the network management [Local Group Functions](local-group-functions.md).</span></span>

<span data-ttu-id="064fa-144">Si vous programmez pour Active Directory, vous pourrez peut-être appeler certaines méthodes d’interface de service d’Active Directory (ADSI) pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant les fonctions de groupe d’administration réseau.</span><span class="sxs-lookup"><span data-stu-id="064fa-144">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management group functions.</span></span> <span data-ttu-id="064fa-145">Pour plus d’informations, consultez [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span><span class="sxs-lookup"><span data-stu-id="064fa-145">For more information, see [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span></span>

 

 