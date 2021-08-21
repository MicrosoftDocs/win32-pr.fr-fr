---
description: Permet au moteur de capture d’utiliser un décodeur qui a des restrictions de champ d’utilisation.
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: Attribut MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690f586325f883595e1336ed946611850b3c51d5443dbd9f6e68830502284a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061067"
---
# <a name="mf_capture_engine_decoder_mft_fieldofuse_unlock_attribute-attribute"></a>\_Attribut d' \_ \_ \_ \_ \_ attribut de DÉverrouillage FIELDOFUSE MFT du décodeur du moteur de capture \_ MF

Permet au moteur de capture d’utiliser un décodeur qui a des restrictions de champ d’utilisation.

## <a name="data-type"></a>Type de données

**IUnknown\***

## <a name="remarks"></a>Remarques

La valeur de cet attribut est un pointeur vers l’interface [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , implémentée par l’appelant. L’implémentation de cette interface par l’appelant est supposée effectuer une négociation avec le décodeur, comme décrit dans [champ de restrictions d’utilisation](field-of-use-restrictions.md). Microsoft Media Foundation ne définit pas le protocole de transfert, en général, il implique un certain type d’échange de chiffrement.

En interne, le moteur de capture définit le pointeur [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) sur le décodeur en définissant l’attribut d' [ \_ \_ \_ attribut de déverrouillage MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) du décodeur.

## <a name="requirements"></a>Conditions requises



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

 

 




