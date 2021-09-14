---
description: Spécifie un nombre compris entre 0 et 100 qui indique le compromis entre la qualité d’encodage et la vitesse d’encodage.
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: Attribut MF_TRANSCODE_QUALITYVSSPEED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4d95fab92276e926189c885dad2ecb8f164a97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313866"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a>\_Attribut QUALITYVSSPEED de transcodage MF \_

Spécifie un nombre compris entre 0 et 100 qui indique le compromis entre la qualité d’encodage et la vitesse d’encodage.

## <a name="data-type"></a>Type de données

**UINT32**

La valeur de cette propriété est comprise dans la plage suivante.



| Valeur                                                                          | Signification                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>0</dt> </dl>   | Une qualité inférieure, un encodage plus rapide.<br/>  |
| <dl> <dt>100</dt> </dl> | Qualité supérieure, encodage plus lent.<br/> |



 

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Cet attribut a la même valeur GUID que la propriété [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) définie pour [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)et a la même interprétation.

l’application peut définir cet attribut sur le profil de transcodage avant de générer la topologie de transcodage pour Windows codecs multimédias. La valeur doit être comprise entre 0 et 100. Pour le flux vidéo, le générateur de topologie de transcodage mappe une valeur à la valeur spécifiée par l’application et fournit la valeur mappée à la propriété **MFPKEY \_ COMPLEXITYEX** de l’encodeur. Des valeurs inférieures permettent à l’encodeur d’utiliser des algorithmes d’encodage moins compliqués. L’utilisation d’algorithmes plus simples produit une sortie de qualité inférieure, mais le processus d’encodage est plus rapide et nécessite moins de puissance de traitement.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API de transcodage](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
