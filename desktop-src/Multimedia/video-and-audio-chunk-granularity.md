---
title: Granularité des blocs vidéo et audio
description: Granularité des blocs vidéo et audio
ms.assetid: 02c94de7-c7cb-4150-8b3e-0542d317c19b
keywords:
- Fichiers AVI, granularité des blocs
- AVICap, classe, blocs de remplissage
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2245b133fbf14bfd6403fa2f3d7e02ed328de6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940079"
---
# <a name="video-and-audio-chunk-granularity"></a><span data-ttu-id="4be70-109">Granularité des blocs vidéo et audio</span><span class="sxs-lookup"><span data-stu-id="4be70-109">Video and Audio Chunk Granularity</span></span>

<span data-ttu-id="4be70-110">La granularité du segment est une taille de bloc logique pour un fichier AVI utilisé pour l’écriture et la récupération des blocs de données audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="4be70-110">The chunk granularity is a logical block size for an AVI file that is used for writing and retrieving audio and video data chunks.</span></span> <span data-ttu-id="4be70-111">Lors de l’écriture de blocs audio et vidéo sur disque, AVICap ajoute des blocs de remplissage (segments RIFF « indésirables ») si nécessaire pour remplir chaque bloc logique de données.</span><span class="sxs-lookup"><span data-stu-id="4be70-111">When writing audio and video chunks to disk, AVICap adds filler chunks (RIFF "JUNK" chunks) as necessary to fill each logical block of data.</span></span>

<span data-ttu-id="4be70-112">Vous pouvez récupérer le paramètre de granularité de segment actuel à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’aide de WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="4be70-112">You can retrieve the current chunk granularity setting by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="4be70-113">La granularité du bloc actuel est stockée dans le membre **wChunkGranularity** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="4be70-113">The current chunk granularity is stored in the **wChunkGranularity** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="4be70-114">Vous pouvez spécifier une nouvelle granularité de bloc en tant que valeur de **wChunkGranularity** , puis envoyer la structure **CAPTUREPARMS** mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="4be70-114">You can specify a new chunk granularity as the value of **wChunkGranularity** and then send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="4be70-115">Vous pouvez également spécifier zéro pour ce membre afin de définir la granularité du segment sur la taille de secteur du disque.</span><span class="sxs-lookup"><span data-stu-id="4be70-115">You can also specify zero for this member to set the chunk granularity to the sector size of the disk.</span></span>

 

 




