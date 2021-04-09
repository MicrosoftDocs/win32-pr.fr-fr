---
title: Format audio
description: Format audio
ms.assetid: a65dbd3f-1539-4f02-8573-c527c4e3c58d
keywords:
- Message WM_CAP_GET_AUDIOFORMAT
- capGetAudioFormat macro)
- capGetAudioFormatSize macro)
- Message WM_CAP_SET_AUDIOFORMAT
- capSetAudioFormat macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e362abd393097ae8763b44b3ee3474685ffd5c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842146"
---
# <a name="audio-format"></a><span data-ttu-id="6769a-108">Format audio</span><span class="sxs-lookup"><span data-stu-id="6769a-108">Audio Format</span></span>

<span data-ttu-id="6769a-109">Vous pouvez récupérer le format de capture actuel pour les données audio ou la taille de la structure du format audio en envoyant le message [**WM \_ Cap \_ \_ AUDIOFORMAT**](wm-cap-get-audioformat.md) (ou les macros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) et [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) ) à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="6769a-109">You can retrieve the current capture format for audio data or the size of the audio format structure by sending the [**WM\_CAP\_GET\_AUDIOFORMAT**](wm-cap-get-audioformat.md) message (or the [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) and [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) macros) to a capture window.</span></span> <span data-ttu-id="6769a-110">Le format de capture audio par défaut est mono, binaire 8 bits, 11 kHz PCM (Pulse Code Modulation).</span><span class="sxs-lookup"><span data-stu-id="6769a-110">The default audio capture format is mono, 8-bit, 11 kHz PCM (Pulse Code Modulation).</span></span> <span data-ttu-id="6769a-111">Lorsque vous récupérez le format à l’aide de WM \_ Cap \_ obtenir \_ AUDIOFORMAT, utilisez toujours la structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) .</span><span class="sxs-lookup"><span data-stu-id="6769a-111">When you retrieve the format by using WM\_CAP\_GET\_AUDIOFORMAT, always use the [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure.</span></span>

<span data-ttu-id="6769a-112">Vous pouvez définir le format de capture pour les données audio en envoyant le message [**WM \_ Cap \_ Set \_ AUDIOFORMAT**](wm-cap-set-audioformat.md) (ou la macro [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) ) à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="6769a-112">You can set the capture format for audio data by sending the [**WM\_CAP\_SET\_AUDIOFORMAT**](wm-cap-set-audioformat.md) message (or the [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) macro) to a capture window.</span></span> <span data-ttu-id="6769a-113">Lorsque vous définissez le format audio, vous pouvez passer un pointeur vers une structure [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat), **WAVEFORMATEX** ou [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) , selon le format audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="6769a-113">When setting the audio format, you can pass a pointer to a [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat), **WAVEFORMATEX**, or [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) structure, depending on the specified audio format.</span></span>

 

 