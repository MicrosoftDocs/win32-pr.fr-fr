---
description: Spécifie si un flux sur une source de capture vidéo est un flux d’image continue.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: Attribut MF_DEVICESTREAM_IMAGE_STREAM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382ce587574d6ec46509a460dfb964e23dd416d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752445"
---
# <a name="mf_devicestream_image_stream-attribute"></a>\_Attribut de \_ flux d’image MF DEVICESTREAM \_

Spécifie si un flux sur une source de capture vidéo est un flux d’image continue.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Certaines caméras vidéo exposent un flux d’image continue qui produit des images haute résolution. Le flux d’image peut produire des images non compressées ou des images JPEG. Si la caméra a un flux d’image, la source du média pour l’appareil de capture affecte la **valeur true** à cet attribut sur le flux de l’image.

Pour accéder à cet attribut, procédez comme suit :

1.  Interrogez la source du média pour l’interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Appelez [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) pour obtenir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pour le flux.
3.  Appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) pour accéder à l’attribut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




