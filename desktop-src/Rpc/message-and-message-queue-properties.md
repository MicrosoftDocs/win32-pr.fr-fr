---
title: Propriétés des messages et des files d’attente de messages
description: Un message contient des propriétés qui spécifient une étiquette, un corps de message et un certain nombre d’options.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0139a588b52f1de1de43d8ec50aebdaf57b995ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310517"
---
# <a name="message-and-message-queue-properties"></a>Propriétés des messages et des files d’attente de messages

Un message contient des propriétés qui spécifient une étiquette, un corps de message et un certain nombre d’options. Les options de propriété de message peuvent inclure la qualité de service, la priorité, la journalisation, les niveaux de confidentialité et d’authentification, ainsi que la durée de vie du message. Dans les applications de mise en file d’attente de messages conventionnels (non RPC), vous spécifiez ces propriétés en appelant les fonctions de l’API MSMQ ou les méthodes de l’objet COM, qui sont décrites dans la documentation du kit de développement logiciel (SDK) MSMQ. Les applications clientes RPC peuvent définir certaines propriétés pour les appels de procédure distante en appelant [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) et [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo). Une fois définis, les propriétés restent en vigueur pour chaque message jusqu’à ce que l’application cliente les réinitialise.

Une file d’attente de messages a son propre ensemble de propriétés, à l’exception de celles des messages. Ces propriétés identifient de façon unique une file d’attente et définissent la classe de service fournie par la file d’attente, les niveaux de confidentialité et d’authentification requis pour les messages de cette file d’attente, et si les messages doivent faire partie d’une transaction distribuée. Comme avec les propriétés de message, vous spécifiez les propriétés d’une file d’attente de messages en appelant les fonctions de l’API MSMQ ou les méthodes de l’objet COM, qui sont décrites dans la documentation MSMQ. Toutefois, une application serveur RPC peut spécifier des propriétés de sa propre file d’attente de réception lorsqu’elle appelle [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) pour établir la liaison.

 

 




