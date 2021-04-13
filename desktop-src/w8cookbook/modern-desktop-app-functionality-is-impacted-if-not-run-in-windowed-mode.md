---
title: Les fonctionnalités des applications de bureau sont affectées si elles ne sont pas exécutées en mode fenêtre
description: Dans Windows 10, les applications Windows ne sont plus plein écran par défaut. en revanche, elles sont affichées sous la forme d’une fenêtre et les opérations telles que la minimisation, la restauration, l’agrandissement, le redimensionnement (et toute autre opération que vous avez toujours pu effectuer à toute autre fenêtre d’application Windows classique) sont désormais possibles.
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aae44fda5847e5b86616b40ab1bf4ab8cbd206b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380224"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a><span data-ttu-id="7b649-103">Les fonctionnalités des applications de bureau sont affectées si elles ne sont pas exécutées en mode fenêtre</span><span class="sxs-lookup"><span data-stu-id="7b649-103">Desktop App functionality is impacted if not run in Windowed Mode</span></span>

<span data-ttu-id="7b649-104">Dans Windows 10, les applications Windows ne sont plus plein écran par défaut. en revanche, elles sont affichées sous la forme d’une fenêtre et les opérations telles que la minimisation, la restauration, l’agrandissement, le redimensionnement (et toute autre opération que vous avez toujours pu effectuer à toute autre fenêtre d’application Windows classique) sont désormais possibles.</span><span class="sxs-lookup"><span data-stu-id="7b649-104">In Windows 10, Windows apps are no longer full-screen by default – instead, they are windowed and operations like minimizing, restoring, maximizing, resizing (and any other operation that you’ve always been able to do to any other Classic Windows application window) is now possible.</span></span>

## <a name="manifestations"></a><span data-ttu-id="7b649-105">Manifestations</span><span class="sxs-lookup"><span data-stu-id="7b649-105">Manifestations</span></span>

<span data-ttu-id="7b649-106">La modification la plus notable est maintenant que vous pouvez atteindre des tailles arbitraires qui ne sont pas simplement la taille de l’écran/la hauteur de l’écran.</span><span class="sxs-lookup"><span data-stu-id="7b649-106">The most noticeable change now is that you can get sized to arbitrary sizes that are not just the size of the screen/height of the screen.</span></span> <span data-ttu-id="7b649-107">Un utilisateur peut redimensionner continuellement la fenêtre de l’application à sa convenance (jusqu’à la taille minimale de la fenêtre de l’application).</span><span class="sxs-lookup"><span data-stu-id="7b649-107">A user can continuously resize the app window to their liking (down to the app’s minimal window size).</span></span> <span data-ttu-id="7b649-108">Cela diffère de Windows 8,0 ou Windows 8.1, où le fait de redimensionner une fenêtre était une action discrète (les utilisateurs redimensionnent une miniature de la fenêtre, ce qui a entraîné le redimensionnement de la fenêtre une fois que l’utilisateur a validé l’action).</span><span class="sxs-lookup"><span data-stu-id="7b649-108">This is different from Windows 8.0 or Windows 8.1, where the act of resizing a window was a discrete action (users resized a thumbnail of the window, which then caused the window to resize once the user committed the action).</span></span> <span data-ttu-id="7b649-109">Aujourd’hui, à la place, lorsque l’utilisateur fait glisser la fenêtre à l’aide du coin inférieur (ou d’un autre emplacement de bordure), il s’agit d’un redimensionnement continu, et l’application reçoit des messages de redimensionnement dans une ligne, au lieu d’une modification de la taille.</span><span class="sxs-lookup"><span data-stu-id="7b649-109">Today instead when the user drags the window by the bottom corner (or other border location) it is a continuous resize, and the app receives resize messages in a row, rather than size change.</span></span>

## <a name="mitigations"></a><span data-ttu-id="7b649-110">Corrections</span><span class="sxs-lookup"><span data-stu-id="7b649-110">Mitigations</span></span>

<span data-ttu-id="7b649-111">Pour atténuer ce risque pour les applications Windows 8,0 et 8,1 :</span><span class="sxs-lookup"><span data-stu-id="7b649-111">To mitigate this for Windows 8.0 and 8.1 apps:</span></span>

-   <span data-ttu-id="7b649-112">Si la fonctionnalité attendue dans la fonctionnalité de l’application est rompue, l’atténuation de l’utilisateur consiste à placer l’application en mode plein écran (à l’aide du bouton « aller à l’écran complet » dans le coin supérieur droit de la barre de titre).</span><span class="sxs-lookup"><span data-stu-id="7b649-112">If the expected feature within the app functionality is broken, then the user mitigation is to place the app into full screen mode (by using the “go full screen button” in the upper right corner of the title bar).</span></span>
-   <span data-ttu-id="7b649-113">Si le démarrage de l’application est affecté qu’elle ne s’ouvre pas comme prévu, l’utilisateur doit toujours être en mesure de basculer en mode tablette pour forcer l’application à démarrer en mode plein écran sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b649-113">If app start-up is impacted that it does not open as expected, then the user should still be able to switch to Tablet Mode to force the app to start in full-screen mode without user intervention.</span></span>

<span data-ttu-id="7b649-114">La meilleure façon de gérer cela consiste à modifier l’application pour qu’elle soit consciente du fait qu’elle peut être dimensionnée à des emplacements/hauteurs non monitorés (c’est-à-dire qu’elle n’a pas de table de hauteur/largeur codée en dur et qu’elle n’attende que celles-ci).</span><span class="sxs-lookup"><span data-stu-id="7b649-114">The best way to handle this is to change the app to be aware of the fact that it can be sized to non-monitor sized places/heights (i.e. don’t have a hardcoded table of height/widths and only expect those, or expect hardcoded ratios as well).</span></span> <span data-ttu-id="7b649-115">Les développeurs d’applications doivent s’attendre à ce que l’application soit redimensionnée, un autre message de redimensionnement peut se produire juste après la remise du message de redimensionnement actuel. par conséquent, si l’application démarre des animations pendant le redimensionnement, il est possible que l’application puisse recevoir un autre message de redimensionnement juste après (il est donc important de s’assurer que ce type de situation n’entraîne pas le blocage de l’application).</span><span class="sxs-lookup"><span data-stu-id="7b649-115">App developers should expect that as the app is being resized, that another resizing message can happen right after the current resize message gets delivered – as a result, if the app starts animations during resize, it’s possible that the app may receive another resize message right after (so it’s important to ensure that this type of situation doesn’t lead to the app crashing).</span></span>

 

 




