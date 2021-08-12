---
description: 'Le tableau suivant décrit les threads sur lesquels les événements d’objet Ink peuvent se déclencher. EventThreadsInkAddedFires sur le thread d’encre ou sur le thread de l’appelant. Un événement InkAdded généré par l’interaction de l’utilisateur avec l’objet InkCollector, l’objet InkOverlay ou le contrôle InkPicture, est déclenché sur le thread Ink. InkDeletedFires sur le thread d’encre ou sur le thread de l’appelant. Un événement InkDeleted généré par l’interaction de l’utilisateur avec l’objet InkCollector, l’objet InkOverlay ou le contrôle InkPicture, est déclenché sur le thread Ink. '
ms.assetid: 410f7126-5c4c-4c0c-8aa6-c94f15c903fc
title: Événements d’objets Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63217f603b06703b7824c19d3a709fdb97f31c9890e3148a6eeefd1e681d63b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451936"
---
# <a name="ink-object-events"></a>Événements d’objets Ink

Le tableau suivant décrit les threads sur lesquels les événements d’objet [**Ink**](inkdisp-class.md) peuvent se déclencher.



| Événement                                    | Threads                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | Se déclenche sur le thread d’encre ou sur le thread de l’appelant.<br/> Un événement [**InkAdded**](inkdisp-inkadded.md) généré par l’interaction de l’utilisateur avec l’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) ou le contrôle [InkPicture](inkpicture-control-reference.md) , est déclenché sur le thread Ink.<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | Se déclenche sur le thread d’encre ou sur le thread de l’appelant.<br/> Un événement [**InkDeleted**](inkdisp-inkdeleted.md) généré par l’interaction de l’utilisateur avec l’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) ou le contrôle [InkPicture](inkpicture-control-reference.md) , est déclenché sur le thread Ink.<br/> |



 

 

 




