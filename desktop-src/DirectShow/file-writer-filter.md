---
description: Filtre du writer de fichier
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtre du writer de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f438f13f8d63b2856efd147c57ba6f071af26ff8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200809"
---
# <a name="file-writer-filter"></a><span data-ttu-id="ca9a7-103">Filtre du writer de fichier</span><span class="sxs-lookup"><span data-stu-id="ca9a7-103">File Writer Filter</span></span>

<span data-ttu-id="ca9a7-104">Le filtre du writer de fichier peut être utilisé pour écrire des fichiers sur le disque, quel que soit le format.</span><span class="sxs-lookup"><span data-stu-id="ca9a7-104">The File Writer filter can be used to write files to disc regardless of format.</span></span> <span data-ttu-id="ca9a7-105">Le filtre écrit simplement sur le disque quelle que soit sa broche d’entrée, il doit donc être connecté en amont à un multiplexeur capable de mettre en forme le fichier correctement.</span><span class="sxs-lookup"><span data-stu-id="ca9a7-105">The filter simply writes to disc whatever it receives on its input pin, so it must be connected upstream to a multiplexer that can format the file correctly.</span></span> <span data-ttu-id="ca9a7-106">Vous pouvez créer un nouveau fichier de sortie avec le writer de fichier ou spécifier un fichier existant ; Si le fichier existe déjà, il sera entièrement remplacé par les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="ca9a7-106">You can create a new output file with the File Writer or specify an existing file; if the file already exists, it will be completely overwritten with the new data.</span></span>

<span data-ttu-id="ca9a7-107">Le filtre du writer de fichier utilise les horodatages du flux d’entrée comme décalages de fichiers et fournit un accès aléatoire au fichier.</span><span class="sxs-lookup"><span data-stu-id="ca9a7-107">The file writer filter uses the input stream's time stamps as file offsets and provides random access to the file.</span></span> <span data-ttu-id="ca9a7-108">Il prend en charge **IStream** pour autoriser la lecture et l’écriture de l’en-tête de fichier une fois que le graphique est arrêté.</span><span class="sxs-lookup"><span data-stu-id="ca9a7-108">It supports **IStream** to allow reading and writing the file header after the graph is stopped.</span></span> <span data-ttu-id="ca9a7-109">Pour améliorer les performances, il prend également en charge les écritures avec chevauchement non mises en mémoire tampon et gère la négociation de mémoire tampon correspondante.</span><span class="sxs-lookup"><span data-stu-id="ca9a7-109">To improve performance it also supports unbuffered overlapped writes and handles the corresponding buffer negotiation.</span></span>

> [!Note]  
> <span data-ttu-id="ca9a7-110">Pour écrire des fichiers ASF, utilisez le filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="ca9a7-110">To write ASF files, use the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

 



|                                          |                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca9a7-111">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="ca9a7-111">Filter Interfaces</span></span>                        | <span data-ttu-id="ca9a7-112">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="ca9a7-112">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span></span> |
| <span data-ttu-id="ca9a7-113">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="ca9a7-113">Input Pin Media Types</span></span>                    | <span data-ttu-id="ca9a7-114">\_Flux de MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="ca9a7-114">MEDIATYPE\_Stream, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                              |
| <span data-ttu-id="ca9a7-115">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="ca9a7-115">Input Pin Interfaces</span></span>                     | <span data-ttu-id="ca9a7-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span><span class="sxs-lookup"><span data-stu-id="ca9a7-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span></span>                                                                                |
| <span data-ttu-id="ca9a7-117">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="ca9a7-117">Output Pin Media Types</span></span>                   | <span data-ttu-id="ca9a7-118">Non applicable</span><span class="sxs-lookup"><span data-stu-id="ca9a7-118">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="ca9a7-119">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="ca9a7-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="ca9a7-120">Non applicable</span><span class="sxs-lookup"><span data-stu-id="ca9a7-120">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="ca9a7-121">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="ca9a7-121">Filter CLSID</span></span>                             | <span data-ttu-id="ca9a7-122">CLSID \_ FileWriter</span><span class="sxs-lookup"><span data-stu-id="ca9a7-122">CLSID\_FileWriter</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="ca9a7-123">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="ca9a7-123">Property Page CLSID</span></span>                      | <span data-ttu-id="ca9a7-124">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="ca9a7-124">No property page</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="ca9a7-125">Exécutable</span><span class="sxs-lookup"><span data-stu-id="ca9a7-125">Executable</span></span>                               | <span data-ttu-id="ca9a7-126">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="ca9a7-126">qcap.dll</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="ca9a7-127">Mérite</span><span class="sxs-lookup"><span data-stu-id="ca9a7-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="ca9a7-128">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="ca9a7-128">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="ca9a7-129">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="ca9a7-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="ca9a7-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="ca9a7-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="ca9a7-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca9a7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca9a7-132">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="ca9a7-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



