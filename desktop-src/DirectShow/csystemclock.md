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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010006"
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



 

 

 



