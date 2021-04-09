---
description: Avertit une transformation de Media Foundation (MFT) que le premier échantillon est sur le point d’être traité.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0edefdecdf75afbe14c851f33e9726400e490d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034161"
---
# <a name="mft_message_notify_start_of_stream"></a>\_ \_ début de la notification par message MFT \_ \_ du \_ flux

Avertit une transformation de Media Foundation (MFT) que le premier échantillon est sur le point d’être traité.

## <a name="message-parameter"></a>Paramètre de message

Aucun.

## <a name="remarks"></a>Notes

Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Pour les MFTs synchrones, il est facultatif d’envoyer ce message.

Pour les MFTs asynchrones, le client doit envoyer ce message.

### <a name="implementation"></a>Implémentation

Une table MFT synchrone n’est pas requise pour répondre au message.

Une table MFT asynchrone doit implémenter ce message, comme décrit dans [MFTS asynchrone](asynchronous-mfts.md).

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

 

 




