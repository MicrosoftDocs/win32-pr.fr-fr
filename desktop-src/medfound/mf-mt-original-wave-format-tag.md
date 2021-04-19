---
description: Contient la balise WAVE format d’origine pour un flux audio.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: Attribut MF_MT_ORIGINAL_WAVE_FORMAT_TAG (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba89171f9ae2bf3ab99df05bd3ae64b7d52be6d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535625"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a>\_Attribut de \_ \_ \_ balise de format Wave d’origine MF MT \_

Contient la balise WAVE format d’origine pour un flux audio.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Notes

En fonction du fichier source, la source du média AVI peut définir cet attribut sur les types de médias qu’elle propose.

Un fichier AVI contient un en-tête de flux pour chaque flux du fichier. La source de média AVI traduit l’en-tête de flux en un type de média. Pour les flux audio, l’en-tête de flux contient une balise de format qui identifie le format audio. (La balise format est contenue dans le membre **wFormatTag** de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .) Dans la plupart des cas, la source de média AVI convertit directement la balise de format en un GUID de sous-type, comme décrit dans la rubrique GUID de sous- [**type audio**](audio-subtype-guids.md). Toutefois, dans certains cas, il mappe la balise de format d’origine à une autre balise de format équivalente. Si c’est le cas, la source du média stocke la balise de format d’origine dans le type de média, à l’aide de l' \_ \_ attribut de \_ \_ balise de format Wave MF d’origine \_ .

Les mappages de format sont stockés dans le Registre sous la clé suivante :

**HKEY \_ CLASSES \_ racine** \\ **MediaFoundation** \\ **MapAudioFormatTag**

Chaque entrée est une valeur **DWORD** . Le nom de l’entrée est la représentation décimale de la balise de format. La valeur de l’entrée correspond à la balise de format équivalente.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 
