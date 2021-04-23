---
description: Horloge de référence système
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Horloge de référence système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8de8b208e32b6ea4772f3183c38a816ea43bb6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909487"
---
# <a name="system-reference-clock"></a><span data-ttu-id="a9ab4-103">Horloge de référence système</span><span class="sxs-lookup"><span data-stu-id="a9ab4-103">System Reference Clock</span></span>

<span data-ttu-id="a9ab4-104">L’objet horloge de référence système implémente une horloge de référence qui retourne l’heure système.</span><span class="sxs-lookup"><span data-stu-id="a9ab4-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="a9ab4-105">Si aucun des filtres du graphique ne fournit une horloge de référence, le gestionnaire de graphique de filtre utilise ce composant pour synchroniser le graphique.</span><span class="sxs-lookup"><span data-stu-id="a9ab4-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="a9ab4-106">Créez cet objet en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="a9ab4-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="a9ab4-107">Étiquette</span><span class="sxs-lookup"><span data-stu-id="a9ab4-107">Label</span></span> | <span data-ttu-id="a9ab4-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9ab4-108">Value</span></span> |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ab4-109">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="a9ab4-109">Class Identifier</span></span> | <span data-ttu-id="a9ab4-110">CLSID \_ SystemClock</span><span class="sxs-lookup"><span data-stu-id="a9ab4-110">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="a9ab4-111">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a9ab4-111">Interfaces</span></span>       | <span data-ttu-id="a9ab4-112">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="a9ab4-112">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a9ab4-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a9ab4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9ab4-114">Objets DirectShow</span><span class="sxs-lookup"><span data-stu-id="a9ab4-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="a9ab4-115">Horloges de référence</span><span class="sxs-lookup"><span data-stu-id="a9ab4-115">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="a9ab4-116">Temps et horloges dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="a9ab4-116">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



