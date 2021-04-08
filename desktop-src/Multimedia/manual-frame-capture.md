---
title: Capture manuelle des frames
description: Capture manuelle des frames
ms.assetid: 7c5576ff-2694-4f44-a386-03bbc6f9c2ed
keywords:
- Message WM_CAP_SINGLE_FRAME_OPEN
- Message WM_CAP_SINGLE_FRAME
- Message WM_CAP_SINGLE_FRAME_CLOSE
- capCaptureSingleFrameOpen macro)
- capCaptureSingleFrame macro)
- capCaptureSingleFrameClose macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26899032d8e81be437e8f29acf36f0a37703c560
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839750"
---
# <a name="manual-frame-capture"></a><span data-ttu-id="f864f-109">Capture manuelle des frames</span><span class="sxs-lookup"><span data-stu-id="f864f-109">Manual Frame Capture</span></span>

<span data-ttu-id="f864f-110">Si vous souhaitez spécifier individuellement les frames à capturer dans un flux vidéo, vous pouvez contrôler la séquence à l’aide des messages de l' [**\_ \_ image unique WM embout \_ \_ Open**](wm-cap-single-frame-open.md), du [**\_ \_ \_ cadre unique WM**](wm-cap-single-frame.md)et du [**\_ \_ \_ \_ cadre unique WM Cap**](wm-cap-single-frame-close.md) (ou des macros [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe)et [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) ).</span><span class="sxs-lookup"><span data-stu-id="f864f-110">If you want to individually specify the frames to capture in a video stream, you can control the sequence by using the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md), [**WM\_CAP\_SINGLE\_FRAME**](wm-cap-single-frame.md), and [**WM\_CAP\_SINGLE\_FRAME\_CLOSE**](wm-cap-single-frame-close.md) messages (or the [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe), and [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) macros).</span></span> <span data-ttu-id="f864f-111">En règle générale, ces messages sont utilisés pour créer une animation en ajoutant des frames individuels au fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="f864f-111">Typically, these messages are used to create animation by appending individual frames to the capture file.</span></span> <span data-ttu-id="f864f-112">Le \_ \_ cadre unique WM Cap \_ \_ Open ouvre un fichier pour une opération de capture pilotée manuellement.</span><span class="sxs-lookup"><span data-stu-id="f864f-112">WM\_CAP\_SINGLE\_FRAME\_OPEN opens a file for a manually driven capture operation.</span></span> <span data-ttu-id="f864f-113">\_ \_ Le frame WM embout unique \_ capture un frame individuel et l’ajoute au fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="f864f-113">WM\_CAP\_SINGLE\_FRAME captures an individual frame and appends it to the capture file.</span></span> <span data-ttu-id="f864f-114">\_ \_ \_ La fermeture de frame unique WM Cap \_ ferme le fichier utilisé pour la capture manuelle de frame.</span><span class="sxs-lookup"><span data-stu-id="f864f-114">WM\_CAP\_SINGLE\_FRAME\_CLOSE closes the file used for manual frame capture.</span></span>

> [!Note]  
> <span data-ttu-id="f864f-115">Cette méthode de capture ne prend pas en charge la capture audio simultanée avec capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="f864f-115">This capture method does not support simultaneous audio capture with video capture.</span></span>

 

 

 




