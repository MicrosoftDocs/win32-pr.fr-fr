---
title: IAgentCharacter GetTTSSpeed
description: IAgentCharacter GetTTSSpeed
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e7fbe4cbba7eaed22f49865e1a0f0994c512867fb6f233ef2bbfa01dcaafcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609869"
---
# <a name="iagentcharactergetttsspeed"></a>IAgentCharacter::GetTTSSpeed

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

Récupère le paramètre de vitesse de sortie TTS du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*
</dt> <dd>

Adresse d’une variable qui reçoit la vitesse de sortie du caractère en mots par minute.

</dd> </dl>

Bien que votre application ne puisse pas écrire cette valeur, vous pouvez inclure des balises de vitesse dans votre texte de sortie qui accélèrent temporairement la sortie d’une énoncé particulière.

Cette propriété retourne le paramètre de vitesse de sortie en cours pour le caractère. Pour les caractères utilisant la sortie TTS, la propriété retourne la sortie TTS réelle pour le caractère. Si TTS n’est pas activé ou que le caractère ne prend pas en charge la sortie TTS, le paramètre reflète le paramètre utilisateur pour la vitesse de sortie.

 

 




