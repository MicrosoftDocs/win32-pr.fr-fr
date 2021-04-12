---
description: L’action DeleteServices arrête un service et supprime son inscription du système. Cette action interroge la table ServiceControl.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Action DeleteServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5fc22bbb0c11cd546f1ffbb9f3ad98e06efae3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319514"
---
# <a name="deleteservices-action"></a><span data-ttu-id="56a1e-104">Action DeleteServices</span><span class="sxs-lookup"><span data-stu-id="56a1e-104">DeleteServices Action</span></span>

<span data-ttu-id="56a1e-105">L’action DeleteServices arrête un service et supprime son inscription du système.</span><span class="sxs-lookup"><span data-stu-id="56a1e-105">The DeleteServices action stops a service and removes its registration from the system.</span></span> <span data-ttu-id="56a1e-106">Cette action interroge la [table ServiceControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="56a1e-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="56a1e-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="56a1e-107">Sequence Restrictions</span></span>

<span data-ttu-id="56a1e-108">Les actions des services doivent être utilisées dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="56a1e-108">The services actions must be used in the following sequence:</span></span>

1.  [<span data-ttu-id="56a1e-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="56a1e-109">StopServices</span></span>](stopservices-action.md)
2.  <span data-ttu-id="56a1e-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="56a1e-110">DeleteServices</span></span>
3.  <span data-ttu-id="56a1e-111">L’une des actions suivantes : les actions [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)et [RemoveDuplicateFiles](removeduplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="56a1e-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>
4.  [<span data-ttu-id="56a1e-112">Action InstallServices</span><span class="sxs-lookup"><span data-stu-id="56a1e-112">InstallServices action</span></span>](installservices-action.md)
5.  [<span data-ttu-id="56a1e-113">StartServices</span><span class="sxs-lookup"><span data-stu-id="56a1e-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="56a1e-114">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="56a1e-114">ActionData Messages</span></span>



| <span data-ttu-id="56a1e-115">Champ</span><span class="sxs-lookup"><span data-stu-id="56a1e-115">Field</span></span> | <span data-ttu-id="56a1e-116">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="56a1e-116">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="56a1e-117">\[1\]</span><span class="sxs-lookup"><span data-stu-id="56a1e-117">\[1\]</span></span> | <span data-ttu-id="56a1e-118">Nom complet du service.</span><span class="sxs-lookup"><span data-stu-id="56a1e-118">Service display name.</span></span>      |
| <span data-ttu-id="56a1e-119">\[2\]</span><span class="sxs-lookup"><span data-stu-id="56a1e-119">\[2\]</span></span> | <span data-ttu-id="56a1e-120">Nom du service</span><span class="sxs-lookup"><span data-stu-id="56a1e-120">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="56a1e-121">Notes</span><span class="sxs-lookup"><span data-stu-id="56a1e-121">Remarks</span></span>

<span data-ttu-id="56a1e-122">Cette action nécessite que l’utilisateur soit un administrateur ou qu’il dispose de privilèges élevés avec l’autorisation de supprimer des services ou que l’application fasse partie d’une installation gérée.</span><span class="sxs-lookup"><span data-stu-id="56a1e-122">This action requires the user be an administrator or have elevated privileges with permission to delete services or that the application be part of a managed installation.</span></span>

 

 



