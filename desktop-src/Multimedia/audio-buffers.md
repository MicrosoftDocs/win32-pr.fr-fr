---
title: Mémoires tampons audio
description: Mémoires tampons audio
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a67f120dc2d2ff956148e5dd4e3992a960641d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672318"
---
# <a name="audio-buffers"></a><span data-ttu-id="352ac-107">Mémoires tampons audio</span><span class="sxs-lookup"><span data-stu-id="352ac-107">Audio Buffers</span></span>

<span data-ttu-id="352ac-108">Vous pouvez contrôler la partie audio d’une opération de capture de trois manières :</span><span class="sxs-lookup"><span data-stu-id="352ac-108">You can control the audio portion of a capture operation in three ways:</span></span>

-   <span data-ttu-id="352ac-109">Incluez ou excluez l’audio de l’opération de capture.</span><span class="sxs-lookup"><span data-stu-id="352ac-109">Include or exclude audio from the capture operation.</span></span>
-   <span data-ttu-id="352ac-110">Demander un nombre spécifique de mémoires tampons audio.</span><span class="sxs-lookup"><span data-stu-id="352ac-110">Request a specific number of audio buffers.</span></span>
-   <span data-ttu-id="352ac-111">Demandez que les tampons audio soient d’une taille spécifique.</span><span class="sxs-lookup"><span data-stu-id="352ac-111">Request that audio buffers be a specific size.</span></span>

<span data-ttu-id="352ac-112">Vous pouvez récupérer les paramètres des mémoires tampons audio à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’extrémité de l’opération WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="352ac-112">You can retrieve the settings for audio buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="352ac-113">Le membre **fCaptureAudio** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) spécifie si l’audio est inclus ou exclu de l’opération de capture.</span><span class="sxs-lookup"><span data-stu-id="352ac-113">The **fCaptureAudio** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure specifies whether audio is included or excluded from the capture operation.</span></span> <span data-ttu-id="352ac-114">Le nombre demandé actuel de mémoires tampons audio est stocké dans le membre **wNumAudioRequested** et la taille de la mémoire tampon audio actuelle est stockée dans le membre **dwAudioBufferSize** .</span><span class="sxs-lookup"><span data-stu-id="352ac-114">The current requested number of audio buffers is stored in the **wNumAudioRequested** member, and the current audio buffer size is stored in the **dwAudioBufferSize** member.</span></span> <span data-ttu-id="352ac-115">Vous pouvez spécifier s’il faut inclure la capture audio, spécifier la taille et le nombre de mémoires tampons audio en mettant à jour ces membres, puis envoyer la structure **CAPTUREPARMS** mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="352ac-115">You can specify whether to include audio capture, specify the size and number of audio buffers by updating these members, and send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

<span data-ttu-id="352ac-116">Par défaut, l’audio est inclus dans l’opération de capture et les quatre mémoires tampons audio sont allouées.</span><span class="sxs-lookup"><span data-stu-id="352ac-116">By default, audio is included in the capture operation, and four audio buffers are allocated.</span></span> <span data-ttu-id="352ac-117">La valeur par défaut de **fCaptureAudio** est **true**.</span><span class="sxs-lookup"><span data-stu-id="352ac-117">The default value of **fCaptureAudio** is **TRUE**.</span></span> <span data-ttu-id="352ac-118">La taille de la mémoire tampon par défaut (la valeur de **dwAudioBufferSize**) peut contenir 0,5 secondes de données audio ou 10 Ko, la valeur la plus élevée étant retenue.</span><span class="sxs-lookup"><span data-stu-id="352ac-118">The default buffer size (the value of **dwAudioBufferSize**) can contain 0.5 seconds of audio data or 10K, whichever is greater.</span></span>

 

 




