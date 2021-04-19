---
title: Lecture en boucle pour MCIWnd
description: Lecture en boucle (MCIWnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d6a22e917cf764b37444bcaf4afb0393e1c1b
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106530067"
---
# <a name="looping-playback-for-mciwnd"></a><span data-ttu-id="14aac-103">Lecture en boucle pour MCIWnd</span><span class="sxs-lookup"><span data-stu-id="14aac-103">Looping Playback for MCIWnd</span></span>

<span data-ttu-id="14aac-104">MCIWnd prend en charge la lecture comme une boucle continue.</span><span class="sxs-lookup"><span data-stu-id="14aac-104">MCIWnd supports playback as a continuous loop.</span></span> <span data-ttu-id="14aac-105">Vous pouvez lire le contenu d’un fichier ou d’un appareil de façon répétée en tant que boucle à l’aide de la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) en combinaison avec le bouton de **lecture** dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="14aac-105">You can play the content of a file or device repeatedly as a loop by using the [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) macro in combination with the **Play** button on the toolbar.</span></span> <span data-ttu-id="14aac-106">L’appareil de lecture vidéo, MCIAVI, prend en charge les boucles de lecture.</span><span class="sxs-lookup"><span data-stu-id="14aac-106">The video playback device, MCIAVI, supports playback loops.</span></span> <span data-ttu-id="14aac-107">Pour déterminer si la lecture continue a été activée, utilisez la macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="14aac-107">To determine if continuous playback has been activated, use the [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) macro.</span></span>

 

 




