---
title: Envoi de messages de System-Exclusive
description: Envoi de messages de System-Exclusive
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- MIDI (Musical Instrument Digital Interface), envoi de messages
- MIDI (Musical Instrument Digital Interface), envoi de messages
- Jeux de fichiers MIDI, envoi de messages
- envoi de messages MIDI
- MIDI (Musical Instrument Digital Interface), messages système-exclusifs
- MIDI (Musical Instrument Digital Interface), messages système-exclusifs
- exécution de fichiers MIDI, messages System-exclusive
- messages MIDI exclusifs système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073ebc0fe111ef19e2edb098e6bdb170c13abc3e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842118"
---
# <a name="sending-system-exclusive-messages"></a><span data-ttu-id="27ed8-111">Envoi de messages de System-Exclusive</span><span class="sxs-lookup"><span data-stu-id="27ed8-111">Sending System-Exclusive Messages</span></span>

<span data-ttu-id="27ed8-112">Les messages système exclusifs MIDI sont les seuls messages MIDI qui ne tiennent pas dans une seule valeur de mot double.</span><span class="sxs-lookup"><span data-stu-id="27ed8-112">MIDI system-exclusive messages are the only MIDI messages that will not fit into a single doubleword value.</span></span> <span data-ttu-id="27ed8-113">Les messages exclusifs système peuvent avoir n’importe quelle longueur.</span><span class="sxs-lookup"><span data-stu-id="27ed8-113">System-exclusive messages can be any length.</span></span> <span data-ttu-id="27ed8-114">Windows fournit la fonction [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) pour l’envoi de messages exclusifs système aux périphériques de sortie MIDI.</span><span class="sxs-lookup"><span data-stu-id="27ed8-114">Windows provides the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) function for sending system-exclusive messages to MIDI output devices.</span></span> <span data-ttu-id="27ed8-115">Pour spécifier des blocs de données système exclusifs MIDI, utilisez la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="27ed8-115">To specify MIDI system-exclusive data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

<span data-ttu-id="27ed8-116">Après avoir envoyé un bloc de données System-exclusive à l’aide de **midiOutLongMsg**, vous devez attendre que le pilote de périphérique se termine avec le bloc de données avant de le libérer.</span><span class="sxs-lookup"><span data-stu-id="27ed8-116">After you send a system-exclusive data block using **midiOutLongMsg**, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="27ed8-117">Si vous envoyez plusieurs blocs de données, vous devez surveiller l’achèvement de chaque bloc de données afin de savoir quand envoyer des blocs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="27ed8-117">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="27ed8-118">Pour plus d’informations sur les différentes techniques d’analyse de la saisie semi-automatique des blocs de données, consultez [gestion des blocs de données MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="27ed8-118">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

> [!Note]  
> <span data-ttu-id="27ed8-119">Tout octet d’État MIDI autre qu’un message système en temps réel met fin à un message système exclusif.</span><span class="sxs-lookup"><span data-stu-id="27ed8-119">Any MIDI status byte other than a system-real-time message will terminate a system-exclusive message.</span></span> <span data-ttu-id="27ed8-120">Si vous utilisez plusieurs blocs de données pour envoyer un seul message système exclusif, n’envoyez pas de messages MIDI autres que des messages du système en temps réel entre les blocs de données.</span><span class="sxs-lookup"><span data-stu-id="27ed8-120">If you are using multiple data blocks to send a single system-exclusive message, do not send any MIDI messages other than system-real-time messages between data blocks.</span></span>

 

 

 