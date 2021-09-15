---
title: Envoi de l’appel au programme serveur
description: Une fois que le temps d’exécution RPC côté client s’est connecté au point de terminaison de serveur, il marshale les arguments et les envoie au serveur.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- Appel de procédure distante RPC, tâches, envoi de l’appel au serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba3a2dac77ec13fb00374faef456a52f0f24e99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413542"
---
# <a name="sending-the-call-to-the-server-program"></a>Envoi de l’appel au programme serveur

Une fois que le temps d’exécution RPC côté client s’est connecté au point de terminaison de serveur, il marshale les arguments et les envoie au serveur. Le temps d’exécution RPC du serveur transmet les arguments marshalés au stub qui les démarshale, puis les passe aux routines du serveur. Lorsque les routines de serveur retournent, le stub récupère \[ les \] paramètres out et \[ in, out \] et la valeur de retour, les marshale et envoie les données marshalées au moment de l’exécution RPC du serveur. Le temps d’exécution RPC renvoie les données au client, où le temps d’exécution RPC du client les transmet au stub côté client qui les démarshale et les retourne à l’appelant.

 

 




