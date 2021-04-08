---
description: Vous pouvez utiliser les fonctions suivantes pour travailler avec les données de performances dans Visual Basic.
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Fonctions des compteurs de performances pour Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777aa887b9dc42a061de95fb6f33dbf9d3dff7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865102"
---
# <a name="performance-counters-functions-for-visual-basic"></a><span data-ttu-id="51b41-103">Fonctions des compteurs de performances pour Visual Basic</span><span class="sxs-lookup"><span data-stu-id="51b41-103">Performance Counters Functions for Visual Basic</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51b41-104">Les fonctions décrites dans cette rubrique peuvent être modifiées ou non disponibles à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="51b41-104">The functions that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="51b41-105">Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="51b41-105">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="51b41-106">Vous pouvez utiliser les fonctions suivantes pour travailler avec les données de performances dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="51b41-106">You can use the following functions to work with performance data in Visual Basic.</span></span>

- [<span data-ttu-id="51b41-107">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="51b41-107">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="51b41-108">**PdhCollectQueryData**</span><span class="sxs-lookup"><span data-stu-id="51b41-108">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="51b41-109">**PdhRemoveCounter**</span><span class="sxs-lookup"><span data-stu-id="51b41-109">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="51b41-110">**PdhVbAddCounter**</span><span class="sxs-lookup"><span data-stu-id="51b41-110">**PdhVbAddCounter**</span></span>](pdhvbaddcounter.md)
- [<span data-ttu-id="51b41-111">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="51b41-111">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
- [<span data-ttu-id="51b41-112">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="51b41-112">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
- [<span data-ttu-id="51b41-113">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="51b41-113">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
- [<span data-ttu-id="51b41-114">**PdhVbGetDoubleCounterValue**</span><span class="sxs-lookup"><span data-stu-id="51b41-114">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
- [<span data-ttu-id="51b41-115">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="51b41-115">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
- [<span data-ttu-id="51b41-116">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="51b41-116">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
- [<span data-ttu-id="51b41-117">**PdhVbIsGoodStatus**</span><span class="sxs-lookup"><span data-stu-id="51b41-117">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
- [<span data-ttu-id="51b41-118">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="51b41-118">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
- [<span data-ttu-id="51b41-119">**PdhVbOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="51b41-119">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
- [<span data-ttu-id="51b41-120">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="51b41-120">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)

> [!NOTE]
> <span data-ttu-id="51b41-121">Les `PdhVb***` fonctions fonctionnent sur une session par processus et ne sont pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="51b41-121">The `PdhVb***` functions work on a per-process session and are not thread-safe.</span></span> <span data-ttu-id="51b41-122">Ces fonctions ne doivent être utilisées qu’à partir d’applications simples à thread unique.</span><span class="sxs-lookup"><span data-stu-id="51b41-122">These functions should only be used from simple single-threaded applications.</span></span>
