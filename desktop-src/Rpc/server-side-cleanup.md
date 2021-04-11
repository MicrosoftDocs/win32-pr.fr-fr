---
title: Nettoyage côté serveur
description: Nettoyage côté serveur et appel de procédure distante (RPC).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a66272fc3cca209d6825ac34d5158094ddff39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029469"
---
# <a name="server-side-cleanup"></a>Nettoyage côté serveur

Imaginez le scénario suivant :

Un client ouvre un handle de contexte, puis arrête ou perd la connexion au serveur. Comment le serveur détecte-t-il que le client a échoué et le descripteur de contexte doit être exécuté ? Il existe deux sous-scénarios : l’un est que le client est arrêté de manière ordonnée. Dans ce cas, il informe le serveur qu’il est en cours d’arrêt, et le serveur peut effectuer un nettoyage, y compris l’exécution de contexte. Si le client ne s’arrête pas de manière ordonnée ou s’il ne peut pas notifier le serveur, le serveur utilise Keep Alive pour déterminer si le client est toujours disponible. Côté serveur, la fonction [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) n’a aucun effet. Au lieu de cela, le serveur utilise le paramètre global par ordinateur – Keep Alive, dont la valeur par défaut est d’environ deux heures. Si le client ne répond pas aux connexions Keep Alive du serveur, la connexion est fermée. Lorsque toutes les connexions à un processus client donné sont fermées, le serveur nettoie et exécute les descripteurs de contexte en suspens.

 

 




