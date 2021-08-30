---
title: E/s asynchrones et RPC asynchrone
description: Les e/s asynchrones sont un moyen efficace pour qu’un seul thread gère simultanément plusieurs demandes d’e/s.
ms.assetid: a9105518-4130-4119-b8d1-e73064b077e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7bdd198143c2f1f1d03aa73249680f47dec6d6ac6f996675df1f1e53fb56137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023809"
---
# <a name="asynchronous-io-and-asynchronous-rpc"></a>E/s asynchrones et RPC asynchrone

Les e/s asynchrones sont un moyen efficace pour qu’un seul thread gère simultanément plusieurs demandes d’e/s. Le RPC asynchrone sur le serveur remplit un rôle similaire pour les demandes RPC. dans les versions de Windows antérieures à Windows Vista, la publication de demandes d’e/s asynchrones à partir de procédures serveur à l’aide de RPC asynchrone est déconseillée. toutefois, dans Windows Vista et les versions ultérieures de Windows, les demandes d’e/s asynchrones associées à un port de terminaison d’e/s sont prises en charge par RPC asynchrone.

avant Windows Vista, un appel de procédure distante asynchrone peut se terminer avant la fin de la requête d’e/s asynchrone. Lorsque l’appel asynchrone est terminé, son thread peut se terminer si le runtime RPC décide qu’il a suffisamment de threads disponibles pour traiter la charge de travail attendue. Le système lie toutes les demandes d’e/s au thread qui les initie. Si le thread se termine, toutes les demandes d’e/s en attente sur ce thread sont abandonnées. Les demandes d’e/s en attente ne peuvent pas être déplacées vers un autre thread.

par conséquent, les concepteurs d’applications ciblant des versions de Windows antérieures à Windows Vista peuvent utiliser des e/s synchrones dans les procédures de serveur ou transférer toutes les requêtes qui impliquent des e/s asynchrones à des procédures qui s’exécutent sur un pool de threads géré par l’application. l’API Windows fournit des fonctions pour la gestion des pools de threads. Consultez [fonctions de processus et de thread](/windows/desktop/ProcThread/process-and-thread-functions).

 

 