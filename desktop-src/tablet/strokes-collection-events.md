---
description: Le tableau suivant décrit les threads sur lesquels les événements de collection de traits peuvent se déclencher. EventThreadsStrokesAddedFires sur le thread d’encre ou sur le thread de l’appelant. Un événement StrokesAdded généré par l’interaction de l’utilisateur avec l’objet InkCollector, l’objet InkOverlay ou le contrôle InkPicture, est déclenché sur le thread Ink. StrokesRemovedFires sur le thread d’encre ou sur le thread de l’appelant. Un événement StrokesRemoved généré par l’interaction de l’utilisateur avec l’objet InkCollector, l’objet InkOverlay ou le contrôle InkPicture, est déclenché sur le thread Ink.
ms.assetid: f9503c3b-6c43-442c-af43-3415ad17626f
title: Événements de collection de traits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24be819f63fa29cd0d650ce27f760984ca6d917886fe5f45e1ec72cf4c9fe2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589779"
---
# <a name="strokes-collection-events"></a>Événements de collection de traits

Le tableau suivant décrit les threads sur lesquels les événements de collection de [**traits**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) peuvent se déclencher.



| Événement                                               | Threads                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**StrokesAdded**](inkstrokes-strokesadded.md)     | Se déclenche sur le thread d’encre ou sur le thread de l’appelant.<br/> Un événement [**StrokesAdded**](inkstrokes-strokesadded.md) généré par l’interaction de l’utilisateur avec l’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) ou le contrôle [InkPicture](inkpicture-control-reference.md) , est déclenché sur le thread Ink.<br/>     |
| [**StrokesRemoved**](inkstrokes-strokesremoved.md) | Se déclenche sur le thread d’encre ou sur le thread de l’appelant.<br/> Un événement [**StrokesRemoved**](inkstrokes-strokesremoved.md) généré par l’interaction de l’utilisateur avec l’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) ou le contrôle [InkPicture](inkpicture-control-reference.md) , est déclenché sur le thread Ink.<br/> |



 

 

 
