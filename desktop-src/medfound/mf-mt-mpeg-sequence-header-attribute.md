---
description: Contient l’en-tête de séquence MPEG-1 ou MPEG-2 pour un type de média vidéo.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: Attribut MF_MT_MPEG_SEQUENCE_HEADER (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4003137ec4d2942bc95f56b2ce54644eb7b678d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227718"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a>\_Attribut d' \_ \_ \_ en-tête de séquence MPEG MF MT

Contient l’en-tête de séquence MPEG-1 ou MPEG-2 pour un type de média vidéo.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Notes

Cet attribut correspond au membre **dwSequenceHeader** de la structure [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) ou au membre **bSequenceHeader** de la structure [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .

Pour la vidéo H264 – et H265, l’objet BLOB contient des [unités nal](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) concaténées au format annexe B, ainsi que leurs codes de début. Plus précisément, pour la vidéo H264 –, il s’agit de SPS & unités PPS NAL. Pour H265, il s’agit de VPS, SPS & PPS.

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

 

 
