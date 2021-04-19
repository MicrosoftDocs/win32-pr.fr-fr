---
description: Utilisation du séparateur MPEG-2
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: Utilisation du séparateur MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60505ef242c2ed9c1eab3031a005a2582b99608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520601"
---
# <a name="using-the-mpeg-2-splitter"></a><span data-ttu-id="d4fdd-103">Utilisation du séparateur MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d4fdd-103">Using the MPEG-2 Splitter</span></span>

> [!Note]  
> <span data-ttu-id="d4fdd-104">À compter de Microsoft® Windows® XP, le filtre de séparateur MPEG-2 est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="d4fdd-105">Utilisez plutôt le [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md) .</span><span class="sxs-lookup"><span data-stu-id="d4fdd-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

 

<span data-ttu-id="d4fdd-106">Le filtre de séparateur MPEG-2 prend en charge la lecture en mode Pull des flux de programme MPEG-2 qui contiennent au moins l’un des types de flux suivants.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-106">The MPEG-2 Splitter filter supports pull-mode playback of MPEG-2 program streams that contain at least one of the following stream types.</span></span>

-   <span data-ttu-id="d4fdd-107">Vidéo MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d4fdd-107">MPEG-2 video</span></span>
-   <span data-ttu-id="d4fdd-108">Audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d4fdd-108">MPEG-2 audio</span></span>
-   <span data-ttu-id="d4fdd-109">Audio Dolby AC-3 encodé comme défini pour DVD-Video</span><span class="sxs-lookup"><span data-stu-id="d4fdd-109">Dolby AC-3 audio encoded as defined for DVD-Video</span></span>
-   <span data-ttu-id="d4fdd-110">LPCM (linéaire Pulse Code modulé) encodé comme défini pour DVD-Video</span><span class="sxs-lookup"><span data-stu-id="d4fdd-110">LPCM (Linear Pulse Code Modulated) audio encoded as defined for DVD-Video</span></span>

<span data-ttu-id="d4fdd-111">Pour obtenir la liste des types de médias pris en charge par le séparateur MPEG-2, consultez [types de média MPEG-2 Splitter](mpeg-2-splitter-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="d4fdd-111">For a list of media types that the MPEG-2 Splitter supports, see [MPEG-2 Splitter Media Types](mpeg-2-splitter-media-types.md).</span></span>

<span data-ttu-id="d4fdd-112">Le séparateur MPEG-2 n’analyse pas les flux de transport.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-112">The MPEG-2 Splitter does not parse transport streams.</span></span> <span data-ttu-id="d4fdd-113">Utilisez le filtre de démultiplexage MPEG-2 pour les flux de transport (mode Push uniquement).</span><span class="sxs-lookup"><span data-stu-id="d4fdd-113">Use the MPEG-2 Demultiplexer filter for transport streams (push mode only).</span></span>

<span data-ttu-id="d4fdd-114">**Horodatages**</span><span class="sxs-lookup"><span data-stu-id="d4fdd-114">**Time Stamps**</span></span>

<span data-ttu-id="d4fdd-115">Lors de la diffusion de flux de programme MPEG-2, le filtre de séparateur MPEG-2 traite la première référence de l’horloge système qu’il rencontre comme origine de l’heure de n’importe quel flux.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-115">When playing back MPEG-2 program streams, the MPEG-2 Splitter filter treats the first system clock reference it encounters as the time origin of any stream.</span></span> <span data-ttu-id="d4fdd-116">Cela diffère du [séparateur de flux MPEG-1](mpeg-1-stream-splitter-filter.md), qui utilise des horodatages de présentation.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-116">This differs from the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), which uses presentation time stamps.</span></span> <span data-ttu-id="d4fdd-117">La méthode [**IAMParse :: GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) retourne l’heure de l’horloge du système de flux (éventuellement estimé) pour les données qu’elle a traitées.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-117">The [**IAMParse::GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) method returns the (possibly estimated) stream system clock time for the data it has processed.</span></span>

