---
description: Avertit une transformation de Media Foundation (MFT) que la diffusion en continu est sur le point de commencer.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa67f58c7246b50292f4b34711e0149eb8f3377
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531704"
---
# <a name="mft_message_notify_begin_streaming"></a>\_notification de \_ début \_ de \_ diffusion de message MFT

Avertit une transformation de Media Foundation (MFT) que la diffusion en continu est sur le point de commencer.

## <a name="message-parameter"></a>Paramètre de message

Aucun.

## <a name="remarks"></a>Notes

Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Le client n’est pas obligé d’envoyer ce message. Si le client envoie ce message, il doit le faire après avoir défini tous les types de média sur la MFT, et avant d’appeler [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). La table MFT peut répondre en allouant des tampons ou d’autres ressources. Si le client n’envoie pas ce message, la table MFT alloue des ressources lors du premier appel à **ProcessInput**. Par conséquent, l’envoi de ce message peut réduire la latence initiale au démarrage de la diffusion en continu.

### <a name="implementation"></a>Implémentation

Aucune table MFT n’est requise pour répondre à ce message.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_type de message MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




