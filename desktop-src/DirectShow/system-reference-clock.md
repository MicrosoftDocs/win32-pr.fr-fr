---
description: Horloge de référence système
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Horloge de référence système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b3b4fa69b2ff9b74b937dd38d8be83203d5cdd43ba9a26d2cac4077c40c811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651839"
---
# <a name="system-reference-clock"></a>Horloge de référence système

L’objet horloge de référence système implémente une horloge de référence qui retourne l’heure système. Si aucun des filtres du graphique ne fournit une horloge de référence, le gestionnaire de graphique de filtre utilise ce composant pour synchroniser le graphique. Créez cet objet en appelant **CoCreateInstance**.



| Étiquette | Valeur |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificateur de classe | CLSID \_ SystemClock                                                                                                                                       |
| Interfaces       | [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Objets](directshow-objects.md)
</dt> <dt>

[Horloges de référence](reference-clocks.md)
</dt> <dt>

[Temps et horloges dans DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



