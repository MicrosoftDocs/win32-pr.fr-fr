---
title: Envoi de l’appel au programme serveur
description: Une fois que le temps d’exécution RPC côté client s’est connecté au point de terminaison de serveur, il marshale les arguments et les envoie au serveur.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- Appel de procédure distante RPC, tâches, envoi de l’appel au serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a02d4fc1d69ba45cc6de3d43fba62724de1277471992790e3098225f579d305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017909"
---
# <a name="sending-the-call-to-the-server-program"></a>Envoi de l’appel au programme serveur

Une fois que le temps d’exécution RPC côté client s’est connecté au point de terminaison de serveur, il marshale les arguments et les envoie au serveur. Le temps d’exécution RPC du serveur transmet les arguments marshalés au stub qui les démarshale, puis les passe aux routines du serveur. Lorsque les routines de serveur retournent, le stub récupère \[ les \] paramètres out et \[ in, out \] et la valeur de retour, les marshale et envoie les données marshalées au moment de l’exécution RPC du serveur. Le temps d’exécution RPC renvoie les données au client, où le temps d’exécution RPC du client les transmet au stub côté client qui les démarshale et les retourne à l’appelant.

 

 




