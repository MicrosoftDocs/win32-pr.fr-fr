---
title: Réception des messages de Running-Status
description: Réception des messages de Running-Status
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- MIDI (Musical Instrument Digital Interface), état d’exécution
- MIDI (Musical Instrument Digital Interface), état d’exécution
- enregistrement de l’audio MIDI, état d’exécution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4d12a19f525a6fa673747063774bf4507d65b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379641"
---
# <a name="receiving-running-status-messages"></a><span data-ttu-id="a76dc-106">Réception des messages de Running-Status</span><span class="sxs-lookup"><span data-stu-id="a76dc-106">Receiving Running-Status Messages</span></span>

<span data-ttu-id="a76dc-107">La spécification *fichiers midi Standard 1,0* permet l’utilisation de l' *État d’exécution* lorsqu’un message a le même octet d’État que le message précédent.</span><span class="sxs-lookup"><span data-stu-id="a76dc-107">The *Standard MIDI Files 1.0* specification allows the use of *running status* when a message has the same status byte as the previous message.</span></span> <span data-ttu-id="a76dc-108">Lorsque l’état d’exécution est utilisé, l’octet d’état des messages suivants peut être omis.</span><span class="sxs-lookup"><span data-stu-id="a76dc-108">When running status is used, the status byte of subsequent messages can be omitted.</span></span> <span data-ttu-id="a76dc-109">Tous les pilotes de périphérique d’entrée MIDI sont requis pour étendre les messages à l’aide de l’état d’exécution dans des messages complets, afin que vous receviez toujours des messages MIDI complets à partir d’un pilote de périphérique d’entrée MIDI.</span><span class="sxs-lookup"><span data-stu-id="a76dc-109">All MIDI input device drivers are required to expand messages using running status into complete messages, so that you always receive complete MIDI messages from a MIDI input device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a76dc-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a76dc-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a76dc-111">Enregistrement d’un fichier audio MIDI</span><span class="sxs-lookup"><span data-stu-id="a76dc-111">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 




