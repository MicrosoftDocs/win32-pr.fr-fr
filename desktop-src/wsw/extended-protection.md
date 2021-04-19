---
title: protection étendue
description: La protection étendue est un mécanisme permettant de lier un canal sécurisé externe tel que SSL à des protocoles d’authentification de canal interne tels que Kerberos-APREQ et l’authentification d’en-tête HTTP.
ms.assetid: 35e48846-05e5-4db9-a3b5-098b62815b66
keywords:
- Protection étendue Native-services Web
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895bdfecf994f6673c2ed7e7367bc3a7b5bd70c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511633"
---
# <a name="extended-protection"></a>protection étendue

La protection étendue est un mécanisme permettant de lier un canal sécurisé externe tel que SSL à des protocoles d’authentification de canal interne tels que Kerberos-APREQ et l’authentification d’en-tête HTTP.

Le concept de protection étendue est défini dans RFC2743.

La protection étendue, le cas échéant, est configurée automatiquement sur le client, mais peut nécessiter une configuration sur le serveur pour les scénarios autres que ceux par défaut.

## <a name="supported-configurations"></a>Configurations prises en charge

La protection étendue est prise en charge lors de l’utilisation de la [**\_ \_ \_ liaison de canal http WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) avec des liaisons de sécurité à l’aide de protocoles d’authentification intégrée de Windows, tels que [**\_ \_ \_ \_ \_ liaison de sécurité d’en-tête WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) et [**\_ \_ \_ \_ \_ liaison de sécurité de message WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding). Il est configuré via les [**Propriétés de sécurité**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)suivantes :

-   [**\_stratégie de \_ \_ protection étendue \_ \_ de la propriété WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_scénario de \_ \_ protection étendue \_ des propriétés WS Security \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_ \_ \_ identités du service de propriétés de sécurité WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)

Les configurations suivantes impliquant la protection étendue sont possibles :

Client

-   [**WS \_ La \_ \_ \_ liaison de sécurité de transport SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) est utilisée avec la liaison de sécurité de [**\_ message WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) ou la liaison de [**\_ \_ \_ \_ sécurité \_ d’en-tête WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding). Dans cette configuration, la liaison d’authentification est liée à la connexion SSL via un jeton de protection étendu qui est automatiquement extrait de la connexion SSL.
-   Aucun SSL n’est utilisé et la [**liaison de sécurité d' \_ \_ \_ authentification \_ \_ des en-têtes WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) est définie. La liaison d’authentification est liée via le nom de principal du serveur (SPN), qui est autonatically déterminé à partir de l' [**\_ \_ adresse du point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address).

Serveur

-   [**WS \_ La \_ \_ \_ liaison de sécurité de transport SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) est utilisée avec la liaison de sécurité de [**\_ message WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) ou la liaison de [**\_ \_ \_ \_ sécurité \_ d’en-tête WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding). Dans cette configuration, la liaison d’authentification est liée à la connexion SSL via un jeton de protection étendu qui est extrait de la connexion SSL et validé automatiquement.
-   Aucun SSL n’est utilisé et la [**liaison de sécurité d' \_ \_ \_ authentification \_ \_ des en-têtes WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) est définie. La liaison d’authentification est liée via le nom de principal du serveur (SPN), qui doit être fourni via les [**\_ \_ \_ \_ identités du service de propriétés de sécurité WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id). Lorsqu’un message est reçu, le SPN est extrait et validé pour une correspondance exacte avec les noms de service fournis. Ne pas fournir de SPN est l’équivalent de la définition de la [**\_ stratégie de protection étendue WS \_ \_ \_ jamais**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy).
-   Aucun SSL n’est utilisé, le [**\_ \_ \_ \_ \_ serveur lié au scénario de protection étendue WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) est spécifié et la [**\_ \_ \_ \_ \_ liaison de sécurité de message WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) est utilisée. Dans cette configuration, [**les \_ \_ \_ \_ identités du service de propriétés WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) ne doivent pas être définies. Aucune vérification du SPN n’est effectuée au-delà de ce qui est fait dans le cadre du protocole Kerberos.
-   [**WS \_ Le \_ \_ \_ \_ protocole SSL terminé du scénario de protection étendue**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) est spécifié et la liaison de sécurité de [**\_ message WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) ou de l' [**\_ \_ en-tête WS \_ \_ \_ http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) est utilisée. [**WS \_ Les \_ \_ \_ identités du service de propriétés de sécurité**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) doivent être définies.

## <a name="supported-platforms"></a>Plateformes prises en charge

La protection étendue est prise en charge sur les plateformes prenant en charge le service informatique dans le système d’exploitation. Windows 7 et Windows Server 2008 R2 offrent une prise en charge intégrée. D’autres plateformes peuvent nécessiter une mise à jour.

Si le système d’exploitation du serveur ne fournit pas de prise en charge, toutes les informations de protection étendue envoyées par le client sont ignorées. Par conséquent, les clients qui utilisent la protection étendue peuvent communiquer avec un serveur de ce type, mais l’avantage de sécurité est perdu. Sur le client, [**la \_ \_ liaison de \_ \_ sécurité de \_ message WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) associée à la [**\_ \_ \_ \_ liaison de sécurité de transport WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) prend uniquement en charge la protection étendue sur Vista et versions ultérieures.

Remarque : la protection étendue non disponible n’empêche pas l’utilisation d’une configuration particulière.

## <a name="interoperability"></a>Interopérabilité

Un serveur configuré par défaut peut communiquer avec les clients SOAP, qu’ils utilisent ou non la protection étendue. La seule exception étant Windows XP et Windows Server 2003, les clients WWSAPI mis à jour pour prendre en charge la protection étendue et utilisent la liaison de [**\_ sécurité de message WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) et la liaison de [**\_ sécurité de \_ transport \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Pour prendre en charge ces clients, la [**\_ stratégie de protection étendue WS ne doit \_ \_ \_ jamais**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy) être spécifiée par le serveur. Les serveurs configurés avec la **stratégie de protection étendue de WS rejettent \_ \_ \_ \_ toujours** les communications des clients qui n’utilisent pas la protection étendue. Sur le client, **la \_ \_ liaison de \_ \_ sécurité de \_ message WS Kerberos APREQ** combinée à la **\_ \_ \_ \_ liaison de sécurité de transport WS SSL** entraîne l’envoi du message à l’aide de l’encodage de transfert en bloc http sur Vista et versions ultérieures. Cela peut entraîner des problèmes d’interopérabilité avec les serveurs qui ne prennent pas en charge le transfert mémorisé en bloc.

Les enums/constantes suivants font partie de la protection étendue :

-   [**\_stratégie de \_ protection \_ étendue WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy)
-   [**\_scénario de \_ protection \_ étendue WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario)

Les structures répertoires suivants font partie de la protection étendue :

-   [**\_ \_ identités de sécurité WS service \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_security_identities)

 

 




