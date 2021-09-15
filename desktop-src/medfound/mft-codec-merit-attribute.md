---
description: Contient la valeur mérite d’un codec matériel.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: Attribut MFT_CODEC_MERIT_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412890"
---
# <a name="mft_codec_merit_attribute-attribute"></a>\_Attribut de \_ mérite du codec MFT \_

Contient la valeur mérite d’un codec matériel.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Cet attribut est défini sur l’objet d’activation d’une Media Foundation transformation (MFT) qui représente un codec matériel. La valeur de l’attribut est la valeur mérite du codec.

Cet attribut contrôle l’ordre dans lequel la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) énumère les codecs, si l’indicateur d' **\_ énumération MFT \_ \_ SORTANDFILTER** est défini. MFTs avec une valeur mérite apparaît plus haut dans la liste que les autres MFTs.

Cet attribut ne contient pas de valeur approuvée. Pour vérifier la valeur réelle de mérite du codec, appelez la fonction [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .

Si la valeur de l' \_ attribut d' \_ attribut mérite du codec MFT \_ ne correspond pas à la valeur mérite récupérée par [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), la méthode [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) échoue et retourne **MF \_ E \_ non valide \_ codec \_ mérite**.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




