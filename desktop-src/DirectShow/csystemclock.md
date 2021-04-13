---
description: La classe CSystemClock implémente une horloge qui retourne l’heure système.
ms.assetid: 22f8b641-6472-433f-bff4-4e62eae25c9b
title: CSystemClock, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock
api_type:
- COM
api_location: ''
ms.openlocfilehash: e9cc5e0bde8983cfd8c544d3898d4af628e10f87
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569101"
---
# <a name="csystemclock-class"></a><span data-ttu-id="94525-103">CSystemClock, classe</span><span class="sxs-lookup"><span data-stu-id="94525-103">CSystemClock class</span></span>

![hiérarchie de la classe csystemclock](images/sclock01.png)

<span data-ttu-id="94525-105">La `CSystemClock` classe implémente une horloge qui retourne l’heure système.</span><span class="sxs-lookup"><span data-stu-id="94525-105">The `CSystemClock` class implements a clock that returns the system time.</span></span>

<span data-ttu-id="94525-106">Cette classe dérive de la classe [**CBaseReferenceClock**](cbasereferenceclock.md) et ajoute la prise en charge des interfaces **IPersist** et [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) .</span><span class="sxs-lookup"><span data-stu-id="94525-106">This class derives from the [**CBaseReferenceClock**](cbasereferenceclock.md) class, and adds support for the **IPersist** and [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) interfaces.</span></span>



| <span data-ttu-id="94525-107">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="94525-107">Public Methods</span></span>                                        | <span data-ttu-id="94525-108">Description</span><span class="sxs-lookup"><span data-stu-id="94525-108">Description</span></span>                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="94525-109">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="94525-109">**CreateInstance**</span></span>](csystemclock-createinstance.md) | <span data-ttu-id="94525-110">Crée une instance de cet objet.</span><span class="sxs-lookup"><span data-stu-id="94525-110">Creates a new instance of this object.</span></span>              |
| [<span data-ttu-id="94525-111">**CSystemClock**</span><span class="sxs-lookup"><span data-stu-id="94525-111">**CSystemClock**</span></span>](csystemclock-csystemclock.md)     | <span data-ttu-id="94525-112">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="94525-112">Constructor method.</span></span>                                 |
| <span data-ttu-id="94525-113">Méthodes IAMClockAdjust</span><span class="sxs-lookup"><span data-stu-id="94525-113">IAMClockAdjust Methods</span></span>                                | <span data-ttu-id="94525-114">Description</span><span class="sxs-lookup"><span data-stu-id="94525-114">Description</span></span>                                         |
| [<span data-ttu-id="94525-115">**SetClockDelta**</span><span class="sxs-lookup"><span data-stu-id="94525-115">**SetClockDelta**</span></span>](csystemclock-setclockdelta.md)   | <span data-ttu-id="94525-116">Ajuste l’heure de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="94525-116">Adjusts the clock time.</span></span>                             |
| <span data-ttu-id="94525-117">IPersist, méthodes</span><span class="sxs-lookup"><span data-stu-id="94525-117">IPersist Methods</span></span>                                      | <span data-ttu-id="94525-118">Description</span><span class="sxs-lookup"><span data-stu-id="94525-118">Description</span></span>                                         |
| [<span data-ttu-id="94525-119">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="94525-119">**GetClassID**</span></span>](csystemclock-getclassid.md)         | <span data-ttu-id="94525-120">Retourne l’identificateur de classe (CLSID) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="94525-120">Returns the class identifier (CLSID) of the object.</span></span> |



 

 

 



