---
title: Inversion de la lecture
description: Inversion de la lecture
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- MCIWndPlayReverse macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379907"
---
# <a name="reversing-playback"></a><span data-ttu-id="c6f1b-104">Inversion de la lecture</span><span class="sxs-lookup"><span data-stu-id="c6f1b-104">Reversing Playback</span></span>

<span data-ttu-id="c6f1b-105">Certains appareils prennent en charge la lecture dans le sens inverse.</span><span class="sxs-lookup"><span data-stu-id="c6f1b-105">Some devices support playback in the reverse direction.</span></span> <span data-ttu-id="c6f1b-106">Vous pouvez lire le contenu d’un tel appareil dans le sens inverse à l’aide de la macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .</span><span class="sxs-lookup"><span data-stu-id="c6f1b-106">You can play the content of such a device in the reverse direction by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span> <span data-ttu-id="c6f1b-107">Cette macro définit l’étendue de lecture à partir de la position de lecture actuelle jusqu’au début du contenu.</span><span class="sxs-lookup"><span data-stu-id="c6f1b-107">This macro defines the playback scope from the current playback position to the beginning of the content.</span></span> <span data-ttu-id="c6f1b-108">Périphérique vidéo numérique, MCIAVI. DRV peut lire en arrière.</span><span class="sxs-lookup"><span data-stu-id="c6f1b-108">The digital-video device, MCIAVI.DRV, can play backward.</span></span> <span data-ttu-id="c6f1b-109">Les appareils qui ne peuvent pas jouer en arrière, tels que les CD audio, peuvent émettre un message d’erreur lorsque **MCIWndPlayReverse** est appelé.</span><span class="sxs-lookup"><span data-stu-id="c6f1b-109">Devices that cannot play backward, such as CD audio, can issue an error message when **MCIWndPlayReverse** is invoked.</span></span>

 

 




