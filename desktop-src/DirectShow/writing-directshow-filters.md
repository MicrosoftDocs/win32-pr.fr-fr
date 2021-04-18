---
description: Écriture de filtres DirectShow
ms.assetid: ffbc92b2-4f45-439b-b140-49a66fc4d914
title: Écriture de filtres DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b266f3bbb9781dddcd2d0fb065b63d895a732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519787"
---
# <a name="writing-directshow-filters"></a><span data-ttu-id="2dea0-103">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="2dea0-103">Writing DirectShow Filters</span></span>

<span data-ttu-id="2dea0-104">Si vous développez un filtre à utiliser dans un graphique de filtre Microsoft DirectShow, lisez les Articles de cette section.</span><span class="sxs-lookup"><span data-stu-id="2dea0-104">If you are developing a filter for use in a Microsoft DirectShow filter graph, read the articles in this section.</span></span> <span data-ttu-id="2dea0-105">En général, vous n’avez pas besoin de lire cette section si vous écrivez une application DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2dea0-105">In general, you do not have to read this section if you are writing a DirectShow application.</span></span> <span data-ttu-id="2dea0-106">La plupart des applications n’accèdent pas aux filtres ou au graphique de filtre au niveau abordé dans cette section.</span><span class="sxs-lookup"><span data-stu-id="2dea0-106">Most applications do not access filters or the filter graph at the level discussed in this section.</span></span>

-   [<span data-ttu-id="2dea0-107">Présentation du développement de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="2dea0-107">Introduction to DirectShow Filter Development</span></span>](introduction-to-directshow-filter-development.md)
-   [<span data-ttu-id="2dea0-108">Génération de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="2dea0-108">Building DirectShow Filters</span></span>](building-directshow-filters.md)
-   [<span data-ttu-id="2dea0-109">Connexion des filtres</span><span class="sxs-lookup"><span data-stu-id="2dea0-109">How Filters Connect</span></span>](how-filters-connect.md)
-   [<span data-ttu-id="2dea0-110">Transmission de données pour les développeurs de filtres</span><span class="sxs-lookup"><span data-stu-id="2dea0-110">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="2dea0-111">Threads et sections critiques</span><span class="sxs-lookup"><span data-stu-id="2dea0-111">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
-   [<span data-ttu-id="2dea0-112">Gestion du contrôle de la qualité</span><span class="sxs-lookup"><span data-stu-id="2dea0-112">Quality-Control Management</span></span>](quality-control-management.md)
-   [<span data-ttu-id="2dea0-113">DirectShow et COM</span><span class="sxs-lookup"><span data-stu-id="2dea0-113">DirectShow and COM</span></span>](directshow-and-com.md)
-   [<span data-ttu-id="2dea0-114">Écriture de filtres source</span><span class="sxs-lookup"><span data-stu-id="2dea0-114">Writing Source Filters</span></span>](writing-source-filters.md)
-   [<span data-ttu-id="2dea0-115">Écriture de filtres de transformation</span><span class="sxs-lookup"><span data-stu-id="2dea0-115">Writing Transform Filters</span></span>](writing-transform-filters.md)
-   [<span data-ttu-id="2dea0-116">Écriture de convertisseurs vidéo</span><span class="sxs-lookup"><span data-stu-id="2dea0-116">Writing Video Renderers</span></span>](writing-video-renderers.md)
-   [<span data-ttu-id="2dea0-117">Écriture de filtres de capture</span><span class="sxs-lookup"><span data-stu-id="2dea0-117">Writing Capture Filters</span></span>](writing-capture-filters.md)
-   [<span data-ttu-id="2dea0-118">Exposition des formats de capture et de compression</span><span class="sxs-lookup"><span data-stu-id="2dea0-118">Exposing Capture and Compression Formats</span></span>](exposing-capture-and-compression-formats.md)
-   [<span data-ttu-id="2dea0-119">Inscription d’un type de fichier personnalisé</span><span class="sxs-lookup"><span data-stu-id="2dea0-119">Registering a Custom File Type</span></span>](registering-a-custom-file-type.md)
-   [<span data-ttu-id="2dea0-120">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="2dea0-120">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)

 

 



