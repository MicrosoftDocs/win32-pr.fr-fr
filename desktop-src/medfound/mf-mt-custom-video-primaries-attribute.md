---
description: Spécifie des couleurs primaires personnalisées pour un type de média vidéo.
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: Attribut MF_MT_CUSTOM_VIDEO_PRIMARIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a0e43e4ac42327ad6876797b9a82e58a8582ebcb254ddecb443cfda0d4011f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104545"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a>\_Attribut de \_ prédictionnaires vidéo personnalisé MF MT \_ \_

Spécifie des couleurs primaires personnalisées pour un type de média vidéo.

## <a name="data-type"></a>Type de données

**UINT32**

Tableau d’octets

## <a name="remarks"></a>Remarques

Les données d’attribut sont une structure de préversion [**\_ \_ vidéo \_ personnalisée MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) .

Cet attribut spécifie le volume de couleurs réel du contenu ou un affichage. Les informations de mastérisation du volume de couleurs CEA-861,3/SMPTE ST. 2086 sont stockées dans cet attribut par décodeurs. Notez que cet attribut ne remplace pas l’attribut de préversions [**\_ \_ vidéo \_ de MF MT**](mf-mt-video-primaries-attribute.md). Cet attribut décrit une indication sur le volume de couleurs du contenu, tandis que les **\_ vidéos MF MT \_ vidéo \_ primaires** décrivent les couleurs primaires dans lesquelles le contenu est effectivement codé (par exemple, la signification de 1,0 dans les canaux R/g/B d’une représentation à virgule flottante).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




