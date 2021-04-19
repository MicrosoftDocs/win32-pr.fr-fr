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
# <a name="system-reference-clock"></a>Horloge de référence système

L’objet horloge de référence système implémente une horloge de référence qui retourne l’heure système. Si aucun des filtres du graphique ne fournit une horloge de référence, le gestionnaire de graphique de filtre utilise ce composant pour synchroniser le graphique. Créez cet objet en appelant **CoCreateInstance**.



|                  |                                                                                                                                                          |
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

 

 



