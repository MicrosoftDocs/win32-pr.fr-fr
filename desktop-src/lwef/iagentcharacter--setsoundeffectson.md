---
title: IAgentCharacter SetSoundEffectsOn
description: IAgentCharacter SetSoundEffectsOn
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71abb6adebf09182d4329202e77355e7dc365899291995e97eca66305a00ab94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725019"
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


 

 




