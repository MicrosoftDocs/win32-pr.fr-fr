---
description: Horloge de référence système
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Horloge de référence système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fab63c4ba8bfd6a7db9c476179d6e649869fb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530129"
---
# <a name="system-reference-clock"></a><span data-ttu-id="b5a2c-103">Horloge de référence système</span><span class="sxs-lookup"><span data-stu-id="b5a2c-103">System Reference Clock</span></span>

<span data-ttu-id="b5a2c-104">L’objet horloge de référence système implémente une horloge de référence qui retourne l’heure système.</span><span class="sxs-lookup"><span data-stu-id="b5a2c-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="b5a2c-105">Si aucun des filtres du graphique ne fournit une horloge de référence, le gestionnaire de graphique de filtre utilise ce composant pour synchroniser le graphique.</span><span class="sxs-lookup"><span data-stu-id="b5a2c-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="b5a2c-106">Créez cet objet en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="b5a2c-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a2c-107">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="b5a2c-107">Class Identifier</span></span> | <span data-ttu-id="b5a2c-108">CLSID \_ SystemClock</span><span class="sxs-lookup"><span data-stu-id="b5a2c-108">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="b5a2c-109">Interfaces</span><span class="sxs-lookup"><span data-stu-id="b5a2c-109">Interfaces</span></span>       | <span data-ttu-id="b5a2c-110">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="b5a2c-110">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b5a2c-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5a2c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5a2c-112">Objets DirectShow</span><span class="sxs-lookup"><span data-stu-id="b5a2c-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="b5a2c-113">Horloges de référence</span><span class="sxs-lookup"><span data-stu-id="b5a2c-113">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="b5a2c-114">Temps et horloges dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="b5a2c-114">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



