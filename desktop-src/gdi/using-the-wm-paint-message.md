---
description: Vous pouvez utiliser le \_ message WM Paint pour effectuer les dessins nécessaires à l’affichage des informations.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Utilisation du message WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77246e04effc74de8158aef9bfc4aaf27471c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202484"
---
# <a name="using-the-wm_paint-message"></a><span data-ttu-id="fb56b-103">Utilisation du \_ message WM Paint</span><span class="sxs-lookup"><span data-stu-id="fb56b-103">Using the WM\_PAINT Message</span></span>

<span data-ttu-id="fb56b-104">Vous pouvez utiliser le message [**WM \_ Paint**](wm-paint.md) pour effectuer les dessins nécessaires à l’affichage des informations.</span><span class="sxs-lookup"><span data-stu-id="fb56b-104">You can use the [**WM\_PAINT**](wm-paint.md) message to carry out the drawing necessary for displaying information.</span></span> <span data-ttu-id="fb56b-105">Étant donné que le système envoie des \_ messages de peinture WM à votre application lorsque celle-ci doit être mise à jour ou lorsque vous demandez explicitement une mise à jour, vous pouvez consolider le code pour le dessin dans la procédure de fenêtre de votre application.</span><span class="sxs-lookup"><span data-stu-id="fb56b-105">Because the system sends WM\_PAINT messages to your application when your window must be updated or when you explicitly request an update, you can consolidate the code for drawing in your application's window procedure.</span></span> <span data-ttu-id="fb56b-106">Vous pouvez ensuite utiliser ce code chaque fois que votre application doit dessiner des informations nouvelles ou existantes.</span><span class="sxs-lookup"><span data-stu-id="fb56b-106">You can then use this code whenever your application must draw either new or existing information.</span></span>

<span data-ttu-id="fb56b-107">Les sections suivantes présentent différentes façons d’utiliser le \_ message de peinture WM pour dessiner dans une fenêtre :</span><span class="sxs-lookup"><span data-stu-id="fb56b-107">The following sections show a variety of ways to use the WM\_PAINT message to draw in a window:</span></span>

-   [<span data-ttu-id="fb56b-108">Dessin dans la zone cliente</span><span class="sxs-lookup"><span data-stu-id="fb56b-108">Drawing in the Client Area</span></span>](drawing-in-the-client-area.md)
-   [<span data-ttu-id="fb56b-109">Redessin de la zone cliente entière</span><span class="sxs-lookup"><span data-stu-id="fb56b-109">Redrawing the Entire Client Area</span></span>](redrawing-the-entire-client-area.md)
-   [<span data-ttu-id="fb56b-110">Redessiner dans la région de mise à jour</span><span class="sxs-lookup"><span data-stu-id="fb56b-110">Redrawing in the Update Region</span></span>](redrawing-in-the-update-region.md)
-   [<span data-ttu-id="fb56b-111">Invalidation de la zone cliente</span><span class="sxs-lookup"><span data-stu-id="fb56b-111">Invalidating the Client Area</span></span>](invalidating-the-client-area.md)
-   [<span data-ttu-id="fb56b-112">Dessin d’une fenêtre réduite</span><span class="sxs-lookup"><span data-stu-id="fb56b-112">Drawing a Minimized Window</span></span>](drawing-a-minimized-window.md)
-   [<span data-ttu-id="fb56b-113">Dessin d’un arrière-plan de fenêtre personnalisé</span><span class="sxs-lookup"><span data-stu-id="fb56b-113">Drawing a Custom Window Background</span></span>](drawing-a-custom-window-background.md)

 

 



