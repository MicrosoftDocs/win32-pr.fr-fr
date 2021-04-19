---
description: L’action StartServices démarre les services système. Cette action interroge la table ServiceControl.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: Action StartServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c150a8970c5852d9cfc53581290e792c00b628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527630"
---
# <a name="startservices-action"></a><span data-ttu-id="2921e-104">Action StartServices</span><span class="sxs-lookup"><span data-stu-id="2921e-104">StartServices Action</span></span>

<span data-ttu-id="2921e-105">L’action StartServices démarre les services système.</span><span class="sxs-lookup"><span data-stu-id="2921e-105">The StartServices action starts system services.</span></span> <span data-ttu-id="2921e-106">Cette action interroge la [table ServiceControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="2921e-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2921e-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="2921e-107">Sequence Restrictions</span></span>

<span data-ttu-id="2921e-108">Les actions des services doivent être utilisées dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="2921e-108">The services actions must be used in the following sequence:</span></span>

-   [<span data-ttu-id="2921e-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="2921e-109">StopServices</span></span>](stopservices-action.md)
-   [<span data-ttu-id="2921e-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="2921e-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="2921e-111">L’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="2921e-111">Any of the following actions:</span></span>

-   [<span data-ttu-id="2921e-112">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="2921e-112">InstallFiles</span></span>](installfiles-action.md)
-   [<span data-ttu-id="2921e-113">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="2921e-113">RemoveFiles</span></span>](removefiles-action.md)
-   [<span data-ttu-id="2921e-114">DuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="2921e-114">DuplicateFiles</span></span>](duplicatefiles-action.md)
-   [<span data-ttu-id="2921e-115">MoveFiles</span><span class="sxs-lookup"><span data-stu-id="2921e-115">MoveFiles</span></span>](movefiles-action.md)
-   [<span data-ttu-id="2921e-116">PatchFiles</span><span class="sxs-lookup"><span data-stu-id="2921e-116">PatchFiles</span></span>](patchfiles-action.md)
-   [<span data-ttu-id="2921e-117">RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="2921e-117">RemoveDuplicateFiles</span></span>](removeduplicatefiles-action.md)
-   [<span data-ttu-id="2921e-118">InstallServices</span><span class="sxs-lookup"><span data-stu-id="2921e-118">InstallServices</span></span>](installservices-action.md)
-   <span data-ttu-id="2921e-119">StartServices</span><span class="sxs-lookup"><span data-stu-id="2921e-119">StartServices</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2921e-120">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="2921e-120">ActionData Messages</span></span>



| <span data-ttu-id="2921e-121">Champ</span><span class="sxs-lookup"><span data-stu-id="2921e-121">Field</span></span> | <span data-ttu-id="2921e-122">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="2921e-122">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="2921e-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2921e-123">\[1\]</span></span> | <span data-ttu-id="2921e-124">Nom complet du service.</span><span class="sxs-lookup"><span data-stu-id="2921e-124">Service display name.</span></span>      |
| <span data-ttu-id="2921e-125">\[2\]</span><span class="sxs-lookup"><span data-stu-id="2921e-125">\[2\]</span></span> | <span data-ttu-id="2921e-126">Nom du service</span><span class="sxs-lookup"><span data-stu-id="2921e-126">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="2921e-127">Notes</span><span class="sxs-lookup"><span data-stu-id="2921e-127">Remarks</span></span>

<span data-ttu-id="2921e-128">Cette action nécessite que l’utilisateur soit un administrateur ou qu’il dispose de privilèges élevés avec l’autorisation de contrôler les services ou que l’application fasse partie d’une installation gérée.</span><span class="sxs-lookup"><span data-stu-id="2921e-128">This action requires that the user be an administrator or have elevated privileges with permission to control services or that the application be part of a managed installation.</span></span>

 

 



