---
description: Écriture de filtres de transformation
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Écriture de filtres de transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d007181e437ef5691f532fec00923aa2b8012f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952185"
---
# <a name="writing-transform-filters"></a><span data-ttu-id="90e60-103">Écriture de filtres de transformation</span><span class="sxs-lookup"><span data-stu-id="90e60-103">Writing Transform Filters</span></span>

<span data-ttu-id="90e60-104">Cette section décrit comment écrire un filtre de transformation, défini en tant que filtre avec une seule broche d’entrée et une seule broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="90e60-104">This section describes how to write a transform filter, defined as a filter that has exactly one input pin and one output pin.</span></span> <span data-ttu-id="90e60-105">Pour illustrer les étapes, cette section décrit un filtre de transformation hypothétique qui produit une vidéo encodée en longueur d’exécution (RLE).</span><span class="sxs-lookup"><span data-stu-id="90e60-105">To illustrate the steps, this section describes a hypothetical transform filter that outputs run-length encoded (RLE) video.</span></span> <span data-ttu-id="90e60-106">Elle ne décrit pas l’algorithme d’encodage RLE proprement dit, mais uniquement les tâches qui sont spécifiques à DirectShow.</span><span class="sxs-lookup"><span data-stu-id="90e60-106">It does not describe the RLE-encoding algorithm itself, only the tasks that are specific to DirectShow.</span></span> <span data-ttu-id="90e60-107">(DirectShow fournit déjà un codec RLE par le biais du filtre de [compresseur AVI](avi-compressor-filter.md) .)</span><span class="sxs-lookup"><span data-stu-id="90e60-107">(DirectShow already provides an RLE codec through the [AVI Compressor](avi-compressor-filter.md) filter.)</span></span>

<span data-ttu-id="90e60-108">Cette section part du principe que vous allez utiliser la bibliothèque de classes de base DirectShow pour créer des filtres.</span><span class="sxs-lookup"><span data-stu-id="90e60-108">This section assumes that you will use the DirectShow base class library to create filters.</span></span> <span data-ttu-id="90e60-109">Bien que vous puissiez écrire un filtre sans celui-ci, la bibliothèque de classes de base est fortement recommandée.</span><span class="sxs-lookup"><span data-stu-id="90e60-109">Although you can write a filter without it, the base class library is strongly recommended.</span></span>

> [!Note]  
> <span data-ttu-id="90e60-110">Avant d’écrire un filtre de transformation, déterminez si un objet multimédia DirectX (DMO) répondra à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="90e60-110">Before writing a transform filter, consider whether a DirectX Media Object (DMO) would fulfill your requirements.</span></span> <span data-ttu-id="90e60-111">DMOs peut faire beaucoup des mêmes choses que les filtres et le modèle de programmation pour DMOs est plus simple.</span><span class="sxs-lookup"><span data-stu-id="90e60-111">DMOs can do many of the same things as filters, and the programming model for DMOs is simpler.</span></span> <span data-ttu-id="90e60-112">Les DMOs sont hébergés dans DirectShow via le filtre de [Wrapper DMO](dmo-wrapper-filter.md) , mais peuvent également être utilisés en dehors de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="90e60-112">DMOs are hosted in DirectShow through the [DMO Wrapper](dmo-wrapper-filter.md) filter, but can also be used outside of DirectShow.</span></span> <span data-ttu-id="90e60-113">Les DMOs sont désormais la solution recommandée pour les encodeurs et les décodeurs.</span><span class="sxs-lookup"><span data-stu-id="90e60-113">DMOs are now the recommended solution for encoders and decoders.</span></span>

 

<span data-ttu-id="90e60-114">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="90e60-114">This section includes the following topics:</span></span>

-   [<span data-ttu-id="90e60-115">Étape 1. Choisir une classe de base</span><span class="sxs-lookup"><span data-stu-id="90e60-115">Step 1. Choose a Base Class</span></span>](step-1--choose-a-base-class.md)
-   [<span data-ttu-id="90e60-116">Étape 2. Déclarer la classe de filtre</span><span class="sxs-lookup"><span data-stu-id="90e60-116">Step 2. Declare the Filter Class</span></span>](step-2--declare-the-filter-class.md)
-   [<span data-ttu-id="90e60-117">Étape 3. Prendre en charge la négociation de type de média</span><span class="sxs-lookup"><span data-stu-id="90e60-117">Step 3. Support Media Type Negotiation</span></span>](step-3--support-media-type-negotiation.md)
-   [<span data-ttu-id="90e60-118">Étape 4. Définir les propriétés d’allocateur</span><span class="sxs-lookup"><span data-stu-id="90e60-118">Step 4. Set Allocator Properties</span></span>](step-4--set-allocator-properties.md)
-   [<span data-ttu-id="90e60-119">Étape 5. Transformer l’image</span><span class="sxs-lookup"><span data-stu-id="90e60-119">Step 5. Transform the Image</span></span>](step-5--transform-the-image.md)
-   [<span data-ttu-id="90e60-120">Étape 6. Ajouter la prise en charge de COM</span><span class="sxs-lookup"><span data-stu-id="90e60-120">Step 6. Add Support for COM</span></span>](step-6--add-support-for-com.md)

## <a name="related-topics"></a><span data-ttu-id="90e60-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90e60-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90e60-122">Génération de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="90e60-122">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="90e60-123">Classes de base DirectShow</span><span class="sxs-lookup"><span data-stu-id="90e60-123">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="90e60-124">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="90e60-124">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



