---
title: Utilisation de PlaySound pour boucler des sons
description: Utilisation de PlaySound pour boucler des sons
ms.assetid: 747b9a76-5ff3-488e-ba85-c4d926e1e723
keywords:
- Wave audio, fonction PlaySound
- audio Wave, sons en boucle
- Wave audio, paramètre fdwSound
- PlaySound, fonction, bouclage des sons
- PlaySound, fonction, paramètre fdwSound
- bouclage des sons Wave Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5373e703c7a02068094e312dee18690a797b330e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381783"
---
# <a name="using-playsound-to-loop-sounds"></a><span data-ttu-id="10e59-109">Utilisation de PlaySound pour boucler des sons</span><span class="sxs-lookup"><span data-stu-id="10e59-109">Using PlaySound to Loop Sounds</span></span>

<span data-ttu-id="10e59-110">Si vous spécifiez la \_ boucle SND et les \_ indicateurs Async SND pour le paramètre *fdwSound* de la fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) , le son continue de fonctionner comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="10e59-110">If you specify the SND\_LOOP and SND\_ASYNC flags for the *fdwSound* parameter of the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function, the sound will continue to play repeatedly as shown in the following example:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



<span data-ttu-id="10e59-111">Si vous souhaitez exécuter en boucle un son, vous devez le lire de façon asynchrone ; vous ne pouvez pas utiliser l' \_ indicateur de synchronisation SND avec l' \_ indicateur de boucle SND.</span><span class="sxs-lookup"><span data-stu-id="10e59-111">If you want to loop a sound, you must play it asynchronously; you cannot use the SND\_SYNC flag with the SND\_LOOP flag.</span></span> <span data-ttu-id="10e59-112">Un son en boucle continue de s’exécuter jusqu’à ce que vous appeliez **PlaySound** pour lire un autre son.</span><span class="sxs-lookup"><span data-stu-id="10e59-112">A looped sound will continue to play until you call **PlaySound** to play another sound.</span></span> <span data-ttu-id="10e59-113">Pour arrêter la lecture d’un son (en boucle ou asynchrone) sans lecture d’un autre son, utilisez l’instruction suivante :</span><span class="sxs-lookup"><span data-stu-id="10e59-113">To stop playing a sound (looped or asynchronous) without playing another sound, use the following statement:</span></span>


```C++
PlaySound(NULL, NULL, 0); 
```



 

 