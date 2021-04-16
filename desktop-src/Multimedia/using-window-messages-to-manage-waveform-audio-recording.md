---
title: Utilisation de messages de fenêtre pour gérer Waveform-Audio enregistrement
description: Utilisation de messages de fenêtre pour gérer Waveform-Audio enregistrement
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- audio Wave, gestion de l’enregistrement avec des messages
- Waveform-interface audio, gestion de l’enregistrement à l’aide de messages
- enregistrement de la forme d’onde audio, gestion de l’enregistrement avec les messages
- sons Waveform, messages
- Waveform-interface audio, messages
- enregistrement de la forme d’onde audio, messages
- Message MM_WIM_CLOSE
- Message MM_WIM_DATA
- Message MM_WIM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bb1cfe1ed0f7ba6052fc1eb6af8fca8355d87d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463003"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a><span data-ttu-id="a2891-112">Utilisation de messages de fenêtre pour gérer Waveform-Audio enregistrement</span><span class="sxs-lookup"><span data-stu-id="a2891-112">Using Window Messages to Manage Waveform-Audio Recording</span></span>

<span data-ttu-id="a2891-113">Les messages suivants peuvent être envoyés à une fonction de procédure de fenêtre pour la gestion de l’enregistrement Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="a2891-113">The following messages can be sent to a window procedure function for managing waveform-audio recording.</span></span>



| <span data-ttu-id="a2891-114">Message</span><span class="sxs-lookup"><span data-stu-id="a2891-114">Message</span></span>                                | <span data-ttu-id="a2891-115">Description</span><span class="sxs-lookup"><span data-stu-id="a2891-115">Description</span></span>                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2891-116">**\_fermeture de Wim de mm \_**</span><span class="sxs-lookup"><span data-stu-id="a2891-116">**MM\_WIM\_CLOSE**</span></span>](mm-wim-close.md) | <span data-ttu-id="a2891-117">Envoyé lorsque l’appareil est fermé à l’aide de la fonction [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) .</span><span class="sxs-lookup"><span data-stu-id="a2891-117">Sent when the device is closed by using the [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) function.</span></span>                                     |
| [<span data-ttu-id="a2891-118">**\_données Wim \_ mm**</span><span class="sxs-lookup"><span data-stu-id="a2891-118">**MM\_WIM\_DATA**</span></span>](mm-wim-data.md)   | <span data-ttu-id="a2891-119">Envoyé lorsque le pilote de périphérique est terminé avec une mémoire tampon envoyée à l’aide de la fonction [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) .</span><span class="sxs-lookup"><span data-stu-id="a2891-119">Sent when the device driver is finished with a buffer sent by using the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function.</span></span> |
| [<span data-ttu-id="a2891-120">**fichier \_ Wim \_ Open**</span><span class="sxs-lookup"><span data-stu-id="a2891-120">**MM\_WIM\_OPEN**</span></span>](mm-wim-open.md)   | <span data-ttu-id="a2891-121">Envoyé lorsque l’appareil est ouvert à l’aide de la fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) .</span><span class="sxs-lookup"><span data-stu-id="a2891-121">Sent when the device is opened by using the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function.</span></span>                                       |



 

<span data-ttu-id="a2891-122">Le paramètre *lParam* des [**\_ \_ données Wim mm**](mm-wim-data.md) spécifie un pointeur vers une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) qui identifie la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a2891-122">The *lParam* parameter of [**MM\_WIM\_DATA**](mm-wim-data.md) specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer.</span></span> <span data-ttu-id="a2891-123">Il se peut que cette mémoire tampon ne soit pas entièrement remplie avec des données Waveform-Audio ; l’enregistrement peut s’arrêter avant que la mémoire tampon ne soit remplie.</span><span class="sxs-lookup"><span data-stu-id="a2891-123">This buffer might not be completely filled with waveform-audio data; recording can stop before the buffer is filled.</span></span> <span data-ttu-id="a2891-124">Utilisez le membre **dwBytesRecorded** de la structure **WAVEHDR** pour déterminer la quantité de données valides présentes dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a2891-124">Use the **dwBytesRecorded** member of the **WAVEHDR** structure to determine the amount of valid data present in the buffer.</span></span>

<span data-ttu-id="a2891-125">Le message le plus utile est probablement de [**mm \_ \_ données Wim**](mm-wim-data.md).</span><span class="sxs-lookup"><span data-stu-id="a2891-125">The most useful message is probably [**MM\_WIM\_DATA**](mm-wim-data.md).</span></span> <span data-ttu-id="a2891-126">Lorsque votre application se termine à l’aide du bloc de données envoyé par le pilote de périphérique, vous pouvez nettoyer et libérer le bloc de données.</span><span class="sxs-lookup"><span data-stu-id="a2891-126">When your application finishes using the data block sent by the device driver, you can clean up and free the data block.</span></span> <span data-ttu-id="a2891-127">À moins que vous n’ayez besoin d’allouer de la mémoire ou d’initialiser des variables, vous n’avez probablement pas besoin d’utiliser les messages d' [**\_ \_ ouverture**](mm-wim-open.md) et de [**\_ \_ fermeture**](mm-wim-close.md) Wim de mm.</span><span class="sxs-lookup"><span data-stu-id="a2891-127">Unless you need to allocate memory or initialize variables, you probably do not need to use the [**MM\_WIM\_OPEN**](mm-wim-open.md) and [**MM\_WIM\_CLOSE**](mm-wim-close.md) messages.</span></span>

<span data-ttu-id="a2891-128">La fonction de rappel pour les périphériques d’entrée Waveform-Audio est fournie par l’application.</span><span class="sxs-lookup"><span data-stu-id="a2891-128">The callback function for waveform-audio input devices is supplied by the application.</span></span> <span data-ttu-id="a2891-129">Pour plus d’informations sur cette fonction de rappel, consultez la fonction [**waveInProc**](/previous-versions//dd743849(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a2891-129">For information about this callback function, see the [**waveInProc**](/previous-versions//dd743849(v=vs.85)) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2891-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2891-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2891-131">Enregistrement de la forme d’onde</span><span class="sxs-lookup"><span data-stu-id="a2891-131">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 