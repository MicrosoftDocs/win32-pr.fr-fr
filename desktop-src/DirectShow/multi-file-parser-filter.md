---
description: Filtre de l’analyseur de fichiers multiples
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Filtre de l’analyseur de fichiers multiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fc83a56bb12c307b85be875a3a2e7e73b744d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515537"
---
# <a name="multi-file-parser-filter"></a><span data-ttu-id="3837e-103">Filtre de l’analyseur de fichiers multiples</span><span class="sxs-lookup"><span data-stu-id="3837e-103">Multi-File Parser Filter</span></span>

<span data-ttu-id="3837e-104">Le filtre de l’analyseur de fichiers multiples analyse un format de fichier simple qui permet de spécifier plusieurs noms de fichiers comme s’il s’agissait d’un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="3837e-104">The Multi-File Parser filter parses a simple file format that enables multiple file names to be specified as though they were one file.</span></span> <span data-ttu-id="3837e-105">Ces fichiers ont le format indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="3837e-105">These files have the format shown in the following example:</span></span>


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



<span data-ttu-id="3837e-106">L’utilisation de ce filtre est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3837e-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="3837e-107">Pour afficher plusieurs fichiers dans le même graphique de filtre, l’application doit simplement appeler **RenderFile** ou **AddSourceFilter** plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="3837e-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3837e-108">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="3837e-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="3837e-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="3837e-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3837e-110">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="3837e-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="3837e-111">Type majeur : MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="3837e-111">Major type: MEDIATYPE_Stream</span></span></li>
<li><span data-ttu-id="3837e-112">Sous-type : CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="3837e-112">Subtype: CLSID_MultFile</span></span></li>
<li><span data-ttu-id="3837e-113">Type de format : GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="3837e-113">Format type: GUID_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3837e-114">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="3837e-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="3837e-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="3837e-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3837e-116">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="3837e-116">Output pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="3837e-117">Type majeur : MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="3837e-117">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="3837e-118">Sous-type : GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="3837e-118">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="3837e-119">Type de format : MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="3837e-119">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3837e-120">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="3837e-120">Output pin interfaces</span></span></td>
<td><span data-ttu-id="3837e-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="3837e-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3837e-122">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="3837e-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="3837e-123">CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="3837e-123">CLSID_MultFile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3837e-124">Exécutable</span><span class="sxs-lookup"><span data-stu-id="3837e-124">Executable</span></span></td>
<td><span data-ttu-id="3837e-125">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="3837e-125">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3837e-126"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="3837e-126"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="3837e-127">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="3837e-127">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3837e-128"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="3837e-128"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="3837e-129">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="3837e-129">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="3837e-130">Notes</span><span class="sxs-lookup"><span data-stu-id="3837e-130">Remarks</span></span>

<span data-ttu-id="3837e-131">Le filtre crée une broche de sortie pour chaque fichier figurant dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="3837e-131">The filter creates one output pin for each file listed in the source file.</span></span> <span data-ttu-id="3837e-132">Le type de sortie est \_ fichier MediaType et le bloc de format pour le type de sortie est une chaîne à caractères larges qui contient le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="3837e-132">The output type is MEDIATYPE\_File, and the format block for the output type is a wide-character string that contains the file name.</span></span> <span data-ttu-id="3837e-133">Chaque code confidentiel se connecte à une instance du filtre de [convertisseur de flux de fichier](file-stream-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="3837e-133">Each pin connects to an instance of the [File Stream Renderer](file-stream-renderer-filter.md) filter.</span></span> <span data-ttu-id="3837e-134">Le filtre de convertisseur de flux de fichier crée une broche de sortie, qui expose l’interface [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) .</span><span class="sxs-lookup"><span data-stu-id="3837e-134">The File Stream Renderer filter creates one output pin, which exposes the [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) interface.</span></span> <span data-ttu-id="3837e-135">La broche de sortie restitue le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="3837e-135">The output pin renders the specified file.</span></span> <span data-ttu-id="3837e-136">Aucune donnée multimédia ne transite entre l’analyseur de fichiers multiples et le convertisseur de flux de fichier.</span><span class="sxs-lookup"><span data-stu-id="3837e-136">No media data travels between the Multi-File Parser and the File Stream Renderer.</span></span>

<span data-ttu-id="3837e-137">Le CLSID du filtre n’est pas défini dans UUID. h.</span><span class="sxs-lookup"><span data-stu-id="3837e-137">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="3837e-138">Utilisez cette macro dans votre propre fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3837e-138">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="3837e-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3837e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3837e-140">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="3837e-140">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



