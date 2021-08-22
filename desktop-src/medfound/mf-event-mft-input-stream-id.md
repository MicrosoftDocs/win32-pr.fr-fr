---
description: Spécifie un flux d’entrée sur une transformation de Media Foundation (MFT).
ms.assetid: 2922af62-3fcc-4153-a26a-aba3c4121a0b
title: Attribut MF_EVENT_MFT_INPUT_STREAM_ID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d211eb30280e6b7390df8509795d49567c7f8a8c9016b2825786858fe888b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973808"
---
# <a name="mf_event_mft_input_stream_id-attribute"></a>\_ \_ \_ Attribut d’ID de \_ flux d’entrée MFT d’événement \_ MF

Spécifie un flux d’entrée sur une transformation de Media Foundation (MFT).

## <a name="data-type"></a>Type de données

**UINT32**

La valeur est un identificateur de flux d’entrée.

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>Remarques

Cet attribut est utilisé avec les événements suivants :

-   [METransformDrainComplete](metransformdraincomplete.md)
-   [METransformNeedInput](metransformneedinput.md)

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs asynchrone](asynchronous-mfts.md)
</dt> <dt>

[Attributs d'événement](event-attributes.md)
</dt> </dl>

 

 




