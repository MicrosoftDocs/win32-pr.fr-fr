---
description: L’action StopServices arrête les services système. Cette action interroge la table ServiceControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Action StopServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb271b99c434a1ac54ab9744697b991e9e1fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534385"
---
# <a name="stopservices-action"></a><span data-ttu-id="a30f5-104">Action StopServices</span><span class="sxs-lookup"><span data-stu-id="a30f5-104">StopServices Action</span></span>

<span data-ttu-id="a30f5-105">L’action StopServices arrête les services système.</span><span class="sxs-lookup"><span data-stu-id="a30f5-105">The StopServices action stops system services.</span></span> <span data-ttu-id="a30f5-106">Cette action interroge la [table ServiceControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="a30f5-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a30f5-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="a30f5-107">Sequence Restrictions</span></span>

<span data-ttu-id="a30f5-108">Les actions des services doivent être utilisées dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="a30f5-108">The services actions must be used in the following sequence:</span></span>

-   <span data-ttu-id="a30f5-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="a30f5-109">StopServices</span></span>
-   [<span data-ttu-id="a30f5-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="a30f5-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="a30f5-111">L’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a30f5-111">Any of the following actions:</span></span>

-   [<span data-ttu-id="a30f5-112">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="a30f5-112">InstallFiles</span></span>](installfiles-action.md)
-   [<span data-ttu-id="a30f5-113">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="a30f5-113">RemoveFiles</span></span>](removefiles-action.md)
-   [<span data-ttu-id="a30f5-114">DuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="a30f5-114">DuplicateFiles</span></span>](duplicatefiles-action.md)
-   [<span data-ttu-id="a30f5-115">MoveFiles</span><span class="sxs-lookup"><span data-stu-id="a30f5-115">MoveFiles</span></span>](movefiles-action.md)
-   [<span data-ttu-id="a30f5-116">PatchFiles</span><span class="sxs-lookup"><span data-stu-id="a30f5-116">PatchFiles</span></span>](patchfiles-action.md)
-   [<span data-ttu-id="a30f5-117">RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="a30f5-117">RemoveDuplicateFiles</span></span>](removeduplicatefiles-action.md)
-   [<span data-ttu-id="a30f5-118">InstallServices</span><span class="sxs-lookup"><span data-stu-id="a30f5-118">InstallServices</span></span>](installservices-action.md)
-   [<span data-ttu-id="a30f5-119">StartServices</span><span class="sxs-lookup"><span data-stu-id="a30f5-119">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="a30f5-120">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="a30f5-120">ActionData Messages</span></span>



| <span data-ttu-id="a30f5-121">Champ</span><span class="sxs-lookup"><span data-stu-id="a30f5-121">Field</span></span> | <span data-ttu-id="a30f5-122">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="a30f5-122">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="a30f5-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a30f5-123">\[1\]</span></span> | <span data-ttu-id="a30f5-124">Nom complet du service.</span><span class="sxs-lookup"><span data-stu-id="a30f5-124">Service display name.</span></span>      |
| <span data-ttu-id="a30f5-125">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a30f5-125">\[2\]</span></span> | <span data-ttu-id="a30f5-126">Nom du service</span><span class="sxs-lookup"><span data-stu-id="a30f5-126">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="a30f5-127">Notes</span><span class="sxs-lookup"><span data-stu-id="a30f5-127">Remarks</span></span>

<span data-ttu-id="a30f5-128">Cette action nécessite que l’utilisateur soit un administrateur ou qu’il dispose de privilèges élevés avec l’autorisation de contrôler les services ou que l’application fasse partie d’une installation gérée.</span><span class="sxs-lookup"><span data-stu-id="a30f5-128">This action requires that the user be an administrator or have elevated privileges with permission to control services or that the application be part of a managed installation.</span></span>

 

 



