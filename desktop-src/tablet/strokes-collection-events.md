---
description: Le tableau suivant décrit les threads sur lesquels les événements de collection de traits peuvent se déclencher. EventThreadsStrokesAddedFires sur le thread d’encre ou sur le thread de l’appelant. Un événement StrokesAdded généré par l’interaction de l’utilisateur avec l’objet InkCollector, l’objet InkOverlay ou le contrôle InkPicture, est déclenché sur le thread Ink. StrokesRemovedFires sur le thread d’encre ou sur le thread de l’appelant. Un événement StrokesRemoved généré par l’interaction de l’utilisateur avec l’objet InkCollector, l’objet InkOverlay ou le contrôle InkPicture, est déclenché sur le thread Ink.
ms.assetid: f9503c3b-6c43-442c-af43-3415ad17626f
title: Événements de collection de traits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04388179c53a4b85c5333ae6061cdd7612967174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535624"
---
# <a name="strokes-collection-events"></a>Événements de collection de traits

Le tableau suivant décrit les threads sur lesquels les événements de collection de [**traits**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) peuvent se déclencher.



| Événement                                               | Threads                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**StrokesAdded**](inkstrokes-strokesadded.md)     | Se déclenche sur le thread d’encre ou sur le thread de l’appelant.<br/> Un événement [**StrokesAdded**](inkstrokes-strokesadded.md) généré par l’interaction de l’utilisateur avec l’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) ou le contrôle [InkPicture](inkpicture-control-reference.md) , est déclenché sur le thread Ink.<br/>     |
| [**StrokesRemoved**](inkstrokes-strokesremoved.md) | Se déclenche sur le thread d’encre ou sur le thread de l’appelant.<br/> Un événement [**StrokesRemoved**](inkstrokes-strokesremoved.md) généré par l’interaction de l’utilisateur avec l’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) ou le contrôle [InkPicture](inkpicture-control-reference.md) , est déclenché sur le thread Ink.<br/> |



 

 

 
