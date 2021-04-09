---
title: Blocs de données audio
description: Blocs de données audio
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- audio multimédia, blocs de données
- audio, blocs de données
- audio Waveform, blocs de données
- blocs de données audio, à propos de
- WAVEHDR, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a81a5a29ec9718e7c11306b6bafc1aa20369e5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940877"
---
# <a name="audio-data-blocks"></a><span data-ttu-id="68c7f-108">Blocs de données audio</span><span class="sxs-lookup"><span data-stu-id="68c7f-108">Audio Data Blocks</span></span>

<span data-ttu-id="68c7f-109">Les fonctions [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) et [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) requièrent que les applications allouent des blocs de données à transmettre aux pilotes de périphérique à des fins d’enregistrement ou de lecture.</span><span class="sxs-lookup"><span data-stu-id="68c7f-109">The [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) and [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) functions require applications to allocate data blocks to pass to the device drivers for recording or playback purposes.</span></span> <span data-ttu-id="68c7f-110">Ces deux fonctions utilisent la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) pour décrire son bloc de données.</span><span class="sxs-lookup"><span data-stu-id="68c7f-110">Both of these functions use the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to describe its data block.</span></span>

<span data-ttu-id="68c7f-111">Avant d’utiliser l’une de ces fonctions pour passer un bloc de données à un pilote de périphérique, vous devez allouer de la mémoire pour le bloc de données et la structure d’en-tête qui décrit le bloc de données.</span><span class="sxs-lookup"><span data-stu-id="68c7f-111">Before using one of these functions to pass a data block to a device driver, you must allocate memory for the data block and the header structure that describes the data block.</span></span> <span data-ttu-id="68c7f-112">Les en-têtes peuvent être préparés et déspréparés à l’aide des fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="68c7f-112">The headers can be prepared and unprepared by using the following functions.</span></span>



