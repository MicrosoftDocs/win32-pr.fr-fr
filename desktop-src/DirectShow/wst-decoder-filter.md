---
description: Filtre de décodage WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtre de décodage WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f2d20873ff9a5e7c009c4a84f7a23c273d6590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863382"
---
# <a name="wst-decoder-filter"></a><span data-ttu-id="f9989-103">Filtre de décodage WST</span><span class="sxs-lookup"><span data-stu-id="f9989-103">WST Decoder Filter</span></span>

<span data-ttu-id="f9989-104">Ce composant a été supprimé de Windows Vista et des systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="f9989-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="f9989-105">Il peut être utilisé dans les systèmes d’exploitation Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f9989-105">It is available for use in the Windows XP and Windows Server 2003 operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="f9989-106">À compter de Windows Vista, DirectShow ne fournit pas de filtre pour décoder le télécode WST (World standard Teletext).</span><span class="sxs-lookup"><span data-stu-id="f9989-106">Starting in Windows Vista, DirectShow does not provide a filter to decode World Standard Teletext (WST).</span></span>

 

<span data-ttu-id="f9989-107">Le décodeur WST est un filtre en mode noyau qui accepte les données de télétexte non standard décodées du [codec WST](wst-codec-filter.md) et remet les bitmaps à la broche 2 sur le [mélangeur de superposition](overlay-mixer-filter.md) à l’aide des polices fournies par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f9989-107">The WST Decoder is a kernel-mode filter that accepts decoded World Standard Teletext data from the [WST Codec](wst-codec-filter.md) and delivers the bitmaps to Pin 2 on the [Overlay Mixer](overlay-mixer-filter.md) using fonts supplied by Microsoft.</span></span> <span data-ttu-id="f9989-108">Seules les langues d’Europe occidentale sont prises en charge pour l’instant ; aucune police Unicode n’est actuellement fournie.</span><span class="sxs-lookup"><span data-stu-id="f9989-108">Only Western European languages are supported at this time; no Unicode fonts are currently provided.</span></span>

<span data-ttu-id="f9989-109">Ce filtre peut être ajouté automatiquement au graphique en appelant [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), à l’aide de la broche de sortie du codec WST.</span><span class="sxs-lookup"><span data-stu-id="f9989-109">This filter can be added to the graph automatically by calling [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), using the output pin of the WST Codec.</span></span>



|                                          |                                                               |
|------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f9989-110">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="f9989-110">Filter Interfaces</span></span>                        | <span data-ttu-id="f9989-111">ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span><span class="sxs-lookup"><span data-stu-id="f9989-111">ISpecifyPropertyPages, [**IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span></span> |
| <span data-ttu-id="f9989-112">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="f9989-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="f9989-113">MEDIATYPE \_ VBI, \_ TÉLÉtexte MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="f9989-113">MEDIATYPE\_VBI, MEDIASUBTYPE\_TELETEXT</span></span>                        |
| <span data-ttu-id="f9989-114">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="f9989-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="f9989-115">**IPin**</span><span class="sxs-lookup"><span data-stu-id="f9989-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="f9989-116">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f9989-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="f9989-117">Vidéo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="f9989-117">MEDIATYPE\_Video</span></span>                                              |
| <span data-ttu-id="f9989-118">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f9989-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="f9989-119">**IPin**</span><span class="sxs-lookup"><span data-stu-id="f9989-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="f9989-120">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="f9989-120">Filter CLSID</span></span>                             | <span data-ttu-id="f9989-121">CLSID \_ WSTDecoder</span><span class="sxs-lookup"><span data-stu-id="f9989-121">CLSID\_WSTDecoder</span></span>                                             |
| <span data-ttu-id="f9989-122">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="f9989-122">Property Page CLSID</span></span>                      | <span data-ttu-id="f9989-123">CLSID \_ WstDecoderPropertyPage</span><span class="sxs-lookup"><span data-stu-id="f9989-123">CLSID\_WstDecoderPropertyPage</span></span>                                 |
| <span data-ttu-id="f9989-124">Exécutable</span><span class="sxs-lookup"><span data-stu-id="f9989-124">Executable</span></span>                               | <span data-ttu-id="f9989-125">Wstdecod.DLL</span><span class="sxs-lookup"><span data-stu-id="f9989-125">Wstdecod.DLL</span></span>                                                  |
| [<span data-ttu-id="f9989-126">Mérite</span><span class="sxs-lookup"><span data-stu-id="f9989-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="f9989-127">MÉRITE \_ normal</span><span class="sxs-lookup"><span data-stu-id="f9989-127">MERIT\_NORMAL</span></span>                                                 |
| [<span data-ttu-id="f9989-128">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="f9989-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="f9989-129">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="f9989-129">CLSID\_LegacyAmFilterCategory</span></span>                                 |



 

## <a name="related-topics"></a><span data-ttu-id="f9989-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f9989-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9989-131">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="f9989-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="f9989-132">Affichage du télétexte standard du monde</span><span class="sxs-lookup"><span data-stu-id="f9989-132">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



