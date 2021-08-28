---
title: canal (Services Web Windows)
description: Les canaux encapsulent un contexte de communication entre deux ou plusieurs tiers et sont utilisés pour envoyer et recevoir des messages.
ms.assetid: 5a04580d-c89f-4505-a4b7-0724ffb788fd
keywords:
- Services Web Channel pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff11601f372416527f1d521f8fb9880c98821f9421b633f9eed059cc5b4f672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026647"
---
# <a name="channel-windows-web-services"></a>canal (Services Web Windows)

Les canaux encapsulent un contexte de communication entre deux ou plusieurs tiers et sont utilisés pour envoyer et recevoir des messages.


Sur le client, utilisez [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) pour créer un canal. Sur le serveur, utilisez [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) pour créer un canal qui peut être accepté par le client à l’aide d’un [écouteur](listener.md).

Lorsque vous créez un canal, vous spécifiez les informations suivantes, qui déterminent à la fois le comportement local du canal et le protocole câble à utiliser.

-   [**Type de \_ canal \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)qui identifie le modèle d’échange de messages du canal.
-   Une [**\_ \_ liaison WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), qui identifie le protocole de transfert à utiliser.
-   Description de la [**\_ \_ sécurité WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), qui spécifie la sécurité utilisée pour le canal. Lors de la création de canaux à utiliser sur un serveur, cela est spécifié une fois pour tous les canaux qui seront acceptés pour un écouteur donné.
-   Un ensemble [**de \_ \_ Propriétés WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), qui spécifient des paramètres facultatifs supplémentaires (pour obtenir la liste de ces paramètres, consultez énumérations de l' [**\_ \_ \_ ID de propriété du canal WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) ).

Avant d’utiliser le canal, vous devez l’ouvrir en appelant la fonction [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) et en spécifiant le canal et l' [adresse du point de terminaison](endpoint-address.md), ainsi que d’autres informations facultatives.

Pour plus d’informations sur les transitions d’état d’un canal, consultez la rubrique [**États du canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) .

Pour plus d’informations sur les canaux, consultez la rubrique [vue d’ensemble](channel-layer-overview.md) de la couche de canal.

Les éléments d’API suivants sont utilisés avec les canaux.

| Rappel                                                                                  | Description                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_rappel de \_ message WS abandon \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)                     | Gère l’appel [**WsAbandonMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage) pour un canal avec une liaison de canal personnalisée.                                              |
| [**\_rappel de \_ canal WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)                         | Gère l’appel [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) pour un canal avec une liaison de canal personnalisée.                                                  |
| [**\_rappel de \_ canal WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)                         | Gère l’appel [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) pour un canal avec une liaison de canal personnalisée.                                                  |
| [**\_rappel de canal WS Create \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)                       | Gère l’appel [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) pour un canal avec une liaison de canal personnalisée.                                                  |
| [**création d’un \_ \_ rappel de décodeur WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)                       | Gère la création d’une instance de décodeur.                                                                                                                  |
| [**création d’un \_ \_ rappel d’encodeur WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)                       | Gère la création d’une instance d’encodeur.                                                                                                                 |
| [**rappel du décodeur WS \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)                       | Décode un message.                                                                                                                                    |
| [**\_rappel de fin du DÉcodeur WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)                             | Décode la fin d’un message.                                                                                                                         |
| [**le \_ DÉcodeur WS \_ obtient le rappel de \_ type de contenu \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback) | Obtient le type de contenu du message.                                                                                                                 |
| [**\_rappel de démarrage du DÉcodeur WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)                         | Démarre le décodage d’un message.                                                                                                                            |
| [**rappel de codage de code d' \_ encodeur WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)                       | Encode un message.                                                                                                                                    |
| [**rappel de fin de l' \_ encodeur WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)                             | Encode la fin d’un message.                                                                                                                         |
| [**\_rappel du \_ \_ type de \_ contenu \_ de l’encodeur WS**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback) | Obtient le type de contenu du message.                                                                                                                 |
| [**rappel de début de l' \_ encodeur WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)                         | Démarre l’encodage d’un message.                                                                                                                            |
| [**\_rappel de \_ canal \_ libre WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)                           | Gère l’appel [**WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel) pour un canal avec une liaison de canal personnalisée.                                                    |
| [**\_rappel du \_ décodeur \_ libre WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)                           | Gère la libération d’une instance de décodeur.                                                                                                                   |
| [**rappel de l' \_ \_ encodeur libre WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)                           | Gère la libération d’une instance d’encodeur.                                                                                                                  |
| [**le \_ rappel de la \_ propriété de canal \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)          | Gère l’appel [**WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty) pour un canal avec une liaison de canal personnalisée.                                      |
| [**\_rappel de \_ redirection WS http \_**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)                         | Appelé lorsqu’un message va être automatiquement redirigé vers un autre service à l’aide de la fonctionnalité de redirection automatique HTTP, comme décrit dans RFC2616. |
| [**\_rappel de \_ canal WS Open \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)                           | Gère l’appel [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) pour un canal avec une liaison de canal personnalisée.                                                    |
| [**\_rappel de \_ fin de message WS Read \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)                  | Gère l’appel [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) pour un canal avec une liaison de canal personnalisée.                                              |
| [**\_rappel de \_ démarrage du message WS Read \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)              | Gère l’appel [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) pour un canal avec une liaison de canal personnalisée.                                              |
| [**\_rappel de \_ canal WS Reset \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)                         | Gère l’appel [**WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel) pour un canal avec une liaison de canal personnalisée.                                                  |
| [**\_rappel de \_ propriété de canal WS Set \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)          | Gère l’appel [**WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty) pour un canal avec une liaison de canal personnalisée.                                      |
| [**\_rappel de \_ canal de session d’arrêt WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)  | Gère l’appel [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel) pour un canal avec une liaison de canal personnalisée.                              |
| [**\_rappel de \_ fin de message WS Write \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)                | Gère l’appel [**WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend) pour un canal avec une liaison de canal personnalisée.                                            |
| [**\_rappel de \_ démarrage du message WS Write \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)            | Gère l’appel [**WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart) pour un canal avec une liaison de canal personnalisée.                                        |



 



| Énumération                                                 | Description                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_liaison WS Channel \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)          | Indique la pile de protocole à utiliser pour le canal.                                                                                      |
| [**\_ID de \_ propriété du canal WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) | Identifie chaque propriété de canal par un ID.                                                                                                |
| [**\_État du canal WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state)              | État du canal.                                                                                                                 |
| [**\_type de canal WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)                | Indique les caractéristiques de base du canal, par exemple s’il s’agit d’une session et quelles directions de communication sont prises en charge. |
| [**\_codage WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding)                         | Les différents encodages (formats de message).                                                                                                |
| [**\_option WS Receive \_**](/windows/desktop/api/WebServices/ne-webservices-ws_receive_option)            | Spécifie si un message est requis lors de la réception d’un canal.                                                                    |
| [**\_mode WS Transfer \_**](/windows/desktop/api/WebServices/ne-webservices-ws_transfer_mode)              | Spécifie si les messages envoyés ou reçus sont diffusés en continu ou mis en mémoire tampon.                                                            |



 



| Fonction                                                         | Description                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**WsAbandonMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage)                     | Ignore le reste d’un message pour un canal.                                                              |
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)                         | Abandonne toutes les e/s en attente sur un canal spécifié et définit l’état du canal sur **WS \_ Channel \_ State \_ Faulted**. |
| [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel)                         | Ferme un canal lorsqu’il n’est plus nécessaire.                                                                |
| [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel)                       | Crée un canal.                                                                                           |
| [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) | Crée un canal pour un écouteur.                                                                            |
| [**WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel)                           | Libère les ressources mémoire associées à un canal.                                                     |
| [**WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty)             | Récupère une propriété du canal référencé par le paramètre de canal.                                     |
| [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel)                           | Ouvre un canal à un point de terminaison.                                                                              |
| [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend)                     | Lit les éléments de fermeture d’un message à partir d’un canal.                                                      |
| [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart)                 | Lit les en-têtes du message suivant à partir du canal et prépare la lecture des éléments du corps.               |
| [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)                     | Reçoit un message et désérialise le corps du message en tant que valeur.                                      |
| [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)                         | Envoie un message de demande et reçoit un message de réponse corrélé.                                             |
| [**WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel)                         | Réinitialiser un canal afin qu’il puisse être réutilisé.                                                                         |
| [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage)                           | Envoie un message sur un canal à l’aide de la sérialisation pour écrire l’élément Body.                                  |
| [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)                 | Envoie un message qui est une réponse à un message reçu.                                                       |
| [**WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty)             | Définit une propriété d’un canal.                                                                                |
| [**WsSetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetmessageproperty)             | Définit la propriété d’un message.                                                                                |
| [**WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend)                   | Écrit les éléments de fermeture d’un message dans le canal.                                                     |
| [**WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart)               | Écrit les en-têtes d’un message dans le canal et prépare l’écriture des éléments du corps.                   |



 



| Handle                        | Description                                 |
|-------------------------------|---------------------------------------------|
| [\_canal WS](ws-channel.md) | Type opaque utilisé pour référencer un canal. |



 



| Structure                                                                          | Description                                                                                                                                                                                      |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DÉcodeur WS Channel \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_decoder)                                 | Ensemble de rappels qui transforment le type de contenu et les octets encodés d’un message reçu.                                                                                                      |
| [**\_encodeur WS Channel \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_encoder)                                 | Ensemble de rappels qui peuvent transformer le type de contenu et les octets encodés d’un message envoyé.                                                                                                      |
| [**\_Propriétés du canal WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_properties)                           | Ensemble de structures [**de \_ \_ propriété WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) .                                                                                                                        |
| [**\_propriété WS Channel \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)                               | Paramètre spécifique au canal.                                                                                                                                                                      |
| [**\_ \_ rappels de canal personnalisé WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_channel_callbacks)              | Ensemble de rappels qui forment l’implémentation d’un canal personnalisé.                                                                                                                             |
| [**\_ \_ proxy HTTP personnalisé \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_http_proxy)                            | utilisé pour spécifier le proxy personnalisé pour le canal, à l’aide de la **propriété WS Channel valeur de proxy \_ \_ \_ \_ http personnalisée** \_ de l’énumération d' [**\_ ID de \_ propriété \_ WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) . |
| [**\_mappage d' \_ en-tête WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_mapping)                        | Représente un en-tête individuel qui est mappé dans le cadre du [**\_ \_ \_ mappage de message http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).                                                                         |
| [**\_mappage de \_ message WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)                      | Informations sur la façon dont une requête ou une réponse HTTP doit être représentée dans un objet de message.                                                                                                     |
| [**\_contexte de \_ rappel de redirection WS http \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_redirect_callback_context) | Spécifie la fonction de rappel et l’État pour contrôler le comportement de redirection automatique HTTP.                                                                                               |
| [**\_Description du message WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)                         | Schéma pour le [ \_ message WS](ws-message.md) d’entrée et de sortie pour une description d’opération donnée.                                                                                             |



 

 

 




