---
description: Contient une valeur définie par l’appelant pour un événement METransformMarker.
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: Attribut MF_EVENT_MFT_CONTEXT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61e8920c119da151df1215e8de8ce0d526220e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127314054"
---
# <a name="mf_event_mft_context-attribute"></a>\_Attribut de \_ \_ contexte MFT de l’événement MF

Contient une valeur définie par l’appelant pour un événement [METransformMarker](metransformmarker.md) .

## <a name="data-type"></a>Type de données

**ULong \_ PTR** stocké comme **UINT64**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>S’applique à

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>Notes

Cet attribut est utilisé avec l’événement [METransformMarker](metransformmarker.md) . La valeur de l’attribut est extraite du paramètre *ulParam* de la méthode [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) .

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

[MFTs asynchrone](asynchronous-mfts.md)
</dt> <dt>

[Attributs d'événement](event-attributes.md)
</dt> </dl>

 

 




