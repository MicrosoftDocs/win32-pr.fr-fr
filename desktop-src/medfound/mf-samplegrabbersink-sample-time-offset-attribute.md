---
description: Décalage entre l’horodatage de chaque échantillon reçu par l’accroche échantillon et l’heure à laquelle l’exemple d’accrochage présente l’exemple.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: Attribut MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99f65c5023bbe8705e21269dfb07d6f24db4190
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227664"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a>Attribut de décalage de l’heure d’exemple MF \_ SAMPLEGRABBERSINK \_ \_ \_

Décalage entre l’horodatage de chaque échantillon reçu par l’accroche échantillon et l’heure à laquelle l’exemple d’accrochage présente l’exemple.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Notes

Vous pouvez définir cet attribut sur l’objet [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) qui est retourné par la fonction [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) . Cet attribut permet à la fonction de rappel de l’exemple de la fonction de rappel de recevoir des exemples antérieurs à l’heure de la présentation.

Lorsque l’exemple d’accrochage reçoit un nouvel échantillon, il présente l’exemple à l’heure *t* − *offset*, où *t* est l’horodatage de l’échantillon et *offset* est la valeur de cet attribut. Si cet attribut n’est pas défini, la valeur par défaut est zéro.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFSampleGrabberSinkCallback**](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




