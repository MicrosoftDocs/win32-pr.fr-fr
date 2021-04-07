---
description: Exposition des formats de capture et de compression
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Exposition des formats de capture et de compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02051d9e68b3ad919b96dca53b674305787b3186
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747637"
---
# <a name="exposing-capture-and-compression-formats"></a><span data-ttu-id="c8388-103">Exposition des formats de capture et de compression</span><span class="sxs-lookup"><span data-stu-id="c8388-103">Exposing Capture and Compression Formats</span></span>

<span data-ttu-id="c8388-104">Cet article explique comment retourner des formats de capture et de compression à l’aide de la méthode [**IAMStreamConfig :: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="c8388-104">This article describes how to return capture and compression formats by using the [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="c8388-105">Cette méthode peut obtenir plus d’informations sur les types de médias acceptés que la méthode classique d’énumération des types de média d’un pin. il est donc préférable de l’utiliser à la place.</span><span class="sxs-lookup"><span data-stu-id="c8388-105">This method can get more information about accepted media types than the traditional way of enumerating a pin's media types, so it should typically be used instead.</span></span> <span data-ttu-id="c8388-106">**GetStreamCaps** peut retourner des informations sur les types de formats autorisés pour l’audio ou la vidéo.</span><span class="sxs-lookup"><span data-stu-id="c8388-106">**GetStreamCaps** can return information about the kinds of formats allowed for audio or video.</span></span> <span data-ttu-id="c8388-107">En outre, cet article fournit un exemple de code qui montre comment reconnecter la broche d’entrée d’un filtre de transformation pour garantir que votre filtre peut produire une sortie particulière.</span><span class="sxs-lookup"><span data-stu-id="c8388-107">Additionally, this article provides some sample code that demonstrates how to reconnect the input pin of a transform filter to ensure your filter can produce a particular output.</span></span>

<span data-ttu-id="c8388-108">La méthode **GetStreamCaps** retourne un tableau de paires de structures de type de média et de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="c8388-108">The **GetStreamCaps** method returns an array of pairs of media type and capabilities structures.</span></span> <span data-ttu-id="c8388-109">Le type de média est une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) et les fonctionnalités sont représentées soit par une structure d' [**\_ \_ \_ embout de la configuration de flux audio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) , soit par une structure de [**\_ \_ configuration \_ de flux vidéo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="c8388-109">The media type is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and the capabilities are represented either by an [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structure or a [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure.</span></span> <span data-ttu-id="c8388-110">La première section de cet article présente un exemple de vidéo et la deuxième présente un exemple audio.</span><span class="sxs-lookup"><span data-stu-id="c8388-110">The first section in this article presents a video example and the second presents an audio example.</span></span>

<span data-ttu-id="c8388-111">Cet article contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8388-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="c8388-112">Fonctionnalités vidéo</span><span class="sxs-lookup"><span data-stu-id="c8388-112">Video Capabilities</span></span>](video-capabilities.md)
-   [<span data-ttu-id="c8388-113">Fonctionnalités audio</span><span class="sxs-lookup"><span data-stu-id="c8388-113">Audio Capabilities</span></span>](audio-capabilities.md)
-   [<span data-ttu-id="c8388-114">Reconnexion de votre entrée pour garantir des types de sortie spécifiques</span><span class="sxs-lookup"><span data-stu-id="c8388-114">Reconnecting Your Input to Ensure Specific Output Types</span></span>](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a><span data-ttu-id="c8388-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c8388-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8388-116">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="c8388-116">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



