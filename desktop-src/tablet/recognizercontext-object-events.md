---
description: Le tableau suivant décrit les threads sur lesquels les événements d’objet RecognizerContext peuvent se déclencher. EventThreadsRecognitionFires sur le thread de reconnaissance en arrière-plan ou sur le thread qui appelle la méthode Recognize de l’objet RecognizerContext. RecognitionWithAlternatesFires sur le thread de reconnaissance en arrière-plan.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Événements de l’objet RecognizerContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c8fa7aad4e7c6ba0dde2b38db4b82437b0732dda565aed8cc42750a339b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091439"
---
# <a name="recognizercontext-object-events"></a>Événements de l’objet RecognizerContext

Le tableau suivant décrit les threads sur lesquels les événements d’objet [**RecognizerContext**](inkrecognizercontext-class.md) peuvent se déclencher.



| Événement                                                                               | Threads                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reconnaissance**](inkrecognizercontext-recognition.md)                             | Se déclenche sur le thread de reconnaissance en arrière-plan ou sur le thread qui appelle la méthode [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) .<br/> |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Se déclenche sur le thread de reconnaissance en arrière-plan.<br/>                                                                                                                                                               |



 

 

 




