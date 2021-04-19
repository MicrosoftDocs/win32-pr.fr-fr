---
description: Contient des données de format supplémentaires pour un type de média.
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: Attribut MF_MT_USER_DATA (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6042ded0e2d441b0f86c5e1f97557959ce08cd1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543525"
---
# <a name="mf_mt_user_data-attribute"></a>\_Attribut de \_ données utilisateur MF MT \_

Contient des données de format supplémentaires pour un type de média.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Notes

La signification des données dans cet attribut dépend du format décrit par le type de média.



| Type de format                                                                                                           | Données de format supplémentaires                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Codec Windows Media.                                                                                                  | Données privées du codec.                                                                                                                       |
| La structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) a été convertie.   | Données supplémentaires qui apparaissent après la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , à l’exclusion de la table de couleurs ou des masques de couleur. |
| La structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ou [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) a été convertie. | Données supplémentaires qui apparaissent après la structure du format audio.                                                                                 |



 

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

 

 
