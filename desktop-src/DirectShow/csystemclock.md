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
ms.openlocfilehash: c608b1d3f44a82d7aa964e803dec147a7216a71e85c6d797135713cf28af3fa0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317222"
---
# <a name="csystemclock-class"></a>CSystemClock, classe

![hiérarchie de la classe csystemclock](images/sclock01.png)

La `CSystemClock` classe implémente une horloge qui retourne l’heure système.

Cette classe dérive de la classe [**CBaseReferenceClock**](cbasereferenceclock.md) et ajoute la prise en charge des interfaces **IPersist** et [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) .



| M&#233;thodes publiques                                        | Description                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [**CreateInstance**](csystemclock-createinstance.md) | Crée une instance de cet objet.              |
| [**CSystemClock**](csystemclock-csystemclock.md)     | Méthode de constructeur.                                 |
| Méthodes IAMClockAdjust                                | Description                                         |
| [**SetClockDelta**](csystemclock-setclockdelta.md)   | Ajuste l’heure de l’horloge.                             |
| IPersist, méthodes                                      | Description                                         |
| [**GetClassID**](csystemclock-getclassid.md)         | Retourne l’identificateur de classe (CLSID) de l’objet. |



 

 

 



