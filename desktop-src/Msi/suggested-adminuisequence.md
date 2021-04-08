---
description: Séquences d’actions suggérées pour une table AdminUISequence de base dans une base de données Windows Installer.
ms.assetid: a5371133-7d55-4041-8e1f-ecc8245c8d3a
title: AdminUISequence suggéré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af34c0662d19070b1d97b88e8942b2276cc64a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755397"
---
# <a name="suggested-adminuisequence"></a><span data-ttu-id="9c5d5-103">AdminUISequence suggéré</span><span class="sxs-lookup"><span data-stu-id="9c5d5-103">Suggested AdminUISequence</span></span>



| <span data-ttu-id="9c5d5-104">Action</span><span class="sxs-lookup"><span data-stu-id="9c5d5-104">Action</span></span>                                      | <span data-ttu-id="9c5d5-105">Condition</span><span class="sxs-lookup"><span data-stu-id="9c5d5-105">Condition</span></span> | <span data-ttu-id="9c5d5-106">Séquence</span><span class="sxs-lookup"><span data-stu-id="9c5d5-106">Sequence</span></span> |
|---------------------------------------------|-----------|----------|
| <span data-ttu-id="9c5d5-107">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="9c5d5-107">FatalErrorDlg</span></span>                               |           | <span data-ttu-id="9c5d5-108">-3</span><span class="sxs-lookup"><span data-stu-id="9c5d5-108">-3</span></span>       |
| <span data-ttu-id="9c5d5-109">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="9c5d5-109">UserExitDlg</span></span>                                 |           | <span data-ttu-id="9c5d5-110">-2</span><span class="sxs-lookup"><span data-stu-id="9c5d5-110">-2</span></span>       |
| <span data-ttu-id="9c5d5-111">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="9c5d5-111">ExitDlg</span></span>                                     |           | <span data-ttu-id="9c5d5-112">-1</span><span class="sxs-lookup"><span data-stu-id="9c5d5-112">-1</span></span>       |
| <span data-ttu-id="9c5d5-113">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="9c5d5-113">PrepareDlg</span></span>                                  |           | <span data-ttu-id="9c5d5-114">140</span><span class="sxs-lookup"><span data-stu-id="9c5d5-114">140</span></span>      |
| [<span data-ttu-id="9c5d5-115">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="9c5d5-115">CostInitialize</span></span>](costinitialize-action.md) |           | <span data-ttu-id="9c5d5-116">800</span><span class="sxs-lookup"><span data-stu-id="9c5d5-116">800</span></span>      |
| [<span data-ttu-id="9c5d5-117">FileCost</span><span class="sxs-lookup"><span data-stu-id="9c5d5-117">FileCost</span></span>](filecost-action.md)             |           | <span data-ttu-id="9c5d5-118">900</span><span class="sxs-lookup"><span data-stu-id="9c5d5-118">900</span></span>      |
| [<span data-ttu-id="9c5d5-119">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="9c5d5-119">CostFinalize</span></span>](costfinalize-action.md)     |           | <span data-ttu-id="9c5d5-120">1 000</span><span class="sxs-lookup"><span data-stu-id="9c5d5-120">1000</span></span>     |
| <span data-ttu-id="9c5d5-121">AdminWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="9c5d5-121">AdminWelcomeDlg</span></span>                             |           | <span data-ttu-id="9c5d5-122">1230</span><span class="sxs-lookup"><span data-stu-id="9c5d5-122">1230</span></span>     |
| <span data-ttu-id="9c5d5-123">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="9c5d5-123">ProgressDlg</span></span>                                 |           | <span data-ttu-id="9c5d5-124">1 280</span><span class="sxs-lookup"><span data-stu-id="9c5d5-124">1280</span></span>     |
| [<span data-ttu-id="9c5d5-125">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="9c5d5-125">ExecuteAction</span></span>](executeaction-action.md)   |           | <span data-ttu-id="9c5d5-126">1 300</span><span class="sxs-lookup"><span data-stu-id="9c5d5-126">1300</span></span>     |



 

 

 



