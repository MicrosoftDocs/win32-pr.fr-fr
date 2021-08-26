---
description: Permet au moteur de capture d’utiliser un encodeur qui a des restrictions de champ d’utilisation.
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: Attribut MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32f2fb9d85c68adbc726fa4b36f2ea960a33e68c4dff836fac0370c8e9e4e3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060819"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a>\_Attribut d' \_ \_ attribut de \_ \_ \_ déverrouillage FIELDOFUSE de l’encodeur du moteur de capture \_ MF

Permet au moteur de capture d’utiliser un encodeur qui a des restrictions de champ d’utilisation.

## <a name="data-type"></a>Type de données

**IUnknown\***

## <a name="remarks"></a>Remarques

La valeur de cet attribut est un pointeur vers l’interface [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , implémentée par l’appelant. L’implémentation de cette interface par l’appelant est supposée effectuer une négociation avec l’encodeur, comme décrit dans [champ de restrictions d’utilisation](field-of-use-restrictions.md). Microsoft Media Foundation ne définit pas le protocole de transfert, en général, il implique un certain type d’échange de chiffrement.

En interne, le moteur de capture définit le pointeur [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) sur l’encodeur en définissant l’attribut d' [ \_ \_ \_ attribut de déverrouillage MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) de l’encodeur.

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

 

 




