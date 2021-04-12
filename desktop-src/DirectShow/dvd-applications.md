---
description: Applications DVD
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: Applications DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acaddc683078acff84b7c90689f82becfb7b1d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317717"
---
# <a name="dvd-applications"></a><span data-ttu-id="250e8-103">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="250e8-103">DVD Applications</span></span>

<span data-ttu-id="250e8-104">DirectShow fournit un composant appelé filtre de la source du [navigateur DVD](dvd-navigator-filter.md) , qui simplifie les tâches de navigation sur les DVD en C++.</span><span class="sxs-lookup"><span data-stu-id="250e8-104">DirectShow provides a component called the [DVD Navigator](dvd-navigator-filter.md) source filter which simplifies DVD navigation tasks in C++.</span></span> <span data-ttu-id="250e8-105">Le navigateur DVD offre toutes les fonctionnalités que vous trouvez sur un lecteur de DVD autonome complet, ainsi que des fonctionnalités supplémentaires spécifiques à la lecture de DVD sur des ordinateurs personnels.</span><span class="sxs-lookup"><span data-stu-id="250e8-105">The DVD Navigator has all the capabilities that you find on a full-featured stand-alone DVD player, plus additional capabilities specific to playing DVDs on personal computers.</span></span> <span data-ttu-id="250e8-106">Grâce au navigateur DVD, les développeurs de scripts et C++ peuvent créer des applications DVD complètes sans faire référence à la spécification DVD.</span><span class="sxs-lookup"><span data-stu-id="250e8-106">Using the DVD Navigator, C++ and scripting developers can create full-featured DVD applications without referring to the DVD specification.</span></span> <span data-ttu-id="250e8-107">Le navigateur DVD, en coordination avec les filtres de décodeur, gère également la gestion régionale et la protection des droits d’auteur (CSS et protection de copie analogique), en isolant les développeurs d’applications de ces détails.</span><span class="sxs-lookup"><span data-stu-id="250e8-107">The DVD Navigator, in coordination with the decoder filters, also handles regional management and copyright protection (CSS and analog copy protection), isolating application developers from these details.</span></span>

<span data-ttu-id="250e8-108">Le filtre de navigateur DVD fonctionne sur l’intégralité d’un volume DVD-Video, qui se compose des fichiers du répertoire de la vidéo \_ TS.</span><span class="sxs-lookup"><span data-stu-id="250e8-108">The DVD Navigator filter works across an entire DVD-Video volume, which consists of the files in the VIDEO\_TS directory.</span></span> <span data-ttu-id="250e8-109">Contrairement à la plupart des filtres sources DirectShow qui fonctionnent avec des fichiers ou flux individuels, le navigateur DVD utilise la structure DVD-Video des titres, des chapitres et des codes de temps.</span><span class="sxs-lookup"><span data-stu-id="250e8-109">Unlike most DirectShow source filters that work with individual streams or files, the DVD Navigator uses the DVD-Video structure of titles, chapters, and time codes.</span></span> <span data-ttu-id="250e8-110">Les développeurs souhaitant lire des fichiers MPEG-2 individuels dans DirectShow doivent utiliser le [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md) au lieu du filtre de navigateur DVD.</span><span class="sxs-lookup"><span data-stu-id="250e8-110">Developers wishing to play individual MPEG-2 files in DirectShow should use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead of the DVD Navigator filter.</span></span> <span data-ttu-id="250e8-111">Pour plus d’informations, consultez [prise en charge de MPEG-2 dans DirectShow](mpeg-2-support-in-directshow.md) .</span><span class="sxs-lookup"><span data-stu-id="250e8-111">See [MPEG-2 Support in DirectShow](mpeg-2-support-in-directshow.md) for more information.</span></span>

> [!Note]  
> <span data-ttu-id="250e8-112">Pour lire des DVD, l’utilisateur doit disposer d’un décodeur MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="250e8-112">To play DVDs, the user must have an MPEG-2 decoder.</span></span>

 

