---
description: Synchronisation de VMR avec la fréquence d’actualisation du moniteur
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: Synchronisation de VMR avec la fréquence d’actualisation du moniteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a9550e96e6a2e35c196048d38dd5b6e5b536d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210458"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a><span data-ttu-id="0df69-103">Synchronisation de VMR avec la fréquence d’actualisation du moniteur</span><span class="sxs-lookup"><span data-stu-id="0df69-103">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>

<span data-ttu-id="0df69-104">Dans de rares scénarios, vous souhaiterez peut-être synchroniser précisément le rendu vidéo avec la fréquence d’actualisation du moniteur, afin qu’un juste nouveau Frame soit présenté chaque fois que l’analyse est actualisée.</span><span class="sxs-lookup"><span data-stu-id="0df69-104">In rare scenarios, you may wish to precisely synchronize video rendering with the monitor's refresh rate, so that exactly one new frame is presented each time the monitor refreshes.</span></span> <span data-ttu-id="0df69-105">La méthode la plus fiable consiste à créer un Allocator-Presenter personnalisé qui utilise une opération de retournement au lieu d’une opération blit pour écrire les bits vidéo dans la surface principale.</span><span class="sxs-lookup"><span data-stu-id="0df69-105">The most reliable way to do this is to create a custom allocator-presenter that uses a flip operation instead of a blit operation to write the video bits into the primary surface.</span></span> <span data-ttu-id="0df69-106">« Flip » est appelé chaque fois que l’analyse est actualisée. par conséquent, si votre flux vidéo ne contient pas de datage, VMR est rendu aussi rapide que possible à la surface principale, mais la surface bloque le flux jusqu’à ce que l’opération de retournement soit terminée.</span><span class="sxs-lookup"><span data-stu-id="0df69-106">"Flip" is called each time the monitor refreshes, so if your video stream contains no time stamps, the VMR will render as fast as possible to the primary surface, but the surface will block the stream until the Flip operation completes.</span></span> <span data-ttu-id="0df69-107">Cela signifie que, tant que le processeur n’est pas surchargé, le frame suivant est toujours en attente dans la surface principale chaque fois que l’analyse est actualisée.</span><span class="sxs-lookup"><span data-stu-id="0df69-107">This means that, as long as the CPU is not overburdened, the next frame will always be waiting in the primary surface each time the monitor refreshes.</span></span> <span data-ttu-id="0df69-108">Toutefois, si un autre processus nécessitant beaucoup de ressources processeur est en cours d’exécution, il risque de priver votre thread de diffusion en continu DirectShow afin qu’il ne puisse pas remettre des images vidéo suffisamment rapidement à la surface principale.</span><span class="sxs-lookup"><span data-stu-id="0df69-108">However, if some other CPU-intensive process is running, it could possibly starve your DirectShow streaming thread so that it cannot deliver video frames fast enough to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0df69-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0df69-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0df69-110">Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)</span><span class="sxs-lookup"><span data-stu-id="0df69-110">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



