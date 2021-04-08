---
title: Structures de mode liste
description: Structures de mode liste
ms.assetid: 12d77514-7281-4873-b456-252ff80ed7f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b603e9acd65448b3c4970aa9552f4d2b91ebccd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761714"
---
# <a name="list-view-structures"></a><span data-ttu-id="84d70-103">Structures de mode liste</span><span class="sxs-lookup"><span data-stu-id="84d70-103">List View Structures</span></span>

## <a name="in-this-section"></a><span data-ttu-id="84d70-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="84d70-104">In This Section</span></span>

-   [<span data-ttu-id="84d70-105">**LVBKIMAGE**</span><span class="sxs-lookup"><span data-stu-id="84d70-105">**LVBKIMAGE**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea)
-   [<span data-ttu-id="84d70-106">**LVCOLUMN**</span><span class="sxs-lookup"><span data-stu-id="84d70-106">**LVCOLUMN**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)
-   [<span data-ttu-id="84d70-107">**LVFINDINFO**</span><span class="sxs-lookup"><span data-stu-id="84d70-107">**LVFINDINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa)
-   [<span data-ttu-id="84d70-108">**LVFOOTERINFO**</span><span class="sxs-lookup"><span data-stu-id="84d70-108">**LVFOOTERINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo)
-   [<span data-ttu-id="84d70-109">**LVFOOTERITEM**</span><span class="sxs-lookup"><span data-stu-id="84d70-109">**LVFOOTERITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem)
-   [<span data-ttu-id="84d70-110">**LVGROUP**</span><span class="sxs-lookup"><span data-stu-id="84d70-110">**LVGROUP**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvgroup)
-   [<span data-ttu-id="84d70-111">**LVGROUPMETRICS**</span><span class="sxs-lookup"><span data-stu-id="84d70-111">**LVGROUPMETRICS**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics)
-   [<span data-ttu-id="84d70-112">**LVHITTESTINFO**</span><span class="sxs-lookup"><span data-stu-id="84d70-112">**LVHITTESTINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo)
-   [<span data-ttu-id="84d70-113">**LVINSERTGROUPSORTED**</span><span class="sxs-lookup"><span data-stu-id="84d70-113">**LVINSERTGROUPSORTED**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
-   [<span data-ttu-id="84d70-114">**LVINSERTMARK**</span><span class="sxs-lookup"><span data-stu-id="84d70-114">**LVINSERTMARK**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark)
-   [<span data-ttu-id="84d70-115">**LVITEM**</span><span class="sxs-lookup"><span data-stu-id="84d70-115">**LVITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvitema)
-   [<span data-ttu-id="84d70-116">**LVITEMINDEX**</span><span class="sxs-lookup"><span data-stu-id="84d70-116">**LVITEMINDEX**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvitemindex)
-   [<span data-ttu-id="84d70-117">**LVSETINFOTIP**</span><span class="sxs-lookup"><span data-stu-id="84d70-117">**LVSETINFOTIP**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip)
-   [<span data-ttu-id="84d70-118">**LVTILEINFO**</span><span class="sxs-lookup"><span data-stu-id="84d70-118">**LVTILEINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo)
-   [<span data-ttu-id="84d70-119">**LVTILEVIEWINFO**</span><span class="sxs-lookup"><span data-stu-id="84d70-119">**LVTILEVIEWINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo)
-   [<span data-ttu-id="84d70-120">**NMITEMACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="84d70-120">**NMITEMACTIVATE**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate)
-   [<span data-ttu-id="84d70-121">**NMLISTVIEW**</span><span class="sxs-lookup"><span data-stu-id="84d70-121">**NMLISTVIEW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlistview)
-   [<span data-ttu-id="84d70-122">**NMLVCACHEHINT**</span><span class="sxs-lookup"><span data-stu-id="84d70-122">**NMLVCACHEHINT**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint)
-   [<span data-ttu-id="84d70-123">**NMLVCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="84d70-123">**NMLVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw)
-   [<span data-ttu-id="84d70-124">**NMLVDISPINFO**</span><span class="sxs-lookup"><span data-stu-id="84d70-124">**NMLVDISPINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa)
-   [<span data-ttu-id="84d70-125">**NMLVEMPTYMARKUP**</span><span class="sxs-lookup"><span data-stu-id="84d70-125">**NMLVEMPTYMARKUP**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup)
-   [<span data-ttu-id="84d70-126">**NMLVFINDITEM**</span><span class="sxs-lookup"><span data-stu-id="84d70-126">**NMLVFINDITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema)
-   [<span data-ttu-id="84d70-127">**NMLVGETINFOTIP**</span><span class="sxs-lookup"><span data-stu-id="84d70-127">**NMLVGETINFOTIP**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa)
-   [<span data-ttu-id="84d70-128">**NMLVKEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="84d70-128">**NMLVKEYDOWN**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown)
-   [<span data-ttu-id="84d70-129">**NMLVLINK**</span><span class="sxs-lookup"><span data-stu-id="84d70-129">**NMLVLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvlink)
-   [<span data-ttu-id="84d70-130">**NMLVODSTATECHANGE**</span><span class="sxs-lookup"><span data-stu-id="84d70-130">**NMLVODSTATECHANGE**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange)
-   [<span data-ttu-id="84d70-131">**NMLVSCROLL**</span><span class="sxs-lookup"><span data-stu-id="84d70-131">**NMLVSCROLL**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll)

 

 




