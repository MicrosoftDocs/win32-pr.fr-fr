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
# <a name="iagentcharactersetsoundeffectson"></a>IAgentCharacter::SetSoundEffectsOn

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

Détermine si les effets sonores du caractère sont joués.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Ble*
</dt> <dd>

Réglage des effets sonores. Si ce paramètre a la **valeur true**, les effets sonores pour les animations sont joués lorsque l’animation est lue. Si la **valeur est false**, les effets sonores ne sont pas joués.

</dd> </dl>

Ce paramètre détermine si les effets sonores compilés dans le cadre du caractère sont joués lorsque vous jouez à une animation associée. Le paramètre de cette propriété s’applique à tous les clients du caractère. Le paramètre est également soumis au paramètre des effets sonores globaux de l’utilisateur dans [**IAgentAudioOutputProperties :: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [ **IAgentAudioOutputProperties :: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




