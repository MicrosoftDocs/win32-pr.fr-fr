---
title: Résultats du traitement de la sécurité
description: Sur un canal sécurisé, seuls les messages qui réussissent les vérifications de sécurité sont remis à l’application.
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- Résultats du traitement de la sécurité services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf6f8964d14c8cfdca3f6bd66b2f24e9fa611d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "106509070"
---
# <a name="security-processing-results"></a>Résultats du traitement de la sécurité

Sur un canal sécurisé, seuls les messages qui réussissent les vérifications de sécurité sont remis à l’application. Pour ces messages, certains résultats de la vérification de sécurité sont joints en tant que propriétés de message, et l’application peut extraire et examiner ces propriétés pour effectuer des étapes supplémentaires, telles que les vérifications d’autorisation.


La fonction [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) peut être utilisée pour récupérer les propriétés liées à la sécurité définies dans [**ID de \_ \_ propriété de \_ message WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id). **WsGetMessageProperty** retourne une erreur pour les requêtes qui demandent des propriétés de sécurité non applicables au type de sécurité utilisé sur le canal. Le message continue à posséder les propriétés retournées par la fonction de requête.

Les éléments d’API suivants sont utilisés avec les résultats du traitement de sécurité.

| Énumération                                                                | Description                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**\_ID de \_ propriété du jeton de sécurité WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | Définit les clés pour les champs et les propriétés qui peuvent être extraits à partir d’un jeton de sécurité. |



 



| Fonction                                                         | Description                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [**WsGetSecurityTokenProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | Extrait un champ ou une propriété d’un jeton de sécurité. |



 



| Handle                                       | Description                                     |
|----------------------------------------------|-------------------------------------------------|
| [\_jeton de sécurité WS \_](ws-security-token.md) | Handle opaque représentant un jeton de sécurité. |



 

 

 




