---
title: Ouverture et fermeture de pilotes de périphérique
description: Ouverture et fermeture de pilotes de périphérique
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- Interface MIDI (Musical Instrument Digital Interface), ouverture d’appareils
- MIDI (Musical Instrument Digital Interface), ouvrir des appareils
- Services MIDI, ouverture d’appareils
- ouverture d’appareils MIDI
- Interface MIDI (Musical Instrument Digital Interface), fermeture des appareils
- MIDI (Musical Instrument Digital Interface), fermer des appareils
- Services MIDI, fermeture d’appareils
- fermeture des appareils MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d7035455baa067b81af7da980a4ae043500c7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725077"
---
# <a name="opening-and-closing-device-drivers"></a><span data-ttu-id="7bb3d-111">Ouverture et fermeture de pilotes de périphérique</span><span class="sxs-lookup"><span data-stu-id="7bb3d-111">Opening and Closing Device Drivers</span></span>

<span data-ttu-id="7bb3d-112">Vous devez ouvrir un appareil MIDI avant de l’utiliser, et vous devez fermer l’appareil dès que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-112">You must open a MIDI device before using it, and you should close the device as soon as you finish using it.</span></span> <span data-ttu-id="7bb3d-113">Windows fournit les fonctions suivantes pour ouvrir et fermer différents types d’appareils MIDI.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-113">Windows provides the following functions to open and close different types of MIDI devices.</span></span>



| <span data-ttu-id="7bb3d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bb3d-114">Value</span></span>                                | <span data-ttu-id="7bb3d-115">Signification</span><span class="sxs-lookup"><span data-stu-id="7bb3d-115">Meaning</span></span>                                            |
|--------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="7bb3d-116">**midiInClose**</span><span class="sxs-lookup"><span data-stu-id="7bb3d-116">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | <span data-ttu-id="7bb3d-117">Ferme un appareil d’entrée MIDI spécifié.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-117">Closes a specified MIDI input device.</span></span>              |
| [<span data-ttu-id="7bb3d-118">**midiInOpen**</span><span class="sxs-lookup"><span data-stu-id="7bb3d-118">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | <span data-ttu-id="7bb3d-119">Ouvre un appareil d’entrée MIDI spécifié pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-119">Opens a specified MIDI input device for recording.</span></span> |
| [<span data-ttu-id="7bb3d-120">**midiOutClose**</span><span class="sxs-lookup"><span data-stu-id="7bb3d-120">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | <span data-ttu-id="7bb3d-121">Ferme un appareil de sortie MIDI spécifié.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-121">Closes a specified MIDI output device.</span></span>             |
| [<span data-ttu-id="7bb3d-122">**midiOutOpen**</span><span class="sxs-lookup"><span data-stu-id="7bb3d-122">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | <span data-ttu-id="7bb3d-123">Ouvre un appareil de sortie MIDI pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-123">Opens a MIDI output device for playback.</span></span>           |



 

<span data-ttu-id="7bb3d-124">Chaque fonction qui ouvre un appareil MIDI prend comme paramètres un identificateur d’appareil, l’adresse d’un emplacement de mémoire et certains paramètres propres aux périphériques MIDI.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-124">Each function that opens a MIDI device takes as parameters a device identifier, an address of a memory location, and some parameters unique to MIDI devices.</span></span> <span data-ttu-id="7bb3d-125">L’emplacement de la mémoire est rempli avec un handle d’appareil, qui est utilisé pour identifier le périphérique audio ouvert dans les appels à d’autres fonctions audio.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-125">The memory location is filled with a device handle, which is used to identify the open audio device in calls to other audio functions.</span></span>

<span data-ttu-id="7bb3d-126">De nombreuses fonctions MIDI peuvent accepter un handle d’appareil ou un identificateur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-126">Many MIDI functions can accept either a device handle or a device identifier.</span></span> <span data-ttu-id="7bb3d-127">Bien que vous puissiez utiliser un handle d’appareil partout où vous utiliseriez un identificateur de périphérique, vous ne pouvez pas toujours utiliser un identificateur de périphérique quand un handle est appelé pour.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-127">Although you can use a device handle wherever you would use a device identifier, you cannot always use a device identifier when a handle is called for.</span></span>

> [!Note]  
> <span data-ttu-id="7bb3d-128">Les périphériques MIDI ne sont pas nécessairement partageables. un appareil particulier peut donc ne pas être disponible lorsqu’un utilisateur le demande.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-128">MIDI devices are not necessarily sharable, so a particular device may not be available when a user requests it.</span></span> <span data-ttu-id="7bb3d-129">Dans ce cas, l’application doit avertir l’utilisateur et permettre à l’utilisateur d’essayer d’ouvrir à nouveau l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-129">If this happens, the application should notify the user and allow the user to try to open the device again.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7bb3d-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7bb3d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bb3d-131">Services MIDI</span><span class="sxs-lookup"><span data-stu-id="7bb3d-131">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 