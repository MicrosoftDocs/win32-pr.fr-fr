---
description: Indique le nombre de mémoires tampons non compressées que le récepteur multimédia EVR (Enhanced Video Renderer) requiert pour l’entrelacement.
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: Attribut MF_SA_REQUIRED_SAMPLE_COUNT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2db64ae093228cc50695fed3ac5e39a8c44987b54d72d6e1295ccae2b6a95f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059410"
---
# <a name="mf_sa_required_sample_count-attribute"></a>\_Attribut de \_ \_ nombre d’exemples requis MF sa \_

Indique le nombre de mémoires tampons non compressées que le récepteur multimédia EVR (Enhanced Video Renderer) requiert pour l’entrelacement.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Il s’agit d’un attribut de niveau flux. Pour récupérer l’attribut à partir du EVR, procédez comme suit :

1.  Appelez [**IMFMediaSink :: GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) pour accéder au récepteur de flux.
2.  Interrogez le récepteur de flux pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
3.  Appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

En interne, le mélangeur fournit cet attribut au EVR. Pour récupérer l’attribut à partir du mélangeur, appelez [**IMFTransform :: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




