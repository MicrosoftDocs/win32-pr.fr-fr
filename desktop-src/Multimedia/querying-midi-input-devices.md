---
title: Interrogation des périphériques d’entrée MIDI
description: Interrogation des périphériques d’entrée MIDI
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- Interface MIDI (Musical Instrument Digital Interface), appareils d’entrée
- MIDI (Musical Instrument Digital Interface), appareils d’entrée
- enregistrement de données audio MIDI, appareils d’entrée
- Périphériques d’entrée MIDI
- Interface MIDI (Musical Instrument Digital Interface), interrogation des périphériques d’entrée
- MIDI (Musical Instrument Digital Interface), interrogation des périphériques d’entrée
- enregistrement d’un fichier audio MIDI, interrogation d’appareils d’entrée
- interrogation des périphériques d’entrée MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a92bec8733887e20c25f37d1de3dd493e555c8a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510679"
---
# <a name="querying-midi-input-devices"></a><span data-ttu-id="bfdcc-111">Interrogation des périphériques d’entrée MIDI</span><span class="sxs-lookup"><span data-stu-id="bfdcc-111">Querying MIDI Input Devices</span></span>

<span data-ttu-id="bfdcc-112">Avant d’enregistrer l’audio MIDI, vous devez utiliser la fonction [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) pour déterminer les fonctionnalités de l’appareil d’entrée MIDI qui est présent dans le système.</span><span class="sxs-lookup"><span data-stu-id="bfdcc-112">Before recording MIDI audio, you should use the [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) function to determine the capabilities of the MIDI input device that is present in the system.</span></span> <span data-ttu-id="bfdcc-113">Cette fonction prend une adresse d’une structure [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) , qu’elle remplit avec des informations sur les fonctionnalités de l’appareil donné.</span><span class="sxs-lookup"><span data-stu-id="bfdcc-113">This function takes an address of a [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) structure, which it fills with information about the capabilities of the given device.</span></span> <span data-ttu-id="bfdcc-114">Ces informations incluent les identificateurs de fabricant et de produit, un nom de produit pour l’appareil et le numéro de version du pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="bfdcc-114">This information includes the manufacturer and product identifiers, a product name for the device, and the version number of the device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfdcc-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bfdcc-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfdcc-116">Enregistrement d’un fichier audio MIDI</span><span class="sxs-lookup"><span data-stu-id="bfdcc-116">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 