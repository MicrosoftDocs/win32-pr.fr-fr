---
title: Récupération du type de division de séquence
description: Récupération du type de division de séquence
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- MIDI (Musical Instrument Digital Interface), type de division de séquence
- MIDI (Musical Instrument Digital Interface), type de division de séquence
- Séquenceur MIDI MCI, type de division
- Commande MCI_STATUS
- type de division de séquence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6586a33fe4a5225fdcdca21e413104388d5831d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939914"
---
# <a name="retrieving-the-sequence-division-type"></a><span data-ttu-id="76a00-108">Récupération du type de division de séquence</span><span class="sxs-lookup"><span data-stu-id="76a00-108">Retrieving the Sequence Division Type</span></span>

<span data-ttu-id="76a00-109">Le *type de division* d’une séquence MIDI détermine la durée entre les événements midi de la séquence.</span><span class="sxs-lookup"><span data-stu-id="76a00-109">The *division type* of a MIDI sequence determines the amount of time between MIDI events in the sequence.</span></span> <span data-ttu-id="76a00-110">Pour déterminer le type de division d’une séquence, utilisez la commande [**MCI \_ Status**](mci-status.md) et définissez le membre **dwItem** de la structure de l' [**\_ état \_ MCI**](mci-status-parms.md) sur MCI \_ Seq \_ Status \_ DIVTYPE.</span><span class="sxs-lookup"><span data-stu-id="76a00-110">To determine the division type of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_DIVTYPE .</span></span>

<span data-ttu-id="76a00-111">Si la commande d' **\_ État MCI** est réussie, le membre **dwReturn** de la structure d' **\_ \_ État MCI** contient l’une des valeurs suivantes pour indiquer le type de division.</span><span class="sxs-lookup"><span data-stu-id="76a00-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure will contain one of the following values to indicate the division type.</span></span>



| <span data-ttu-id="76a00-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="76a00-112">Value</span></span>                        | <span data-ttu-id="76a00-113">Type de division</span><span class="sxs-lookup"><span data-stu-id="76a00-113">Division type</span></span>                     |
|------------------------------|-----------------------------------|
| <span data-ttu-id="76a00-114">MCI \_ Seq \_ div \_ PPQN</span><span class="sxs-lookup"><span data-stu-id="76a00-114">MCI\_SEQ\_DIV\_PPQN</span></span>          | <span data-ttu-id="76a00-115">PPQN (note de pièces par trimestre)</span><span class="sxs-lookup"><span data-stu-id="76a00-115">PPQN (parts-per-quarter note)</span></span>     |
| <span data-ttu-id="76a00-116">MCI \_ Seq \_ div \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="76a00-116">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>     | <span data-ttu-id="76a00-117">SMPTE, 24 fps (images par seconde)</span><span class="sxs-lookup"><span data-stu-id="76a00-117">SMPTE, 24 fps (frames per second)</span></span> |
| <span data-ttu-id="76a00-118">MCI \_ Seq \_ div \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="76a00-118">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>     | <span data-ttu-id="76a00-119">SMPTE, 25 i/s</span><span class="sxs-lookup"><span data-stu-id="76a00-119">SMPTE, 25 fps</span></span>                     |
| <span data-ttu-id="76a00-120">MCI \_ Seq \_ div \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="76a00-120">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>     | <span data-ttu-id="76a00-121">SMPTE, 30 i/s</span><span class="sxs-lookup"><span data-stu-id="76a00-121">SMPTE, 30 fps</span></span>                     |
| <span data-ttu-id="76a00-122">MCI \_ Seq \_ div \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="76a00-122">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span> | <span data-ttu-id="76a00-123">SMPTE, trame de dépôt de 30 i/s</span><span class="sxs-lookup"><span data-stu-id="76a00-123">SMPTE, 30 fps drop frame</span></span>          |



 

<span data-ttu-id="76a00-124">Vous devez connaître le type de division d’une séquence à modifier ou interroger son tempo.</span><span class="sxs-lookup"><span data-stu-id="76a00-124">You must know the division type of a sequence to change or query its tempo.</span></span> <span data-ttu-id="76a00-125">Vous ne pouvez pas modifier le type de division d’une séquence à l’aide du séquenceur MCI.</span><span class="sxs-lookup"><span data-stu-id="76a00-125">You cannot change the division type of a sequence by using the MCI sequencer.</span></span>

 

 