| <span data-ttu-id="68c7f-113">Fonction</span><span class="sxs-lookup"><span data-stu-id="68c7f-113">Function</span></span>                                                 | <span data-ttu-id="68c7f-114">Description</span><span class="sxs-lookup"><span data-stu-id="68c7f-114">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="68c7f-115">**waveInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="68c7f-115">**waveInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | <span data-ttu-id="68c7f-116">Prépare un bloc de données d’entrée Waveform Audio.</span><span class="sxs-lookup"><span data-stu-id="68c7f-116">Prepares a waveform-audio input data block.</span></span>                      |
| [<span data-ttu-id="68c7f-117">**waveInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="68c7f-117">**waveInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | <span data-ttu-id="68c7f-118">Nettoie la préparation sur un bloc de données d’entrée Waveform Audio.</span><span class="sxs-lookup"><span data-stu-id="68c7f-118">Cleans up the preparation on a waveform-audio input data block.</span></span>  |
| [<span data-ttu-id="68c7f-119">**waveOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="68c7f-119">**waveOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | <span data-ttu-id="68c7f-120">Prépare un bloc de données de sortie Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="68c7f-120">Prepares a waveform-audio output data block.</span></span>                     |
| [<span data-ttu-id="68c7f-121">**waveOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="68c7f-121">**waveOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | <span data-ttu-id="68c7f-122">Nettoie la préparation sur un bloc de données de sortie Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="68c7f-122">Cleans up the preparation on a waveform-audio output data block.</span></span> |



 

<span data-ttu-id="68c7f-123">Avant de passer un bloc de données audio à un pilote de périphérique, vous devez préparer le bloc de données en le transmettant à [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) ou [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader).</span><span class="sxs-lookup"><span data-stu-id="68c7f-123">Before you pass an audio data block to a device driver, you must prepare the data block by passing it to either [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) or [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader).</span></span> <span data-ttu-id="68c7f-124">Lorsque le pilote de périphérique est terminé avec le bloc de données et le retourne, vous devez nettoyer cette préparation en passant le bloc de données à [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) ou [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) avant que toute mémoire allouée puisse être libérée.</span><span class="sxs-lookup"><span data-stu-id="68c7f-124">When the device driver is finished with the data block and returns it, you must clean up this preparation by passing the data block to either [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) or [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) before any allocated memory can be freed.</span></span>

<span data-ttu-id="68c7f-125">Sauf si les données d’entrée et de sortie Waveform-Audio sont suffisamment petites pour être contenues dans un bloc de données unique, les applications doivent fournir continuellement le pilote de périphérique avec des blocs de données jusqu’à la fin de la lecture ou de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="68c7f-125">Unless the waveform-audio input and output data is small enough to be contained in a single data block, applications must continually supply the device driver with data blocks until playback or recording is complete.</span></span>

<span data-ttu-id="68c7f-126">Même si un bloc de données unique est utilisé, une application doit être en mesure de déterminer à quel moment un pilote de périphérique est terminé avec le bloc de données pour que l’application puisse libérer la mémoire associée au bloc de données et à la structure d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="68c7f-126">Even if a single data block is used, an application must be able to determine when a device driver is finished with the data block so the application can free the memory associated with the data block and header structure.</span></span> <span data-ttu-id="68c7f-127">Il existe plusieurs façons de déterminer quand un pilote de périphérique est terminé avec un bloc de données :</span><span class="sxs-lookup"><span data-stu-id="68c7f-127">There are several ways to determine when a device driver is finished with a data block:</span></span>

-   <span data-ttu-id="68c7f-128">En spécifiant une fonction de rappel pour recevoir un message envoyé par le pilote lorsqu’il se termine par un bloc de données</span><span class="sxs-lookup"><span data-stu-id="68c7f-128">By specifying a callback function to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="68c7f-129">À l’aide d’un rappel d’événement</span><span class="sxs-lookup"><span data-stu-id="68c7f-129">By using an event callback</span></span>
-   <span data-ttu-id="68c7f-130">En spécifiant une fenêtre ou un thread pour recevoir un message envoyé par le pilote lorsqu’il se termine avec un bloc de données</span><span class="sxs-lookup"><span data-stu-id="68c7f-130">By specifying a window or thread to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="68c7f-131">En interrogeant le \_ bit WHDR Done dans le membre **dwFlags** de la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) envoyée avec chaque bloc de données</span><span class="sxs-lookup"><span data-stu-id="68c7f-131">By polling the WHDR\_DONE bit in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure sent with each data block</span></span>

<span data-ttu-id="68c7f-132">Si une application n’obtient pas de bloc de données au pilote de périphérique si nécessaire, il peut y avoir un décalage audible en lecture ou une perte d’informations enregistrées.</span><span class="sxs-lookup"><span data-stu-id="68c7f-132">If an application does not get a data block to the device driver when needed, there can be an audible gap in playback or a loss of incoming recorded information.</span></span> <span data-ttu-id="68c7f-133">Cela nécessite au moins un schéma de double mise en mémoire tampon, en conservant au moins un bloc de données avant le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="68c7f-133">This requires at least a double-buffering scheme — staying at least one data block ahead of the device driver.</span></span>

<span data-ttu-id="68c7f-134">Les rubriques suivantes décrivent les différentes façons de déterminer quand un pilote de périphérique est terminé avec un bloc de données :</span><span class="sxs-lookup"><span data-stu-id="68c7f-134">The following topics describe ways to determine when a device driver is finished with a data block:</span></span>

<span data-ttu-id="68c7f-135">Utilisation d’une fonction de rappel pour traiter des messages de pilote</span><span class="sxs-lookup"><span data-stu-id="68c7f-135">Using a Callback Function to Process Driver Messages</span></span>

-   [<span data-ttu-id="68c7f-136">Utilisation d’une fonction de rappel pour traiter des messages de pilote</span><span class="sxs-lookup"><span data-stu-id="68c7f-136">Using a Callback Function to Process Driver Messages</span></span>](using-a-callback-function-to-process-driver-messages.md)
-   [<span data-ttu-id="68c7f-137">Utilisation d’un rappel d’événement pour traiter des messages de pilote</span><span class="sxs-lookup"><span data-stu-id="68c7f-137">Using an Event Callback to Process Driver Messages</span></span>](using-an-callback-to-process-driver-messages.md)
-   [<span data-ttu-id="68c7f-138">Utilisation d’une fenêtre ou d’un thread pour traiter des messages de pilote</span><span class="sxs-lookup"><span data-stu-id="68c7f-138">Using a Window or Thread to Process Driver Messages</span></span>](using-a-window-or-thread-to-process-driver-messages.md)
-   [<span data-ttu-id="68c7f-139">Gestion des blocs de données par interrogation</span><span class="sxs-lookup"><span data-stu-id="68c7f-139">Managing Data Blocks by Polling</span></span>](managing-data-blocks-by-polling.md)

 

 