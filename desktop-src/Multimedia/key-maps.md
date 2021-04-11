---
title: Cartes clés
description: Cartes clés
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, mappages de clés
- cartes clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffafd99e6d813f12c388b633997980b7a58d62dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939815"
---
# <a name="key-maps"></a><span data-ttu-id="b3732-107">Cartes clés</span><span class="sxs-lookup"><span data-stu-id="b3732-107">Key Maps</span></span>

<span data-ttu-id="b3732-108">Chaque entrée dans la table de traduction de mappage de correctifs peut être associée à un mappage de clés.</span><span class="sxs-lookup"><span data-stu-id="b3732-108">Each entry in the patch-map translation table can have an associated key map.</span></span> <span data-ttu-id="b3732-109">Les mappages de clés affectent les messages Remarque on, note-OFF et Polyphonic-Key-aftertouch.</span><span class="sxs-lookup"><span data-stu-id="b3732-109">Key maps affect note-on, note-off, and polyphonic-key-aftertouch messages.</span></span> <span data-ttu-id="b3732-110">Un mappage de clés a une table de traduction avec une entrée pour chacune des valeurs de clé MIDI 128.</span><span class="sxs-lookup"><span data-stu-id="b3732-110">A key map has a translation table with an entry for each of the 128 MIDI key values.</span></span> <span data-ttu-id="b3732-111">Par exemple, si l’entrée pour la valeur de clé 60 est 72, le Mappeur MIDI modifie les messages de note MIDI, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="b3732-111">For example, if the entry for key value 60 is 72, the MIDI Mapper modifies MIDI note-on messages as shown in the following illustration.</span></span>

![image du mappeur midi](images/mmap-a06.gif)

<span data-ttu-id="b3732-113">Les cartes clés sont utiles avec les synthétiseurs qui ont des instruments à percussion basés sur des clés avec un son de percussion particulier affecté à chaque clé.</span><span class="sxs-lookup"><span data-stu-id="b3732-113">Key maps are useful with synthesizers that have key-based percussion instruments with a particular percussion sound assigned to each key.</span></span> <span data-ttu-id="b3732-114">Les mappages de clés sont généralement affectés au premier correctif dans les mappages de correctifs sur les canaux à percussion (10 et 16).</span><span class="sxs-lookup"><span data-stu-id="b3732-114">Key maps are usually assigned to the first patch in the patch maps on the percussion channels (10 and 16).</span></span>

 

 




