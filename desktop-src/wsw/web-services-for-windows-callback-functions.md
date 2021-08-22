---
title: Windows Fonctions de rappel des services Web
description: Les rappels permettent à une application d’appeler une fonction définie au niveau d’une autre couche ou d’un autre niveau.
ms.assetid: 7398ec42-388a-494c-9fe4-5bd62aa009cb
keywords:
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a78bce5c4023d889748af103148088462cb4b267192b1c0b3845fc735fd1bb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926869"
---
# <a name="windows-web-services-callback-functions"></a>Windows Fonctions de rappel des services Web

Les rappels permettent à une application d’appeler une fonction définie au niveau d’une autre couche ou d’un autre niveau. L’application inscrit l’argument de fonction en tant que gestionnaire qui doit être appelé de manière asynchrone ultérieurement, en fonction des besoins. Le rappel est appelé si la fonction se termine de façon asynchrone, indiquant la réussite ou l’erreur de la fonction. Le rappel n’est pas appelé si l’opération se termine de façon synchrone.

l’API des Services Web Windows comprend les fonctions de rappel suivantes :

-   [**\_rappel de \_ message WS abandon \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)
-   [**\_rappel de \_ canal WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)
-   [**rappel de l' \_ \_ écouteur WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**\_rappel de \_ canal d’acceptation WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**\_rappel WS asynchrone \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
-   [**WS \_ Async, \_ fonction**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function)
-   [**\_rappel de \_ notification de \_ liste \_ d' \_ émetteurs WS CERT**](/windows/desktop/api/WebServices/nc-webservices-ws_cert_issuer_list_notification_callback)
-   [**\_rappel de \_ validation de certificat WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_certificate_validation_callback)
-   [**\_rappel de \_ canal WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)
-   [**rappel de l' \_ \_ écouteur WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**\_rappel de canal WS Create \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)
-   [**WS \_ créer un \_ canal \_ pour le rappel de l' \_ écouteur \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**création d’un \_ \_ rappel de décodeur WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)
-   [**création d’un \_ \_ rappel d’encodeur WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)
-   [**création d’un \_ \_ rappel d’ÉCOUTEur WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**rappel du décodeur WS \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)
-   [**\_rappel de fin du DÉcodeur WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)
-   [**le \_ DÉcodeur WS \_ obtient le rappel de \_ type de contenu \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback)
-   [**\_rappel de démarrage du DÉcodeur WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)
-   [**rappel de comparaison de la \_ durée WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**\_rappel de \_ chaîne \_ dynamique WS**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**rappel de codage de code d' \_ encodeur WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)
-   [**rappel de fin de l' \_ encodeur WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)
-   [**\_rappel du \_ \_ type de \_ contenu \_ de l’encodeur WS**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback)
-   [**rappel de début de l' \_ encodeur WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)
-   [**\_rappel de \_ canal \_ libre WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)
-   [**\_rappel du \_ décodeur \_ libre WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)
-   [**rappel de l' \_ \_ encodeur libre WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)
-   [**rappel de l' \_ \_ écouteur gratuit WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**le \_ \_ rappel du certificat \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)
-   [**le \_ rappel de la \_ propriété de canal \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)
-   [**rappel de la propriété de l' \_ \_ ÉCOUTEur WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**\_rappel de \_ redirection WS http \_**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)
-   [**WS \_ est \_ le \_ rappel de valeur par défaut \_**](/windows/desktop/api/WebServices/nc-webservices-ws_is_default_value_callback)
-   [**rappel de la \_ fin du message WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback)
-   [**\_rappel de \_ canal WS Open \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)
-   [**rappel de l' \_ \_ écouteur WS Open \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**rappel d’annulation de l' \_ opération WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)
-   [**\_rappel de \_ l' \_ état \_ libre de l’opération WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)
-   [**\_rappel de \_ message de proxy WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback)
-   [**rappel de WS \_ pull \_ octets \_**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**\_rappel d' \_ octets WS Push \_**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**\_rappel WS Read \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)
-   [**\_rappel de \_ fin de message WS Read \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)
-   [**\_rappel de \_ démarrage du message WS Read \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)
-   [**\_rappel de \_ type WS Read \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**\_rappel de \_ canal WS Reset \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)
-   [**rappel de l' \_ écouteur de réinitialisation WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**\_rappel de \_ canal d’acceptation de service Web \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback)
-   [**\_rappel de \_ canal de fermeture du service WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)
-   [**rappel de réception d’un \_ message WS service \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**\_rappel de \_ sécurité WS service \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)
-   [**\_rappel de \_ stub de service Web \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)
-   [**\_rappel de \_ propriété de canal WS Set \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)
-   [**rappel de la propriété de l' \_ \_ écouteur WS Set \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)
-   [**\_rappel de \_ canal de session d’arrêt WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)
-   [**le \_ \_ rappel de mot de passe WS Validate \_**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback)
-   [**\_validation du \_ rappel SAML WS Validate \_**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)
-   [**\_rappel d’écriture WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)
-   [**\_rappel de \_ fin de message WS Write \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)
-   [**\_rappel de \_ démarrage du message WS Write \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)
-   [**\_rappel de \_ type WS Write \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

 

 




