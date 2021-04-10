---
title: Énumérations Windows Defender
description: Énumérations utilisées par les applications lors de l’appel de pour demander des analyses, des mises à jour de signature ou des informations de Windows Defender.
ms.assetid: AC84ED57-6221-4A19-8A1D-E4E2811B027E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02400576ddeccf7ffb79f6aeceafba725be78516
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309569"
---
# <a name="windows-defender-enumerations"></a><span data-ttu-id="c285c-103">Énumérations Windows Defender</span><span class="sxs-lookup"><span data-stu-id="c285c-103">Windows Defender Enumerations</span></span>

<span data-ttu-id="c285c-104">Énumérations utilisées par les applications lors de l’appel de pour demander des analyses, des mises à jour de signature ou des informations de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="c285c-104">Enumerations used by apps when calling to request scans, signature updates, or information from Windows Defender.</span></span>



| <span data-ttu-id="c285c-105">Énumération</span><span class="sxs-lookup"><span data-stu-id="c285c-105">Enumeration</span></span>                                                       | <span data-ttu-id="c285c-106">Description</span><span class="sxs-lookup"><span data-stu-id="c285c-106">Description</span></span>                                                           |
|-------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="c285c-107">**\_type MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="c285c-107">**MPCALLBACK\_TYPE**</span></span>](mpcallback-type.md)                       | <span data-ttu-id="c285c-108">Types de rappel possibles.</span><span class="sxs-lookup"><span data-stu-id="c285c-108">Possible callback types.</span></span><br/>                                   |
| [<span data-ttu-id="c285c-109">**\_ID MPCOMPONENT**</span><span class="sxs-lookup"><span data-stu-id="c285c-109">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)                         | <span data-ttu-id="c285c-110">Composants possibles pour le gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="c285c-110">Possible components for the malware protection manager.</span></span><br/>    |
| [<span data-ttu-id="c285c-111">**MPDETECTION \_ origine**</span><span class="sxs-lookup"><span data-stu-id="c285c-111">**MPDETECTION\_ORIGIN**</span></span>](mpdetection-origin.md)                 | <span data-ttu-id="c285c-112">Origine de la détection.</span><span class="sxs-lookup"><span data-stu-id="c285c-112">Detection origin.</span></span><br/>                                          |
| [<span data-ttu-id="c285c-113">**État de MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="c285c-113">**MPDETECTION\_STATE**</span></span>](mpdetection-state.md)                   | <span data-ttu-id="c285c-114">État de la menace actuellement détectée.</span><span class="sxs-lookup"><span data-stu-id="c285c-114">The state of the currently detected threat.</span></span><br/>                |
| [<span data-ttu-id="c285c-115">**État de MPEXECUTION \_**</span><span class="sxs-lookup"><span data-stu-id="c285c-115">**MPEXECUTION\_STATUS**</span></span>](mpexecution-status.md)                 | <span data-ttu-id="c285c-116">État d’exécution de la menace possible.</span><span class="sxs-lookup"><span data-stu-id="c285c-116">Possible threat execution status.</span></span><br/>                          |
| [<span data-ttu-id="c285c-117">**\_type de FASTPATH MP \_**</span><span class="sxs-lookup"><span data-stu-id="c285c-117">**MP\_FASTPATH\_TYPE**</span></span>](mp-fastpath-type.md)                    | <span data-ttu-id="c285c-118">Type de FastPath.</span><span class="sxs-lookup"><span data-stu-id="c285c-118">FastPath type.</span></span><br/>                                             |
| [<span data-ttu-id="c285c-119">**\_type de hachage MP \_**</span><span class="sxs-lookup"><span data-stu-id="c285c-119">**MP\_HASH\_TYPE**</span></span>](mp-hash-type.md)                            | <span data-ttu-id="c285c-120">Types de hachage possibles.</span><span class="sxs-lookup"><span data-stu-id="c285c-120">Possible hash types.</span></span><br/>                                       |
| [<span data-ttu-id="c285c-121">**MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="c285c-121">**MPNOTIFY**</span></span>](mpnotify.md)                                      | <span data-ttu-id="c285c-122">Notifications de rappel possibles.</span><span class="sxs-lookup"><span data-stu-id="c285c-122">Possible callback notifications.</span></span><br/>                           |
| [<span data-ttu-id="c285c-123">**\_type de limite de persistance MP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c285c-123">**MP\_PERSISTENCE\_LIMIT\_TYPE**</span></span>](mp-persistence-limit-type.md) | <span data-ttu-id="c285c-124">Type de limite de persistance.</span><span class="sxs-lookup"><span data-stu-id="c285c-124">Persistence limit type.</span></span><br/>                                    |
| [<span data-ttu-id="c285c-125">**raison de la suppression du pack d' \_ installation \_**</span><span class="sxs-lookup"><span data-stu-id="c285c-125">**MP\_REMOVAL\_REASON**</span></span>](mp-removal-reason.md)                  | <span data-ttu-id="c285c-126">Raison de la suppression de la signature FastPath.</span><span class="sxs-lookup"><span data-stu-id="c285c-126">FastPath signature removal reason.</span></span><br/>                         |
| [<span data-ttu-id="c285c-127">**\_raison MPRESOLVED**</span><span class="sxs-lookup"><span data-stu-id="c285c-127">**MPRESOLVED\_REASON**</span></span>](mpresolved-reason.md)                   | <span data-ttu-id="c285c-128">Raisons possibles d’une défaillance de correction en cours de résolution.</span><span class="sxs-lookup"><span data-stu-id="c285c-128">Possible reasons for a remediation failure being resolved.</span></span><br/> |
| [<span data-ttu-id="c285c-129">**\_type MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="c285c-129">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)                               | <span data-ttu-id="c285c-130">Type d’analyse effectuée.</span><span class="sxs-lookup"><span data-stu-id="c285c-130">Type of scan performed.</span></span><br/>                                    |
| [<span data-ttu-id="c285c-131">**\_type de signature MP \_**</span><span class="sxs-lookup"><span data-stu-id="c285c-131">**MP\_SIGNATURE\_TYPE**</span></span>](mp-signature-type.md)                  | <span data-ttu-id="c285c-132">Types de signature possibles.</span><span class="sxs-lookup"><span data-stu-id="c285c-132">Possible signature types.</span></span><br/>                                  |
| [<span data-ttu-id="c285c-133">**MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="c285c-133">**MPSOURCE**</span></span>](mpsource.md)                                      | <span data-ttu-id="c285c-134">Catégorie possible de la source.</span><span class="sxs-lookup"><span data-stu-id="c285c-134">Possible category of source.</span></span><br/>                               |
| [<span data-ttu-id="c285c-135">**\_indicateur MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="c285c-135">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)                           | <span data-ttu-id="c285c-136">Indicateurs de bits d’état de produit globaux possibles.</span><span class="sxs-lookup"><span data-stu-id="c285c-136">Possible overall product status bit flags.</span></span><br/>                 |
| [<span data-ttu-id="c285c-137">**\_action MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="c285c-137">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)                       | <span data-ttu-id="c285c-138">Actions possibles sur les menaces.</span><span class="sxs-lookup"><span data-stu-id="c285c-138">Possible threat actions.</span></span><br/>                                   |
| [<span data-ttu-id="c285c-139">**\_catégorie MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="c285c-139">**MPTHREAT\_CATEGORY**</span></span>](mpthreat-category.md)                   | <span data-ttu-id="c285c-140">Catégories de menaces possibles.</span><span class="sxs-lookup"><span data-stu-id="c285c-140">Possible threat categories.</span></span><br/>                                |
| [<span data-ttu-id="c285c-141">**\_détection MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="c285c-141">**MPTHREAT\_DETECTION**</span></span>](mpthreat-detection.md)                 | <span data-ttu-id="c285c-142">Types de détection de menaces incorrects connus possibles.</span><span class="sxs-lookup"><span data-stu-id="c285c-142">Possible known bad threat detection types.</span></span><br/>                 |
| [<span data-ttu-id="c285c-143">**\_gravité MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="c285c-143">**MPTHREAT\_SEVERITY**</span></span>](mpthreat-severity.md)                   | <span data-ttu-id="c285c-144">Risque de gravité des menaces.</span><span class="sxs-lookup"><span data-stu-id="c285c-144">Possible threat severities.</span></span><br/>                                |
| [<span data-ttu-id="c285c-145">**État de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="c285c-145">**MPTHREAT\_STATUS**</span></span>](mpthreat-status.md)                       | <span data-ttu-id="c285c-146">État possible de la menace.</span><span class="sxs-lookup"><span data-stu-id="c285c-146">Possible threat status.</span></span><br/>                                    |
| [<span data-ttu-id="c285c-147">**\_type MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="c285c-147">**MPTHREAT\_TYPE**</span></span>](mpthreat-type.md)                           | <span data-ttu-id="c285c-148">Types de menaces possibles.</span><span class="sxs-lookup"><span data-stu-id="c285c-148">Possible threat types.</span></span><br/>                                     |



 

 

 





