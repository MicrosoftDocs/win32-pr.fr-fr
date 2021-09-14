---
description: Permet à l’application de remplacer les paramètres par défaut sur les différentes propriétés du DSP de capture vocale.
ms.assetid: 1c11e817-36bd-4a5d-9c2b-6a91e86f623f
title: MFPKEY_WMAAECMA_FEATURE_MODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a47ef86a2acf83131800e9cb55b86de2cd3d98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295379"
---
# <a name="mfpkey_wmaaecma_feature_mode-property"></a>MFPKEY \_ \_ propriété mode de fonctionnalité WMAAECMA \_

Permet à l’application de remplacer les paramètres par défaut sur les différentes propriétés du DSP de capture vocale.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="default-value"></a>Valeur par défaut

VARIANTE \_ false

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Notes

Si cette propriété a la \_ valeur true, l’application peut définir les propriétés suivantes sur le DSP :

-   [MFPKEY \_ WMAAECMA \_ fonceur \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)
-   [MFPKEY \_ WMAAECMA \_ Fonct, \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)
-   [\_clip du \_ \_ Centre \_ d’MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-center-clipproperty.md)
-   [longueur de l' \_ \_ écho du Feature WMAAECMA MFPKEY \_ \_](mfpkey-wmaaecma-featr-echo-lengthproperty.md)
-   [\_taille du \_ \_ frame \_ de MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-frame-sizeproperty.md)
-   [\_ \_ \_ mode MICARR MFPKEY WMAAECMA \_](mfpkey-wmaaecma-featr-micarr-modeproperty.md)
-   [MFPKEY \_ WMAAECMA \_ Feature \_ MICARR \_ préproc](mfpkey-wmaaecma-featr-micarr-preprocproperty.md)
-   [\_remplissage du \_ \_ bruit \_ du MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-noise-fillproperty.md)
-   [MFPKEY \_ WMAAECMA \_ Feature \_](mfpkey-wmaaecma-featr-nsproperty.md)
-   [\_VAD MFPKEY WMAAECMA \_ Fonct \_](mfpkey-wmaaecma-featr-vadproperty.md)

Si cette propriété a \_ la valeur false, le DSP ignore ces propriétés et utilise ses paramètres par défaut. La valeur par défaut de cette propriété est \_ false false.

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

 

 
