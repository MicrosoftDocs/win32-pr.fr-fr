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
ms.openlocfilehash: cf97321a72ab566bf622e725700dbf336ddba6d92b9b8e6df9150357492656f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136117"
---
# <a name="using-playsound-to-loop-sounds"></a>Utilisation de PlaySound pour boucler des sons

Si vous spécifiez la \_ boucle SND et les \_ indicateurs Async SND pour le paramètre *fdwSound* de la fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) , le son continue de fonctionner comme indiqué dans l’exemple suivant :


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



Si vous souhaitez exécuter en boucle un son, vous devez le lire de façon asynchrone ; vous ne pouvez pas utiliser l' \_ indicateur de synchronisation SND avec l' \_ indicateur de boucle SND. Un son en boucle continue de s’exécuter jusqu’à ce que vous appeliez **PlaySound** pour lire un autre son. Pour arrêter la lecture d’un son (en boucle ou asynchrone) sans lecture d’un autre son, utilisez l’instruction suivante :


```C++
PlaySound(NULL, NULL, 0); 
```



 

 