---
description: La session multimédia est un objet qui gère le workflow de données dans le pipeline. Il peut être utilisé à la fois pour la diffusion et l’encodage de fichiers.
ms.assetid: dac99908-be90-415d-8837-2f97d573feb5
title: Session multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3df4597e5461788f990f620875bce946570ab97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106535745"
---
# <a name="media-session"></a><span data-ttu-id="ef7fd-104">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="ef7fd-104">Media Session</span></span>

<span data-ttu-id="ef7fd-105">La session multimédia est un objet qui gère le workflow de données dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="ef7fd-105">The Media Session is an object that manages data flow in the pipeline.</span></span> <span data-ttu-id="ef7fd-106">Il peut être utilisé à la fois pour la diffusion et l’encodage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ef7fd-106">It can be used for both playing and encoding files.</span></span>

<span data-ttu-id="ef7fd-107">Cette section décrit la session multimédia du point de vue architectural.</span><span class="sxs-lookup"><span data-stu-id="ef7fd-107">This section describes the Media Session from an architectural standpoint.</span></span> <span data-ttu-id="ef7fd-108">Il contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="ef7fd-108">It contains the following sections:</span></span>



| <span data-ttu-id="ef7fd-109">Rubrique</span><span class="sxs-lookup"><span data-stu-id="ef7fd-109">Topic</span></span>                                                                                        | <span data-ttu-id="ef7fd-110">Description</span><span class="sxs-lookup"><span data-stu-id="ef7fd-110">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef7fd-111">À propos de la session multimédia</span><span class="sxs-lookup"><span data-stu-id="ef7fd-111">About the Media Session</span></span>](about-the-media-session.md)                                       | <span data-ttu-id="ef7fd-112">Fournit une vue d’ensemble de la session multimédia, de la façon dont une application peut créer la session multimédia et de la façon dont la session multimédia gère l’heure de la présentation.</span><span class="sxs-lookup"><span data-stu-id="ef7fd-112">Provides an overview of the Media Session, how an application can create the Media Session, and how the Media Session manages presentation time.</span></span> |
| [<span data-ttu-id="ef7fd-113">Topologies</span><span class="sxs-lookup"><span data-stu-id="ef7fd-113">Topologies</span></span>](topologies.md)                                                                 | <span data-ttu-id="ef7fd-114">Une topologie est un objet qui représente le workflow de données dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="ef7fd-114">A topology is an object that represents the flow of data in the pipeline.</span></span>                                                                        |
| [<span data-ttu-id="ef7fd-115">Événements de session multimédia</span><span class="sxs-lookup"><span data-stu-id="ef7fd-115">Media Session Events</span></span>](media-session-events.md)                                             | <span data-ttu-id="ef7fd-116">Décrit les événements qu’une application peut recevoir de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="ef7fd-116">Describes the events that an application might receive from the Media Session.</span></span>                                                                   |
| [<span data-ttu-id="ef7fd-117">Comment contrôler les États de présentation</span><span class="sxs-lookup"><span data-stu-id="ef7fd-117">How to Control Presentation States</span></span>](how-to-control-presentation-states.md)                 | <span data-ttu-id="ef7fd-118">Décrit les contrôles de transport de session de média : lecture, pause et arrêt.</span><span class="sxs-lookup"><span data-stu-id="ef7fd-118">Describes the Media Session transport controls: Play, Pause, and Stop.</span></span>                                                                           |
| [<span data-ttu-id="ef7fd-119">Utilisation de sources multimédias avec la session multimédia</span><span class="sxs-lookup"><span data-stu-id="ef7fd-119">Using Media Sources with the Media Session</span></span>](using-media-sources-with-the-media-session.md) | <span data-ttu-id="ef7fd-120">Comment utiliser des sources multimédias avec la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="ef7fd-120">How to use media sources with the Media Session.</span></span>                                                                                                 |
| [<span data-ttu-id="ef7fd-121">Contrôle de la fréquence</span><span class="sxs-lookup"><span data-stu-id="ef7fd-121">Rate Control</span></span>](rate-control.md)                                                             | <span data-ttu-id="ef7fd-122">Décrit comment contrôler la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="ef7fd-122">Describes how to control playback rate.</span></span>                                                                                                          |
| [<span data-ttu-id="ef7fd-123">Gestion de la qualité vidéo</span><span class="sxs-lookup"><span data-stu-id="ef7fd-123">Video Quality Management</span></span>](video-quality-management.md)                                     | <span data-ttu-id="ef7fd-124">Décrit les améliorations apportées au pipeline vidéo dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ef7fd-124">Describes improvements to the video pipeline in Windows 7.</span></span>                                                                                       |
| [<span data-ttu-id="ef7fd-125">Session média PMP</span><span class="sxs-lookup"><span data-stu-id="ef7fd-125">PMP Media Session</span></span>](pmp-media-session.md)                                                   | <span data-ttu-id="ef7fd-126">Décrit comment créer la session multimédia à l’intérieur d’un processus PMP (Protected Media Path).</span><span class="sxs-lookup"><span data-stu-id="ef7fd-126">Describes how to create the Media Session inside a Protected Media Path (PMP) process.</span></span>                                                           |



 

<span data-ttu-id="ef7fd-127">Les rubriques suivantes décrivent comment utiliser la session multimédia dans des scénarios d’application spécifiques :</span><span class="sxs-lookup"><span data-stu-id="ef7fd-127">The following topics describe how to use the Media Session in specific application scenarios:</span></span>

-   [<span data-ttu-id="ef7fd-128">Lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="ef7fd-128">Audio/Video Playback</span></span>](audio-video-playback.md)
-   [<span data-ttu-id="ef7fd-129">Codage et création de fichier</span><span class="sxs-lookup"><span data-stu-id="ef7fd-129">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)

## <a name="related-topics"></a><span data-ttu-id="ef7fd-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef7fd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef7fd-131">Architecture Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ef7fd-131">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="ef7fd-132">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="ef7fd-132">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> </dl>

 

 



