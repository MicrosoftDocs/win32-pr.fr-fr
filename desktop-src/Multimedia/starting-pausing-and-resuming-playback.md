---
title: Démarrage, suspension et reprise de la lecture
description: Démarrage, suspension et reprise de la lecture
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- MCIWndPlay macro)
- MCIWndPause macro)
- MCIWndResume macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734a186b90b8d6701923d0ffa1f743cc8c5ae378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197402"
---
# <a name="starting-pausing-and-resuming-playback"></a><span data-ttu-id="f5654-106">Démarrage, suspension et reprise de la lecture</span><span class="sxs-lookup"><span data-stu-id="f5654-106">Starting, Pausing, and Resuming Playback</span></span>

<span data-ttu-id="f5654-107">[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) est la macro de lecture la plus générale.</span><span class="sxs-lookup"><span data-stu-id="f5654-107">[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) is the most general playback macro.</span></span> <span data-ttu-id="f5654-108">Cette macro vous permet de lire un fichier ou un appareil à partir de la position de lecture actuelle.</span><span class="sxs-lookup"><span data-stu-id="f5654-108">This macro lets you play a file or device from the current playback position.</span></span> <span data-ttu-id="f5654-109">La lecture continue jusqu’à la fin du contenu, sauf si elle est interrompue.</span><span class="sxs-lookup"><span data-stu-id="f5654-109">Playback continues through the end of the content unless it is interrupted.</span></span>

<span data-ttu-id="f5654-110">Vous pouvez interrompre temporairement un appareil qui est en train de fonctionner à l’aide de la macro [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) .</span><span class="sxs-lookup"><span data-stu-id="f5654-110">You can temporarily interrupt a device that is playing by using the [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) macro.</span></span> <span data-ttu-id="f5654-111">Pour reprendre la lecture à partir de la position suspendue, utilisez la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) .</span><span class="sxs-lookup"><span data-stu-id="f5654-111">To resume playback from the paused position, use the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro.</span></span> <span data-ttu-id="f5654-112">Certains appareils ne prennent pas en charge les commandes de suspension et de reprise.</span><span class="sxs-lookup"><span data-stu-id="f5654-112">Some devices do not support the pause and resume commands.</span></span> <span data-ttu-id="f5654-113">Ces appareils mappent généralement **MCIWndPause** à la macro [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) , qui arrête la lecture ou l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f5654-113">These devices usually map **MCIWndPause** to the [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) macro, which stops playback or recording.</span></span> <span data-ttu-id="f5654-114">Vous pouvez redémarrer un appareil qui ne prend pas en charge la suspension ou la reprise à l’aide de **MCIWndPlay**, qui démarre la lecture à partir de la position de lecture actuelle.</span><span class="sxs-lookup"><span data-stu-id="f5654-114">You can restart a device that does not support pause or resume by using **MCIWndPlay**, which starts playback from the current playback position.</span></span>

 

 




