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
# <a name="system-reference-clock"></a>Horloge de référence système

L’objet horloge de référence système implémente une horloge de référence qui retourne l’heure système. Si aucun des filtres du graphique ne fournit une horloge de référence, le gestionnaire de graphique de filtre utilise ce composant pour synchroniser le graphique. Créez cet objet en appelant **CoCreateInstance**.



| Étiquette | Valeur |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificateur de classe | CLSID \_ SystemClock                                                                                                                                       |
| Interfaces       | [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets DirectShow](directshow-objects.md)
</dt> <dt>

[Horloges de référence](reference-clocks.md)
</dt> <dt>

[Temps et horloges dans DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



