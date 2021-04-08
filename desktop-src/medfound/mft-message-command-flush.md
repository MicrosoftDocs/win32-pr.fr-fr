---
description: Demande à une transformation de Media Foundation (MFT) de vider toutes les données stockées.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68f5e52cda9cca3470fb1dd903b5083a0cbc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753949"
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

 

 




