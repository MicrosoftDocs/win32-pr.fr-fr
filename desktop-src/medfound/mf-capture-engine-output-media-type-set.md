---
description: 'Indique que le type de sortie a été défini sur le moteur de capture en réponse à IMFCaptureSink2 :: SetOutputType.'
ms.assetid: A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC
title: Attribut MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138a5893d4ccdd014354e00718a98eda9ba41616c1f1507c8749c9b36dcc0c29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013409"
---
# <a name="mf_capture_engine_output_media_type_set-attribute"></a>\_Attribut de \_ \_ définition de \_ type de média de sortie du \_ moteur de capture \_ MF

Indique que le type de sortie a été défini sur le moteur de capture en réponse à [**IMFCaptureSink2 :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Remarques

Vous pouvez appeler [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) pour déterminer si l’opération a réussi ou non.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Mfcaptureengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
</dt> </dl>

 

 




