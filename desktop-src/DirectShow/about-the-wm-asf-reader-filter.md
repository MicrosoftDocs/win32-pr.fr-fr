---
description: À propos du filtre du Lecteur WM ASF
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: À propos du filtre du Lecteur WM ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350e6597aa6aa66193af37a30ed54c37139d5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846630"
---
# <a name="about-the-wm-asf-reader-filter"></a><span data-ttu-id="c7161-103">À propos du filtre du Lecteur WM ASF</span><span class="sxs-lookup"><span data-stu-id="c7161-103">About the WM ASF Reader Filter</span></span>

<span data-ttu-id="c7161-104">La lecture des fichiers ASF est gérée par le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="c7161-104">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="c7161-105">Lorsque le lecteur ASF WM lit un fichier, il crée automatiquement une broche de sortie pour chaque flux, y compris les flux Web, les flux de commandes de script et tout autre type de flux arbitraire.</span><span class="sxs-lookup"><span data-stu-id="c7161-105">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="c7161-106">Dans le cas de plusieurs fichiers à vitesse de transmission, les codes confidentiels sont créés uniquement pour les flux actuellement sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="c7161-106">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span> <span data-ttu-id="c7161-107">Pour lire un fichier ASF avec le filtre de lecteur ASF WM, appelez [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) ou [**IGraphBuilder :: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span><span class="sxs-lookup"><span data-stu-id="c7161-107">To play an ASF file with the WM ASF Reader filter, call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

<span data-ttu-id="c7161-108">Le lecteur ASF WM prend en charge l’interface DirectShow [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , qui permet aux applications d’effectuer une recherche temporelle dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="c7161-108">The WM ASF Reader supports the DirectShow [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="c7161-109">Toutefois, la lecture à des vitesses autres que 1,0 (comme spécifié dans [**IMediaSeeking ::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)sesente) n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c7161-109">However, playback at speeds other than 1.0 (as specified in [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) is not supported.</span></span>

<span data-ttu-id="c7161-110">Le filtre de lecteur ASF WM expose également plusieurs interfaces du kit de développement logiciel (SDK) du format Windows Media, comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c7161-110">The WM ASF Reader filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span> <span data-ttu-id="c7161-111">Ces interfaces sont documentées dans la documentation du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="c7161-111">These interfaces are documented in the Windows Media Format SDK documentation.</span></span>



| <span data-ttu-id="c7161-112">Interface</span><span class="sxs-lookup"><span data-stu-id="c7161-112">Interface</span></span>                                             | <span data-ttu-id="c7161-113">Exposition</span><span class="sxs-lookup"><span data-stu-id="c7161-113">How exposed</span></span>                                 | <span data-ttu-id="c7161-114">Commentaires</span><span class="sxs-lookup"><span data-stu-id="c7161-114">Comments</span></span>                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7161-115">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="c7161-115">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="c7161-116">Via **IServiceProvider** sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="c7161-116">Through **IServiceProvider** on the filter.</span></span> | <span data-ttu-id="c7161-117">Fourni pour les applications qui doivent lire du contenu protégé par des Rights Management numériques (DRM).</span><span class="sxs-lookup"><span data-stu-id="c7161-117">Provided for applications that need to play content protected by Digital Rights Management (DRM)..</span></span>                             |
| [<span data-ttu-id="c7161-118">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="c7161-118">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="c7161-119">**QueryInterface** sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="c7161-119">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="c7161-120">Fourni pour permettre aux applications de lire les attributs de fichier et de contenu, ainsi que les informations de marqueur et de script et les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c7161-120">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>     |
| [<span data-ttu-id="c7161-121">**IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="c7161-121">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="c7161-122">**QueryInterface** sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="c7161-122">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="c7161-123">Partiellement implémenté sur le filtre afin que les applications puissent accéder aux méthodes d’information sur l’objet WM Reader.</span><span class="sxs-lookup"><span data-stu-id="c7161-123">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>         |
| [<span data-ttu-id="c7161-124">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="c7161-124">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="c7161-125">**QueryInterface** sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="c7161-125">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="c7161-126">Partiellement implémenté sur le filtre afin que les applications puissent accéder aux méthodes d’information sur l’objet de lecteur du kit de développement logiciel (SDK) de format.</span><span class="sxs-lookup"><span data-stu-id="c7161-126">Partially implemented on the filter so that applications can access the informational methods on the Format SDK Reader Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c7161-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c7161-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7161-128">Lecture de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="c7161-128">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



