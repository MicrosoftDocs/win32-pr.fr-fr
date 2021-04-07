---
title: Télécharger les meilleures pratiques
description: Highloads peut provoquer diverses conditions de délai d’attente du serveur, ce qui peut, à son tour, augmenter la charge lorsque le client effectue une nouvelle tentative.
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95a229ff1e229c41fde8fd377e347f91cf43010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028657"
---
# <a name="upload-best-practices"></a><span data-ttu-id="1b5e9-103">Télécharger les meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="1b5e9-103">Upload Best Practices</span></span>

<span data-ttu-id="1b5e9-104">Highloads peut provoquer diverses conditions de délai d’attente du serveur, ce qui peut, à son tour, augmenter la charge lorsque le client effectue une nouvelle tentative.</span><span class="sxs-lookup"><span data-stu-id="1b5e9-104">Highloads may cause various server timeout conditions, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="1b5e9-105">En outre, un grand nombre de connexions en suspens consommeront plus de ressources serveur et compliqueront la situation.</span><span class="sxs-lookup"><span data-stu-id="1b5e9-105">Also, a large number of outstanding connections will consume more server resources and make the situation worse.</span></span> <span data-ttu-id="1b5e9-106">En plus de cela, si l’application principale n’est pas écrite pour gérer les conditions de charge élevée, elle peut se bloquer ou se comporter de façon inappropriée.</span><span class="sxs-lookup"><span data-stu-id="1b5e9-106">On top of that, if backend app is not written to handle high load conditions, it may crash or mal-behave.</span></span> <span data-ttu-id="1b5e9-107">L’application doit effectuer les étapes suivantes pour limiter la charge sur le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="1b5e9-107">The app shall perform the following steps to limit the load on the backend.</span></span>

<span data-ttu-id="1b5e9-108">Si l’application serveur n’est pas écrite pour gérer des volumes élevés, des conditions d’expiration peuvent se produire, ce qui peut, à son tour, augmenter la charge lorsque le client effectue une nouvelle tentative.</span><span class="sxs-lookup"><span data-stu-id="1b5e9-108">If the server application is not written to handle high volumes, timeout conditions may occur, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="1b5e9-109">En outre, un grand nombre de connexions en suspens consommeront plus de ressources serveur.</span><span class="sxs-lookup"><span data-stu-id="1b5e9-109">Also, a large number of outstanding connections will consume more server resources.</span></span>

<span data-ttu-id="1b5e9-110">Lors du test de votre application serveur, testez avec la charge la plus élevée possible.</span><span class="sxs-lookup"><span data-stu-id="1b5e9-110">When testing your server application, test with highest load possible.</span></span> <span data-ttu-id="1b5e9-111">Vous devez utiliser plusieurs ordinateurs clients, chacun avec plusieurs travaux de BITS de premier plan simultanés, et mesurer le débit maximal au niveau du serveur principal.</span><span class="sxs-lookup"><span data-stu-id="1b5e9-111">You should use multiple client machines, each with several concurrent, foreground BITS jobs, and measure the maximum throughput at the backend.</span></span> <span data-ttu-id="1b5e9-112">Si vous ne pouvez pas mesurer le débit, vous devrez estimer le débit.</span><span class="sxs-lookup"><span data-stu-id="1b5e9-112">If you cannot measure the throughput, you will have to estimate the throughput.</span></span>

<span data-ttu-id="1b5e9-113">L’application serveur doit résider sur une URL différente de l’URL de téléchargement (voir la propriété IIS de BITS, **BITSServerNotificationURL**).</span><span class="sxs-lookup"><span data-stu-id="1b5e9-113">The server application should reside on a different URL from the upload URL (see the BITS IIS property, **BITSServerNotificationURL**).</span></span>

<span data-ttu-id="1b5e9-114">Il est conseillé de limiter la charge sur le serveur d’applications en fonction des valeurs de débit éprouvées.</span><span class="sxs-lookup"><span data-stu-id="1b5e9-114">It is good practice to limit the load on the application server based on proven throughput values.</span></span> <span data-ttu-id="1b5e9-115">Vous devez utiliser les propriétés IIS, **MaxBandwidth** et **MaxConnections**, pour limiter la charge sur le serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="1b5e9-115">You should use the IIS properties, **MaxBandwidth** and **MaxConnections**, to limit the load on the application server.</span></span>

 

 




