---
description: Contient des données de format supplémentaires pour un type de média.
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: Attribut MF_MT_USER_DATA (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0196e8fea06bb84fe5a78a8b486f95864e0c6d889692dfa6f3ee9b1103da518a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012780"
---
# <a name="mf_mt_user_data-attribute"></a>\_Attribut de \_ données utilisateur MF MT \_

Contient des données de format supplémentaires pour un type de média.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Remarques

La signification des données dans cet attribut dépend du format décrit par le type de média.



| Type de format                                                                                                           | Données de format supplémentaires                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Codec de média.                                                                                                  | Données privées du codec.                                                                                                                       |
| La structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) a été convertie.   | Données supplémentaires qui apparaissent après la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , à l’exclusion de la table de couleurs ou des masques de couleur. |
| La structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ou [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) a été convertie. | Données supplémentaires qui apparaissent après la structure du format audio.                                                                                 |



 

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

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

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 
