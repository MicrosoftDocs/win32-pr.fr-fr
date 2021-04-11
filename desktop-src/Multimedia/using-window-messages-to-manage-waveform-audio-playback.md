---
title: Utilisation de messages de fenêtre pour gérer Waveform-Audio lecture
description: Utilisation de messages de fenêtre pour gérer Waveform-Audio lecture
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- sons Waveform, gestion de la lecture avec les messages
- Waveform-interface audio, gestion de la lecture avec des messages
- lecture de fichiers Waveform-Audio, gestion de la lecture avec des messages
- sons Waveform, messages
- Waveform-interface audio, messages
- lecture des fichiers Waveform-Audio, messages
- Message MM_WOM_CLOSE
- Message MM_WOM_DONE
- Message MM_WOM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02794222274e10498e31e0f38939d930ef3745
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314855"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a><span data-ttu-id="20daa-112">Utilisation de messages de fenêtre pour gérer Waveform-Audio lecture</span><span class="sxs-lookup"><span data-stu-id="20daa-112">Using Window Messages to Manage Waveform-Audio Playback</span></span>

<span data-ttu-id="20daa-113">Les messages suivants peuvent être envoyés à une fonction de procédure de fenêtre pour la gestion de la lecture Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="20daa-113">The following messages can be sent to a window procedure function for managing waveform-audio playback.</span></span>



| <span data-ttu-id="20daa-114">Message</span><span class="sxs-lookup"><span data-stu-id="20daa-114">Message</span></span>                                | <span data-ttu-id="20daa-115">Description</span><span class="sxs-lookup"><span data-stu-id="20daa-115">Description</span></span>                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20daa-116">**MM \_ WOM \_ Fermer**</span><span class="sxs-lookup"><span data-stu-id="20daa-116">**MM\_WOM\_CLOSE**</span></span>](mm-wom-close.md) | <span data-ttu-id="20daa-117">Envoyé lorsque l’appareil est fermé à l’aide de la fonction [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) .</span><span class="sxs-lookup"><span data-stu-id="20daa-117">Sent when the device is closed by using the [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) function.</span></span>                                 |
| [<span data-ttu-id="20daa-118">**MM \_ WOM \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="20daa-118">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)   | <span data-ttu-id="20daa-119">Envoyé lorsque le pilote de périphérique est terminé avec un bloc de données envoyé à l’aide de la fonction [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) .</span><span class="sxs-lookup"><span data-stu-id="20daa-119">Sent when the device driver is finished with a data block sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> |
| [<span data-ttu-id="20daa-120">**MM \_ WOM \_ ouverts**</span><span class="sxs-lookup"><span data-stu-id="20daa-120">**MM\_WOM\_OPEN**</span></span>](mm-wom-open.md)   | <span data-ttu-id="20daa-121">Envoyé lorsque l’appareil est ouvert à l’aide de la fonction [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="20daa-121">Sent when the device is opened by using the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>                                   |



 

<span data-ttu-id="20daa-122">Un paramètre *wParam* et *lParam* est associé à chacun de ces messages.</span><span class="sxs-lookup"><span data-stu-id="20daa-122">A *wParam* and *lParam* parameter is associated with each of these messages.</span></span> <span data-ttu-id="20daa-123">Le paramètre *wParam* spécifie toujours un handle du périphérique Wave-Audio ouvert.</span><span class="sxs-lookup"><span data-stu-id="20daa-123">The *wParam* parameter always specifies a handle of the open waveform-audio device.</span></span> <span data-ttu-id="20daa-124">Pour le message [**mm \_ WOM \_ done**](mm-wom-done.md) , *lParam* spécifie un pointeur vers une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) qui identifie le bloc de données terminé.</span><span class="sxs-lookup"><span data-stu-id="20daa-124">For the [**MM\_WOM\_DONE**](mm-wom-done.md) message, *lParam* specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the completed data block.</span></span> <span data-ttu-id="20daa-125">Le paramètre *lParam* n’est pas utilisé pour les messages Open [**\_ WOM \_ Fermer**](mm-wom-close.md) et [**mm \_ WOM \_ Open**](mm-wom-open.md) .</span><span class="sxs-lookup"><span data-stu-id="20daa-125">The *lParam* parameter is unused for the [**MM\_WOM\_CLOSE**](mm-wom-close.md) and [**MM\_WOM\_OPEN**](mm-wom-open.md) messages.</span></span>

<span data-ttu-id="20daa-126">Le message le plus utile est probablement de MM \_ WOM \_ .</span><span class="sxs-lookup"><span data-stu-id="20daa-126">The most useful message is probably MM\_WOM\_DONE.</span></span> <span data-ttu-id="20daa-127">Lorsque ce message signale que la lecture d’un bloc de données est terminée, vous pouvez nettoyer et libérer le bloc de données.</span><span class="sxs-lookup"><span data-stu-id="20daa-127">When this message signals that playback of a data block is complete, you can clean up and free the data block.</span></span> <span data-ttu-id="20daa-128">À moins que vous n’ayez besoin d’allouer de la mémoire ou d’initialiser des variables, vous n’avez probablement pas besoin de traiter les \_ \_ messages WOM Open et mm \_ WOM \_ Close.</span><span class="sxs-lookup"><span data-stu-id="20daa-128">Unless you need to allocate memory or initialize variables, you probably do not need to process the MM\_WOM\_OPEN and MM\_WOM\_CLOSE messages.</span></span>

<span data-ttu-id="20daa-129">La fonction de rappel pour les périphériques de sortie Waveform-Audio est fournie par l’application.</span><span class="sxs-lookup"><span data-stu-id="20daa-129">The callback function for waveform-audio output devices is supplied by the application.</span></span> <span data-ttu-id="20daa-130">Pour plus d’informations sur cette fonction de rappel, consultez la fonction [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="20daa-130">For information about this callback function, see the [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) function.</span></span>

 

 