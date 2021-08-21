---
description: Spécifie la taille de trame audio utilisée par le DSP de capture vocal.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: MFPKEY_WMAAECMA_FEATR_FRAME_SIZE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812a9c7b85a36b730caffe7679cc742a3bc029546a12839afd95a8c8ab58bfeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973288"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a>\_Propriété de \_ taille de \_ trame MFPKEY WMAAECMA \_

Spécifie la taille de trame audio utilisée par le DSP de capture vocal.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Remarques

L’algorithme d’annulation de l’écho acoustique traite les échantillons audio PCM un frame à la fois. La valeur de cette propriété est la taille du cadre audio, en échantillons. Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.

Le DSP de capture vocale prend en charge les tailles d’image suivantes :

-   80
-   128
-   160
-   240
-   256
-   320

Si la valeur de cette propriété est égale à zéro, le DSP sélectionne la taille de trame en fonction du mode système et du format de sortie.

Toutefois, pour des performances optimales, il est recommandé que les applications utilisent la valeur par défaut. Si le mode de traitement est un tableau de microphones uniquement, la valeur par défaut est 320 exemples. Pour tous les autres modes de traitement, la valeur par défaut est 160 exemples. Pour plus d’informations sur les modes de traitement du DSP de capture vocale, consultez [ \_ \_ \_ mode système MFPKEY WMAAECMA](mfpkey-wmaaecma-system-modeproperty.md).

Après le premier appel à [**IMediaObject :: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) ou [**IMediaObject ::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), vous pouvez lire cette propriété pour obtenir la taille de frame réelle en cours d’utilisation, même si le [**\_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA**](mfpkey-wmaaecma-feature-modeproperty.md) est false.

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

 

 
