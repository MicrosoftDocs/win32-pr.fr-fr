---
title: Réinitialisation de la sortie MIDI
description: Réinitialisation de la sortie MIDI
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- Interface MIDI (Musical Instrument Digital Interface), réinitialisation des périphériques de sortie
- MIDI (Musical Instrument Digital Interface), réinitialisation des périphériques de sortie
- Jeux de fichiers MIDI, réinitialisation des périphériques de sortie
- réinitialisation des périphériques de sortie
- Appareil de sortie MIDI (Musical Instrument Digital Interface)
- MIDI (Musical Instrument Digital Interface), périphériques de sortie
- Jeux de fichiers MIDI, périphériques de sortie
- Périphériques de sortie MIDI
- EOX (fin de l’exclusivité)
- fin de l’exclusivité (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15778fc8a1a48c34b69915aafb7e3139153b5882
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314687"
---
# <a name="resetting-midi-output"></a><span data-ttu-id="65835-113">Réinitialisation de la sortie MIDI</span><span class="sxs-lookup"><span data-stu-id="65835-113">Resetting MIDI Output</span></span>

<span data-ttu-id="65835-114">La fonction [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) désactive toutes les notes sur tous les canaux MIDI pour un périphérique MIDI spécifié.</span><span class="sxs-lookup"><span data-stu-id="65835-114">The [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) function turns off all notes on all MIDI channels for a specified MIDI device.</span></span> <span data-ttu-id="65835-115">Ensuite, la fonction marque toutes les mémoires tampons système exclusives en attente comme terminées et les retourne à l’application.</span><span class="sxs-lookup"><span data-stu-id="65835-115">Then, the function marks any pending system-exclusive buffers as done and returns them to the application.</span></span> <span data-ttu-id="65835-116">Cette fonction peut être utile dans une application qui utilise une sortie MIDI pour fournir à l’utilisateur la possibilité de réinitialiser la sortie MIDI.</span><span class="sxs-lookup"><span data-stu-id="65835-116">This function can be useful in an application that uses MIDI output to provide the user with the ability to reset MIDI output.</span></span>

> [!Note]  
> <span data-ttu-id="65835-117">L’arrêt d’un message système sans envoi d’un octet EOX (fin d’exclusivité) peut entraîner des problèmes pour l’appareil de réception.</span><span class="sxs-lookup"><span data-stu-id="65835-117">Terminating a system-exclusive message without sending an EOX (end-of-exclusive) byte can cause problems for the receiving device.</span></span> <span data-ttu-id="65835-118">La fonction **midiOutReset** n’envoie pas d’octet EOX lorsqu’elle met fin à un message système, car les applications sont chargées de le faire.</span><span class="sxs-lookup"><span data-stu-id="65835-118">The **midiOutReset** function does not send an EOX byte when it terminates a system-exclusive message, because applications are responsible for doing this.</span></span>

 

 

 