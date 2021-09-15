---
description: Spécifie si un flux d’images ASF est un type JPEG dégradable.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: Attribut MF_MT_IMAGE_LOSS_TOLERANT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412974"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a>Attribut de tolérance de perte de l' \_ image MT MF \_ \_ \_

Spécifie si un flux d’images ASF est un type JPEG dégradable.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Notes

Cet attribut s’applique au type de média pour les flux d’images en ASF. Si la valeur est **true**, le flux est un type d’image JPEG dégradable. Dans le cas contraire, le flux est un type d’image JFIF. Pour plus d’informations sur ces types de flux, consultez la spécification ASF.

En plus de l’attribut de tolérance de perte d’image MF MF \_ \_ \_ \_ , le type de média pour un flux d’images ASF contient les attributs suivants :



| Attribut                                                 | Description                                |
|-----------------------------------------------------------|--------------------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md) | Contient la valeur de l' **\_ image MFMediaType**. |
| [**\_taille de \_ trame MF MF \_**](mf-mt-frame-size-attribute.md) | Donne la taille de l’image en pixels.            |



 

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




