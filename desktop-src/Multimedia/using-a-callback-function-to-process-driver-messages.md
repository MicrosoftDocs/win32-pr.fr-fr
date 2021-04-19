---
title: Utilisation d’une fonction de rappel pour traiter des messages de pilote
description: Utilisation d’une fonction de rappel pour traiter des messages de pilote
ms.assetid: 7fef400f-5040-4d33-9a2f-bb12aa9369e0
keywords:
- sons Waveform, fonctions de rappel
- blocs de données audio, fonctions de rappel
- audio Wave, traitement des messages de pilote
- blocs de données audio, traitement des messages de pilote
- traitement des messages du pilote
- waveInOpen fonction)
- waveOutOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3e7541a00b43b5fb2267a17d4de8bb017823c3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510879"
---
# <a name="using-a-callback-function-to-process-driver-messages"></a><span data-ttu-id="0e697-110">Utilisation d’une fonction de rappel pour traiter des messages de pilote</span><span class="sxs-lookup"><span data-stu-id="0e697-110">Using a Callback Function to Process Driver Messages</span></span>

<span data-ttu-id="0e697-111">Vous pouvez écrire votre propre fonction de rappel pour traiter les messages envoyés par le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="0e697-111">You can write your own callback function to process messages sent by the device driver.</span></span> <span data-ttu-id="0e697-112">Pour utiliser une fonction de rappel, spécifiez l’indicateur de fonction de rappel \_ dans le paramètre *fdwOpen* et l’adresse du rappel dans le paramètre *DwCallback* de la fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) ou [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="0e697-112">To use a callback function, specify the CALLBACK\_FUNCTION flag in the *fdwOpen* parameter and the address of the callback in the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>

<span data-ttu-id="0e697-113">Les messages envoyés à une fonction de rappel sont similaires aux messages envoyés à une fenêtre, sauf qu’ils ont deux paramètres **DWORD** au lieu d’un paramètre **uint** et d’un paramètre **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0e697-113">Messages sent to a callback function are similar to messages sent to a window, except they have two **DWORD** parameters instead of a **UINT** and a **DWORD** parameter.</span></span> <span data-ttu-id="0e697-114">Pour plus d’informations sur ces messages, consultez [playing Waveform-Audio Files](playing-waveform-audio-files.md).</span><span class="sxs-lookup"><span data-stu-id="0e697-114">For details on these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

<span data-ttu-id="0e697-115">Pour passer des données d’instance d’une application à une fonction de rappel, utilisez l’une des techniques suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e697-115">To pass instance data from an application to a callback function, use one of the following techniques:</span></span>

-   <span data-ttu-id="0e697-116">Transmettez les données de l’instance à l’aide du paramètre *dwInstance* de la fonction qui ouvre le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="0e697-116">Pass the instance data using the *dwInstance* parameter of the function that opens the device driver.</span></span>
-   <span data-ttu-id="0e697-117">Transmettez les données d’instance à l’aide du membre **dwUser** de la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) qui identifie un bloc de données audio envoyé à un pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="0e697-117">Pass the instance data using the **dwUser** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies an audio data block being sent to a device driver.</span></span>

<span data-ttu-id="0e697-118">Si vous avez besoin de plus de 32 bits de données d’instance, transmettez un pointeur vers une structure contenant les informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0e697-118">If you need more than 32 bits of instance data, pass a pointer to a structure containing the additional information.</span></span>

 

 