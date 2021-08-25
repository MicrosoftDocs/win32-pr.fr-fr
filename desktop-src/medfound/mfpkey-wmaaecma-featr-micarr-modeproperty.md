---
description: Spécifie comment le DSP de capture vocale effectue le traitement du tableau de microphone.
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: MFPKEY_WMAAECMA_FEATR_MICARR_MODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb948ff15655ccbdc0bf647194b2f6d3d7d1a40c36da32f6d65479152c76c3e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953519"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a>\_Propriété du \_ \_ mode MICARR MFPKEY WMAAECMA Feature \_

Spécifie comment le DSP de capture vocale effectue le traitement du tableau de microphone.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

MICARRAY \_ un seul \_ faisceau

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Remarques

La valeur de cette propriété est un membre de l’énumération du [ \_ \_ mode de tableau MIC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) . La valeur par défaut est MICARRAY \_ simple \_ Beam. Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.

Le DSP utilise cette propriété uniquement lorsque le traitement du tableau du microphone est activé.

## <a name="requirements"></a>Configuration requise



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

 

 
