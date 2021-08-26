---
title: Écoute des appels de procédure distante
description: Une fois que le programme serveur a inscrit ses informations de liaison et publié sa présence dans une base de données de service de noms, il peut commencer à écouter le point de terminaison pour les appels de procédure distante.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb60b6d383c7c31b7eb59aab6f17fcdad1fde108b6f26d4fa73627d34f74340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020109"
---
# <a name="listening-for-remote-procedure-calls"></a>Écoute des appels de procédure distante

Une fois que le programme serveur a inscrit ses informations de liaison et publié sa présence dans une base de données de service de noms, il peut commencer à écouter le point de terminaison pour les appels de procédure distante. Les programmes serveur appellent la fonction [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) pour surveiller les points de terminaison pour les appels clients de procédures distantes.

La spécification DCE de [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indique qu’elle ne doit pas être retournée tant qu’une fonction du programme serveur n’a pas appelé [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening). L’implémentation Microsoft RPC de **RpcServerListen** utilise deux paramètres qui n’apparaissent pas dans la spécification DCE : *DontWait* et *MinimumCallThreads*. Votre programme serveur peut passer une valeur différente de zéro pour le paramètre *DontWait* . Si c’est le cas, la fonction **RpcServerListen** est immédiatement retournée. Utilisez la routine [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) pour effectuer l’opération d’attente généralement associée à **RpcServerListen**.

 

 




