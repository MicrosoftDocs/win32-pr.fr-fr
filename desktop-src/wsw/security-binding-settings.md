---
title: Paramètres de liaison de sécurité
description: Les paramètres de liaison de sécurité contrôlent la façon dont un jeton de sécurité est obtenu ou utilisé.
ms.assetid: 4bc03cb4-1ac2-4ad1-a45d-eae8f50f5355
keywords:
- liaison de sécurité Paramètres les Services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea7a4d761a030636951ba1d637769c5daa907d20379cbe554e871aecb17736e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054639"
---
# <a name="security-binding-settings"></a>Paramètres de liaison de sécurité

Les paramètres de liaison de sécurité contrôlent la façon dont un jeton de sécurité est obtenu ou utilisé. Elles sont représentées sous la forme d’une collection de paires propriété-valeur, avec les clés de propriété définies par la propriété de liaison d’énumération [**WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property). Chaque propriété de la collection a une valeur par défaut raisonnable. Par conséquent, il est possible de définir et d’utiliser une description de sécurité sans spécifier les paramètres de liaison de sécurité.


pour plus d’informations sur les paramètres de sécurité à l’ensemble du canal, avec les propriétés dont les clés sont définies par l’énumération de l' [**\_ ID de \_ propriété \_ WS security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) , consultez [Paramètres security channel](security-channel-settings.md).

Les éléments d’API suivants sont utilisés avec les paramètres de liaison de sécurité.

| Énumération                                                                          | Description                                                                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_échec du certificat WS \_**](/windows/win32/api/webservices/ne-webservices-ws_value_type)                                         | Définit les échecs liés à la validation du certificat.                                                                                                               |
| [**\_schéma d' \_ authentification des en-têtes WS http \_ \_**](https://technet.microsoft.com/windows/dd401907(v=vs.60))                 | Définit les options d’exécution de l’authentification du client à l’aide des en-têtes d’authentification HTTP.                                                                       |
| [**\_cible d' \_ authentification d’en-tête WS http \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_http_header_auth_target)                 | Définit la cible pour la liaison de sécurité d’authentification d’en-tête HTTP.                                                                                           |
| [**\_action de \_ jeton de sécurité de demande WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_action)     | Définit l’ensemble d’actions à utiliser lors de la négociation des jetons de sécurité à l’aide de WS-Trust.                                                                              |
| [**nom de la \_ \_ suite d’algorithmes de sécurité WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_suite_name)     | Suite d’algorithmes de sécurité utilisés pour des tâches telles que la signature et encryting.                                                                                      |
| [**\_ID de \_ propriété de liaison WS Security \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id)       | Identifie les propriétés utilisées pour spécifier les paramètres de liaison de sécurité.                                                                                              |
| [**\_mode d' \_ \_ entropie de la clé de sécurité WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode)             | Définit comment la randomisation doit être apportée à la clé émise pendant une négociation de jeton de sécurité effectuée avec la sécurité en mode mixte et le message.                     |
| [**\_type de \_ clé de sécurité WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_type)                              | Type de clé d’un jeton de sécurité.                                                                                                                                 |
| [**\_mode de \_ Référence du jeton de sécurité WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_reference_mode)     | mécanisme à utiliser pour faire référence à un jeton de sécurité à partir des signatures, des éléments chiffrés et des jetons dérivés dans le contexte des liaisons de sécurité de message et en mode mixte. |
| [**\_version WS Trust \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version)                                       | Définit la version de spécification WS-Trust à utiliser avec la sécurité de message et la sécurité en mode mixte.                                                              |
| [**\_package d' \_ \_ authentification intégrée WS Windows \_**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_package) | définit le package SSP spécifique à utiliser pour l’authentification intégrée Windows.                                                                                |



 



| Structure                                                               | Description                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [**\_propriété de \_ liaison de sécurité WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) | Spécifie un paramètre spécifique de liaison de sécurité. |



 

 

 




