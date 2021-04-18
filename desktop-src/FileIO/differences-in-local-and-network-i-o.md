---
description: Différences entre les e/s locales et les e/s réseau sur Windows.
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: Différences dans les e/s locales et réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30c4faf6b7358a1c7c134dccdeb12298309c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526131"
---
# <a name="differences-in-local-and-network-io"></a><span data-ttu-id="b6257-103">Différences dans les e/s locales et réseau</span><span class="sxs-lookup"><span data-stu-id="b6257-103">Differences in Local and Network I/O</span></span>

<span data-ttu-id="b6257-104">Il existe des différences notables entre les e/s locales et les e/s réseau sur Windows :</span><span class="sxs-lookup"><span data-stu-id="b6257-104">There are some notable differences between local I/O and network I/O on Windows:</span></span>

-   <span data-ttu-id="b6257-105">La prise en charge des e/s réseau dépend du redirecteur et du protocole réseau.</span><span class="sxs-lookup"><span data-stu-id="b6257-105">Network I/O support depends on the redirector and the network protocol.</span></span>
-   <span data-ttu-id="b6257-106">Les performances d’e/s réseau dépendent du nombre d’opérations d’e/s réseau effectuées et de la vitesse de la connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="b6257-106">Network I/O performance depends on how many network I/O operations are taking place and the speed of the network connection.</span></span> <span data-ttu-id="b6257-107">Votre application doit être en mesure de gérer les opérations d’e/s réseau avec des serveurs qui peuvent être beaucoup plus rapides ou plus lents que votre ordinateur local, ainsi que des modifications transitoires de la capacité du réseau.</span><span class="sxs-lookup"><span data-stu-id="b6257-107">Your application must be able to handle network I/O operations with servers that may be much faster or slower than your local machine, as well as transient changes in network capacity.</span></span> <span data-ttu-id="b6257-108">Dans ce cas, votre application peut avoir besoin de plus de temps pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="b6257-108">In these cases, your application may need to allow more time for the operation to complete.</span></span>
-   <span data-ttu-id="b6257-109">Les fonctions que vous utilisez pour effectuer des e/s de fichier local peuvent se comporter différemment sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="b6257-109">The functions you use to perform local file I/O may behave differently over the network.</span></span> <span data-ttu-id="b6257-110">Par exemple, une opération d’e/s réseau qui prend beaucoup de temps pour s’exécuter peut expirer. Dans certains cas, les descripteurs de fichiers peuvent être laissés ouverts indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="b6257-110">For example, a network I/O operation that takes a long time to complete may time out. In some situations, file handles may be left open indefinitely because of this.</span></span> <span data-ttu-id="b6257-111">Autre exemple : les fonctions peuvent retourner des codes d’erreur que votre application doit traiter et qui sont spécifiques aux e/s réseau.</span><span class="sxs-lookup"><span data-stu-id="b6257-111">Another example is that functions may return error codes for your application to process that are specific to network I/O.</span></span>

 

 



