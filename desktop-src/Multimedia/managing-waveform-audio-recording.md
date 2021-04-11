---
title: Gestion de l’enregistrement Waveform-Audio
description: Gestion de l’enregistrement Waveform-Audio
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- audio Wave, enregistrement
- Waveform-interface audio, enregistrement
- enregistrement de la forme d’onde audio, à propos de
- WAVEHDR, structure
- waveInAddBuffer fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314772"
---
# <a name="managing-waveform-audio-recording"></a><span data-ttu-id="8ba5f-108">Gestion de l’enregistrement Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="8ba5f-108">Managing Waveform-Audio Recording</span></span>

<span data-ttu-id="8ba5f-109">Après avoir ouvert un périphérique d’entrée Waveform-Audio, vous pouvez commencer à enregistrer des données Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-109">After you open a waveform-audio input device, you can begin recording waveform-audio data.</span></span> <span data-ttu-id="8ba5f-110">Les données Waveform-Audio sont enregistrées dans des mémoires tampons fournies par l’application spécifiées par une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) .</span><span class="sxs-lookup"><span data-stu-id="8ba5f-110">Waveform-audio data is recorded into application-supplied buffers specified by a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure.</span></span> <span data-ttu-id="8ba5f-111">Ces blocs de données doivent être préparés avant d’être utilisés ; Pour plus d’informations, consultez [blocs de données audio](audio-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="8ba5f-111">These data blocks must be prepared before they are used; for more information, see [Audio Data Blocks](audio-data-blocks.md).</span></span>

<span data-ttu-id="8ba5f-112">Windows fournit les fonctions suivantes pour gérer l’enregistrement Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-112">Windows provides the following functions to manage waveform-audio recording.</span></span>



| <span data-ttu-id="8ba5f-113">Fonction</span><span class="sxs-lookup"><span data-stu-id="8ba5f-113">Function</span></span>                                   | <span data-ttu-id="8ba5f-114">Description</span><span class="sxs-lookup"><span data-stu-id="8ba5f-114">Description</span></span>                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ba5f-115">**waveInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="8ba5f-115">**waveInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | <span data-ttu-id="8ba5f-116">Envoie une mémoire tampon au pilote de périphérique pour qu’elle puisse être remplie avec des données Waveform-audio enregistrées.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-116">Sends a buffer to the device driver so it can be filled with recorded waveform-audio data.</span></span> |
| [<span data-ttu-id="8ba5f-117">**waveInReset**</span><span class="sxs-lookup"><span data-stu-id="8ba5f-117">**waveInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | <span data-ttu-id="8ba5f-118">Arrête l’enregistrement Waveform-Audio et marque toutes les mémoires tampons en attente comme terminées.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-118">Stops waveform-audio recording and marks all pending buffers as done.</span></span>                      |
| [<span data-ttu-id="8ba5f-119">**waveInStart**</span><span class="sxs-lookup"><span data-stu-id="8ba5f-119">**waveInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | <span data-ttu-id="8ba5f-120">Démarre l’enregistrement Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-120">Starts waveform-audio recording.</span></span>                                                           |
| [<span data-ttu-id="8ba5f-121">**waveInStop**</span><span class="sxs-lookup"><span data-stu-id="8ba5f-121">**waveInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | <span data-ttu-id="8ba5f-122">Arrête l’enregistrement Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-122">Stops waveform-audio recording.</span></span>                                                            |



 

<span data-ttu-id="8ba5f-123">Utilisez la fonction [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) pour envoyer des tampons au pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-123">Use the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function to send buffers to the device driver.</span></span> <span data-ttu-id="8ba5f-124">Étant donné que les tampons sont remplis avec des données Waveform-audio enregistrées, l’application est avertie par un message de fenêtre, un message de rappel, un message de thread ou un événement, en fonction de l’indicateur spécifié lors de l’ouverture de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-124">As the buffers are filled with recorded waveform-audio data, the application is notified with a window message, callback message, thread message, or event, depending on the flag specified when the device was opened.</span></span>

<span data-ttu-id="8ba5f-125">Avant de commencer l’enregistrement à l’aide de [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), vous devez envoyer au moins une mémoire tampon au pilote, ou les données entrantes peuvent être perdues.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-125">Before you begin recording by using [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), you should send at least one buffer to the driver, or incoming data could be lost.</span></span>

<span data-ttu-id="8ba5f-126">Avant de fermer l’appareil à l’aide de [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), appelez [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) pour marquer tous les blocs de données en attente comme étant terminés.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-126">Before closing the device using [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), call [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) to mark any pending data blocks as being done.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ba5f-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ba5f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ba5f-128">Enregistrement de la forme d’onde</span><span class="sxs-lookup"><span data-stu-id="8ba5f-128">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 