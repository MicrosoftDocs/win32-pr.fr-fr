---
description: Le tableau suivant décrit les threads sur lesquels les événements d’objet RecognizerContext peuvent se déclencher. EventThreadsRecognitionFires sur le thread de reconnaissance en arrière-plan ou sur le thread qui appelle la méthode Recognize de l’objet RecognizerContext. RecognitionWithAlternatesFires sur le thread de reconnaissance en arrière-plan.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Événements de l’objet RecognizerContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc520801ae3391288966e6286d24449be4741b87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952532"
---
# <a name="recognizercontext-object-events"></a><span data-ttu-id="26551-103">Événements de l’objet RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="26551-103">RecognizerContext Object Events</span></span>

<span data-ttu-id="26551-104">Le tableau suivant décrit les threads sur lesquels les événements d’objet [**RecognizerContext**](inkrecognizercontext-class.md) peuvent se déclencher.</span><span class="sxs-lookup"><span data-stu-id="26551-104">The following table describes which threads the [**RecognizerContext**](inkrecognizercontext-class.md) object events can fire on.</span></span>



| <span data-ttu-id="26551-105">Événement</span><span class="sxs-lookup"><span data-stu-id="26551-105">Event</span></span>                                                                               | <span data-ttu-id="26551-106">Threads</span><span class="sxs-lookup"><span data-stu-id="26551-106">Threads</span></span>                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26551-107">**Reconnaissance**</span><span class="sxs-lookup"><span data-stu-id="26551-107">**Recognition**</span></span>](inkrecognizercontext-recognition.md)                             | <span data-ttu-id="26551-108">Se déclenche sur le thread de reconnaissance en arrière-plan ou sur le thread qui appelle la méthode [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="26551-108">Fires on the background recognition thread, or on the thread which calls the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method.</span></span><br/> |
| [<span data-ttu-id="26551-109">**RecognitionWithAlternates**</span><span class="sxs-lookup"><span data-stu-id="26551-109">**RecognitionWithAlternates**</span></span>](inkrecognizercontext-recognitionwithalternates.md) | <span data-ttu-id="26551-110">Se déclenche sur le thread de reconnaissance en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="26551-110">Fires on the background recognition thread.</span></span><br/>                                                                                                                                                               |



 

 

 




