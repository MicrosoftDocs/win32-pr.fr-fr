---
title: Le Mappeur MIDI et Windows
description: Le Mappeur MIDI et Windows
ms.assetid: a077f935-e085-4148-9975-7926ac018f0c
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad3cee4fb37de6ecbfdc4f81860afcb9f589d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031173"
---
# <a name="the-midi-mapper-and-windows"></a><span data-ttu-id="b5fd5-106">Le Mappeur MIDI et Windows</span><span class="sxs-lookup"><span data-stu-id="b5fd5-106">The MIDI Mapper and Windows</span></span>

<span data-ttu-id="b5fd5-107">Le Mappeur MIDI fait partie du logiciel système.</span><span class="sxs-lookup"><span data-stu-id="b5fd5-107">The MIDI Mapper is part of the system software.</span></span> <span data-ttu-id="b5fd5-108">L’illustration suivante montre comment le Mappeur MIDI se réfère à d’autres éléments des services audio.</span><span class="sxs-lookup"><span data-stu-id="b5fd5-108">The following illustration shows how the MIDI Mapper relates to other elements of the audio services.</span></span>

![relation entre le Mappeur midi et les autres éléments de l’image des services audio](images/mmap-a01.gif)

<span data-ttu-id="b5fd5-110">Du point de vue d’une application, le Mappeur MIDI ressemble à un autre périphérique de sortie MIDI.</span><span class="sxs-lookup"><span data-stu-id="b5fd5-110">From the viewpoint of an application, the MIDI Mapper looks like another MIDI output device.</span></span> <span data-ttu-id="b5fd5-111">Le Mappeur MIDI reçoit les messages qui lui sont envoyés par les fonctions de sortie MIDI de bas niveau [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) et [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg).</span><span class="sxs-lookup"><span data-stu-id="b5fd5-111">The MIDI Mapper receives messages sent to it by the low-level MIDI output functions [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) and [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg).</span></span> <span data-ttu-id="b5fd5-112">Le Mappeur MIDI modifie ces messages et les redirige vers un périphérique de sortie MIDI en fonction de la carte d’installation MIDI en cours.</span><span class="sxs-lookup"><span data-stu-id="b5fd5-112">The MIDI Mapper modifies these messages and redirects them to a MIDI output device according to the current MIDI setup map.</span></span> <span data-ttu-id="b5fd5-113">La carte d’installation MIDI active est sélectionnée par l’utilisateur au moyen de l’option du panneau de configuration MIDI.</span><span class="sxs-lookup"><span data-stu-id="b5fd5-113">The current MIDI setup map is selected by the user by means of the MIDI Control Panel option.</span></span> <span data-ttu-id="b5fd5-114">Seul l’utilisateur peut sélectionner le plan d’installation actuel ; les applications ne peuvent pas modifier la carte d’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="b5fd5-114">Only the user can select the current setup map; applications cannot change the current setup map.</span></span>

 

 