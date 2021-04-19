---
description: Spécifie comment un décodeur audio doit transformer l’audio multicanal en sortie stéréo. Ce processus est également appelé « repliable ».
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: Attribut MF_MT_AUDIO_FOLDDOWN_MATRIX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bb8aa00835ab31f6c05eaa9a1d0e5d9d126b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524550"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a>\_Attribut de \_ \_ matrice FOLDDOWN audio MF MT \_

Spécifie comment un décodeur audio doit transformer l’audio multicanal en sortie stéréo. Ce processus est également appelé « *repliable »*.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Notes

Cet attribut s’applique aux types de média audio.

La valeur de cet attribut est une structure de [**\_ matrice MFFOLDDOWN**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                        |
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

 

 




