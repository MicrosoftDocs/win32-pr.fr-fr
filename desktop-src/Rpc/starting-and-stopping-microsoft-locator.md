---
title: Démarrage et arrêt de Microsoft Locator
description: Les bibliothèques Runtime RPC démarrent automatiquement le localisateur Microsoft si nécessaire. Vous pouvez arrêter et démarrer manuellement le localisateur si, par exemple, vous devez effacer la base de données lors du débogage d’une application distribuée.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028495"
---
# <a name="starting-and-stopping-microsoft-locator"></a><span data-ttu-id="9ba40-104">Démarrage et arrêt de Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="9ba40-104">Starting and Stopping Microsoft Locator</span></span>

<span data-ttu-id="9ba40-105">Les bibliothèques Runtime RPC démarrent automatiquement le localisateur Microsoft si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9ba40-105">The RPC run-time libraries automatically start Microsoft Locator when necessary.</span></span> <span data-ttu-id="9ba40-106">Vous pouvez arrêter et démarrer manuellement le localisateur si, par exemple, vous devez effacer la base de données lors du débogage d’une application distribuée.</span><span class="sxs-lookup"><span data-stu-id="9ba40-106">You can manually stop and start the Locator if, for example, you need to clear the database while debugging a distributed application.</span></span>

<span data-ttu-id="9ba40-107">**Pour arrêter et démarrer Microsoft Locator**</span><span class="sxs-lookup"><span data-stu-id="9ba40-107">**To stop and start Microsoft Locator**</span></span>

1.  <span data-ttu-id="9ba40-108">Dans le panneau de configuration, cliquez sur l’icône Services.</span><span class="sxs-lookup"><span data-stu-id="9ba40-108">From Control Panel, click the Services icon.</span></span>

    <span data-ttu-id="9ba40-109">La boîte de dialogue **services** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9ba40-109">The **Services** dialog box appears.</span></span>

2.  <span data-ttu-id="9ba40-110">Dans la boîte de dialogue **service** , sélectionnez **Microsoft Locator** , puis cliquez sur **Démarrer** ou **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="9ba40-110">In the **Service** dialog box, select **Microsoft Locator** and then click **Start** or **Stop**.</span></span>

<span data-ttu-id="9ba40-111">Vous pouvez également démarrer et arrêter Microsoft Locator à partir de la ligne de commande en tapant ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="9ba40-111">You can also start and stop Microsoft Locator from the command line by typing:</span></span>

<span data-ttu-id="9ba40-112">**\[RPCLOCATOR net start/stop \]**</span><span class="sxs-lookup"><span data-stu-id="9ba40-112">**net \[start/stop\] rpclocator**</span></span>

<span data-ttu-id="9ba40-113">Seul un administrateur peut démarrer Microsoft Locator une fois qu’il est arrêté.</span><span class="sxs-lookup"><span data-stu-id="9ba40-113">Only an administrator can start Microsoft Locator once it is stopped.</span></span> <span data-ttu-id="9ba40-114">Si elle est arrêtée, elle est redémarrée en fonction des besoins des bibliothèques Runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="9ba40-114">If stopped, it will be restarted as necessary by the RPC run-time libraries.</span></span>

 

 




