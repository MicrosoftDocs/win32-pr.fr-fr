---
title: Envoi de l’appel au programme serveur
description: Une fois que le temps d’exécution RPC côté client s’est connecté au point de terminaison de serveur, il marshale les arguments et les envoie au serveur.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- Appel de procédure distante RPC, tâches, envoi de l’appel au serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba3a2dac77ec13fb00374faef456a52f0f24e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310933"
---
# <a name="sending-the-call-to-the-server-program"></a><span data-ttu-id="5e37d-104">Envoi de l’appel au programme serveur</span><span class="sxs-lookup"><span data-stu-id="5e37d-104">Sending the Call to the Server Program</span></span>

<span data-ttu-id="5e37d-105">Une fois que le temps d’exécution RPC côté client s’est connecté au point de terminaison de serveur, il marshale les arguments et les envoie au serveur.</span><span class="sxs-lookup"><span data-stu-id="5e37d-105">Once the client side RPC run time has connected to the server endpoint, it marshalls the arguments and sends them to the server.</span></span> <span data-ttu-id="5e37d-106">Le temps d’exécution RPC du serveur transmet les arguments marshalés au stub qui les démarshale, puis les passe aux routines du serveur.</span><span class="sxs-lookup"><span data-stu-id="5e37d-106">The server RPC run time gives the marshalled arguments to the stub that unmarshalls them, and then passes them to the server routines.</span></span> <span data-ttu-id="5e37d-107">Lorsque les routines de serveur retournent, le stub récupère \[ les \] paramètres out et \[ in, out \] et la valeur de retour, les marshale et envoie les données marshalées au moment de l’exécution RPC du serveur.</span><span class="sxs-lookup"><span data-stu-id="5e37d-107">When the server routines return, the stub picks up the \[out\] and \[in,out\] parameters and the return value, marshalls them, and sends the marshalled data to the server RPC run time.</span></span> <span data-ttu-id="5e37d-108">Le temps d’exécution RPC renvoie les données au client, où le temps d’exécution RPC du client les transmet au stub côté client qui les démarshale et les retourne à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="5e37d-108">The RPC run time sends the data back to the client, where the client RPC run time hands them off to the client side stub that unmarshalls them and returns them to the caller.</span></span>

 

 




