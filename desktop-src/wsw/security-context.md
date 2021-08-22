---
title: Contexte de sécurité
description: Les contextes de sécurité permettent d’établir un contexte de sécurité de message conformément à WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- Contexte de sécurité natif-services Web
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06dc1754133f47cf06c5c12e7318a94525be3c821f3db52a7e7513349c3100be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083173"
---
# <a name="security-context"></a>Contexte de sécurité

Les contextes de sécurité permettent d’établir un contexte de sécurité de message conformément à WS-SecureConversation. Ce contexte peut ensuite être utilisé pour sécuriser les messages en guise d’alternative à la sécurité à un seul moment où les informations d’identification sont transmises pour chaque demande. Le contexte de sécurité établi est une méthode plus efficace pour sécuriser les messages lors de l’échange de plusieurs messages.


Les contextes de sécurité nécessitent la présence des informations d’identification de sécurité de démarrage utilisées pour sécuriser les messages envoyés dans le contexte. Les structures de liaison de sécurité de message WS [**\_ Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), de [**\_ \_ \_ \_ \_ liaison**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)de sécurité de message de jeton WS XML et [**WS \_ UserName \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) peuvent être utilisées à cette fin.

Les contextes de sécurité sont une fonctionnalité de sécurité des messages et sont configurés par le biais de liaisons de sécurité de message.

## <a name="client"></a>Client

Du côté client, le contexte de sécurité est lié à un canal particulier. Il est configuré à l’aide de la [**liaison de sécurité de message de \_ contexte de sécurité \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding). Le comportement et la durée de vie du contexte sont déterminés par le canal. Lorsque le premier message est envoyé sur le canal, le contexte de sécurité est établi. Après cela, le contexte est renouvelé de manière proactive à un intervalle configurable. Si le serveur retourne une erreur indiquant que le contexte nécessite un renouvellement, le contexte est renouvelé lors de l’envoi du message suivant. Si le canal est à l’état ouvert, le contexte est annulé par un message d’annulation lorsque le canal est fermé.

## <a name="server"></a>Serveur

Sur le serveur, un contexte de sécurité est configuré de la même façon que sur le client. Toutefois, il n’est pas lié à un canal particulier. Au lieu de cela, tous les canaux créés pour l’écouteur qui a le jeu de [**liaisons de sécurité de message du \_ contexte de sécurité \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) peuvent recevoir des messages avec l’un des contextes de sécurité qui ont été établis sur les canaux de cet écouteur.

Lorsqu’un message arrive sur un canal qui prend en charge les contextes de sécurité, le contexte utilisé par ce message peut être obtenu en appelant la fonction [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) avec le contexte de sécurité de la [**propriété de \_ message \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id). La valeur récupérée peut être utilisée avec [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) et [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).

## <a name="metadata"></a>Métadonnées

La structure de contrainte de liaison de [**\_ \_ sécurité de \_ message de \_ \_ \_ contexte**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) de sécurité WS est utilisée pour extraire la stratégie de contexte de sécurité des métadonnées. Pour plus d’informations, consultez [importation de métadonnées](metadata-import.md).

Les éléments d’API suivants sont utilisés avec les contextes de sécurité.

| Énumération                                                                    | Description                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [**\_ID de \_ propriété de contexte WS Security \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | Identifie une propriété d’un objet de contexte de sécurité. |



 



| Fonction                                                             | Description                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | Obtient une propriété du contexte de sécurité spécifié. |
| [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | Révoque un contexte de sécurité.                        |



 



| Handle                                           | Description                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [\_contexte de sécurité WS \_](ws-security-context.md) | Type opaque utilisé pour référencer un objet de contexte de sécurité. |



 



| Structure                                                               | Description                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**\_propriété de \_ contexte de sécurité WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | Définit une propriété d’un [ \_ \_ contexte de sécurité WS](ws-security-context.md). |



 

 

 




