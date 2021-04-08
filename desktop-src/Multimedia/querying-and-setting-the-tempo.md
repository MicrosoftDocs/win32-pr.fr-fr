---
title: Interrogation et définition du tempo
description: Interrogation et définition du tempo
ms.assetid: 84eba230-88b6-4cba-9e90-ba0b4bcfc691
keywords:
- MIDI (Musical Instrument Digital Interface), tempo
- MIDI (Musical Instrument Digital Interface), tempo
- Séquenceur MIDI MCI, tempo
- Commande MCI_STATUS
- tempo de séquence
- tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3927d2f04e1b073b25c262437620325dc5cd040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675918"
---
# <a name="querying-and-setting-the-tempo"></a><span data-ttu-id="e7805-109">Interrogation et définition du tempo</span><span class="sxs-lookup"><span data-stu-id="e7805-109">Querying and Setting the Tempo</span></span>

<span data-ttu-id="e7805-110">Pour récupérer le tempo d’une séquence, utilisez la commande [**MCI \_ Status**](mci-status.md) et définissez le membre **dwItem** de la structure d' [**\_ état \_ MCI**](mci-status-parms.md) sur le tempo d’état de MCI \_ Seq \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e7805-110">To retrieve the tempo of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_TEMPO.</span></span> <span data-ttu-id="e7805-111">Si la commande d' **\_ État MCI** est réussie, le membre **dwReturn** de la structure d' **\_ \_ État MCI** contient le tempo en cours.</span><span class="sxs-lookup"><span data-stu-id="e7805-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure contains the current tempo.</span></span>

<span data-ttu-id="e7805-112">Pour modifier le tempo, utilisez la commande [**MCI \_ Set**](mci-set.md) avec la structure [**MCI \_ Seq \_ Set \_ PARMS**](mci-seq-set-parms.md) , en spécifiant l' \_ indicateur de tempo du paramètre MCI Seq \_ \_ et en définissant le tempo souhaité dans le membre **dwTempo** de la structure.</span><span class="sxs-lookup"><span data-stu-id="e7805-112">To change tempo, use the [**MCI\_SET**](mci-set.md) command with the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, specifying the MCI\_SEQ\_SET\_TEMPO flag and setting the **dwTempo** member of the structure to the desired tempo.</span></span>

<span data-ttu-id="e7805-113">La façon dont le tempo est représenté dépend du type de division de la séquence.</span><span class="sxs-lookup"><span data-stu-id="e7805-113">The way tempo is represented depends on the division type of the sequence.</span></span> <span data-ttu-id="e7805-114">Si le type de division est PPQN, le tempo est représenté en temps par minute.</span><span class="sxs-lookup"><span data-stu-id="e7805-114">If the division type is PPQN, the tempo is represented in beats per minute.</span></span> <span data-ttu-id="e7805-115">Si le type de division est l’un des types de division SMPTE, le tempo est représenté en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="e7805-115">If the division type is one of the SMPTE division types, the tempo is represented in frames per second.</span></span> <span data-ttu-id="e7805-116">Pour plus d’informations sur la détermination du type de division d’une séquence, consultez [récupération du type de division de séquence](retrieving-the-sequence-division-type.md).</span><span class="sxs-lookup"><span data-stu-id="e7805-116">For information about determining the division type of a sequence, see [Retrieving the Sequence Division Type](retrieving-the-sequence-division-type.md).</span></span>

 

 




