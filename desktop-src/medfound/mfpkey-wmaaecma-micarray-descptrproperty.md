---
description: Spécifie la géométrie du tableau du microphone pour le DSP de capture vocale.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: MFPKEY_WMAAECMA_MICARRAY_DESCPTR, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231731"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a>MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR, propriété

Spécifie la géométrie du tableau du microphone pour le DSP de capture vocale.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

\_objet BLOB VT

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Notes

La valeur de cette propriété est une [**structure \_ \_ \_ Geometry de tableau KSAUDIO MIC**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) . Cette structure est définie dans le fichier d’en-tête KsMedia. h. Pour obtenir la géométrie du tableau du microphone, interrogez le périphérique audio pour la \_ \_ \_ propriété Geometry du tableau MIC audio KSPROPERTY \_ en appelant la méthode **IKsControl :: KSPROPERTY** sur l’appareil. pour plus d’informations sur les tableaux de microphones, téléchargez le livre blanc [comment créer et utiliser des tableaux de microphone pour Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

Définissez cette propriété si vous utilisez le DSP en mode filtre et si le traitement du tableau du microphone est activé. Si vous utilisez le DSP en mode Source, le DSP interroge automatiquement l’appareil pour obtenir les informations géométriques.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de capture vocale](voicecapturedmo.md)
</dt> </dl>

 

 
