---
title: IAgentCharacter GetSoundEffectsOn
description: IAgentCharacter GetSoundEffectsOn
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a40f18a4fb8e7778c116c54391a7dc50e5267af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509821"
---
# <a name="iagentcharactergetsoundeffectson"></a><span data-ttu-id="51475-103">IAgentCharacter::GetSoundEffectsOn</span><span class="sxs-lookup"><span data-stu-id="51475-103">IAgentCharacter::GetSoundEffectsOn</span></span>

<span data-ttu-id="51475-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51475-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

<span data-ttu-id="51475-105">Récupère si le paramètre effets sonores du caractère est activé.</span><span class="sxs-lookup"><span data-stu-id="51475-105">Retrieves whether the character's sound effects setting is enabled.</span></span>

-   <span data-ttu-id="51475-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="51475-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="51475-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span><span class="sxs-lookup"><span data-stu-id="51475-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="51475-108">Adresse d’une variable qui reçoit la **valeur true** si le paramètre effets sonores du caractère est activé, **false** s’il est désactivé.</span><span class="sxs-lookup"><span data-stu-id="51475-108">Address of a variable that receives **True** if the character's sound effects setting is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="51475-109">Le paramètre effets sonores du caractère détermine si les effets sonores compilés en tant que partie du caractère sont joués lorsque vous jouez à une animation associée.</span><span class="sxs-lookup"><span data-stu-id="51475-109">The character's sound effects setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="51475-110">Le paramètre est soumis au paramètre des effets sonores globaux de l’utilisateur dans [**IAgentAudioOutputProperties :: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span><span class="sxs-lookup"><span data-stu-id="51475-110">The setting is subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="51475-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51475-111">See Also</span></span>

<span data-ttu-id="51475-112">[**IAgentCharacter :: SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [ **IAgentAudioOutputProperties :: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="51475-112">[**IAgentCharacter::SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




