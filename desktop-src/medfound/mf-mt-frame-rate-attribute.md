---
description: Fréquence d’images d’un type de média vidéo, en images par seconde.
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: Attribut MF_MT_FRAME_RATE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb49da7667286c17bfa500a8a90a9f7083e786483120e40ba2d635710668a4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113809"
---
# <a name="mf_mt_frame_rate-attribute"></a>\_Attribut de \_ fréquence d’images MF MF \_

Fréquence d’images d’un type de média vidéo, en images par seconde.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Remarques

La fréquence d’images est exprimée sous la forme d’un rapport. Les 32 bits supérieurs de la valeur de l’attribut contiennent le numérateur et les 32 inférieurs contiennent le dénominateur. Par exemple, si la fréquence d’images est de 30 images par seconde (FPS), le ratio est de 30/1. Si la fréquence d’images est de 29,97 fps, le ratio est de 30000/1001.

Pour définir la valeur, utilisez la fonction [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) . Pour récupérer la valeur, utilisez la fonction [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="examples"></a>Exemples

L’exemple suivant définit la fréquence d’images sur un type de média vidéo.


```
// Helper function to set the frame rate on a video media type.
inline HRESULT SetFrameRate(
    IMFMediaType *pType, 
    UINT32 numerator, 
    UINT32 denominator
    )
{
    return MFSetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        numerator, 
        denominator
        );
}
```



L’exemple suivant obtient la fréquence d’images à partir d’un type de média vidéo.


```
// Helper function to get the frame rate from a video media type.
inline HRESULT GetFrameRate(
    IMFMediaType *pType, 
    UINT32 *pNumerator, 
    UINT32 *pDenominator
    )
{
    return MFGetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        pNumerator, 
        pDenominator
        );
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> <dt>

[**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 




