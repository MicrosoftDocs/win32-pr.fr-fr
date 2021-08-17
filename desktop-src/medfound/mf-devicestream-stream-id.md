---
description: Spécifie l’identificateur de diffusion en continu de noyau (KS) pour un flux sur un appareil de capture vidéo.
ms.assetid: 03C48CBA-FAD0-4127-89E5-3F1874BF32DB
title: Attribut MF_DEVICESTREAM_STREAM_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb5b4004ae2e280806411e51f7adfe83f9a4f28d71103a3d3c6e9a247f2011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973848"
---
# <a name="mf_devicestream_stream_id-attribute"></a>\_Attribut d' \_ ID de flux DEVICESTREAM MF \_

Spécifie l’identificateur de diffusion en continu de noyau (KS) pour un flux sur un appareil de capture vidéo.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Pour accéder à cet attribut, procédez comme suit :

1.  Interrogez la source du média pour l’interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Appelez [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) pour obtenir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pour le flux.
3.  Appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) pour accéder à l’attribut.

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

 

 




