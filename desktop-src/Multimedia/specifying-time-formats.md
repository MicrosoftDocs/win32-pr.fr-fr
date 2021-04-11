---
title: Spécification des formats d’heure
description: Spécification des formats d’heure
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- MCIWndGetTimeFormat macro)
- MCIWndSetTimeFormat macro)
- MCIWndUseTime macro)
- MCIWndUseFrames macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e390e811bde4d797572c19f372923906f6b738b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310070"
---
# <a name="specifying-time-formats"></a><span data-ttu-id="4b3da-107">Spécification des formats d’heure</span><span class="sxs-lookup"><span data-stu-id="4b3da-107">Specifying Time Formats</span></span>

<span data-ttu-id="4b3da-108">Les types de données multimédias peuvent généralement utiliser le temps pour identifier des positions importantes dans leur contenu.</span><span class="sxs-lookup"><span data-stu-id="4b3da-108">Multimedia data types typically can use time to identify significant positions within their content.</span></span> <span data-ttu-id="4b3da-109">Les formats d’heure courants sont les millisecondes, les pistes et les frames. d’autres formats d’heure moins courants, tels que SMPTE (la société de motion et les ingénieurs de télévision) 24, existent également.</span><span class="sxs-lookup"><span data-stu-id="4b3da-109">Common time formats are milliseconds, tracks, and frames; other less common time formats, such as SMPTE (Society of Motion Picture and Television Engineers) 24, also exist.</span></span> <span data-ttu-id="4b3da-110">L’heure correspond au format et au système de référence pour les données audio Waveform, audio, MIDI et CD.</span><span class="sxs-lookup"><span data-stu-id="4b3da-110">Time is the format and reference system for waveform-audio, MIDI, and CD audio data.</span></span> <span data-ttu-id="4b3da-111">La vidéo prend en charge l’heure même si elle est enregistrée sous la forme d’une séquence de trames (flux) qui est généralement jouée à une vitesse spécifique.</span><span class="sxs-lookup"><span data-stu-id="4b3da-111">Video supports time even though it is recorded as a sequence of frames (stream) that is typically played at a specific speed.</span></span> <span data-ttu-id="4b3da-112">Plusieurs macros sont disponibles pour désigner le format d’heure.</span><span class="sxs-lookup"><span data-stu-id="4b3da-112">Several macros are available for designating time format.</span></span>

<span data-ttu-id="4b3da-113">Vous pouvez récupérer le format d’heure actuel d’un fichier ou d’un périphérique à l’aide de la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="4b3da-113">You can retrieve the current time format for a file or device by using the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span> <span data-ttu-id="4b3da-114">Vous pouvez modifier le format d’heure actuel en utilisant un autre format d’heure pris en charge par un appareil à l’aide de la macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="4b3da-114">You can change the current time format to any other time format supported by a device by using the [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) macro.</span></span> <span data-ttu-id="4b3da-115">Ou vous pouvez définir le format d’heure sur millisecondes ou frames à l’aide des macros [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) ou [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) .</span><span class="sxs-lookup"><span data-stu-id="4b3da-115">Or you can the set the time format to milliseconds or frames by using the [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) or [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) macros.</span></span>

> [!Note]  
> <span data-ttu-id="4b3da-116">Les formats incontinus, tels que Tracks et SMPTE, peuvent entraîner un comportement anormal de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="4b3da-116">Noncontinuous formats, such as tracks and SMPTE, can cause the toolbar to behave erratically.</span></span> <span data-ttu-id="4b3da-117">Pour ces formats d’heure, vous souhaiterez peut-être désactiver la barre d’outils en spécifiant le \_ style de fenêtre MCIWNDF NOPLAYBAR lors de la création d’une fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="4b3da-117">For these time formats, you might want to turn off the toolbar by specifying the MCIWNDF\_NOPLAYBAR window style when creating an MCIWnd window.</span></span>

 

 

 




