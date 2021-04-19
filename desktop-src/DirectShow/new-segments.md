---
description: Nouveaux segments
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Nouveaux segments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438cb3b457ed8ea0f77bd2ac1dcc5d6d2c72698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517365"
---
# <a name="new-segments"></a><span data-ttu-id="4ae8b-103">Nouveaux segments</span><span class="sxs-lookup"><span data-stu-id="4ae8b-103">New Segments</span></span>

<span data-ttu-id="4ae8b-104">Un *segment* est un groupe d’exemples de médias qui partagent une heure de début, une heure d’arrêt et une vitesse de lecture communes.</span><span class="sxs-lookup"><span data-stu-id="4ae8b-104">A *segment* is a group of media samples that share a common start time, stop time, and playback rate.</span></span> <span data-ttu-id="4ae8b-105">La méthode [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) signale le début d’un nouveau segment.</span><span class="sxs-lookup"><span data-stu-id="4ae8b-105">The [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method signals the start of a new segment.</span></span> <span data-ttu-id="4ae8b-106">Il permet à un filtre source d’informer les filtres en aval que les informations relatives au temps et au taux ont changé.</span><span class="sxs-lookup"><span data-stu-id="4ae8b-106">It provides a way for a source filter to inform downstream filters that the time and rate information has changed.</span></span> <span data-ttu-id="4ae8b-107">Par exemple, si le filtre source cherche à un nouveau point dans le flux, il appelle **NewSegment** avec la nouvelle heure de début.</span><span class="sxs-lookup"><span data-stu-id="4ae8b-107">For example, if the source filter seeks to a new point in the stream, it calls **NewSegment** with the new start time.</span></span>

<span data-ttu-id="4ae8b-108">Certains filtres en aval utilisent les informations de segment lorsqu’ils traitent des exemples.</span><span class="sxs-lookup"><span data-stu-id="4ae8b-108">Some downstream filters use the segment information when they process samples.</span></span> <span data-ttu-id="4ae8b-109">Par exemple, dans un format qui utilise la compression interframe, si l’heure d’arrêt tombe sur un frame Delta, le filtre source peut avoir besoin d’envoyer des échantillons supplémentaires après l’heure d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="4ae8b-109">For example, in a format that uses interframe compression, if the stop time falls on a delta frame, the source filter may need to send additional samples after the stop time.</span></span> <span data-ttu-id="4ae8b-110">Cela permet au décodeur de décoder le frame Delta final.</span><span class="sxs-lookup"><span data-stu-id="4ae8b-110">This enables the decoder to decode the final delta frame.</span></span> <span data-ttu-id="4ae8b-111">Pour déterminer le cadre final correct, le décodeur fait référence à l’heure d’arrêt du segment.</span><span class="sxs-lookup"><span data-stu-id="4ae8b-111">To determine the correct final frame, the decoder refers to the segment stop time.</span></span> <span data-ttu-id="4ae8b-112">Autre exemple, les convertisseurs audio utilisent le taux de segment, ainsi que le taux d’échantillonnage audio pour générer la sortie audio correcte.</span><span class="sxs-lookup"><span data-stu-id="4ae8b-112">As another example, audio renderers use the segment rate along with the audio sampling rate to generate the correct audio output.</span></span>

<span data-ttu-id="4ae8b-113">Dans le modèle push, le filtre source lance l’appel **NewSegment** .</span><span class="sxs-lookup"><span data-stu-id="4ae8b-113">In the push model, the source filter initiates the **NewSegment** call.</span></span> <span data-ttu-id="4ae8b-114">Dans le modèle d’extraction, cette opération est effectuée par le filtre de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="4ae8b-114">In the pull model, this is done by the parser filter.</span></span> <span data-ttu-id="4ae8b-115">Dans les deux cas, le filtre appelle **NewSegment** sur la broche d’entrée en aval, qui propage l’appel au filtre suivant, jusqu’à ce que l’appel atteigne le convertisseur.</span><span class="sxs-lookup"><span data-stu-id="4ae8b-115">In either case, the filter calls **NewSegment** on the downstream input pin, which propagates the call to the next filter, until the call reaches the renderer.</span></span> <span data-ttu-id="4ae8b-116">Les filtres doivent sérialiser les appels **NewSegment** avec d’autres appels de diffusion, tels que [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span><span class="sxs-lookup"><span data-stu-id="4ae8b-116">Filters must serialize **NewSegment** calls with other streaming calls, such as [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span></span>

<span data-ttu-id="4ae8b-117">Temps de flux rétablit à zéro après chaque nouveau segment.</span><span class="sxs-lookup"><span data-stu-id="4ae8b-117">Stream time resets to zero after each new segment.</span></span> <span data-ttu-id="4ae8b-118">Horodatages sur les échantillons fournis après le début du segment à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="4ae8b-118">Time stamps on samples delivered after the segment start from zero.</span></span>

 

 



