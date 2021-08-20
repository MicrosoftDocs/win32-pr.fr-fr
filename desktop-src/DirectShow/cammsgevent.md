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
ms.openlocfilehash: c7c4d3c8268f06e81d1bd1a5285f7e4785459889397ccf249bbde7f0dd627f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955432"
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
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