<span data-ttu-id="250e8-113">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="250e8-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="250e8-114">Fonctionnalités de prise en charge des DVD dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="250e8-114">DVD Support Features in DirectShow</span></span>](dvd-support-features-in-directshow.md)
-   [<span data-ttu-id="250e8-115">Notions de base sur les DVD</span><span class="sxs-lookup"><span data-stu-id="250e8-115">DVD Basics</span></span>](dvd-basics.md)
-   [<span data-ttu-id="250e8-116">Génération du graphique de filtre de DVD</span><span class="sxs-lookup"><span data-stu-id="250e8-116">Building the DVD Filter Graph</span></span>](building-the-dvd-filter-graph.md)
-   [<span data-ttu-id="250e8-117">Obtention des pointeurs d’interface DVD</span><span class="sxs-lookup"><span data-stu-id="250e8-117">Obtaining the DVD Interface Pointers</span></span>](obtaining-the-dvd-interface-pointers.md)
-   [<span data-ttu-id="250e8-118">Commandes de DVD</span><span class="sxs-lookup"><span data-stu-id="250e8-118">DVD Commands</span></span>](dvd-commands.md)
-   [<span data-ttu-id="250e8-119">Identification des opérations DVD valides</span><span class="sxs-lookup"><span data-stu-id="250e8-119">Identifying Valid DVD Operations</span></span>](identifying-valid-dvd-operations.md)
-   [<span data-ttu-id="250e8-120">Synchronisation des commandes de DVD</span><span class="sxs-lookup"><span data-stu-id="250e8-120">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
-   [<span data-ttu-id="250e8-121">Data Flow dans le navigateur DVD</span><span class="sxs-lookup"><span data-stu-id="250e8-121">Data Flow in the DVD Navigator</span></span>](data-flow-in-the-dvd-navigator.md)
-   [<span data-ttu-id="250e8-122">Gestion des notifications d’événements DVD</span><span class="sxs-lookup"><span data-stu-id="250e8-122">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
-   [<span data-ttu-id="250e8-123">Utilisation des menus de DVD</span><span class="sxs-lookup"><span data-stu-id="250e8-123">Working With DVD Menus</span></span>](working-with-dvd-menus.md)
-   [<span data-ttu-id="250e8-124">Flux audio et sous-image</span><span class="sxs-lookup"><span data-stu-id="250e8-124">Audio and Subpicture Streams</span></span>](audio-and-subpicture-streams.md)
-   [<span data-ttu-id="250e8-125">Application des niveaux de gestion parentale</span><span class="sxs-lookup"><span data-stu-id="250e8-125">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
-   [<span data-ttu-id="250e8-126">Enregistrement et restauration d’objets DvdState</span><span class="sxs-lookup"><span data-stu-id="250e8-126">Saving and Restoring DvdState Objects</span></span>](saving-and-restoring-dvdstate-objects.md)
-   [<span data-ttu-id="250e8-127">Utilisation des chaînes de texte de DVD</span><span class="sxs-lookup"><span data-stu-id="250e8-127">Working with DVD Text Strings</span></span>](working-with-dvd-text-strings.md)
-   [<span data-ttu-id="250e8-128">Lecture des flux audio karaoké</span><span class="sxs-lookup"><span data-stu-id="250e8-128">Playing Karaoke Audio Streams</span></span>](playing-karaoke-audio-streams.md)
-   [<span data-ttu-id="250e8-129">Gestion des éjections de disque</span><span class="sxs-lookup"><span data-stu-id="250e8-129">Handling Disc Ejections</span></span>](handling-disc-ejections.md)
-   [<span data-ttu-id="250e8-130">Améliorations de la lecture de DVD dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="250e8-130">DVD Playback Enhancements in Windows Vista</span></span>](dvd-playback-enhancements-in-windows-vista.md)
-   [<span data-ttu-id="250e8-131">Configuration du graphique de filtre DVD</span><span class="sxs-lookup"><span data-stu-id="250e8-131">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
-   [<span data-ttu-id="250e8-132">Raccourcis vers les pages de référence des DVD C++</span><span class="sxs-lookup"><span data-stu-id="250e8-132">Shortcuts to C++ DVD Reference Pages</span></span>](shortcuts-to-c-dvd-reference-pages.md)

<span data-ttu-id="250e8-133">Pour obtenir des références sur le développement d’un décodeur de DVD/MPEG2, consultez [développement d’un décodeur de DVD dans DirectShow](dvd-decoder-development-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="250e8-133">For references on DVD/MPEG2 decoder development, see [DVD Decoder Development in DirectShow](dvd-decoder-development-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="250e8-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="250e8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="250e8-135">Utilisation de DirectShow</span><span class="sxs-lookup"><span data-stu-id="250e8-135">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



