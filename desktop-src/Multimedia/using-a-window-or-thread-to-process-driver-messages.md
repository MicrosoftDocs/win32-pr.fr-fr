---
title: Utilisation d’une fenêtre ou d’un thread pour traiter des messages de pilote
description: Utilisation d’une fenêtre ou d’un thread pour traiter des messages de pilote
ms.assetid: 7a9eaaa1-d3b0-400e-8fbf-ee5fe59efc32
keywords:
- audio Wave, rappel de fenêtre
- blocs de données audio, rappel de fenêtre
- audio Wave, rappel de thread
- blocs de données audio, rappel de thread
- audio Wave, traitement des messages de pilote
- blocs de données audio, traitement des messages de pilote
- traitement des messages du pilote
- waveInOpen fonction)
- waveOutOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a147bd86b3c8045456ef9961039f645fd4023f13
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940985"
---
# <a name="using-a-window-or-thread-to-process-driver-messages"></a><span data-ttu-id="3e7fb-112">Utilisation d’une fenêtre ou d’un thread pour traiter des messages de pilote</span><span class="sxs-lookup"><span data-stu-id="3e7fb-112">Using a Window or Thread to Process Driver Messages</span></span>

<span data-ttu-id="3e7fb-113">Pour utiliser une fonction de rappel de fenêtre, spécifiez l' \_ indicateur de fenêtre de rappel dans le paramètre *fdwOpen* et un handle de fenêtre dans le mot de poids faible du paramètre *DwCallback* de la fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) ou [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="3e7fb-113">To use a window callback function, specify the CALLBACK\_WINDOW flag in the *fdwOpen* parameter and a window handle in the low-order word of the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span> <span data-ttu-id="3e7fb-114">Les messages du pilote seront envoyés à la procédure de fenêtre pour la fenêtre identifiée par le descripteur dans *dwCallback*.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-114">Driver messages will be sent to the window procedure for the window identified by the handle in *dwCallback*.</span></span>

<span data-ttu-id="3e7fb-115">De même, pour utiliser un rappel de thread, spécifiez \_ le thread de rappel et un handle de thread dans l’appel à **WaveInOpen** ou **waveOutOpen**.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-115">Similarly, to use a thread callback, specify CALLBACK\_THREAD and a thread handle in the call to **waveInOpen** or **waveOutOpen**.</span></span> <span data-ttu-id="3e7fb-116">Dans ce cas, les messages sont publiés dans le thread spécifié et non dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-116">In this case, messages are posted to the specified thread instead of to a window.</span></span>

<span data-ttu-id="3e7fb-117">Les messages envoyés au rappel de la fenêtre ou du thread sont spécifiques au type de périphérique audio utilisé.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-117">Messages sent to the window or thread callback are specific to the audio device type used.</span></span> <span data-ttu-id="3e7fb-118">Pour plus d’informations sur ces messages, consultez [playing Waveform-Audio Files](playing-waveform-audio-files.md).</span><span class="sxs-lookup"><span data-stu-id="3e7fb-118">For more information about these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

 

 