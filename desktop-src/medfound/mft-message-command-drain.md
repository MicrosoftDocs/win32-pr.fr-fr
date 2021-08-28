---
description: MFT_MESSAGE_COMMAND_DRAIN-demande une table de Media Foundation pour vider toutes les données stockées.
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8faf20ca1169d87370a7dc1b5a128b11c9f17937a514f4aaea37631aee4d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012619"
---
# <a name="mft_message_command_drain"></a>\_drain de \_ commande de message MFT \_

Demande à une transformation de Media Foundation (MFT) de vider toutes les données stockées.

## <a name="message-parameter"></a>Paramètre de message

Aucun.

## <a name="remarks"></a>Notes

Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Après l’envoi de ce message, le flux d’entrée spécifié n’accepte pas d’entrée tant que la table MFT n’a pas traité toutes les données des appels précédents à [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

Le processus de drainage varie légèrement entre les MFTs synchrones et les MFTs asynchrones :

**MFTs synchrone**

1.  Une fois que le client a envoyé ce message, il appelle [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) dans une boucle, jusqu’à ce que **ProcessOutput** retourne le code **d’erreur MF \_ E \_ Transform \_ nécessite \_ plus \_ d’entrée**.
2.  Tant que la table MFT a toujours des données à traiter, les appels ultérieurs à [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) échouent. La table MFT continue à produire la sortie jusqu’à ce qu’elle utilise toutes les données stockées. La table MFT ignore toutes les données qui ne peuvent pas être traitées dans un exemple complet de sortie. (Par exemple, il doit supprimer une image vidéo partielle.)

**MFTs asynchrone**

1.  La table MFT continue à envoyer des événements [METransformHaveOutput](metransformhaveoutput.md) jusqu’à ce qu’elle n’ait plus aucune donnée à traiter. Elle n’envoie pas d’événements [METransformNeedInput](metransformneedinput.md) pendant cette période.
2.  Une fois que la table MFT envoie le dernier événement [METransformHaveOutput](metransformhaveoutput.md) , elle envoie un événement [METransformDrainComplete](metransformdraincomplete.md) .
3.  Une fois l’opération de drainage terminée, la table MFT n’envoie pas d’autre événement [METransformNeedInput](metransformneedinput.md) tant qu’elle n’a pas reçu de message [**MFT \_ message \_ \_ \_ de démarrage de \_ flux**](mft-message-notify-start-of-stream.md) du client.

Une fois que le client a vidé la MFT, le client peut envoyer plus de données d’entrée. Le premier échantillon après l’opération de drainage doit avoir l’attribut discontinu ([**MFSampleExtension \_ discontinu**](mfsampleextension-discontinuity-attribute.md) ).

> [!Note]  
> Les versions antérieures de cette documentation indiquaient que le paramètre d’événement *ulParam* est membre de l’énumération du [**\_ \_ \_ type de drainage MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) . C’est inexact. *UlParam* contient un identificateur de flux.

 

### <a name="implementation"></a>Implémentation

Une table MFT asynchrone doit toujours retourner [METransformDrainComplete](metransformdraincomplete.md) une fois qu’elle a été vidée.

Une table MFT synchrone peut ignorer ce message et retourner \_ la valeur OK si les conditions suivantes sont remplies :

-   La table MFT ne stocke jamais plus d’un échantillon d’entrée à la fois.
-   Chaque exemple d’entrée produit un seul échantillon de sortie.

Dans le cas contraire, un MFT synchrone doit implémenter ce message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_type de message MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[MFTs asynchrone](asynchronous-mfts.md)
</dt> </dl>

 

 




