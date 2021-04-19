---
title: Capturer sans utiliser Stockage sur disque
description: Capturer sans utiliser Stockage sur disque
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- Message WM_CAP_SEQUENCE_NOFILE
- capCaptureSequenceNoFile macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508970"
---
# <a name="capture-without-using-disk-storage"></a><span data-ttu-id="121df-105">Capturer sans utiliser Stockage sur disque</span><span class="sxs-lookup"><span data-stu-id="121df-105">Capture Without Using Disk Storage</span></span>

<span data-ttu-id="121df-106">Vous pouvez utiliser les services de capture sans écrire les données dans un fichier de disque à l’aide du message de [**\_ \_ séquence \_**](wm-cap-sequence-nofile.md) de la limite WM (ou de la macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) ).</span><span class="sxs-lookup"><span data-stu-id="121df-106">You can use capture services without writing the data to a disk file by using the [**WM\_CAP\_SEQUENCE\_NOFILE**](wm-cap-sequence-nofile.md) message (or the [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) macro).</span></span> <span data-ttu-id="121df-107">Ce message est utile uniquement avec les fonctions de rappel qui permettent à votre application d’utiliser directement les données vidéo et audio.</span><span class="sxs-lookup"><span data-stu-id="121df-107">This message is useful only in conjunction with callback functions that allow your application to use the video and audio data directly.</span></span> <span data-ttu-id="121df-108">Par exemple, les applications de visioconférence peuvent utiliser ce message pour obtenir des images vidéo en streaming.</span><span class="sxs-lookup"><span data-stu-id="121df-108">For example, videoconferencing applications might use this message to obtain streaming video frames.</span></span> <span data-ttu-id="121df-109">Les fonctions de rappel transfèrent les images capturées à l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="121df-109">The callback functions would transfer the captured images to the remote computer.</span></span>

 

 




