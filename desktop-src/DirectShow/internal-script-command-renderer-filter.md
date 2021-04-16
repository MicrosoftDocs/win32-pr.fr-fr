---
description: Filtre de convertisseur de commande de script interne
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Filtre de convertisseur de commande de script interne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b241643d991e9348015dc51ea5b2f1c4875f079d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521596"
---
# <a name="internal-script-command-renderer-filter"></a><span data-ttu-id="7c037-103">Filtre de convertisseur de commande de script interne</span><span class="sxs-lookup"><span data-stu-id="7c037-103">Internal Script Command Renderer Filter</span></span>

<span data-ttu-id="7c037-104">Reçoit des commandes de script et les distribue à l’application.</span><span class="sxs-lookup"><span data-stu-id="7c037-104">Receives script commands and dispatches them to the application.</span></span>

<span data-ttu-id="7c037-105">Ce filtre accepte les commandes de script dans l’un des deux formats suivants :</span><span class="sxs-lookup"><span data-stu-id="7c037-105">This filter accepts script commands in one of two formats:</span></span>

-   <span data-ttu-id="7c037-106">Texte du MEDIATYPE \_ : chaque exemple de média contient une chaîne de texte ANSI.</span><span class="sxs-lookup"><span data-stu-id="7c037-106">MEDIATYPE\_Text: Each media sample contains an ANSI text string.</span></span>
-   <span data-ttu-id="7c037-107">MEDIATYPE \_ commande : chaque exemple de média contient deux chaînes Unicode se terminant par un caractère null, concaténées ensemble.</span><span class="sxs-lookup"><span data-stu-id="7c037-107">MEDIATYPE\_ScriptCommand: Each media sample contains two NULL-terminated Unicode strings, concatenated together.</span></span> <span data-ttu-id="7c037-108">La première chaîne décrit le type de commande et la deuxième chaîne est la commande de script.</span><span class="sxs-lookup"><span data-stu-id="7c037-108">The first string describes the command type and the second string is the script command.</span></span>

    <span data-ttu-id="7c037-109">Lorsque le filtre reçoit un exemple, il envoie une notification d’événement d' [**\_ \_ événement OLE EC**](ec-ole-event.md) .</span><span class="sxs-lookup"><span data-stu-id="7c037-109">When the filter receives a sample, it sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="7c037-110">Le premier paramètre d’événement est un **BSTR** avec le type de commande, ou `Text` si le format est du texte de MediaType \_ .</span><span class="sxs-lookup"><span data-stu-id="7c037-110">The first event parameter is a **BSTR** with the command type, or `Text` if the format is MEDIATYPE\_Text.</span></span> <span data-ttu-id="7c037-111">Le deuxième paramètre d’événement est un **BSTR** avec la commande de script.</span><span class="sxs-lookup"><span data-stu-id="7c037-111">The second event parameter is a **BSTR** with the script command.</span></span> <span data-ttu-id="7c037-112">L’application peut récupérer l’événement et répondre à la commande de script.</span><span class="sxs-lookup"><span data-stu-id="7c037-112">The application can retrieve the event and respond to the script command.</span></span>

<span data-ttu-id="7c037-113">Pour obtenir un exemple d’utilisation de ce filtre, consultez l’article sur l' [analyseur sami (CC)](sami--cc--parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="7c037-113">For an example of how to use this filter, see [SAMI (CC) Parser](sami--cc--parser-filter.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7c037-114">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="7c037-114">Filter Interfaces</span></span></td>
<td><span data-ttu-id="7c037-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="7c037-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c037-116">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="7c037-116">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="7c037-117">MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="7c037-117">MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</span></span></li>
<li><span data-ttu-id="7c037-118">MEDIATYPE_Text, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="7c037-118">MEDIATYPE_Text, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7c037-119">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="7c037-119">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="7c037-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="7c037-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c037-121">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="7c037-121">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="7c037-122">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7c037-122">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7c037-123">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="7c037-123">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="7c037-124">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7c037-124">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c037-125">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="7c037-125">Filter CLSID</span></span></td>
<td><span data-ttu-id="7c037-126">{48025243-2D39-11CE-875D-00608CB78066}</span><span class="sxs-lookup"><span data-stu-id="7c037-126">{48025243-2D39-11CE-875D-00608CB78066}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7c037-127">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="7c037-127">Property Page CLSID</span></span></td>
<td><span data-ttu-id="7c037-128">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="7c037-128">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c037-129">Exécutable</span><span class="sxs-lookup"><span data-stu-id="7c037-129">Executable</span></span></td>
<td><span data-ttu-id="7c037-130">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="7c037-130">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7c037-131"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="7c037-131"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="7c037-132">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="7c037-132">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7c037-133"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="7c037-133"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="7c037-134">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="7c037-134">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7c037-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c037-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c037-136">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="7c037-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



