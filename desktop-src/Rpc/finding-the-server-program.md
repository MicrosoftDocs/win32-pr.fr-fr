---
title: Recherche du programme serveur
description: Une fois que l’exécution RPC côté client se connecte à un système hôte serveur demandé dans le handle de liaison, la bibliothèque Runtime RPC du client recherche le processus serveur.
ms.assetid: 0c863018-746a-4793-abe7-1838d988e0f4
keywords:
- Appel de procédure distante RPC, tâches, recherche du programme serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b822dbca1a927e13f01d7c91aa7c78267db4d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106530783"
---
# <a name="finding-the-server-program"></a><span data-ttu-id="24389-104">Recherche du programme serveur</span><span class="sxs-lookup"><span data-stu-id="24389-104">Finding the Server Program</span></span>

<span data-ttu-id="24389-105">Une fois que l’exécution RPC côté client se connecte à un système hôte serveur demandé dans le handle de liaison, la bibliothèque Runtime RPC du client recherche le processus serveur.</span><span class="sxs-lookup"><span data-stu-id="24389-105">After the client side RPC run time connects to a server host system requested in the binding handle, the client RPC run-time library finds the server process.</span></span> <span data-ttu-id="24389-106">Pour ce faire, il interroge le mappage du point de terminaison sur le système hôte du serveur.</span><span class="sxs-lookup"><span data-stu-id="24389-106">To do this, it queries the endpoint map on the server host system.</span></span> <span data-ttu-id="24389-107">Le mappage de point de terminaison contient des informations sur le point de terminaison sur lequel le serveur est à l’écoute.</span><span class="sxs-lookup"><span data-stu-id="24389-107">The endpoint map contains information about which endpoint the server is listening to.</span></span>

 

 




