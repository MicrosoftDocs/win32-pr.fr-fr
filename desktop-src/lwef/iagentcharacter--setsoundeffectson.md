---
title: IAgentCharacter SetSoundEffectsOn
description: IAgentCharacter SetSoundEffectsOn
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a454a6ebeecc763cb7e5a964bb1f2897df6c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513685"
---
# <a name="iagentcharactersetsoundeffectson"></a><span data-ttu-id="0fa9a-103">IAgentCharacter::SetSoundEffectsOn</span><span class="sxs-lookup"><span data-stu-id="0fa9a-103">IAgentCharacter::SetSoundEffectsOn</span></span>

<span data-ttu-id="0fa9a-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0fa9a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

<span data-ttu-id="0fa9a-105">Détermine si les effets sonores du caractère sont joués.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-105">Determines whether the character's sound effects are played.</span></span>

-   <span data-ttu-id="0fa9a-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0fa9a-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Ble*</span><span class="sxs-lookup"><span data-stu-id="0fa9a-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="0fa9a-108">Réglage des effets sonores.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-108">Sound effects setting.</span></span> <span data-ttu-id="0fa9a-109">Si ce paramètre a la **valeur true**, les effets sonores pour les animations sont joués lorsque l’animation est lue. Si la **valeur est false**, les effets sonores ne sont pas joués.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-109">If this parameter is **True**, the sound effects for animations are played when the animation plays; if **False**, sound effects are not played.</span></span>

</dd> </dl>

<span data-ttu-id="0fa9a-110">Ce paramètre détermine si les effets sonores compilés dans le cadre du caractère sont joués lorsque vous jouez à une animation associée.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-110">This setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="0fa9a-111">Le paramètre de cette propriété s’applique à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="0fa9a-112">Le paramètre est également soumis au paramètre des effets sonores globaux de l’utilisateur dans [**IAgentAudioOutputProperties :: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span><span class="sxs-lookup"><span data-stu-id="0fa9a-112">The setting is also subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0fa9a-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fa9a-113">See Also</span></span>

<span data-ttu-id="0fa9a-114">[**IAgentCharacter :: GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [ **IAgentAudioOutputProperties :: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="0fa9a-114">[**IAgentCharacter::GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




