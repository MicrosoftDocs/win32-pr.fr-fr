---
description: Largeur et hauteur d’une image vidéo, en pixels.
ms.assetid: 9f10a972-406f-47ef-b71c-86ed771c9a9a
title: Attribut MF_MT_FRAME_SIZE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3d6278cdbd4c279c498839cb183b3331fe1efc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313981"
---
# <a name="mf_mt_frame_size-attribute"></a>\_Attribut de \_ taille de trame MT MF \_

Largeur et hauteur d’une image vidéo, en pixels.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Notes

Les 32 bits de poids fort contiennent la largeur et les 32 inférieurs contiennent la hauteur.

Pour définir cet attribut, utilisez la fonction [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) . Pour récupérer cet attribut, utilisez la fonction [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="examples"></a>Exemples


```
// Helper function to set the frame size on a video media type.
inline HRESULT SetFrameSize(IMFMediaType *pType, UINT32 width, UINT32 height)
{
    return MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
}

// Helper function to get the frame size from a video media type.
inline HRESULT GetFrameSize(IMFMediaType *pType, UINT32 *pWidth, UINT32 *pHeight)
{
    return MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, pWidth, pHeight);
}
```



## <a name="requirements"></a>Spécifications



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
</dt> </dl>

 

 




