---
title: Taille d'index
description: Taille d'index
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cd9e59c23376a7aa201673ef71743c8a192b60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673922"
---
# <a name="index-size"></a><span data-ttu-id="c3142-107">Taille d'index</span><span class="sxs-lookup"><span data-stu-id="c3142-107">Index Size</span></span>

<span data-ttu-id="c3142-108">Chaque fichier AVI utilise un index d’une taille spécifiée pour localiser des blocs de données vidéo et audio dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="c3142-108">Each AVI file uses an index of a specified size to locate video and audio data chunks within the file.</span></span> <span data-ttu-id="c3142-109">Une entrée dans l’index localise une image vidéo ou un tampon Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="c3142-109">An entry in the index locates one video frame or waveform-audio buffer.</span></span> <span data-ttu-id="c3142-110">Par conséquent, la valeur de la taille de l’index définit indirectement la limite supérieure du nombre de trames qui peuvent être capturées dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="c3142-110">Consequently, the value of the index size indirectly sets the upper limit on the number of frames that can be captured in a file.</span></span>

<span data-ttu-id="c3142-111">Vous pouvez récupérer la taille actuelle de l’index à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’aide de WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="c3142-111">You can retrieve the current index size by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="c3142-112">La taille actuelle de l’index est stockée dans le membre **dwIndexSize** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="c3142-112">The current index size is stored in the **dwIndexSize** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="c3142-113">Vous pouvez spécifier une nouvelle taille d’index comme valeur de **dwIndexSize** , puis envoyer la structure **CAPTUREPARMS** mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="c3142-113">You can specify a new index size as the value of **dwIndexSize** and then send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="c3142-114">La taille de l’index par défaut est de 34 952 entrées (ce qui permet d’obtenir des trames de 32 Ko et un nombre proportionnel de mémoires tampons audio).</span><span class="sxs-lookup"><span data-stu-id="c3142-114">The default index size is 34,952 entries (allowing 32K frames and a proportional number of audio buffers).</span></span>

 

 




