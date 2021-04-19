---
description: Avertit une transformation de Media Foundation (MFT) qu’un flux d’entrée est terminé.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476781b149553bec1d48632e0621ff0a38ad8d21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517626"
---
# <a name="mft_message_notify_end_of_stream"></a>\_ \_ \_ fin \_ de flux de notification de message MFT \_

Avertit une transformation de Media Foundation (MFT) qu’un flux d’entrée est terminé.

## <a name="message-parameter"></a>Paramètre de message

Le paramètre *ulParam* contient l’identificateur du flux d’entrée, spécifié sous la forme d’une valeur **DWORD** . Dans les applications 64 bits, placez cette valeur dans les 32 bits inférieurs du **\_ pointeur PTR**.

## <a name="remarks"></a>Notes

Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Le client n’est pas obligé d’envoyer ce message.

Après la fin d’un flux, le client peut appeler [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) à nouveau pour envoyer de nouvelles données pour ce flux. Dans ce cas, le client doit définir l’attribut discontinu ([**MFSampleExtension \_ discontinu**](mfsampleextension-discontinuity-attribute.md) ) sur le premier exemple d’entrée après la fin du flux. (Le client doit toujours définir cet attribut sur le premier nouvel échantillon après la fin d’un flux, que le client ait envoyé le message **\_ \_ \_ de fin \_ de \_ message de fin de message MFT** ou non). Pour plus d’informations sur la gestion des discontinuités, consultez [modèle de traitement MFT de base](basic-mft-processing-model.md).)

Après l’envoi de ce message pour chaque flux d’entrée, le client envoie généralement une commande de **\_ drainage de \_ commande \_ de message MFT** , puis collecte la sortie restante. Toutefois, le client n’est pas obligé de vider la MFT. Si le client ne draine pas la MFT, la MFT ignore généralement les données non traitées lors de l’appel suivant à [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), lorsqu’il détecte la discontinuité du flux. Le client peut également vider la MFT avant d’appeler **ProcessInput**.

Ce message ne supprime pas le flux d’entrée ou ne réinitialise pas le type de média.

### <a name="implementation"></a>Implémentation

Aucune table MFT n’est requise pour répondre à ce message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_type de message MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




