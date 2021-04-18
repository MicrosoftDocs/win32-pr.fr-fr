---
title: Attributs asynchrones
description: Lorsqu’un programme appelle une procédure dans une interface, la procédure peut s’exécuter de façon synchrone ou asynchrone.
ms.assetid: 3e6c6c13-1524-41b2-96dc-3885eadb847c
keywords:
- IDL MIDL, attributs MIDL, asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aca2276bf1fa5178f1dca3ae4803544066d983
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512307"
---
# <a name="asynchronous-attributes"></a>Attributs asynchrones

Lorsqu’un programme appelle une procédure dans une interface, la procédure peut s’exécuter de façon synchrone ou asynchrone. Une procédure synchrone entraîne l’attente du programme appelant jusqu’à ce que la procédure soit retournée avant que le programme puisse continuer. Une procédure asynchrone est retournée immédiatement sans attendre les résultats. Le programme appelant doit se resynchroniser ultérieurement avec la procédure d’interface pour recevoir des données. Pour plus d’informations, consultez [RPC asynchrone](/windows/desktop/Rpc/asynchronous-rpc).

Vous pouvez utiliser les attributs suivants pour assurer la prise en charge des appels de procédure distante asynchrones.



| Attribut                         | Utilisation                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)            | En cas d’application à un paramètre de fonction, définit un handle qui permet à l’appelant de passer un appel asynchrone et de retourner immédiatement sans attendre les résultats, puis de se resynchroniser ultérieurement avec la fonction appelée pour recevoir des données une fois l’appel terminé. L’attribut [**Async**](async.md) est également utilisé dans les fichiers ACF pour définir un handle asynchrone pour une procédure ou une interface entière. Pour les interfaces COM, cette interface est obsolète et ne peut pas être utilisée pour les nouvelles interfaces. |
| [**\_UUID asynchrone**](async-uuid.md) | Indique au compilateur MIDL de définir à la fois les versions synchrones et asynchrones d’une interface COM.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**environ**](maybe.md)            | Le client qui effectue cet appel de procédure distante n’attend aucune réponse indiquant la remise ou la fin de l’appel, et la remise n’est pas garantie. Cela diffère des opérations de **message** quand aucune réponse n’est attendue, mais que la remise est garantie.                                                                                                                                                                                                                    |
| [**Message**](message.md)        | L’appel de procédure distante doit être traité comme un message asynchrone du client au serveur. Le client effectue l’appel et le retourne immédiatement, tandis que l’appel réel est géré par le transport de mise en file d’attente de messages ([**ncadg \_ MQ**](ncadg-mq.md)).                                                                                                                                                                                                                              |



 

 

 