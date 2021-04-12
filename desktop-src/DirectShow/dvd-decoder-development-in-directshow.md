---
description: Développement d’un décodeur de DVD dans DirectShow
ms.assetid: c00ff132-fee1-47b5-8a8a-df7cb920ad89
title: Développement d’un décodeur de DVD dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3de64b3c1d91dbf5f22ba3e4b4ae8fe78edda5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482432"
---
# <a name="dvd-decoder-development-in-directshow"></a><span data-ttu-id="b3c5b-103">Développement d’un décodeur de DVD dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="b3c5b-103">DVD Decoder Development in DirectShow</span></span>

<span data-ttu-id="b3c5b-104">Cette section contient des pointeurs vers les pages de référence pour tous les jeux de propriétés DirectShow et les interfaces qui sont propres à un DVD ou qui sont largement utilisées dans le décodage de DVD.</span><span class="sxs-lookup"><span data-stu-id="b3c5b-104">This section contains pointers to the reference pages for all the DirectShow property sets and interfaces that are either DVD-specific or else used extensively in DVD decoding.</span></span> <span data-ttu-id="b3c5b-105">En plus de ce qui est répertorié ici, un décodeur et ses pin doivent également prendre en charge les interfaces de filtre DirectShow génériques, comme décrit dans [écriture de filtres DirectShow](writing-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b3c5b-105">In addition to what is listed here, a decoder and its pins must also support the generic DirectShow filter interfaces as described in [Writing DirectShow Filters](writing-directshow-filters.md).</span></span>

<span data-ttu-id="b3c5b-106">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3c5b-106">This section contains the following topics.</span></span>

-   [<span data-ttu-id="b3c5b-107">Contrôle du volume du décodeur</span><span class="sxs-lookup"><span data-stu-id="b3c5b-107">Decoder Volume Control</span></span>](decoder-volume-control.md)
-   [<span data-ttu-id="b3c5b-108">Prise en charge des modifications de région de DVD dans Windows</span><span class="sxs-lookup"><span data-stu-id="b3c5b-108">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)

<span data-ttu-id="b3c5b-109">Voir aussi :</span><span class="sxs-lookup"><span data-stu-id="b3c5b-109">See also:</span></span>

-   [<span data-ttu-id="b3c5b-110">**Jeu de propriétés Karaoké DVD**</span><span class="sxs-lookup"><span data-stu-id="b3c5b-110">**DVD Karaoke Property Set**</span></span>](dvd-karaoke-property-set.md)
-   [<span data-ttu-id="b3c5b-111">**Jeu de propriétés protection de copie de DVD**</span><span class="sxs-lookup"><span data-stu-id="b3c5b-111">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   [<span data-ttu-id="b3c5b-112">**Jeu de propriétés de sous-image de DVD**</span><span class="sxs-lookup"><span data-stu-id="b3c5b-112">**DVD Subpicture Property Set**</span></span>](dvd-subpicture-property-set.md)
-   [<span data-ttu-id="b3c5b-113">Épingler le jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="b3c5b-113">Pin Property Set</span></span>](pin-property-set.md)
-   [<span data-ttu-id="b3c5b-114">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="b3c5b-114">**IKsPropertySet**</span></span>](ikspropertyset.md)
-   <span data-ttu-id="b3c5b-115">[**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) (décodeurs matériels uniquement)</span><span class="sxs-lookup"><span data-stu-id="b3c5b-115">[**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) (hardware decoders only)</span></span>
-   <span data-ttu-id="b3c5b-116">[**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) (décodeurs matériels uniquement)</span><span class="sxs-lookup"><span data-stu-id="b3c5b-116">[**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) (hardware decoders only)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3c5b-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3c5b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3c5b-118">Interfaces et spécifications du décodeur</span><span class="sxs-lookup"><span data-stu-id="b3c5b-118">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



