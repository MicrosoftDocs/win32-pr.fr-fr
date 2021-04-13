---
title: IAgentCharacter GetTTSSpeed
description: IAgentCharacter GetTTSSpeed
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551074e1647cffc88e0b5f9f530cea931cd21ff9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380443"
---
# <a name="iagentcharactergetttsspeed"></a><span data-ttu-id="30f87-103">IAgentCharacter::GetTTSSpeed</span><span class="sxs-lookup"><span data-stu-id="30f87-103">IAgentCharacter::GetTTSSpeed</span></span>

<span data-ttu-id="30f87-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="30f87-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

<span data-ttu-id="30f87-105">Récupère le paramètre de vitesse de sortie TTS du caractère.</span><span class="sxs-lookup"><span data-stu-id="30f87-105">Retrieves the character's TTS output speed setting.</span></span>

-   <span data-ttu-id="30f87-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="30f87-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="30f87-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*</span><span class="sxs-lookup"><span data-stu-id="30f87-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="30f87-108">Adresse d’une variable qui reçoit la vitesse de sortie du caractère en mots par minute.</span><span class="sxs-lookup"><span data-stu-id="30f87-108">Address of a variable that receives the output speed of the character in words per minute.</span></span>

</dd> </dl>

<span data-ttu-id="30f87-109">Bien que votre application ne puisse pas écrire cette valeur, vous pouvez inclure des balises de vitesse dans votre texte de sortie qui accélèrent temporairement la sortie d’une énoncé particulière.</span><span class="sxs-lookup"><span data-stu-id="30f87-109">Although your application cannot write this value, you can include speed tags in your output text that will temporarily speed up the output for a particular utterance.</span></span>

<span data-ttu-id="30f87-110">Cette propriété retourne le paramètre de vitesse de sortie en cours pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="30f87-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="30f87-111">Pour les caractères utilisant la sortie TTS, la propriété retourne la sortie TTS réelle pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="30f87-111">For characters using TTS output, the property returns the actual TTS output for the character.</span></span> <span data-ttu-id="30f87-112">Si TTS n’est pas activé ou que le caractère ne prend pas en charge la sortie TTS, le paramètre reflète le paramètre utilisateur pour la vitesse de sortie.</span><span class="sxs-lookup"><span data-stu-id="30f87-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

 

 




