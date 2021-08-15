---
description: Identifie le composant qui a généré un événement de capture.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: Attribut MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88efff7cea540c1fae2c14d44dd7676c4f523b562a66a4c4f4bc4dffea59d5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474467"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a>\_ \_ \_ \_ Attribut Guid du générateur d’événements du moteur de capture MF \_

Identifie le composant qui a généré un événement de capture.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Remarques

Cet attribut apparaît sur certains événements du moteur de capture. Pour récupérer cet attribut, appelez [**IMFAttributes :: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) sur l’objet d’événement. L’objet d’événement est passé à l’application par le biais de la méthode [**IMFCaptureEngineOnEventCallback :: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .

La valeur est un identificateur d’interface pour le composant qui a généré l’événement. Par exemple, la valeur **IID \_ IMFCapturePreviewSink** indique le récepteur d’aperçu ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)). Tous les événements de capture ne contiennent pas cet attribut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du moteur de capture](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine :: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




