---
description: 'Contient un pointeur vers le jeton qui a été fourni à la méthode IMFMediaStream :: RequestSample.'
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: Attribut MFSampleExtension_Token (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17331ad098f80c2676e9d057e1688a776cee305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106532097"
---
# <a name="mfsampleextension_token-attribute"></a>\_Attribut de jeton MFSampleExtension

Contient un pointeur vers le jeton qui a été fourni à la méthode [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .

## <a name="data-type"></a>Type de données

**IUnknown \** _

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>S’applique à

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Notes

Cet attribut s’applique aux exemples de supports. La valeur de l’attribut est le pointeur **IUnknown** qui est passé au paramètre *pToken* de la méthode [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) . L’appelant utilise cet attribut pour suivre l’état de la demande.

Si vous écrivez une source de média personnalisée, définissez cet attribut sur l’exemple lorsque le flux de média fournit un exemple en réponse à la méthode [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) , sauf si la valeur de *pToken* est **null**.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Exemples d’attributs](sample-attributes.md)
</dt> <dt>

[Exemples de supports](media-samples.md)
</dt> </dl>

 

 




