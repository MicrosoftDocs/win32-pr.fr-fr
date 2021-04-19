---
description: Utilisation du convertisseur de mixage vidéo
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: Utilisation du convertisseur de mixage vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5baf7d559eed0d3111876924520952b55c6da2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518771"
---
# <a name="using-the-video-mixing-renderer"></a><span data-ttu-id="c1645-103">Utilisation du convertisseur de mixage vidéo</span><span class="sxs-lookup"><span data-stu-id="c1645-103">Using the Video Mixing Renderer</span></span>

<span data-ttu-id="c1645-104">En termes de performances et d’étendue des fonctionnalités, le filtre de mixage vidéo (VMR) représente la prochaine génération de rendu vidéo sur la plateforme Windows.</span><span class="sxs-lookup"><span data-stu-id="c1645-104">In terms of both performance and breadth of features, the Video Mixing Renderer (VMR) filter represents the next generation in video rendering on the Windows platform.</span></span> <span data-ttu-id="c1645-105">VMR remplace le [mélangeur de recouvrement](overlay-mixer-filter.md) et le [convertisseur vidéo](video-renderer-filter.md), et ajoute de nombreuses nouvelles fonctionnalités de mixage.</span><span class="sxs-lookup"><span data-stu-id="c1645-105">The VMR replaces the [Overlay Mixer](overlay-mixer-filter.md) and [Video Renderer](video-renderer-filter.md), and adds many new mixing features.</span></span>

<span data-ttu-id="c1645-106">Il existe deux versions de VMR :</span><span class="sxs-lookup"><span data-stu-id="c1645-106">There are two versions of the VMR:</span></span>

-   <span data-ttu-id="c1645-107">VMR-7, qui utilise DirectDraw 7 pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="c1645-107">The VMR-7, which uses DirectDraw 7 for rendering.</span></span>
-   <span data-ttu-id="c1645-108">VMR-9, qui utilise Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c1645-108">The VMR-9, which uses Direct3D 9.</span></span>

<span data-ttu-id="c1645-109">VMR-7 est disponible sur Windows XP et versions ultérieures, mais n’est pas disponible pour la redistribution.</span><span class="sxs-lookup"><span data-stu-id="c1645-109">The VMR-7 is available on Windows XP and later, but is not available for redistribution.</span></span> <span data-ttu-id="c1645-110">VMR-9 est disponible pour la redistribution sur toutes les plateformes prises en charge par DirectX 9.</span><span class="sxs-lookup"><span data-stu-id="c1645-110">The VMR-9 is available for redistribution on all platforms supported by DirectX 9.</span></span> <span data-ttu-id="c1645-111">Les deux filtres VMR sont très similaires dans leur implémentation et les interfaces qu’ils exposent.</span><span class="sxs-lookup"><span data-stu-id="c1645-111">The two VMR filters are very similar in their implementation and the interfaces that they expose.</span></span>

<span data-ttu-id="c1645-112">VMR-9 possède son propre CLSID et son propre ensemble d’interfaces, de structures et de types d’énumération qui ne sont pas toujours identiques aux types de données correspondants pour VMR-7, en raison des différences sous-jacentes entre DirectDraw 7 et Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c1645-112">The VMR-9 has its own CLSID and its own set of interfaces, structures and enumeration types which are not always identical to the corresponding data types for the VMR-7, due to the underlying differences between DirectDraw 7 and Direct3D 9.</span></span> <span data-ttu-id="c1645-113">Les interfaces VMR-9 se terminent toutes par « 9 », par exemple **IVMRStreamConfig9**, et les types de structures et d’énumération ont tous « VMR9 » dans leur nom pour les distinguer des types de données utilisés avec VMR-7.</span><span class="sxs-lookup"><span data-stu-id="c1645-113">The VMR-9 interfaces all end with "9", for example **IVMRStreamConfig9**, and the structures and enumeration types all have "VMR9" in their name to distinguish them from the data types used with the VMR-7.</span></span>

<span data-ttu-id="c1645-114">Pour garantir la compatibilité descendante, VMR-9 n’est pas le convertisseur par défaut sur un système.</span><span class="sxs-lookup"><span data-stu-id="c1645-114">To ensure backward-compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="c1645-115">Pour utiliser VMR-9, vous devez l’ajouter explicitement au graphique de filtre à l’aide de la méthode [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , puis le configurer avant de le connecter à des filtres en amont.</span><span class="sxs-lookup"><span data-stu-id="c1645-115">To use the VMR-9, you must explicitly add it to the filter graph using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method, and configure it before connecting it to any upstream filters.</span></span>

<span data-ttu-id="c1645-116">Cet article contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c1645-116">This article contains the following sections.</span></span> <span data-ttu-id="c1645-117">Sauf mention contraire, les informations contenues dans ces sections s’appliquent aux filtres VMR-7 et VMR-9.</span><span class="sxs-lookup"><span data-stu-id="c1645-117">Except where noted, the information in these sections applies to both the VMR-7 and the VMR-9 filters.</span></span>

-   [<span data-ttu-id="c1645-118">À propos du rendu de mixage vidéo</span><span class="sxs-lookup"><span data-stu-id="c1645-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
-   [<span data-ttu-id="c1645-119">Modes de fonctionnement VMR</span><span class="sxs-lookup"><span data-stu-id="c1645-119">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
-   [<span data-ttu-id="c1645-120">Création d’un graphique de filtre VMR-9</span><span class="sxs-lookup"><span data-stu-id="c1645-120">Building a VMR-9 Filter Graph</span></span>](building-a-vmr-9-filter-graph.md)
-   [<span data-ttu-id="c1645-121">Utilisation du mode de mixage VMR</span><span class="sxs-lookup"><span data-stu-id="c1645-121">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
-   [<span data-ttu-id="c1645-122">Définition des préférences de désentrelacement</span><span class="sxs-lookup"><span data-stu-id="c1645-122">Setting Deinterlace Preferences</span></span>](setting-deinterlace-preferences.md)
-   [<span data-ttu-id="c1645-123">Utilisation de VMR pour les développeurs de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="c1645-123">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
-   [<span data-ttu-id="c1645-124">Utilisation du protocole COPP (Certified Output Protection Protocol)</span><span class="sxs-lookup"><span data-stu-id="c1645-124">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a><span data-ttu-id="c1645-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c1645-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1645-126">Filtre de convertisseur de mixage vidéo 7</span><span class="sxs-lookup"><span data-stu-id="c1645-126">Video Mixing Renderer Filter 7</span></span>](video-mixing-renderer-filter-7.md)
</dt> <dt>

[<span data-ttu-id="c1645-127">Filtre de convertisseur de mixage vidéo 9</span><span class="sxs-lookup"><span data-stu-id="c1645-127">Video Mixing Renderer Filter 9</span></span>](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



