---
title: Énumération des membres d’un groupe
description: Les membres d’un groupe sont stockés dans un attribut à valeurs multiples appelé member.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Énumération des membres d’un groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2d051999bf8efeadb0c5a8899b31f813b8bf42
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101452"
---
# <a name="enumerating-members-in-a-group"></a><span data-ttu-id="2b866-104">Énumération des membres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="2b866-104">Enumerating Members in a Group</span></span>

<span data-ttu-id="2b866-105">Les membres d’un groupe sont stockés dans un attribut à valeurs multiples appelé **member**.</span><span class="sxs-lookup"><span data-stu-id="2b866-105">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="2b866-106">Pour les groupes avec une appartenance de petite à moyenne taille, utilisez la méthode [**IADsGroup. Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) pour obtenir un pointeur vers un objet [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) qui contient la liste de tous les membres.</span><span class="sxs-lookup"><span data-stu-id="2b866-106">For groups with a small to medium-sized membership, use the [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) method to get a pointer to an [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) object that contains the list of all members.</span></span> <span data-ttu-id="2b866-107">Utilisez ensuite la [**\_ \_ NewEnum IADsMembers :: acobtiens**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) pour récupérer un objet énumérateur que vous pouvez utiliser pour énumérer les membres.</span><span class="sxs-lookup"><span data-stu-id="2b866-107">Then use the [**IADsMembers::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) to get an enumerator object that you can use to enumerate the members.</span></span>

<span data-ttu-id="2b866-108">Si l’appartenance à un groupe anticipée sera de 1000 membres ou plus, utilisez pour récupérer des utilisateurs une plage à la fois.</span><span class="sxs-lookup"><span data-stu-id="2b866-108">If the anticipated group membership will be 1000 or more members, use ranging to retrieve users one range at a time.</span></span> <span data-ttu-id="2b866-109">Pour plus d’informations sur l’utilisation de pour énumérer des membres, consultez [énumération des groupes qui contiennent de nombreux membres](enumerating-groups-that-contain-many-members.md).</span><span class="sxs-lookup"><span data-stu-id="2b866-109">For more information about using ranging to enumerate members, see [Enumerating Groups That Contain Many Members](enumerating-groups-that-contain-many-members.md).</span></span>

 

 