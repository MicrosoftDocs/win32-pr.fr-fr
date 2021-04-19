---
description: Séquences d’actions suggérées pour une table InstalUISequence de base dans une base de données Windows Installer.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: InstallUISequence suggéré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523252"
---
# <a name="suggested-installuisequence"></a><span data-ttu-id="2b975-103">InstallUISequence suggéré</span><span class="sxs-lookup"><span data-stu-id="2b975-103">Suggested InstallUISequence</span></span>



| <span data-ttu-id="2b975-104">Action</span><span class="sxs-lookup"><span data-stu-id="2b975-104">Action</span></span>                                          | <span data-ttu-id="2b975-105">Condition</span><span class="sxs-lookup"><span data-stu-id="2b975-105">Condition</span></span>                                                                                                  | <span data-ttu-id="2b975-106">Séquence</span><span class="sxs-lookup"><span data-stu-id="2b975-106">Sequence</span></span> |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="2b975-107">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="2b975-107">FatalErrorDlg</span></span>                                   |                                                                                                            | <span data-ttu-id="2b975-108">-3</span><span class="sxs-lookup"><span data-stu-id="2b975-108">-3</span></span>       |
| <span data-ttu-id="2b975-109">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="2b975-109">UserExitDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="2b975-110">-2</span><span class="sxs-lookup"><span data-stu-id="2b975-110">-2</span></span>       |
| <span data-ttu-id="2b975-111">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="2b975-111">ExitDlg</span></span>                                         |                                                                                                            | <span data-ttu-id="2b975-112">-1</span><span class="sxs-lookup"><span data-stu-id="2b975-112">-1</span></span>       |
| [<span data-ttu-id="2b975-113">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="2b975-113">LaunchConditions</span></span>](launchconditions-action.md) |                                                                                                            | <span data-ttu-id="2b975-114">100</span><span class="sxs-lookup"><span data-stu-id="2b975-114">100</span></span>      |
| <span data-ttu-id="2b975-115">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="2b975-115">PrepareDlg</span></span>                                      |                                                                                                            | <span data-ttu-id="2b975-116">140</span><span class="sxs-lookup"><span data-stu-id="2b975-116">140</span></span>      |
| [<span data-ttu-id="2b975-117">AppSearch</span><span class="sxs-lookup"><span data-stu-id="2b975-117">AppSearch</span></span>](appsearch-action.md)               |                                                                                                            | <span data-ttu-id="2b975-118">400</span><span class="sxs-lookup"><span data-stu-id="2b975-118">400</span></span>      |
| [<span data-ttu-id="2b975-119">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="2b975-119">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="2b975-120">NON [ **installé**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="2b975-120">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="2b975-121">500</span><span class="sxs-lookup"><span data-stu-id="2b975-121">500</span></span>      |
| [<span data-ttu-id="2b975-122">RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="2b975-122">RMCCPSearch</span></span>](rmccpsearch-action.md)           | <span data-ttu-id="2b975-123">NON [ **installé**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="2b975-123">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="2b975-124">600</span><span class="sxs-lookup"><span data-stu-id="2b975-124">600</span></span>      |
| [<span data-ttu-id="2b975-125">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="2b975-125">CostInitialize</span></span>](costinitialize-action.md)     |                                                                                                            | <span data-ttu-id="2b975-126">800</span><span class="sxs-lookup"><span data-stu-id="2b975-126">800</span></span>      |
| [<span data-ttu-id="2b975-127">FileCost</span><span class="sxs-lookup"><span data-stu-id="2b975-127">FileCost</span></span>](filecost-action.md)                 |                                                                                                            | <span data-ttu-id="2b975-128">900</span><span class="sxs-lookup"><span data-stu-id="2b975-128">900</span></span>      |
| [<span data-ttu-id="2b975-129">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="2b975-129">CostFinalize</span></span>](costfinalize-action.md)         |                                                                                                            | <span data-ttu-id="2b975-130">1 000</span><span class="sxs-lookup"><span data-stu-id="2b975-130">1000</span></span>     |
| <span data-ttu-id="2b975-131">WelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="2b975-131">WelcomeDlg</span></span>                                      | <span data-ttu-id="2b975-132">NON [ **installé**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="2b975-132">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="2b975-133">1230</span><span class="sxs-lookup"><span data-stu-id="2b975-133">1230</span></span>     |
| <span data-ttu-id="2b975-134">ResumeDlg</span><span class="sxs-lookup"><span data-stu-id="2b975-134">ResumeDlg</span></span>                                       | <span data-ttu-id="2b975-135">[**Installé**](installed.md) ET ( [**reprendre**](resume.md) ou [**présélectionner**](preselected.md))</span><span class="sxs-lookup"><span data-stu-id="2b975-135">[**Installed**](installed.md) AND ( [**RESUME**](resume.md) OR [**Preselected**](preselected.md))</span></span>       | <span data-ttu-id="2b975-136">1240</span><span class="sxs-lookup"><span data-stu-id="2b975-136">1240</span></span>     |
| <span data-ttu-id="2b975-137">MaintenanceWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="2b975-137">MaintenanceWelcomeDlg</span></span>                           | <span data-ttu-id="2b975-138">[**Installé**](installed.md) ET ne pas [**reprendre**](resume.md) et ne pas [**présélectionner**](preselected.md)</span><span class="sxs-lookup"><span data-stu-id="2b975-138">[**Installed**](installed.md) AND NOT [**RESUME**](resume.md) AND NOT [**Preselected**](preselected.md)</span></span> | <span data-ttu-id="2b975-139">1250</span><span class="sxs-lookup"><span data-stu-id="2b975-139">1250</span></span>     |
| <span data-ttu-id="2b975-140">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="2b975-140">ProgressDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="2b975-141">1 280</span><span class="sxs-lookup"><span data-stu-id="2b975-141">1280</span></span>     |
| [<span data-ttu-id="2b975-142">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="2b975-142">ExecuteAction</span></span>](executeaction-action.md)       |                                                                                                            | <span data-ttu-id="2b975-143">1 300</span><span class="sxs-lookup"><span data-stu-id="2b975-143">1300</span></span>     |



 

 

 



