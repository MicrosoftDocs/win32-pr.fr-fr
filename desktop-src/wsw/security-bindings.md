---
title: Liaisons de sécurité
description: Une liaison de sécurité est la spécification d’un jeton de sécurité et indique au runtime comment obtenir et utiliser un jeton de sécurité pour la sécurité du canal.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Services Web des liaisons de sécurité pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a263c1a79212f3438e77c3dca519f6493cf40e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411320"
---
# <a name="security-bindings"></a>Liaisons de sécurité

Une liaison de sécurité est la spécification d’un jeton de sécurité et indique au runtime comment obtenir et utiliser un jeton de sécurité pour la sécurité du canal. Le jeton de sécurité contient des informations sur le droit d’accéder aux ressources. Elle peut également avoir une clé de chiffrement associée pour effectuer des signatures et un chiffrement.


Chaque liaison de sécurité contient sa propre collection de [paramètres de liaison de sécurité](security-binding-settings.md) facultatifs qui sont étendus au jeton de sécurité qu’elle définit. Il contient également des [informations d’identification de sécurité](security-credentials.md), qui représentent les preuves de sécurité (telles que le nom d’utilisateur et les mots de passe ou les certificats) nécessaires à la création de jetons de sécurité.

Les rappels suivants font partie de la liaison de sécurité :

-   [**\_validation du \_ rappel SAML WS Validate \_**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

Les énumérations suivantes font partie de la liaison de sécurité :

-   [**utilisation de la \_ sécurité WS message \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [**TYPE d’authentificateur de WS \_ SAML \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [**\_type de \_ liaison de sécurité WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [**\_type de \_ handle de clé de sécurité WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

Les fonctions suivantes font partie de la liaison de sécurité :

-   [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [**WsFreeSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

Les structures suivantes font partie de la liaison de sécurité :

-   [**\_handle de \_ \_ clé de sécurité asymétrique WS CAPI \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [**\_ \_ \_ AUTHENTIFICATEUR SAML signé WS \_ CERT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [**\_liaison de \_ sécurité d’authentification d’en-tête WS http \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [**\_liaison de \_ \_ sécurité de message WS Kerberos APREQ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [**\_liaison de \_ \_ sécurité de transport SSPI WS NAMEDPIPE \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**\_handle de \_ \_ clé de sécurité asymétrique WS NCRYPT \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [**\_handle de \_ \_ clé de sécurité symétrique WS brut \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [**\_authentificateur SAML \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [**\_liaison de \_ sécurité de message WS SAML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [**\_liaison de sécurité WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [**\_liaison de \_ sécurité de message de contexte de sécurité WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [**\_handle de \_ clé de sécurité WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [**\_liaison de \_ sécurité de transport WS SSL \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [**liaison de sécurité de transport de WS \_ TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [**\_liaison de \_ sécurité de message WS username \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [**\_liaison de \_ \_ sécurité de message de jeton XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




