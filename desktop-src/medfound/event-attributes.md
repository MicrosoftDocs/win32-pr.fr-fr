---
description: Attributs d'événement
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Attributs d’événement (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633e8f3857582422fe4a2d65ba34e68be483e7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524532"
---
# <a name="event-attributes-microsoft-media-foundation"></a><span data-ttu-id="c23ad-103">Attributs d’événement (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="c23ad-103">Event Attributes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="c23ad-104">Les attributs suivants s’appliquent aux événements.</span><span class="sxs-lookup"><span data-stu-id="c23ad-104">The following attributes apply to events.</span></span>



| <span data-ttu-id="c23ad-105">Attribut</span><span class="sxs-lookup"><span data-stu-id="c23ad-105">Attribute</span></span>                                                                                                        | <span data-ttu-id="c23ad-106">Description</span><span class="sxs-lookup"><span data-stu-id="c23ad-106">Description</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c23ad-107">**\_événement MF \_ - \_ éclaircir**</span><span class="sxs-lookup"><span data-stu-id="c23ad-107">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)                                                | <span data-ttu-id="c23ad-108">Quand une source de média demande un nouveau taux de lecture, spécifie si la source demande également une éclaircie.</span><span class="sxs-lookup"><span data-stu-id="c23ad-108">When a media source requests a new playback rate, specifies whether the source also requests thinning.</span></span>                |
| [<span data-ttu-id="c23ad-109">**\_ \_ nœud sortie de l’événement MF \_**</span><span class="sxs-lookup"><span data-stu-id="c23ad-109">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)                                                | <span data-ttu-id="c23ad-110">Identifie le nœud de topologie d’un récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="c23ad-110">Identifies the topology node for a stream sink.</span></span>                                                                       |
| [<span data-ttu-id="c23ad-111">**décalage de l’heure de présentation de l' \_ événement MF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c23ad-111">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)                     | <span data-ttu-id="c23ad-112">Décalage entre l’heure de présentation et les horodatages de la source du média.</span><span class="sxs-lookup"><span data-stu-id="c23ad-112">Offset between the presentation time and the media source's time stamps.</span></span>                                              |
| [<span data-ttu-id="c23ad-113">**\_ \_ heure SCRUBSAMPLE de l’événement MF \_**</span><span class="sxs-lookup"><span data-stu-id="c23ad-113">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)                                      | <span data-ttu-id="c23ad-114">Durée de présentation d’un échantillon rendu lors du nettoyage.</span><span class="sxs-lookup"><span data-stu-id="c23ad-114">Presentation time for a sample that was rendered while scrubbing.</span></span>                                                     |
| [<span data-ttu-id="c23ad-115">**\_SESSIONCAPS d’événements MF \_**</span><span class="sxs-lookup"><span data-stu-id="c23ad-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)                                                 | <span data-ttu-id="c23ad-116">Contient des indicateurs qui définissent les fonctionnalités de la session multimédia, en fonction de la présentation actuelle.</span><span class="sxs-lookup"><span data-stu-id="c23ad-116">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>                  |
| [<span data-ttu-id="c23ad-117">**\_ \_ SESSIONCAPS Delta d’événement MF \_**</span><span class="sxs-lookup"><span data-stu-id="c23ad-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md)                                    | <span data-ttu-id="c23ad-118">Contient des indicateurs qui indiquent les fonctionnalités qui ont changé dans la session multimédia, en fonction de la présentation actuelle.</span><span class="sxs-lookup"><span data-stu-id="c23ad-118">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span> |
| [<span data-ttu-id="c23ad-119">**\_ \_ \_ début réel de la source de l’événement MF \_**</span><span class="sxs-lookup"><span data-stu-id="c23ad-119">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)                               | <span data-ttu-id="c23ad-120">Contient l’heure de début de redémarrage d’une source de média à partir de sa position actuelle.</span><span class="sxs-lookup"><span data-stu-id="c23ad-120">Contains the start time when a media source restarts from its current position.</span></span>                                       |
| [<span data-ttu-id="c23ad-121">**caractéristiques de la \_ source d’événements MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c23ad-121">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)                          | <span data-ttu-id="c23ad-122">Spécifie les caractéristiques actuelles de la source du média.</span><span class="sxs-lookup"><span data-stu-id="c23ad-122">Specifies the current characteristics of the media source.</span></span>                                                            |
| [<span data-ttu-id="c23ad-123">**caractéristiques de la \_ source d’événements MF \_ \_ \_ Old**</span><span class="sxs-lookup"><span data-stu-id="c23ad-123">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)                 | <span data-ttu-id="c23ad-124">Spécifie les caractéristiques précédentes de la source du média.</span><span class="sxs-lookup"><span data-stu-id="c23ad-124">Specifies the previous characteristics of the media source.</span></span>                                                           |
| [<span data-ttu-id="c23ad-125">**début du substitut de la \_ source d’événement MF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c23ad-125">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)                                   | <span data-ttu-id="c23ad-126">Spécifie si la topologie du segment actuel est vide.</span><span class="sxs-lookup"><span data-stu-id="c23ad-126">Specifies whether the current segment topology is empty.</span></span>                                                              |
| [<span data-ttu-id="c23ad-127">**\_ \_ PROJECTSTART source de l’événement MF \_**</span><span class="sxs-lookup"><span data-stu-id="c23ad-127">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)                                | <span data-ttu-id="c23ad-128">Spécifie l’heure de début d’une topologie de segment.</span><span class="sxs-lookup"><span data-stu-id="c23ad-128">Specifies the start time for a segment topology.</span></span>                                                                      |
| [<span data-ttu-id="c23ad-129">**TOPOLOGIE de la \_ source d’événements MF \_ \_ \_ annulée**</span><span class="sxs-lookup"><span data-stu-id="c23ad-129">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)                     | <span data-ttu-id="c23ad-130">Spécifie si la source de Sequencer a annulé une topologie.</span><span class="sxs-lookup"><span data-stu-id="c23ad-130">Specifies whether the sequencer source canceled a topology.</span></span>                                                           |
| [<span data-ttu-id="c23ad-131">**heure de la présentation du démarrage de l' \_ événement MF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c23ad-131">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)                       | <span data-ttu-id="c23ad-132">Heure de début de la présentation, en unités de 100 nanosecondes, mesurée en fonction de l’horloge de la présentation.</span><span class="sxs-lookup"><span data-stu-id="c23ad-132">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>               |
| [<span data-ttu-id="c23ad-133">**\_ \_ \_ heure de début de la présentation de l’événement MF \_ \_ à la \_ sortie**</span><span class="sxs-lookup"><span data-stu-id="c23ad-133">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md) | <span data-ttu-id="c23ad-134">Heure de présentation à laquelle les récepteurs multimédia affichent le premier exemple de la nouvelle topologie.</span><span class="sxs-lookup"><span data-stu-id="c23ad-134">The presentation time at which the media sinks will render the first sample of the new topology.</span></span>                      |
| [<span data-ttu-id="c23ad-135">**État de la \_ topologie des événements MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c23ad-135">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)                                        | <span data-ttu-id="c23ad-136">Spécifie l’état d’une topologie pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="c23ad-136">Specifies the status of a topology during playback.</span></span>                                                                   |
| [<span data-ttu-id="c23ad-137">**heure d’occurrence de l' \_ \_ événement d’environ session \_ \_ MF \_**</span><span class="sxs-lookup"><span data-stu-id="c23ad-137">**MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME**</span></span>](mf-session-approx-event-occurrence-time-attribute.md)        | <span data-ttu-id="c23ad-138">Heure approximative à laquelle la session multimédia a déclenché un événement.</span><span class="sxs-lookup"><span data-stu-id="c23ad-138">The approximate time when the Media Session raised an event.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="c23ad-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c23ad-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c23ad-140">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="c23ad-140">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[<span data-ttu-id="c23ad-141">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c23ad-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="c23ad-142">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c23ad-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



