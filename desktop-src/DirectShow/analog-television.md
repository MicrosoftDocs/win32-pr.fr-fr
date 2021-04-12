---
description: Télévision analogique
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Télévision analogique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af8ba94831afed59d783598dbf6bc0eaee0ec6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109002"
---
# <a name="analog-television"></a><span data-ttu-id="28f94-103">Télévision analogique</span><span class="sxs-lookup"><span data-stu-id="28f94-103">Analog Television</span></span>

<span data-ttu-id="28f94-104">La télévision analogique diffère des autres scénarios de capture vidéo de plusieurs façons :</span><span class="sxs-lookup"><span data-stu-id="28f94-104">Analog television differs from other video capture scenarios in several ways:</span></span>

-   <span data-ttu-id="28f94-105">La carte tuner est paramétrée sur un signal analogique, qui est ensuite numérisé.</span><span class="sxs-lookup"><span data-stu-id="28f94-105">The tuner card tunes to an analog signal, which is then digitized.</span></span>
-   <span data-ttu-id="28f94-106">L’audio est transporté dans le signal analogique.</span><span class="sxs-lookup"><span data-stu-id="28f94-106">Audio is carried in the analog signal.</span></span> <span data-ttu-id="28f94-107">La façon dont le son atteint la carte audio varie en fonction du matériel.</span><span class="sxs-lookup"><span data-stu-id="28f94-107">How the audio reaches the sound card varies depending on the hardware.</span></span>
-   <span data-ttu-id="28f94-108">Le signal peut contenir des données supplémentaires dans l’intervalle de parasite vertical (VBI), par exemple les sous-titres (CC), le télétexte universel standard (WST) et les services de données étendus (XDS).</span><span class="sxs-lookup"><span data-stu-id="28f94-108">The signal may contain additional data in the vertical blanking interval (VBI), such as closed captions (CC), World Standard Teletext (WST), and extended data services (XDS).</span></span>

<span data-ttu-id="28f94-109">Le diagramme suivant montre un graphique de filtre classique pour la préversion de la télévision.</span><span class="sxs-lookup"><span data-stu-id="28f94-109">The following diagram shows a typical filter graph for television preview.</span></span>

![graphique de télévision analogique](images/vidcap06.png)

-   <span data-ttu-id="28f94-111">Le filtre [Tuner TV](tv-tuner-filter.md) contrôle le paramétrage.</span><span class="sxs-lookup"><span data-stu-id="28f94-111">The [TV Tuner](tv-tuner-filter.md) filter controls tuning.</span></span>
-   <span data-ttu-id="28f94-112">Le filtre [audio TV](tv-audio-filter.md) contrôle le décodage audio.</span><span class="sxs-lookup"><span data-stu-id="28f94-112">The [TV Audio](tv-audio-filter.md) filter controls the audio decoding.</span></span>
-   <span data-ttu-id="28f94-113">Si la carte tuner a plusieurs entrées physiques, le filtre de la barre d' [affichage vidéo analogique](analog-video-crossbar-filter.md) permet à l’application de sélectionner l’entrée qui est décodée et rendue.</span><span class="sxs-lookup"><span data-stu-id="28f94-113">If the tuner card has more than one physical input, the [Analog Video Crossbar](analog-video-crossbar-filter.md) filter enables the application to select which input is decoded and rendered.</span></span>
-   <span data-ttu-id="28f94-114">Le filtre de [capture vidéo WDM](wdm-video-capture-filter.md) remet le flux vidéo numérisé.</span><span class="sxs-lookup"><span data-stu-id="28f94-114">The [WDM Video Capture](wdm-video-capture-filter.md) filter delivers the digitized video stream.</span></span>

<span data-ttu-id="28f94-115">Le générateur de graphiques de capture insère automatiquement tous les filtres qui sont requis en amont du filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="28f94-115">The Capture Graph Builder automatically inserts any filters that are required upstream from the capture filter.</span></span>

<span data-ttu-id="28f94-116">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="28f94-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="28f94-117">Réglage de la télévision analogique</span><span class="sxs-lookup"><span data-stu-id="28f94-117">Analog Television Tuning</span></span>](analog-television-tuning.md)
-   [<span data-ttu-id="28f94-118">Télévision analogique audio</span><span class="sxs-lookup"><span data-stu-id="28f94-118">Analog Television Audio</span></span>](analog-television-audio.md)
-   [<span data-ttu-id="28f94-119">Sous-titres et télétexte</span><span class="sxs-lookup"><span data-stu-id="28f94-119">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)

## <a name="related-topics"></a><span data-ttu-id="28f94-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28f94-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28f94-121">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="28f94-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



