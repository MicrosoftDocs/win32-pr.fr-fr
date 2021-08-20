---
description: Spécifie le rectangle source pour le mixage vidéo du convertisseur vidéo amélioré (EVR). Le rectangle source est la partie de la trame vidéo que le mixer BLITS à la surface de destination.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: Attribut VIDEO_ZOOM_RECT (EVR. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e6ce19c808545d400f53b9c0091cdbcc20c8efbc13372ae5386e419d244143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737144"
---
# <a name="video_zoom_rect-attribute"></a>IMAGE de l' \_ \_ attribut Rect de zoom

Spécifie le rectangle source pour le mixage vidéo du [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR). Le rectangle source est la partie de la trame vidéo que le mixer BLITS à la surface de destination.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Remarques

La valeur de cet attribut est une structure [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .

Le rectangle source est défini par rapport à un système de coordonnées normalisé, dans lequel la totalité de la trame vidéo occupe un rectangle avec des coordonnées {0, 0,1, 1}. Le rectangle source doit tenir dans le cadre de la vidéo. les coordonnées du rectangle source ont une plage de (0... 1).

Le présentateur EVR standard définit cet attribut sur le mélangeur. Pour définir l’attribut, procédez comme suit :

1.  Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le mixer pour récupérer le magasin d’attributs du mélangeur.
2.  Appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) pour définir l' **attribut \_ \_ Rect de zoom vidéo** sur le mélangeur. La valeur est une structure [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .

Dans un présentateur EVR personnalisé, vous pouvez utiliser cet attribut pour implémenter la méthode [**IMFVideoDisplayControl :: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) . Pour plus d’informations, consultez [rectangles source et destination](how-to-write-an-evr-presenter.md).

La constante GUID de cet attribut est exportée à partir de strmiids. lib.

## <a name="examples"></a>Exemples

L’exemple suivant définit le rectangle source sur le mélangeur.


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Evr. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de convertisseur vidéo améliorés](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Comment écrire un présentateur EVR](how-to-write-an-evr-presenter.md)
</dt> <dt>

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




