---
title: Définition de l’étendue de lecture
description: Définition de l’étendue de lecture
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- MCIWndPlayFrom macro)
- MCIWndPlayTo macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518fc80588147c4ccbbca619452b714333a8a34d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939937"
---
# <a name="defining-playback-scope"></a><span data-ttu-id="57cd3-105">Définition de l’étendue de lecture</span><span class="sxs-lookup"><span data-stu-id="57cd3-105">Defining Playback Scope</span></span>

<span data-ttu-id="57cd3-106">MCIWnd fournit des macros qui vous permettent de définir l' *étendue* de lecture.</span><span class="sxs-lookup"><span data-stu-id="57cd3-106">MCIWnd provides macros that allow you to define the playback *scope*.</span></span> <span data-ttu-id="57cd3-107">L’étendue correspond à la partie de la lecture que vous souhaitez lire.</span><span class="sxs-lookup"><span data-stu-id="57cd3-107">The scope is the portion of the playback you want to play.</span></span> <span data-ttu-id="57cd3-108">Par exemple, vous pouvez lire le contenu à partir d’une position autre que la position de début à l’aide de la macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .</span><span class="sxs-lookup"><span data-stu-id="57cd3-108">For example, you can play the content from a position other than the beginning position by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span> <span data-ttu-id="57cd3-109">Cette macro passe à la position spécifiée, commence la lecture et continue jusqu’à la fin du contenu.</span><span class="sxs-lookup"><span data-stu-id="57cd3-109">This macro moves to the specified position, begins playback, and continues to the end of the content.</span></span> <span data-ttu-id="57cd3-110">De même, vous pouvez lire le contenu à un point de terminaison spécifié à l’aide de la macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .</span><span class="sxs-lookup"><span data-stu-id="57cd3-110">Similarly, you can play the content to a specified end point by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span> <span data-ttu-id="57cd3-111">Cette macro démarre à la position de lecture actuelle et s’exécute jusqu’à ce qu’elle atteigne la position spécifiée ou que la fin du contenu soit atteinte, selon la première entrée.</span><span class="sxs-lookup"><span data-stu-id="57cd3-111">This macro starts at the current playback position and plays until it reaches the specified position or the end of the content is reached, whichever comes first.</span></span>

<span data-ttu-id="57cd3-112">En outre, vous pouvez définir à la fois les positions de début et de fin à l’aide de la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="57cd3-112">Also, you can define both the beginning and ending positions by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span> <span data-ttu-id="57cd3-113">Cette macro se déplace à la position de départ spécifiée et s’exécute jusqu’à ce que la position de fin spécifiée ou la fin du contenu soit atteinte.</span><span class="sxs-lookup"><span data-stu-id="57cd3-113">This macro moves to the specified starting position and plays until the specified ending position or the end of the content is reached.</span></span>

 

 