<span data-ttu-id="d4fdd-118">Si le filtre de séparateur MPEG-2 rencontre un exemple d’entrée avec le jeu de propriétés de discontinu (la propriété discontinu peut être définie à l’aide de [**IMediaSample :: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) ou [**IMediaSample2 :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), il ignore les données jusqu’à ce qu’il trouve le premier pack dans les données et ajuste ses horodatages afin que la référence de l’horloge système (SCR) de ce pack soit considérée comme identique à l’heure SCR avant la discontinuation.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-118">If the MPEG-2 splitter filter encounters an input sample with the discontinuity property set (the discontinuity property can be set by using [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) or [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), it skips data until it finds the first pack in the data and adjusts its time stamps so that the system clock reference (SCR) for that pack is considered identical to the SCR time before the discontinuity.</span></span> <span data-ttu-id="d4fdd-119">Si l’horloge SCR s’affiche pour aller vers le haut ou pour avancer d’une seconde, puis (en ligne avec la spécification du flux de programme MPEG-2), elle est également traitée comme une discontinuité d’horloge et l’écart d’horloge apparent est soustrait des horodatages passés aux filtres en aval.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-119">If the SCR clock appears either to jump backward or to jump forward by more than a second, then (in line with the MPEG-2 program stream specification), this is also treated as a clock discontinuity and the apparent clock discrepancy is subtracted from the time stamps passed to downstream filters.</span></span>

<span data-ttu-id="d4fdd-120">**Sélection de flux**</span><span class="sxs-lookup"><span data-stu-id="d4fdd-120">**Stream Selection**</span></span>

<span data-ttu-id="d4fdd-121">Lors de la lecture du flux de programme MPEG-2, le premier flux vidéo et le premier flux audio trouvés parcourant le flux de programme sont choisis.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-121">When playing back the MPEG-2 program stream, the first video stream and first audio stream found traversing the program stream are chosen.</span></span> <span data-ttu-id="d4fdd-122">Jusqu’à un audio et une broche de sortie vidéo sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-122">Up to one audio and one video output pin are supported.</span></span> <span data-ttu-id="d4fdd-123">Par le biais de l’interface [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) , différents flux du même type peuvent être sélectionnés jusqu’au nombre spécifié par la limite audio dans l’en-tête système.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-123">Through the [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) interface, different streams of the same type can be selected up to the number specified by the audio limit in the system header.</span></span> <span data-ttu-id="d4fdd-124">Pour le son MPEG-2, il est actuellement supposé que les flux forment une plage contiguë à partir du flux 0xC0.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-124">For MPEG-2 audio, it is currently assumed the streams form a contiguous range starting at stream 0xC0.</span></span>

<span data-ttu-id="d4fdd-125">**Interfaces prises en charge**</span><span class="sxs-lookup"><span data-stu-id="d4fdd-125">**Supported Interfaces**</span></span>

<span data-ttu-id="d4fdd-126">Le filtre de séparateur MPEG-2 prend en charge les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-126">The MPEG-2 splitter filter supports the following interfaces.</span></span>

-   <span data-ttu-id="d4fdd-127">[**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse).</span><span class="sxs-lookup"><span data-stu-id="d4fdd-127">[**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse).</span></span> <span data-ttu-id="d4fdd-128">Flux de programme MPEG-2 uniquement.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-128">MPEG-2 program stream only.</span></span>
-   <span data-ttu-id="d4fdd-129">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect).</span><span class="sxs-lookup"><span data-stu-id="d4fdd-129">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect).</span></span> <span data-ttu-id="d4fdd-130">Flux de programme MPEG-2 uniquement, flux audio uniquement.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-130">MPEG-2 program stream only, audio streams only.</span></span>
-   <span data-ttu-id="d4fdd-131">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking).</span><span class="sxs-lookup"><span data-stu-id="d4fdd-131">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking).</span></span> <span data-ttu-id="d4fdd-132">Comprend la recherche en mode octet.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-132">Includes byte mode seeking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4fdd-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d4fdd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4fdd-134">Prise en charge MPEG-2 dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="d4fdd-134">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



