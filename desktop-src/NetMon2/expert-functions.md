---
description: Les fonctions d’assistance suivantes peuvent être appelées uniquement par des experts qui exportent la fonction exécuter ou configurer.
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: Fonctions d’experts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7441289008c7dcd647775c2932e210ccd09b24bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862026"
---
# <a name="expert-functions"></a><span data-ttu-id="bbe3c-103">Fonctions d’experts</span><span class="sxs-lookup"><span data-stu-id="bbe3c-103">Expert Functions</span></span>

<span data-ttu-id="bbe3c-104">Les fonctions d’assistance suivantes peuvent être appelées uniquement par des experts qui exportent la fonction [exécuter](run.md) ou [configurer](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="bbe3c-104">The following helper functions can only be called by experts that export the [Run](run.md) or [Configure](configure.md) function.</span></span>



| <span data-ttu-id="bbe3c-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="bbe3c-105">Function</span></span>                                         | <span data-ttu-id="bbe3c-106">Description</span><span class="sxs-lookup"><span data-stu-id="bbe3c-106">Description</span></span>                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbe3c-107">ExpertGetFrame</span><span class="sxs-lookup"><span data-stu-id="bbe3c-107">ExpertGetFrame</span></span>](expertgetframe.md)             | <span data-ttu-id="bbe3c-108">Récupère un frame donné de la capture.</span><span class="sxs-lookup"><span data-stu-id="bbe3c-108">Retrieves a given frame from the capture.</span></span>                                               |
| [<span data-ttu-id="bbe3c-109">ExpertIndicateStatus</span><span class="sxs-lookup"><span data-stu-id="bbe3c-109">ExpertIndicateStatus</span></span>](expertindicatestatus.md) | <span data-ttu-id="bbe3c-110">Indique le pourcentage d’achèvement de l’analyse de capture de l’expert.</span><span class="sxs-lookup"><span data-stu-id="bbe3c-110">Indicates the percentage of completion of the expert's analysis of capture.</span></span>             |
| [<span data-ttu-id="bbe3c-111">ExpertGetStartupInfo</span><span class="sxs-lookup"><span data-stu-id="bbe3c-111">ExpertGetStartupInfo</span></span>](expertgetstartupinfo.md) | <span data-ttu-id="bbe3c-112">Récupère les informations de démarrage de l’expert.</span><span class="sxs-lookup"><span data-stu-id="bbe3c-112">Retrieves the startup information for the expert.</span></span>                                       |
| [<span data-ttu-id="bbe3c-113">ExpertMemorySize</span><span class="sxs-lookup"><span data-stu-id="bbe3c-113">ExpertMemorySize</span></span>](expertmemorysize.md)         | <span data-ttu-id="bbe3c-114">Récupère la taille de la mémoire allouée par un appel à la fonction **ExpertAllocMemory** .</span><span class="sxs-lookup"><span data-stu-id="bbe3c-114">Retrieves the size of memory allocated by a call to the **ExpertAllocMemory** function.</span></span> |
| [<span data-ttu-id="bbe3c-115">ExpertSubmitEvent</span><span class="sxs-lookup"><span data-stu-id="bbe3c-115">ExpertSubmitEvent</span></span>](expertsubmitevent.md)       | <span data-ttu-id="bbe3c-116">Indique un problème et récupère des informations sur le problème, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="bbe3c-116">Indicates a problem and retrieves information about the problem if one exists.</span></span>          |
| [<span data-ttu-id="bbe3c-117">ExpertAllocMemory</span><span class="sxs-lookup"><span data-stu-id="bbe3c-117">ExpertAllocMemory</span></span>](expertallocmemory.md)       | <span data-ttu-id="bbe3c-118">Alloue de la mémoire à l’expert.</span><span class="sxs-lookup"><span data-stu-id="bbe3c-118">Allocates memory for the expert.</span></span>                                                        |
| [<span data-ttu-id="bbe3c-119">ExpertReallocMemory</span><span class="sxs-lookup"><span data-stu-id="bbe3c-119">ExpertReallocMemory</span></span>](expertreallocmemory.md)   | <span data-ttu-id="bbe3c-120">Modifie la taille de la mémoire allouée par la fonction **ExpertAllocMemory** .</span><span class="sxs-lookup"><span data-stu-id="bbe3c-120">Changes the size of the memory allocated by the **ExpertAllocMemory** function.</span></span>         |
| [<span data-ttu-id="bbe3c-121">ExpertFreeMemory</span><span class="sxs-lookup"><span data-stu-id="bbe3c-121">ExpertFreeMemory</span></span>](expertfreememory.md)         | <span data-ttu-id="bbe3c-122">Libère de la mémoire allouée par l’expert.</span><span class="sxs-lookup"><span data-stu-id="bbe3c-122">Frees memory allocated by the expert.</span></span>                                                   |



 

<span data-ttu-id="bbe3c-123">Pour plus d’informations sur les fonctions d’exportation, les fonctions d’assistance qui peuvent être appelées par des experts et des analyseurs, des structures et des énumérations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="bbe3c-123">For information about export functions, helper functions that can be called by experts and parsers, structures, and enumerations, see the following topics:</span></span>



| <span data-ttu-id="bbe3c-124">Pour obtenir des informations sur</span><span class="sxs-lookup"><span data-stu-id="bbe3c-124">For information about</span></span>                                             | <span data-ttu-id="bbe3c-125">Consultez</span><span class="sxs-lookup"><span data-stu-id="bbe3c-125">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bbe3c-126">Fonctions exportées par des experts</span><span class="sxs-lookup"><span data-stu-id="bbe3c-126">Functions that are exported by experts</span></span>                            | [<span data-ttu-id="bbe3c-127">Fonctions d’exportation de DLL d’experts</span><span class="sxs-lookup"><span data-stu-id="bbe3c-127">Expert DLL Export Functions</span></span>](expert-dll-export-functions.md)               |
| <span data-ttu-id="bbe3c-128">Structures utilisées par les fonctions d’experts</span><span class="sxs-lookup"><span data-stu-id="bbe3c-128">Structures that are used by expert functions</span></span>                      | [<span data-ttu-id="bbe3c-129">Structures d’experts</span><span class="sxs-lookup"><span data-stu-id="bbe3c-129">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="bbe3c-130">Énumérations utilisées par les structures et fonctions d’experts</span><span class="sxs-lookup"><span data-stu-id="bbe3c-130">Enumerations used by expert structures and functions</span></span>              | [<span data-ttu-id="bbe3c-131">Énumérations d’experts</span><span class="sxs-lookup"><span data-stu-id="bbe3c-131">Expert Enumerations</span></span>](expert-enumerations.md)                               |
| <span data-ttu-id="bbe3c-132">Fonctions d’assistance courantes qui peuvent être appelées par des experts et des analyseurs</span><span class="sxs-lookup"><span data-stu-id="bbe3c-132">Common helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="bbe3c-133">Fonctions courantes des experts et de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="bbe3c-133">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |



 

 

 



