---
description: Spécifie la poutre que le DSP de capture vocale utilise pour le traitement du tableau de microphone.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: MFPKEY_WMAAECMA_FEATR_MICARR_BEAM, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9165eec0dee87fa5d9f6a751f41e81d0de2d9958
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313766"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a>MFPKEY \_ WMAAECMA \_ Feature \_ MICARR \_ Beam, propriété

Spécifie la poutre que le DSP de capture vocale utilise pour le traitement du tableau de microphone.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Notes

Définissez cette propriété si la valeur de la propriété [MFPKEY \_ WMAAECMA \_ Feature \_ MICARR \_ mode](mfpkey-wmaaecma-featr-micarr-modeproperty.md) est MICARRAY \_ extern \_ Beam.

Si la valeur du [**\_ \_ \_ \_ mode de MICARR MFPKEY WMAAECMA**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) est MICARRAY \_ un seul \_ faisceau, vous pouvez lire cette propriété pour interroger le faisceau qui a été sélectionné par le DSP.

Cette propriété peut avoir les valeurs suivantes. Les valeurs sont en degrés horizontaux.



| Valeur | Description              |
|-------|--------------------------|
| 0     | -50 degrés.             |
| 1     | -40 degrés.             |
| 2     | -30 degrés.             |
| 3     | -20 degrés.             |
| 4     | -10 degrés.             |
| 5     | 0 degré (poutre centrale). |
| 6     | 10 degrés.              |
| 7     | 20 degrés.              |
| 8     | 30 degrés.              |
| 9     | 40 degrés.              |
| 10    | 50 degrés.              |



 

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

 

 
