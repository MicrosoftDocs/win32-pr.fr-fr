---
description: À propos de la source de Sequencer
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: À propos de la source de Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8de3e0ff46cab1e68b767294633ecd09ebc161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526613"
---
# <a name="about-the-sequencer-source"></a><span data-ttu-id="308d0-103">À propos de la source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="308d0-103">About the Sequencer Source</span></span>

<span data-ttu-id="308d0-104">La source de Sequencer permet à une application de lire une collection de [sources multimédias](media-sources.md) séquentiellement, avec des transitions transparents entre les sources.</span><span class="sxs-lookup"><span data-stu-id="308d0-104">The sequencer source enables an application to play a collection of [Media Sources](media-sources.md) sequentially, with seamless transitions between the sources.</span></span> <span data-ttu-id="308d0-105">La source de Sequencer peut être utilisée pour les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="308d0-105">The sequencer source can be used for the following scenarios:</span></span>

-   <span data-ttu-id="308d0-106">Créer une sélection qui bascule en toute transparence d’une source de média à la suivante.</span><span class="sxs-lookup"><span data-stu-id="308d0-106">Create a playlist that switches seamlessly from one media source to the next.</span></span>
-   <span data-ttu-id="308d0-107">Lire des flux à partir de plusieurs sources simultanément ; par exemple, lire l’audio d’un fichier avec la vidéo d’un autre fichier.</span><span class="sxs-lookup"><span data-stu-id="308d0-107">Play streams from multiple sources simultaneously; for example, play the audio from one file with the video from another.</span></span>
-   <span data-ttu-id="308d0-108">Basculer entre les flux dans différentes sources de média dans des entrées de playlist consécutives ; par exemple, une sélection peut avoir des entrées qui partagent la même source vidéo, tandis que chaque entrée contient une source audio différente.</span><span class="sxs-lookup"><span data-stu-id="308d0-108">Switch between streams in different media sources in consecutive playlist entries; for example, a playlist can have entries that share the same video source while each entry contains a different audio source.</span></span>

<span data-ttu-id="308d0-109">Pour chaque élément d’une sélection, l’application crée une topologie distincte.</span><span class="sxs-lookup"><span data-stu-id="308d0-109">For each element of a playlist, the application creates a separate topology.</span></span> <span data-ttu-id="308d0-110">Les sources multimédias de ces topologies sont appelées *sources natives* pour les distinguer de la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="308d0-110">The media sources in these topologies are referred to as *native sources*, to distinguish them from the sequencer source.</span></span> <span data-ttu-id="308d0-111">Pendant la lecture, l’ensemble de la séquence de topologies est appelé une *Présentation*, et chaque topologie de la séquence est appelée un *segment*.</span><span class="sxs-lookup"><span data-stu-id="308d0-111">During playback, the entire sequence of topologies is called a *presentation*, and each topology within the sequence is called a *segment*.</span></span>

<span data-ttu-id="308d0-112">La lecture est contrôlée par la [session multimédia](media-session.md), qui fournit des contrôles de transport, tels que lecture, pause et arrêt.</span><span class="sxs-lookup"><span data-stu-id="308d0-112">Playback is controlled by the [Media Session](media-session.md), which provides transport controls, such as play, pause, and stop.</span></span> <span data-ttu-id="308d0-113">La session multimédia gère également l’heure de présentation et envoie des événements à l’application.</span><span class="sxs-lookup"><span data-stu-id="308d0-113">The Media Session also manages the presentation time and sends events to the application.</span></span> <span data-ttu-id="308d0-114">(Les événements de la source de Sequencer sont transférés à l’application via la session multimédia.)</span><span class="sxs-lookup"><span data-stu-id="308d0-114">(Events from the sequencer source are forwarded to the application through the Media Session.)</span></span>

<span data-ttu-id="308d0-115">Pour créer une sélection, l’application crée une ou plusieurs topologies de lecture et les met en file d’attente sur la source de Sequencer dans l’ordre de lecture souhaité.</span><span class="sxs-lookup"><span data-stu-id="308d0-115">To create a playlist, the application creates one or more playback topologies and queues them on the sequencer source in the desired order of playback.</span></span> <span data-ttu-id="308d0-116">En interne, la source de Sequencer modifie les topologies afin que les nœuds sources pointent vers la source de Sequencer au lieu de la source native.</span><span class="sxs-lookup"><span data-stu-id="308d0-116">Internally, the sequencer source modifies the topologies so that the source nodes point to the sequencer source instead of the native source.</span></span> <span data-ttu-id="308d0-117">L’application envoie ces topologies modifiées, plutôt que les topologies d’origine, à la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="308d0-117">The application sends these modified topologies, rather than the original topologies, to the Media Session.</span></span> <span data-ttu-id="308d0-118">Cela permet à la source de Sequencer d’agréger les sources natives et de communiquer avec la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="308d0-118">This enables the sequencer source to aggregate the native sources and to communicate with the Media Session.</span></span>

<span data-ttu-id="308d0-119">Pour obtenir des transitions transparents entre les segments, la source de Sequencer préroll chaque segment.</span><span class="sxs-lookup"><span data-stu-id="308d0-119">To achieve seamless transitions between segments, the sequencer source prerolls each segment.</span></span> <span data-ttu-id="308d0-120">Pendant la lecture d’un segment, et avant qu’il soit temps de lire le segment suivant, la source de Sequencer déclenche un événement [MENewPresentation](menewpresentation.md) contenant un descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="308d0-120">While one segment is playing, and before it is time to play the following segment, the sequencer source fires an [MENewPresentation](menewpresentation.md) event that contains a presentation descriptor.</span></span> <span data-ttu-id="308d0-121">L’application utilise ce descripteur de présentation pour obtenir la topologie du segment suivant dans la présentation et met en file d’attente la topologie sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="308d0-121">The application uses this presentation descriptor to get the topology for the next segment in the presentation, and queues the topology on the Media Session.</span></span>

<span data-ttu-id="308d0-122">L’illustration suivante montre le workflow pour les entrées de playlist à travers la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="308d0-122">The following illustration shows the data flow for playlist entries through the sequencer source.</span></span> <span data-ttu-id="308d0-123">L’application utilise le programme de résolution source pour créer les sources natives, génère des topologies pour chaque segment et met les topologies en file d’attente sur la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="308d0-123">The application uses the source resolver to create the native sources, builds topologies for each segment, and queues the topologies on the sequencer source.</span></span>

![Diagramme montrant le workflow des segments imfmediasession, imfsequencersource et playlist conduisant à imfmediasource](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a><span data-ttu-id="308d0-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="308d0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="308d0-126">Comment créer une sélection</span><span class="sxs-lookup"><span data-stu-id="308d0-126">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="308d0-127">Topologies</span><span class="sxs-lookup"><span data-stu-id="308d0-127">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="308d0-128">Utilisation de la source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="308d0-128">Using the Sequencer Source</span></span>](using-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="308d0-129">Source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="308d0-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



