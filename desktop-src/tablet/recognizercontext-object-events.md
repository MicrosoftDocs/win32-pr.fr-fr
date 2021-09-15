---
description: Le tableau suivant décrit les threads sur lesquels les événements d’objet RecognizerContext peuvent se déclencher. EventThreadsRecognitionFires sur le thread de reconnaissance en arrière-plan ou sur le thread qui appelle la méthode Recognize de l’objet RecognizerContext. RecognitionWithAlternatesFires sur le thread de reconnaissance en arrière-plan.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Événements de l’objet RecognizerContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc520801ae3391288966e6286d24449be4741b87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411440"
---
# <a name="recognizercontext-object-events"></a>Événements de l’objet RecognizerContext

Le tableau suivant décrit les threads sur lesquels les événements d’objet [**RecognizerContext**](inkrecognizercontext-class.md) peuvent se déclencher.



| Événement                                                                               | Threads                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reconnaissance**](inkrecognizercontext-recognition.md)                             | Se déclenche sur le thread de reconnaissance en arrière-plan ou sur le thread qui appelle la méthode [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) .<br/> |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Se déclenche sur le thread de reconnaissance en arrière-plan.<br/>                                                                                                                                                               |



 

 

 




