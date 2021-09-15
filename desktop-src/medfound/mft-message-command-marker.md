---
description: Marque un point dans le flux. Ce message s’applique uniquement aux MFTs asynchrones.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3802cb94c9183d4f392fbcedcf48c0c01071298e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531709"
---
# <a name="mft_message_command_marker"></a>\_ \_ marqueur de commande de message MFT \_

Marque un point dans le flux. Ce message s’applique uniquement aux [MFTS asynchrones](asynchronous-mfts.md).

## <a name="message-parameter"></a>Paramètre de message

Valeur arbitraire. La table MFT retourne la valeur au client dans l’événement [METransformMarker](metransformmarker.md) .

## <a name="remarks"></a>Notes

Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

La table MFT répond à ce message, comme suit :

1.  La table MFT génère autant d’exemples de sortie que possible des données d’entrée existantes, en envoyant un événement [METransformHaveOutput](metransformhaveoutput.md) pour chaque exemple de sortie.
2.  Une fois que toutes les sorties sont générées, la table MFT envoie un événement [METransformMarker](metransformmarker.md) . Cet événement doit être envoyé après tous les événements [METransformHaveOutput](metransformhaveoutput.md) .

Le client n’est pas obligé d’envoyer ce message et ne doit envoyer ce message qu’à un MFTs asynchrone. Une table MFT synchrone n’enverra pas d’événement [METransformMarker](metransformmarker.md) en réponse à ce message.

### <a name="implementation"></a>Implémentation

Les MFTs asynchrones doivent répondre à ce message comme décrit. Le MFTs synchrone doit ignorer ce message.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_type de message MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




