---
description: Types de médias
ms.assetid: 690fda6e-dcbd-44dc-968d-cc949126da81
title: Types de médias (Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acbfb1b637eef6acb664d3d95a0488f155c6916
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321625"
---
# <a name="media-types-media-foundation"></a><span data-ttu-id="db29a-103">Types de médias (Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="db29a-103">Media Types (Media Foundation)</span></span>

<span data-ttu-id="db29a-104">Un *type de média* est un moyen de décrire le format d’un flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="db29a-104">A *media type* is a way to describe the format of a media stream.</span></span> <span data-ttu-id="db29a-105">Dans Media Foundation, les types de média sont représentés par l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="db29a-105">In Media Foundation, media types are represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="db29a-106">Les applications utilisent des types de médias pour découvrir le format d’un fichier multimédia ou d’un flux de média.</span><span class="sxs-lookup"><span data-stu-id="db29a-106">Applications use media types to discover the format of a media file or media stream.</span></span> <span data-ttu-id="db29a-107">Les objets du pipeline Media Foundation utilisent des types de média pour négocier les formats qu’ils distribueront ou recevront.</span><span class="sxs-lookup"><span data-stu-id="db29a-107">Objects in the Media Foundation pipeline use media types to negotiate the formats they will deliver or receive.</span></span>

<span data-ttu-id="db29a-108">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="db29a-108">This section contains the following topics.</span></span>



| <span data-ttu-id="db29a-109">Rubrique</span><span class="sxs-lookup"><span data-stu-id="db29a-109">Topic</span></span>                                                                    | <span data-ttu-id="db29a-110">Description</span><span class="sxs-lookup"><span data-stu-id="db29a-110">Description</span></span>                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="db29a-111">À propos des types de média</span><span class="sxs-lookup"><span data-stu-id="db29a-111">About Media Types</span></span>](about-media-types.md)                               | <span data-ttu-id="db29a-112">Vue d’ensemble générale des types de médias dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="db29a-112">General overview of media types in Media Foundation.</span></span>                             |
| [<span data-ttu-id="db29a-113">GUID de type de média</span><span class="sxs-lookup"><span data-stu-id="db29a-113">Media Type GUIDs</span></span>](media-type-guids.md)                                 | <span data-ttu-id="db29a-114">Répertorie les GUID définis pour les principaux types et sous-types.</span><span class="sxs-lookup"><span data-stu-id="db29a-114">Lists the defined GUIDs for major types and subtypes.</span></span>                            |
| [<span data-ttu-id="db29a-115">Types de média audio</span><span class="sxs-lookup"><span data-stu-id="db29a-115">Audio Media Types</span></span>](audio-media-types.md)                               | <span data-ttu-id="db29a-116">Comment créer des types de média pour les formats audio.</span><span class="sxs-lookup"><span data-stu-id="db29a-116">How to create media types for audio formats.</span></span>                                     |
| [<span data-ttu-id="db29a-117">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="db29a-117">Video Media Types</span></span>](video-media-types.md)                               | <span data-ttu-id="db29a-118">Comment créer des types de média pour les formats vidéo.</span><span class="sxs-lookup"><span data-stu-id="db29a-118">How to create media types for video formats.</span></span>                                     |
| [<span data-ttu-id="db29a-119">Types de média complets et partiels</span><span class="sxs-lookup"><span data-stu-id="db29a-119">Complete and Partial Media Types</span></span>](complete-and-partial-media-types.md) | <span data-ttu-id="db29a-120">Décrit la différence entre les types de média complets et les types de média partiels.</span><span class="sxs-lookup"><span data-stu-id="db29a-120">Describes the difference between complete media types and partial media types.</span></span>   |
| [<span data-ttu-id="db29a-121">Conversions de type de média</span><span class="sxs-lookup"><span data-stu-id="db29a-121">Media Type Conversions</span></span>](media-type-conversions.md)                     | <span data-ttu-id="db29a-122">Comment effectuer une conversion entre des types de média Media Foundation et des structures de format plus anciennes.</span><span class="sxs-lookup"><span data-stu-id="db29a-122">How to convert between Media Foundation media types and older format structures.</span></span> |
| [<span data-ttu-id="db29a-123">Fonctions d’assistance du type de média</span><span class="sxs-lookup"><span data-stu-id="db29a-123">Media Type Helper Functions</span></span>](media-type-helper-functions.md)           | <span data-ttu-id="db29a-124">Liste des fonctions qui manipulent ou obtiennent des informations à partir d’un type de média.</span><span class="sxs-lookup"><span data-stu-id="db29a-124">A list of functions that manipulate or get information from a media type.</span></span>        |
| [<span data-ttu-id="db29a-125">Code de débogage du type de média</span><span class="sxs-lookup"><span data-stu-id="db29a-125">Media Type Debugging Code</span></span>](media-type-debugging-code.md)               | <span data-ttu-id="db29a-126">Exemple de code qui montre comment afficher un type de média lors du débogage.</span><span class="sxs-lookup"><span data-stu-id="db29a-126">Example code that shows how to view a media type while debugging.</span></span>                |



 

## <a name="related-topics"></a><span data-ttu-id="db29a-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db29a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db29a-128">Primitives de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="db29a-128">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> <dt>

[<span data-ttu-id="db29a-129">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="db29a-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 



