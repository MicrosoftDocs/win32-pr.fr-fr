---
description: La classe CAMMsgEvent est un wrapper pour les objets d’événement qui effectuent le traitement des messages.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: CAMMsgEvent, classe (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ebac7aae11f7a7b7d6b846e262e93b5759210b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536040"
---
# <a name="cammsgevent-class"></a>CAMMsgEvent, classe

![hiérarchie de la classe cammsgevent](images/util06.png)

La `CAMMsgEvent` classe est un wrapper pour les objets d’événement qui effectuent le traitement des messages.

Cette classe dérive de l’objet [**CAMEvent**](camevent.md) . Elle ajoute une méthode, [**CAMMsgEvent :: WaitMsg**](cammsgevent-waitmsg.md), qui distribue les messages entrants en attente.



| M&#233;thodes publiques                                 | Description                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [**CAMMsgEvent**](cammsgevent-cammsgevent.md) | Constructeur.                                                         |
| [**WaitMsg**](cammsgevent-waitmsg.md)         | Attend que l’événement soit signalé, tout en distribuant les messages envoyés. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




