---
description: Avertit une transformation de Media Foundation (MFT) que le premier échantillon est sur le point d’être traité.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ed40d9d3514dfa6223d4e20f2eb411caec497e16f2e97c456f16e14442c407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973028"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_type de message MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




