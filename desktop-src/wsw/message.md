---
title: Message (services web Windows)
description: Un message est un objet qui encapsule des données transmises ou reçues.
ms.assetid: edc810d9-7d78-4b79-8cbb-e87401f6ae41
keywords:
- Services Web de message pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704df318e10521bd56e62632af16e683b7baccfc
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104569550"
---
# <a name="message-windows-web-services"></a>Message (services web Windows)

Un message est un objet qui encapsule des données transmises ou reçues. La structure d’un message est définie par SOAP et comprend un ensemble d’en-têtes et un corps. Les en-têtes sont toujours mis en mémoire tampon, mais le corps est lu et écrit avec une API de streaming.

![Diagramme montrant un message avec l’en-tête mis en mémoire tampon et le corps qui est diffusé en continu.](images/messageenvelope.png)


Les messages ont un ensemble de propriétés qui peuvent être utilisées pour spécifier des paramètres facultatifs qui contrôlent le comportement d’un message et pour fournir un moyen de récupérer des informations supplémentaires sur les messages reçus (tels que les informations de sécurité). Pour obtenir la liste complète des propriétés de message, consultez [**\_ ID de \_ propriété \_ de message WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) .

Un message est adressé à une [adresse de point de terminaison](endpoint-address.md)spécifique.

Une [**\_ erreur WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) est un type spécial de contenu de message utilisé pour représenter les échecs renvoyés par à partir d’un point de terminaison distant.

Les messages subissent un encodage qui transforme le XML en un format de câble linéaire avant d’être transmis.

Pour plus d’informations sur les messages, consultez la rubrique [vue d’ensemble](channel-layer-overview.md) de la couche de canal.

Les exemples suivants illustrent l’utilisation de messages dans WWSAPI.

| Exemple                                              | Description                                  |
|------------------------------------------------------|----------------------------------------------|
| [CustomHeaderExample](customheaderexample.md)       | Illustre l’utilisation d’en-têtes de message personnalisés.    |
| [MessageEncodingExample](messageencodingexample.md) | Illustre l’encodage et le décodage d’un message. |
| [ForwardMessageExample](forwardmessageexample.md)   | Illustre le transfert d’un message.            |



 

Les éléments d’API suivants sont utilisés avec les messages.

| Rappel                                                        | Description                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**rappel de la \_ fin du message WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback) | Avertit l’appelant que le message a terminé son utilisation de la structure de \_ lecteur XML WS \_ qui a été fournie à la fonction WsReadEnvelopeStart, ou de la \_ structure d’enregistreur XML WS \_ fournie à la fonction WsWriteEnvelopeStart. |



 



| Énumération                                                      | Description                                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**\_version d’adressage WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)         | Version de la spécification utilisée pour les en-têtes d’adressage.                                        |
| [**VERSION de l' \_ enveloppe WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_envelope_version)             | Version de la spécification utilisée pour la structure d’enveloppe.                                        |
| [**\_attributs d’en-tête WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type)           | Ensemble d’indicateurs représentant les attributs SOAP mustUnderstand et Relay d’un en-tête.                    |
| [**\_type d’en-tête WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type)                       | Type de l’en-tête.                                                                                  |
| [**\_initialisation des messages WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) | Spécifie les en-têtes que le [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage) doit ajouter au message. |
| [**\_ID de \_ propriété du message WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)      | ID de chaque propriété de message.                                                                         |
| [**\_État du message WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_state)                   | État du message.                                                                                |



 



| Fonction                                                             | Description                                                                                                                                            |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage)                         | Attribue une adresse de destination à un message.                                                                                                            |
| [**WsCheckMustUnderstandHeaders**](/windows/desktop/api/WebServices/nf-webservices-wscheckmustunderstandheaders) | Vérifie que les en-têtes spécifiés ont été correctement compris par le destinataire.                                                                         |
| [**WsCreateMessage**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessage)                           | Crée une instance d’un objet de [ \_ message WS](ws-message.md) .                                                                                         |
| [**WsCreateMessageForChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessageforchannel)       | Crée un message approprié pour une utilisation avec un canal spécifique.                                                                                 |
| [**WsFillBody**](/windows/desktop/api/WebServices/nf-webservices-wsfillbody)                                     | Garantit que le nombre d’octets disponibles dans un message est suffisant pour la lecture.                                                                |
| [**WsFlushBody**](/windows/desktop/api/WebServices/nf-webservices-wsflushbody)                                   | Vide toutes les données de corps de message accumulées qui ont été écrites.                                                                                       |
| [**WsFreeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsfreemessage)                               | Libère la ressource mémoire associée à un message.                                                                                                |
| [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader)                       | Recherche l’en-tête défini par l’application du message et le désérialise.                                                                               |
| [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)                                   | Recherche un en-tête standard particulier dans le message et le désérialise.                                                                                 |
| [**WsGetHeaderAttributes**](/windows/desktop/api/WebServices/nf-webservices-wsgetheaderattributes)               | Remplit un paramètre ULONG avec les [**attributs d' \_ en \_ -tête WS**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type) à partir de l’élément d’en-tête sur lequel le lecteur est positionné. |
| [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty)                 | Récupère une propriété d’objet message spécifiée.                                                                                                         |
| [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage)                   | Initialise les en-têtes du message en préparation du traitement.                                                                                 |
| [**WsMarkHeaderAsUnderstood**](/windows/desktop/api/WebServices/nf-webservices-wsmarkheaderasunderstood)         | Marque un en-tête comme interprété par l’application.                                                                                                       |
| [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody)                                     | Désérialise une valeur du lecteur XML du message.                                                                                               |
| [**WsReadEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopeend)                       | Lit les éléments de fermeture d’un message.                                                                                                               |
| [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)                   | Lit les en-têtes du message et prépare la lecture des éléments du corps.                                                                               |
| [**WsRemoveCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremovecustomheader)                 | Supprime un en-tête personnalisé du message.                                                                                                              |
| [**WsRemoveHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremoveheader)                             | Supprime l’objet [**de \_ \_ type d’en-tête WS**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type) standard d’un message.                                                                 |
| [**WsResetMessage**](/windows/desktop/api/WebServices/nf-webservices-wsresetmessage)                             | Définit l’état du message sur **WS \_ message \_ State \_ Empty**.                                                                                          |
| [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader)                                   | Ajoute ou remplace l’en-tête standard spécifié dans le message.                                                                                         |
| [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody)                                   | Écrit une valeur dans le corps d’un message.                                                                                                               |
| [**WsWriteEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopeend)                     | Écrit les éléments de fermeture d’un message.                                                                                                              |
| [**WsWriteEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopestart)                 | Écrit le début du message, y compris l’ensemble actuel des en-têtes du message, et prépare l’écriture des éléments du corps.                           |



 



| Handle                        | Description                                         |
|-------------------------------|-----------------------------------------------------|
| [\_message WS](ws-message.md) | Type opaque utilisé pour référencer un objet de message. |



 



| Structure                                                | Description                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**\_erreur WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)                            | Valeur d’erreur dans le corps d’un message qui indique un échec de traitement. |
| [**\_code d’erreur WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)                 | Représente un code d’erreur.                                                             |
| [**raison de l' \_ erreur WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)             | Contient une explication de l’erreur.                                                |
| [**\_Propriétés du message WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_properties) | Spécifie un ensemble de structures de [**\_ \_ Propriétés de message WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property) .  |
| [**\_propriété de message WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property)     | Spécifie un paramètre de message spécifique.                                                |



 

 

 




