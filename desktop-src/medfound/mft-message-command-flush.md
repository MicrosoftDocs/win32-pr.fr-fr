---
description: MFT_MESSAGE_COMMAND_FLUSH-demande une table de Media Foundation pour vider toutes les données stockées.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34959303a2835e67202256341b0f5998b63d16b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092737"
---
# <a name="mft_message_command_flush"></a>\_vidage de \_ commande de message MFT \_

Demande à une transformation de Media Foundation (MFT) de vider toutes les données stockées.

## <a name="message-parameter"></a>Paramètre de message

Aucun.

## <a name="remarks"></a>Notes

Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Une fois ce message envoyé, la MFT peut accepter de nouveaux exemples d’entrée. Les types de médias actuels ne sont pas invalidés.

### <a name="implementation"></a>Implémentation

Toutes les MFTs doivent implémenter ce message. Lorsqu’il reçoit ce message, la MFT doit supprimer tous les échantillons de support qu’il contient.

[MFTS asynchrone](asynchronous-mfts.md): la table MFT n’envoie pas d’autre événement [METransformNeedInput](metransformneedinput.md) jusqu’à ce qu’elle reçoive un message [**\_ \_ \_ \_ de \_ flux de message de démarrage de flux MFT**](mft-message-notify-start-of-stream.md) du client.

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

 

 




