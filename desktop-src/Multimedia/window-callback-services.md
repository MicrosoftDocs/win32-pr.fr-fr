---
title: Services de rappel de fenêtre
description: Services de rappel de fenêtre
ms.assetid: 227602e5-7ea1-4afd-ac88-cfeabe746d1f
keywords:
- audio multimédia, services de rappel de fenêtre
- audio, services de rappel de fenêtre
- mixages audio, services de rappel de fenêtre
- mixages, services de rappel de fenêtre
- services de rappel de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48faf2dd94b61f5d4fc47e073fe0f3875bcbb503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463071"
---
# <a name="window-callback-services"></a><span data-ttu-id="a8e68-108">Services de rappel de fenêtre</span><span class="sxs-lookup"><span data-stu-id="a8e68-108">Window Callback Services</span></span>

<span data-ttu-id="a8e68-109">Les services de mixage fournissent des services de rappel de fenêtre afin que votre application puisse traiter les messages des pilotes de mixage.</span><span class="sxs-lookup"><span data-stu-id="a8e68-109">The mixer services provide window callback services so that your application can process messages from mixer drivers.</span></span> <span data-ttu-id="a8e68-110">Pour utiliser ces services, spécifiez l' \_ indicateur de fenêtre de rappel dans le paramètre *fdwOpen* et un handle de fenêtre dans le paramètre *DwCallback* de la fonction [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) .</span><span class="sxs-lookup"><span data-stu-id="a8e68-110">To use these services, specify the CALLBACK\_WINDOW flag in the *fdwOpen* parameter and a window handle in the *dwCallback* parameter of the [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) function.</span></span> <span data-ttu-id="a8e68-111">Les messages de pilote sont envoyés à la fonction de procédure de fenêtre pour la fenêtre identifiée par le handle dans *dwCallback*.</span><span class="sxs-lookup"><span data-stu-id="a8e68-111">Driver messages are sent to the window procedure function for the window identified by the handle in *dwCallback*.</span></span> <span data-ttu-id="a8e68-112">Les messages sont spécifiques au type de périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="a8e68-112">The messages are specific to the audio device type.</span></span>

 

 