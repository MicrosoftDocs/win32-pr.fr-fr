---
description: 'Déclenché par une autorité de confiance de sortie (OTA) lorsque la méthode IMFOutputTrustAuthority :: SetPolicy se termine de façon asynchrone.'
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: Événement MEPolicySet (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238af6cbd740e62825ae0b661769c1cf1bf880ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531821"
---
# <a name="mepolicyset-event"></a>Événement MEPolicySet

Déclenché par une autorité de confiance de sortie (OTA) lorsque la méthode [**IMFOutputTrustAuthority :: SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) se termine de façon asynchrone.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |
| VT \_ UI4<br/> | Identificateur qui peut être défini sur un [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) via l’attribut [MF_POLICY_ID](mf-policy-id.md) .<br/> <br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




