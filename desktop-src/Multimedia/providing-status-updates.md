---
title: Fourniture de mises à jour d’État
description: Fourniture de mises à jour d’État
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- MCIWndSetActiveTimer macro)
- MCIWndSetInactiveTimer macro)
- MCIWndGetActiveTimer macro)
- MCIWndGetInactiveTimer macro)
- MCIWndSetTimers macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd53c9580f3ae9be09817979178d10e60765ea3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379863"
---
# <a name="providing-status-updates"></a><span data-ttu-id="10fe9-108">Fourniture de mises à jour d’État</span><span class="sxs-lookup"><span data-stu-id="10fe9-108">Providing Status Updates</span></span>

<span data-ttu-id="10fe9-109">MCIWnd utilise des minuteries pour mettre régulièrement à jour les informations dans la barre de titre et la barre de défilement de la fenêtre, et pour envoyer des messages de notification à la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="10fe9-109">MCIWnd uses timers to periodically update information in the window title bar and scroll bar, and to send notification messages to the parent window.</span></span> <span data-ttu-id="10fe9-110">Une minuterie contrôle la période de mise à jour de la fenêtre active MCIWnd et une deuxième minuterie contrôle la période de mise à jour pour les fenêtres MCIWnd qui sont inactives.</span><span class="sxs-lookup"><span data-stu-id="10fe9-110">One timer controls the update period of the active MCIWnd window, and a second timer controls the update period for MCIWnd windows that are inactive.</span></span> <span data-ttu-id="10fe9-111">Votre application peut utiliser les macros du minuteur MCIWnd pour récupérer les paramètres du minuteur en cours et ajuster les périodes de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="10fe9-111">Your application can use the MCIWnd timer macros to retrieve the current timer settings and to adjust the update periods.</span></span>

<span data-ttu-id="10fe9-112">Vous pouvez définir la période de mise à jour utilisée par le minuteur de fenêtre active à l’aide de la macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="10fe9-112">You can set the update period used by the active window timer by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span> <span data-ttu-id="10fe9-113">Cette macro définit la période utilisée par MCIWnd pour mettre à jour la barre de suivi, pour mettre à jour la position de lecture indiquée dans la barre de titre de la fenêtre et pour informer la fenêtre parente que le média a changé.</span><span class="sxs-lookup"><span data-stu-id="10fe9-113">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window title bar, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="10fe9-114">Vous pouvez récupérer la période de mise à jour actuelle utilisée par le minuteur de fenêtre active à l’aide de la macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="10fe9-114">You can retrieve the current update period used by the active window timer by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span> <span data-ttu-id="10fe9-115">La période de mise à jour par défaut du minuteur de fenêtre active est de 500 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="10fe9-115">The default update period for the active window timer is 500 milliseconds.</span></span>

<span data-ttu-id="10fe9-116">Vous pouvez définir la période de mise à jour utilisée par le minuteur de fenêtre inactive à l’aide de la macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="10fe9-116">You can set the update period used by the inactive window timer by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span> <span data-ttu-id="10fe9-117">Cette macro définit la période utilisée par MCIWnd pour mettre à jour la barre de suivi, pour mettre à jour la position de lecture signalée dans le titre de la fenêtre et pour informer la fenêtre parent que le média a changé.</span><span class="sxs-lookup"><span data-stu-id="10fe9-117">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window caption, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="10fe9-118">Vous pouvez récupérer la période de mise à jour actuelle utilisée par le minuteur de fenêtre inactive à l’aide de la macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="10fe9-118">You can retrieve the current update period used by the inactive window timer by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span> <span data-ttu-id="10fe9-119">La période de mise à jour par défaut du minuteur de fenêtre inactive est de 2000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="10fe9-119">The default update period for the inactive window timer is 2000 milliseconds.</span></span>

<span data-ttu-id="10fe9-120">Votre application peut définir simultanément la période de mise à jour pour les deux minuteurs à l’aide de la macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .</span><span class="sxs-lookup"><span data-stu-id="10fe9-120">Your application can simultaneously set the update period for both timers by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span> <span data-ttu-id="10fe9-121">Le stockage de la valeur de la période de mise à jour est limité à 16 bits.</span><span class="sxs-lookup"><span data-stu-id="10fe9-121">The storage for the value of the update period is limited to 16 bits.</span></span> <span data-ttu-id="10fe9-122">Si vous avez besoin d’une quantité plus importante pour une période de mise à jour, définissez les minuteries individuellement.</span><span class="sxs-lookup"><span data-stu-id="10fe9-122">If a larger quantity for either update period is needed, set the timers individually.</span></span>

 

 




