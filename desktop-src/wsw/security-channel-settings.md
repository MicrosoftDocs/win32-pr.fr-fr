---
title: Paramètres de canal de sécurité
description: Les paramètres de canal de sécurité contrôlent la façon dont la sécurité est appliquée et vérifiée sur un canal.
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- canal de sécurité Paramètres les Services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3d6cef77da7a908598e2150ebf09de13a0899a6910a562335c4a5b91d6cf8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927009"
---
# <a name="security-channel-settings"></a>Paramètres de canal de sécurité

Les paramètres de canal de sécurité contrôlent la façon dont la sécurité est appliquée et vérifiée sur un canal. Chaque paramètre de canal de sécurité est représenté par une collection de paires propriété-valeur, avec les clés de propriété définies par l’ID de propriété d’énumération [**WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id). Chaque propriété de la collection a une valeur par défaut raisonnable. En raison de ces valeurs par défaut, il est possible de définir et d’utiliser une description de sécurité sans spécifier les paramètres du canal de sécurité.


Les [paramètres de liaison de sécurité](security-binding-settings.md) contiennent des collections similaires de paires propriété-valeur dont les clés sont définies par la structure de [**\_ \_ \_ propriété de liaison de sécurité WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) . La différence entre ces deux types de paramètres est que les paramètres de canal de sécurité sont étendus à une description de sécurité (autrement dit, ils contiennent des propriétés de sécurité au niveau du canal), alors que les paramètres de liaison de sécurité sont étendus à l’une des liaisons de sécurité et qu’il peut y avoir de nombreuses liaisons de sécurité. Par exemple, une description de sécurité personnalisée qui contient trois liaisons de sécurité aura un sac de paramètres de canal de sécurité pour le canal entier et trois conteneurs de paramètres de liaison de sécurité, un pour chaque liaison de sécurité.

Les énumérations suivantes sont utilisées avec les paramètres de canal de sécurité :

-   [**\_niveau de protection WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [**\_ID de \_ propriété du jeton de sécurité de demande WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [**\_ID d' \_ algorithme WS Security \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [**ID de propriété de l' \_ algorithme de sécurité WS \_ \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [**\_disposition d' \_ en-tête WS Security \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [**\_version d' \_ en-tête WS Security \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [**\_ID de \_ propriété de sécurité WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_utilisation des \_ horodateurs de sécurité WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [**\_ID de \_ propriété du jeton de sécurité WS XML \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

Les structures suivantes sont utilisées avec les paramètres de canal de sécurité :

-   [**\_propriété de \_ jeton de sécurité de demande WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [**propriété de l' \_ algorithme de sécurité WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [**\_suite d' \_ algorithmes de sécurité de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [**\_propriété de sécurité WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [**\_propriété de \_ jeton de sécurité WS XML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




