---
title: Description de la sécurité
description: Une description de la sécurité est représentée par une \_ \_ structure de description de la sécurité WS et une instance d’une description de sécurité est fournie quand vous appelez la fonction WsCreateChannel pour créer un canal sécurisé ou la fonction WsCreateListener pour créer un écouteur.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Services Web de la description de la sécurité pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c06e8553441b7eb813106213dbfa089810aad74c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411315"
---
# <a name="security-description"></a>Description de la sécurité

Une description de la sécurité est représentée par une structure de [**\_ \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) de la sécurité WS et une instance d’une description de sécurité est fournie quand vous appelez la fonction [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) pour créer un canal sécurisé ou la fonction [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) pour créer un écouteur.


## <a name="structure-of-a-security-description"></a>Structure d’une description de sécurité

Le modèle de base de sécurité de canal est qu’un canal est sécurisé avec un ou plusieurs jetons de sécurité. Reflétant ce modèle, la structure de [**\_ \_ Description de la sécurité WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contient une liste de liaisons de sécurité, représentées par les structures de [**\_ \_ liaison WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) , et chaque liaison de sécurité décrit comment un jeton de sécurité est obtenu et utilisé sur le canal. Le type de sécurité utilisé sur un canal est déterminé par la sélection des sous-types de liaison de sécurité inclus dans la description de la sécurité.

Les paramètres de sécurité facultatifs spécifiques à une liaison de sécurité sont spécifiés en tant que [paramètres de liaison](security-binding-settings.md) de sécurité dans la structure de liaison de sécurité. Toutefois, les paramètres au niveau du canal indépendamment des liaisons de sécurité sont directement spécifiés en tant que [paramètres de canal de sécurité](security-channel-settings.md) dans le champ des **Propriétés** de la description de sécurité proprement dite.

![Diagramme montrant la structure d’une description de sécurité.](images/securitydescription.png)

Les éléments d’API suivants sont utilisés avec les descriptions de sécurité.

| Structure                                                    | Description                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Description de la sécurité de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | Structure de niveau supérieur utilisée pour spécifier les exigences de sécurité pour un canal (côté client) ou un écouteur (côté serveur). |



 

 

 




