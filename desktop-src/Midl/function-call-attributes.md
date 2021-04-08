---
title: Attributs d’appel de fonction
description: Les programmes peuvent utiliser ces attributs sur des fonctions individuelles au sein de l’interface et affectent uniquement cette fonction.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- IDL MIDL, attributs, appel de fonction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d53407abf464d7b201c49d9cb2b1d3f3625b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675589"
---
# <a name="function-call-attributes"></a>Attributs d’appel de fonction

Les programmes peuvent utiliser ces attributs sur des fonctions individuelles au sein de l’interface et affectent uniquement cette fonction.



| Attribut                        | Utilisation                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Message**](message.md)       | L’appel de procédure distante doit être traité comme un message asynchrone du client au serveur. Le client effectue l’appel et le retourne immédiatement, tandis que l’appel réel est géré par le transport de mise en file d’attente de messages ([**ncadg \_ MQ**](ncadg-mq.md)). |
| [**environ**](maybe.md)           | Le client qui effectue cet appel de procédure distante n’attend aucune réponse indiquant la remise ou l’achèvement de l’appel. Cela diffère des opérations de [**message**](message.md) quand aucune réponse n’est attendue, mais que la remise est garantie.        |
| [**diffusion**](broadcast.md)   | L’appel de procédure distante doit être envoyé à tous les serveurs sur le réseau. Le client accepte le premier retour, les réponses suivantes provenant d’autres serveurs sont ignorées.                                                                                    |
| [**idempotent**](idempotent.md) | L’appel ne change pas d’État et retourne les mêmes informations chaque fois qu’il est appelé avec les mêmes paramètres d’entrée.                                                                                                                                     |
| [**rappel**](callback.md)     | Désigne une fonction qui réside dans l’application cliente, que le serveur peut appeler pour obtenir des informations à partir du client.                                                                                                                             |
| [**appeler \_ en tant que**](call-as.md)      | Mappe une fonction qui n’est pas accessible à distance à un appel de procédure distante.                                                                                                                                                                                                   |
| [**localisé**](local.md)           | Désigne une procédure locale pour laquelle MIDL ne génère pas de code stub.                                                                                                                                                                                   |



 

Sur les interfaces qui ne sont pas des [**objets**](object.md) , vous pouvez également appliquer l’attribut de [**\_ handle de contexte**](context-handle.md) à une fonction pour spécifier les caractéristiques de la valeur de retour.

 

 




