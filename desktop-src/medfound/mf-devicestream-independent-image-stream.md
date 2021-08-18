---
description: Spécifie si le flux d’image sur une source de capture vidéo est indépendant du flux vidéo.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: Attribut MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f52392839c5f196159692bc9c4624cbda67b869471d6737c4cff60c847f890e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956679"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a>\_Attribut de \_ \_ flux d’image indépendant DEVICESTREAM MF \_

Spécifie si le flux d’image sur une source de capture vidéo est indépendant du flux vidéo.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Remarques

Certaines caméras vidéo USB exposent un flux qui produit des images fixes. Dans certains appareils photo, le flux d’image retourne simplement le frame suivant à partir du flux vidéo. Dans d’autres caméras, le flux d’image fonctionne indépendamment du flux vidéo. Si l’appareil photo possède un flux d’image indépendant, la source du média pour l’appareil de capture affecte la **valeur true** à cet attribut sur le flux de l’image.

Pour accéder à cet attribut, procédez comme suit :

1.  Interrogez la source du média pour l’interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Appelez [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) pour obtenir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pour le flux.
3.  Appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) pour accéder à l’attribut.

Cet attribut s’applique uniquement lorsque l’attribut de [ \_ \_ \_ flux d’image DEVICESTREAM MF](mf-devicestream-image-stream.md) a la **valeur true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




