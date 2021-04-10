---
title: Détermination de l’appartenance d’un utilisateur ou d’un groupe à un groupe
description: La méthode IADsGroup. IsMember peut être utilisée pour déterminer si un objet est membre d’un groupe.
ms.assetid: c7168781-4ae4-4ce3-8d8a-2eefc7def62b
ms.tgt_platform: multiple
keywords:
- Détermination de l’appartenance d’un utilisateur ou d’un groupe à un groupe AD
- regroupe Active Directory, en déterminant l’appartenance d’un utilisateur ou d’un groupe à un groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b520146079fdfaa5fa1adc99975b3b25d2e78c05
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031019"
---
# <a name="determining-a-users-or-groups-membership-in-a-group"></a><span data-ttu-id="618f5-105">Détermination de l’appartenance d’un utilisateur ou d’un groupe à un groupe</span><span class="sxs-lookup"><span data-stu-id="618f5-105">Determining a User's or Group's Membership in a Group</span></span>

<span data-ttu-id="618f5-106">La méthode [**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) peut être utilisée pour déterminer si un objet est membre d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="618f5-106">The [**IADsGroup.IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) method can be used to determine if an object is a member of a group.</span></span> <span data-ttu-id="618f5-107">Cette méthode retourne la **valeur true** si l’objet spécifié est un membre direct du groupe, autrement dit, si la propriété de membre du groupe contient l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="618f5-107">This method returns **TRUE** if the specified object is a direct member of the group, that is, the group's member property contains the specified object.</span></span>

<span data-ttu-id="618f5-108">Un groupe peut contenir d’autres groupes.</span><span class="sxs-lookup"><span data-stu-id="618f5-108">A group can contain other groups.</span></span> <span data-ttu-id="618f5-109">La méthode [**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) ne vérifie pas de manière récursive les membres des groupes dans sa propriété de membre, les groupes au sein de ces groupes, etc.</span><span class="sxs-lookup"><span data-stu-id="618f5-109">The [**IADsGroup.IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) method does not recursively verify the members of groups in its member property, groups within those groups, and so on.</span></span> <span data-ttu-id="618f5-110">Pour vérifier de manière récursive qu’un objet est membre d’un groupe, énumérez les groupes dans la propriété de membre, vérifiez les membres de ces groupes pour déterminer si l’objet est un membre et, si ces groupes contiennent d’autres groupes, vérifiez leurs membres, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="618f5-110">To recursively verify that an object is a member of a group, enumerate the groups in the member property, verify the members of those groups to see if the object is a member, and if those groups contain other groups, check their members, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="618f5-111">Comme les groupes peuvent être imbriqués, l’appartenance à un groupe peut avoir des boucles.</span><span class="sxs-lookup"><span data-stu-id="618f5-111">Since groups can be nested, group membership may have loops.</span></span> <span data-ttu-id="618f5-112">Tout script qui énumère plusieurs groupes doit conserver une liste interne de groupes pour terminer la récursivité si un groupe a déjà été visité.</span><span class="sxs-lookup"><span data-stu-id="618f5-112">Any script that enumerates over many groups should keep an internal list of groups to end recursion if a group has already been visited.</span></span>

 

 

 