---
description: Interrogation des fonctionnalités de recherche
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Interrogation des fonctionnalités de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa763ab11267da0a9a13a920285491d83273a8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846570"
---
# <a name="querying-for-seeking-capabilities"></a><span data-ttu-id="d40c3-103">Interrogation des fonctionnalités de recherche</span><span class="sxs-lookup"><span data-stu-id="d40c3-103">Querying for Seeking Capabilities</span></span>

<span data-ttu-id="d40c3-104">Microsoft® DirectShow® prend en charge la recherche par le biais de l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="d40c3-104">Microsoft® DirectShow® supports seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="d40c3-105">Le gestionnaire de graphique de filtre expose cette interface, mais la fonctionnalité de recherche est toujours implémentée par des filtres dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="d40c3-105">The Filter Graph Manager exposes this interface, but the seeking functionality is always implemented by filters in the graph.</span></span>

<span data-ttu-id="d40c3-106">Certaines données ne peuvent pas être recherchées.</span><span class="sxs-lookup"><span data-stu-id="d40c3-106">Some data cannot be seeked.</span></span> <span data-ttu-id="d40c3-107">Par exemple, vous ne pouvez pas Rechercher un flux vidéo en direct à partir d’une caméra.</span><span class="sxs-lookup"><span data-stu-id="d40c3-107">For example, you cannot seek a live video stream from a camera.</span></span> <span data-ttu-id="d40c3-108">Toutefois, si un flux peut faire l’objet d’une recherche, il peut prendre en charge différents types de recherche.</span><span class="sxs-lookup"><span data-stu-id="d40c3-108">If a stream is seekable, however, there are various types of seeking it might support.</span></span> <span data-ttu-id="d40c3-109">Il s’agit, entre autres, des suivantes :</span><span class="sxs-lookup"><span data-stu-id="d40c3-109">These include:</span></span>

-   <span data-ttu-id="d40c3-110">Recherche d’une position arbitraire dans le flux.</span><span class="sxs-lookup"><span data-stu-id="d40c3-110">Seeking to an arbitrary position in the stream.</span></span>
-   <span data-ttu-id="d40c3-111">Récupération de la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="d40c3-111">Retrieving the duration of the stream.</span></span>
-   <span data-ttu-id="d40c3-112">Récupération de la position actuelle dans le flux.</span><span class="sxs-lookup"><span data-stu-id="d40c3-112">Retrieving the current position within the stream.</span></span>
-   <span data-ttu-id="d40c3-113">Lit en sens inverse.</span><span class="sxs-lookup"><span data-stu-id="d40c3-113">Playing in reverse.</span></span>

<span data-ttu-id="d40c3-114">L’interface **IMediaSeeking** définit un jeu d’indicateurs, qui [**recherche des \_ \_ \_ fonctionnalités de recherche**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), qui décrivent les fonctionnalités de recherche possibles.</span><span class="sxs-lookup"><span data-stu-id="d40c3-114">The **IMediaSeeking** interface defines a set of flags, [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), that describe the possible seeking capabilities.</span></span> <span data-ttu-id="d40c3-115">Pour récupérer les fonctionnalités du flux, appelez la méthode [**IMediaSeeking :: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="d40c3-115">To retrieve the stream's capabilities, call the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="d40c3-116">La méthode retourne une combinaison d’opérations de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="d40c3-116">The method returns a bitwise combination of flags.</span></span> <span data-ttu-id="d40c3-117">L’application peut les tester à l’aide de l’opérateur & **(and au niveau du** bit).</span><span class="sxs-lookup"><span data-stu-id="d40c3-117">The application can test them using the & (bitwise **AND**) operator.</span></span> <span data-ttu-id="d40c3-118">Par exemple, le code suivant vérifie si le graphique peut effectuer une recherche sur une position arbitraire :</span><span class="sxs-lookup"><span data-stu-id="d40c3-118">For example, the following code checks whether the graph can seek to an arbitrary position:</span></span>


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



