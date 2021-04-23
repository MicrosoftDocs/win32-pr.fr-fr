---
description: Filtre du writer de fichier
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtre du writer de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991536d505ee1bdfcaaaca5ce8660c4480decf6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909687"
---
# <a name="file-writer-filter"></a><span data-ttu-id="203cd-103">Filtre du writer de fichier</span><span class="sxs-lookup"><span data-stu-id="203cd-103">File Writer Filter</span></span>

<span data-ttu-id="203cd-104">Le filtre du writer de fichier peut être utilisé pour écrire des fichiers sur le disque, quel que soit le format.</span><span class="sxs-lookup"><span data-stu-id="203cd-104">The File Writer filter can be used to write files to disc regardless of format.</span></span> <span data-ttu-id="203cd-105">Le filtre écrit simplement sur le disque quelle que soit sa broche d’entrée, il doit donc être connecté en amont à un multiplexeur capable de mettre en forme le fichier correctement.</span><span class="sxs-lookup"><span data-stu-id="203cd-105">The filter simply writes to disc whatever it receives on its input pin, so it must be connected upstream to a multiplexer that can format the file correctly.</span></span> <span data-ttu-id="203cd-106">Vous pouvez créer un nouveau fichier de sortie avec le writer de fichier ou spécifier un fichier existant ; Si le fichier existe déjà, il sera entièrement remplacé par les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="203cd-106">You can create a new output file with the File Writer or specify an existing file; if the file already exists, it will be completely overwritten with the new data.</span></span>

<span data-ttu-id="203cd-107">Le filtre du writer de fichier utilise les horodatages du flux d’entrée comme décalages de fichiers et fournit un accès aléatoire au fichier.</span><span class="sxs-lookup"><span data-stu-id="203cd-107">The file writer filter uses the input stream's time stamps as file offsets and provides random access to the file.</span></span> <span data-ttu-id="203cd-108">Il prend en charge **IStream** pour autoriser la lecture et l’écriture de l’en-tête de fichier une fois que le graphique est arrêté.</span><span class="sxs-lookup"><span data-stu-id="203cd-108">It supports **IStream** to allow reading and writing the file header after the graph is stopped.</span></span> <span data-ttu-id="203cd-109">Pour améliorer les performances, il prend également en charge les écritures avec chevauchement non mises en mémoire tampon et gère la négociation de mémoire tampon correspondante.</span><span class="sxs-lookup"><span data-stu-id="203cd-109">To improve performance it also supports unbuffered overlapped writes and handles the corresponding buffer negotiation.</span></span>

> [!Note]  
> <span data-ttu-id="203cd-110">Pour écrire des fichiers ASF, utilisez le filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="203cd-110">To write ASF files, use the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

 



| <span data-ttu-id="203cd-111">Étiquette</span><span class="sxs-lookup"><span data-stu-id="203cd-111">Label</span></span> | <span data-ttu-id="203cd-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="203cd-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="203cd-113">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="203cd-113">Filter Interfaces</span></span>                        | <span data-ttu-id="203cd-114">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="203cd-114">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span></span> |
| <span data-ttu-id="203cd-115">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="203cd-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="203cd-116">\_Flux de MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="203cd-116">MEDIATYPE\_Stream, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                              |
| <span data-ttu-id="203cd-117">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="203cd-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="203cd-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span><span class="sxs-lookup"><span data-stu-id="203cd-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span></span>                                                                                |
| <span data-ttu-id="203cd-119">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="203cd-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="203cd-120">Non applicable</span><span class="sxs-lookup"><span data-stu-id="203cd-120">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="203cd-121">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="203cd-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="203cd-122">Non applicable</span><span class="sxs-lookup"><span data-stu-id="203cd-122">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="203cd-123">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="203cd-123">Filter CLSID</span></span>                             | <span data-ttu-id="203cd-124">CLSID \_ FileWriter</span><span class="sxs-lookup"><span data-stu-id="203cd-124">CLSID\_FileWriter</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="203cd-125">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="203cd-125">Property Page CLSID</span></span>                      | <span data-ttu-id="203cd-126">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="203cd-126">No property page</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="203cd-127">Exécutable</span><span class="sxs-lookup"><span data-stu-id="203cd-127">Executable</span></span>                               | <span data-ttu-id="203cd-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="203cd-128">qcap.dll</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="203cd-129">Mérite</span><span class="sxs-lookup"><span data-stu-id="203cd-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="203cd-130">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="203cd-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="203cd-131">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="203cd-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="203cd-132">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="203cd-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="203cd-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="203cd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="203cd-134">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="203cd-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



