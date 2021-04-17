---
description: Filtre de convertisseur de flux de fichier
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filtre de convertisseur de flux de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64c8d8a0c87dab3aa811c8246be24ded8ee04dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522316"
---
# <a name="file-stream-renderer-filter"></a><span data-ttu-id="de89b-103">Filtre de convertisseur de flux de fichier</span><span class="sxs-lookup"><span data-stu-id="de89b-103">File Stream Renderer Filter</span></span>

<span data-ttu-id="de89b-104">Le filtre de convertisseur de flux de fichier restitue les noms de fichiers qui sont analysés par le filtre de l' [Analyseur de fichiers multiples](multi-file-parser-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="de89b-104">The File Stream Renderer filter renders file names that are parsed by the [Multi-File Parser](multi-file-parser-filter.md) filter.</span></span> <span data-ttu-id="de89b-105">Pour plus d’informations, consultez la documentation de ce filtre.</span><span class="sxs-lookup"><span data-stu-id="de89b-105">For more information, see the documentation for that filter.</span></span>

<span data-ttu-id="de89b-106">L’utilisation de ce filtre est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="de89b-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="de89b-107">Pour afficher plusieurs fichiers dans le même graphique de filtre, l’application doit simplement appeler **RenderFile** ou **AddSourceFilter** plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="de89b-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de89b-108">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="de89b-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="de89b-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="de89b-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de89b-110">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="de89b-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="de89b-111">Type majeur : MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="de89b-111">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="de89b-112">Sous-type : GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="de89b-112">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="de89b-113">Type de format : MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="de89b-113">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de89b-114">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="de89b-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="de89b-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="de89b-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de89b-116">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="de89b-116">Output pin media types</span></span></td>
<td><span data-ttu-id="de89b-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="de89b-117">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de89b-118">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="de89b-118">Output pin interfaces</span></span></td>
<td><span data-ttu-id="de89b-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></span><span class="sxs-lookup"><span data-stu-id="de89b-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de89b-120">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="de89b-120">Filter CLSID</span></span></td>
<td><span data-ttu-id="de89b-121">CLSID_FileRend</span><span class="sxs-lookup"><span data-stu-id="de89b-121">CLSID_FileRend</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de89b-122">Exécutable</span><span class="sxs-lookup"><span data-stu-id="de89b-122">Executable</span></span></td>
<td><span data-ttu-id="de89b-123">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="de89b-123">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de89b-124"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="de89b-124"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="de89b-125">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="de89b-125">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de89b-126"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="de89b-126"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="de89b-127">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="de89b-127">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="de89b-128">Notes</span><span class="sxs-lookup"><span data-stu-id="de89b-128">Remarks</span></span>

<span data-ttu-id="de89b-129">Le CLSID du filtre n’est pas défini dans UUID. h.</span><span class="sxs-lookup"><span data-stu-id="de89b-129">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="de89b-130">Utilisez cette macro dans votre propre fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="de89b-130">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="de89b-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de89b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de89b-132">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="de89b-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



