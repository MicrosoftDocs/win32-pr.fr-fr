---
description: Spécifie les périphériques audio utilisés par le DSP de capture vocale pour la capture et le rendu audio.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: MFPKEY_WMAAECMA_DEVICE_INDEXES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863438"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a>Propriété d’index de l' \_ appareil MFPKEY WMAAECMA \_ \_

Spécifie les périphériques audio utilisés par le DSP de capture vocale pour la capture et le rendu audio.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

(-1,-1).

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Notes

Définissez cette propriété si vous utilisez le DSP en mode Source. Le DSP ignore cette propriété en mode filtre.

La valeur de la propriété est compressée par un **mot** de 2 16 bits dans une valeur **DWORD**. Les 16 bits supérieurs spécifient le périphérique de rendu audio (généralement un orateur) et les 16 bits inférieurs spécifient l’appareil de capture (généralement un microphone). Chaque appareil est spécifié en tant qu’index dans le regroupement de périphériques audio. Si l’index est-1, l’appareil par défaut est utilisé.

L’index de l’appareil correspond à l’index de collection utilisé dans l’interface [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) . L’application doit jouer la voix extrême sur le périphérique de rendu sélectionné. (La voix extrême est la voix de la personne à l’autre extrémité de la ligne téléphonique, qui est jouée par l’orateur sur l’ordinateur de l’utilisateur.) Si le périphérique de rendu sélectionné n’a pas de flux actif, le DSP ne peut pas traiter de sortie.

La valeur par défaut de cette propriété est (-1,-1).

L’exemple suivant montre comment initialiser le **PROPVARIANT** pour cette propriété.


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de capture vocale](voicecapturedmo.md)
</dt> </dl>

 

 
