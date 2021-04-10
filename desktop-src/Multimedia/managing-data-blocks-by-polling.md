---
title: Gestion des blocs de données par interrogation
description: Gestion des blocs de données par interrogation
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- sons Waveform, interrogation des blocs de données
- blocs de données audio, interrogation
- interrogation des blocs de données audio
- WAVEHDR, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e5580ff64425eae1bc6650268b065e60b90f43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031101"
---
# <a name="managing-data-blocks-by-polling"></a><span data-ttu-id="632af-107">Gestion des blocs de données par interrogation</span><span class="sxs-lookup"><span data-stu-id="632af-107">Managing Data Blocks by Polling</span></span>

<span data-ttu-id="632af-108">Outre l’utilisation d’une fonction de rappel, vous pouvez interroger le membre **dwFlags** d’une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) pour déterminer quand un périphérique audio est terminé avec un bloc de données.</span><span class="sxs-lookup"><span data-stu-id="632af-108">In addition to using a callback function, you can poll the **dwFlags** member of a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to determine when an audio device is finished with a data block.</span></span> <span data-ttu-id="632af-109">Il est parfois préférable d’interroger **dwFlags** plutôt que d’attendre qu’un autre mécanisme reçoit des messages des pilotes.</span><span class="sxs-lookup"><span data-stu-id="632af-109">Sometimes it is better to poll **dwFlags** than to wait for another mechanism to receive messages from the drivers.</span></span> <span data-ttu-id="632af-110">Par exemple, après avoir appelé la fonction [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) pour libérer des blocs de données en attente, vous pouvez immédiatement interroger pour vous assurer que les blocs de données ont été libérés avant d’appeler [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) et de libérer de la mémoire pour le bloc de données.</span><span class="sxs-lookup"><span data-stu-id="632af-110">For example, after you call the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function to release pending data blocks, you can immediately poll to be sure that the data blocks have been released before calling [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) and freeing the memory for the data block.</span></span>

<span data-ttu-id="632af-111">Vous pouvez utiliser l' \_ indicateur WHDR Done pour tester le membre **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="632af-111">You can use the WHDR\_DONE flag to test the **dwFlags** member.</span></span> <span data-ttu-id="632af-112">Dès que l’indicateur WHDR \_ done est défini dans le membre **dwFlags** de la structure **WAVEHDR** , le pilote est terminé avec le bloc de données.</span><span class="sxs-lookup"><span data-stu-id="632af-112">As soon as the WHDR\_DONE flag is set in the **dwFlags** member of the **WAVEHDR** structure, the driver is finished with the data block.</span></span>

 

 