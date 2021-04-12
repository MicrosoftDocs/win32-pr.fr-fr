---
description: Demande une table de Media Foundation (MFT) à laquelle la diffusion en continu est sur le point de se terminer.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527915"
---
# <a name="mft_message_notify_end_streaming"></a>\_notification de \_ fin \_ de \_ diffusion de message MFT

Demande une table de Media Foundation (MFT) à laquelle la diffusion en continu est sur le point de se terminer.

## <a name="message-parameter"></a>Paramètre de message

Aucun.

## <a name="remarks"></a>Notes

Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Le client n’est pas obligé d’envoyer ce message, même si le client a précédemment envoyé le message de notification de démarrage de la **\_ diffusion en \_ \_ \_ continu du message MFT** .

### <a name="implementation"></a>Implémentation

La table MFT peut répondre à ce message en libérant des mémoires tampons et d’autres ressources. La table MFT n’efface pas les données d’entrée et ne réinitialise pas les types de média en réponse à ce message. Aucune table MFT n’est requise pour répondre à ce message.

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

 

 




