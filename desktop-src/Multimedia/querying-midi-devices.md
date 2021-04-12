---
title: Interrogation d’appareils MIDI
description: Interrogation d’appareils MIDI
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- Interface MIDI (Musical Instrument Digital Interface), interrogation des appareils
- MIDI (Musical Instrument Digital Interface), interroger des appareils
- Services MIDI, interrogation des appareils
- interrogation d’appareils MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066648d6e9ce89e03b26940cb27f3b62b6a03c07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381822"
---
# <a name="querying-midi-devices"></a><span data-ttu-id="f6041-107">Interrogation d’appareils MIDI</span><span class="sxs-lookup"><span data-stu-id="f6041-107">Querying MIDI Devices</span></span>

<span data-ttu-id="f6041-108">Avant de lancer ou d’enregistrer des données MIDI, vous devez déterminer les fonctionnalités du matériel MIDI présent dans le système.</span><span class="sxs-lookup"><span data-stu-id="f6041-108">Before playing or recording MIDI data, you must determine the capabilities of the MIDI hardware present in the system.</span></span> <span data-ttu-id="f6041-109">La fonctionnalité MIDI peut varier d’un ordinateur multimédia à l’autre. les applications ne doivent pas faire d’hypothèses sur le matériel présent dans un système donné.</span><span class="sxs-lookup"><span data-stu-id="f6041-109">MIDI capability can vary from one multimedia computer to the next; applications should not make assumptions about the hardware present in a given system.</span></span>

<span data-ttu-id="f6041-110">Windows fournit les fonctions suivantes pour déterminer le nombre de périphériques MIDI disponibles pour l’entrée ou la sortie dans un système donné.</span><span class="sxs-lookup"><span data-stu-id="f6041-110">Windows provides the following functions to determine how many MIDI devices are available for input or output in a given system.</span></span>



| <span data-ttu-id="f6041-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6041-111">Value</span></span>                                          | <span data-ttu-id="f6041-112">Signification</span><span class="sxs-lookup"><span data-stu-id="f6041-112">Meaning</span></span>                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="f6041-113">**midiInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="f6041-113">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | <span data-ttu-id="f6041-114">Récupère le nombre d’appareils d’entrée MIDI présents dans le système.</span><span class="sxs-lookup"><span data-stu-id="f6041-114">Retrieves the number of MIDI input devices present in the system.</span></span>  |
| [<span data-ttu-id="f6041-115">**midiOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="f6041-115">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | <span data-ttu-id="f6041-116">Récupère le nombre d’appareils de sortie MIDI présents dans le système.</span><span class="sxs-lookup"><span data-stu-id="f6041-116">Retrieves the number of MIDI output devices present in the system.</span></span> |



 

<span data-ttu-id="f6041-117">Comme les autres périphériques audio, les périphériques MIDI sont identifiés par un identificateur de périphérique, qui est déterminé implicitement à partir du nombre d’appareils présents dans un système donné.</span><span class="sxs-lookup"><span data-stu-id="f6041-117">Like other audio devices, MIDI devices are identified by a device identifier, which is determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="f6041-118">Les identificateurs d’appareil sont compris entre zéro et le nombre d’appareils présents, moins un.</span><span class="sxs-lookup"><span data-stu-id="f6041-118">Device identifiers range from zero to the number of devices present, minus one.</span></span> <span data-ttu-id="f6041-119">Par exemple, s’il existe deux périphériques de sortie MIDI dans un système, les identificateurs d’appareil valides sont 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="f6041-119">For example, if there are two MIDI output devices in a system, valid device identifiers are 0 and 1.</span></span>

<span data-ttu-id="f6041-120">Une fois que vous avez déterminé le nombre de périphériques d’entrée ou de sortie MIDI présents dans un système, vous pouvez vous renseigner sur les fonctionnalités de chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="f6041-120">After you determine how many MIDI input or output devices are present in a system, you can inquire about the capabilities of each device.</span></span> <span data-ttu-id="f6041-121">Windows fournit les fonctions suivantes pour déterminer les fonctionnalités des périphériques audio.</span><span class="sxs-lookup"><span data-stu-id="f6041-121">Windows provides the following functions to determine the capabilities of audio devices.</span></span>



| <span data-ttu-id="f6041-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6041-122">Value</span></span>                                          | <span data-ttu-id="f6041-123">Signification</span><span class="sxs-lookup"><span data-stu-id="f6041-123">Meaning</span></span>                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6041-124">**midiInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="f6041-124">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | <span data-ttu-id="f6041-125">Récupère les fonctionnalités d’un appareil d’entrée MIDI donné et place ces informations dans la structure [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) .</span><span class="sxs-lookup"><span data-stu-id="f6041-125">Retrieves the capabilities of a given MIDI input device and places this information in the [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) structure.</span></span>    |
| [<span data-ttu-id="f6041-126">**midiOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="f6041-126">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | <span data-ttu-id="f6041-127">Récupère les fonctionnalités d’un appareil de sortie MIDI donné et place ces informations dans la structure [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) .</span><span class="sxs-lookup"><span data-stu-id="f6041-127">Retrieves the capabilities of a given MIDI output device and places this information in the [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) structure.</span></span> |



 

<span data-ttu-id="f6041-128">Chacune de ces fonctions a un paramètre qui spécifie l’adresse d’une structure que la fonction remplit à l’aide d’informations sur les fonctionnalités d’un appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="f6041-128">Each of these functions has a parameter specifying the address of a structure that the function fills with information about the capabilities of a specified device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6041-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6041-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6041-130">Services MIDI</span><span class="sxs-lookup"><span data-stu-id="f6041-130">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 