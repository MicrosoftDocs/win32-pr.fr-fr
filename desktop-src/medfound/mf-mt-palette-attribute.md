---
description: Contient les entrées de palette pour un type de média vidéo. Utilisez cet attribut pour les formats vidéo en palette, tels que RVB 8.
ms.assetid: 3efc124b-073e-4c48-9550-c100e29f2d6f
title: Attribut MF_MT_PALETTE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dcfc596ae463cf642cc462da1c73dc641356d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313957"
---
# <a name="mf_mt_palette-attribute"></a>\_Attribut de \_ palette MF MT

Contient les entrées de palette pour un type de média vidéo. Utilisez cet attribut pour les formats vidéo en palette, tels que RVB 8.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Notes

Les données d’attribut sont un tableau d’unions [**MFPaletteEntry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

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

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




