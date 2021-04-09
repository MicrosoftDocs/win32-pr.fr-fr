---
description: Développement d’encodeur et de décodeur
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Développement d’encodeur et de décodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109203"
---
# <a name="encoder-and-decoder-development"></a><span data-ttu-id="33db7-103">Développement d’encodeur et de décodeur</span><span class="sxs-lookup"><span data-stu-id="33db7-103">Encoder and Decoder Development</span></span>

<span data-ttu-id="33db7-104">Cette section contient des articles sur le développement d’encodeurs et de décodeurs pour DirectShow.</span><span class="sxs-lookup"><span data-stu-id="33db7-104">This section contains articles about encoder and decoder development for DirectShow.</span></span> <span data-ttu-id="33db7-105">Ces rubriques ne sont pas pertinentes pour les développeurs d’applications.</span><span class="sxs-lookup"><span data-stu-id="33db7-105">These topics are not relevant for application developers.</span></span>

<span data-ttu-id="33db7-106">Un décodeur logiciel qui prend en charge DirectX Video Acceleration (VA) doit être implémenté en tant que filtre de transformation de copie DirectShow.</span><span class="sxs-lookup"><span data-stu-id="33db7-106">A software decoder that supports DirectX Video Acceleration (VA) must be implemented as a DirectShow copy transform filter.</span></span> <span data-ttu-id="33db7-107">Si le décodeur ne prend pas en charge DirectX VA, il peut également être implémenté en tant qu’objet de média DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="33db7-107">If the decoder does not support DirectX VA, it can also be implemented as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="33db7-108">Un décodeur qui se connecte à un convertisseur vidéo ne doit pas être implémenté comme un filtre TRANS-in-place, car cela entraîne une dégradation significative des performances.</span><span class="sxs-lookup"><span data-stu-id="33db7-108">A decoder that connects to a video renderer should not be implemented as a trans-in-place filter, because this will result in significant performance degradation.</span></span> <span data-ttu-id="33db7-109">Pour plus d’informations sur l’écriture d’un filtre de transformation de copie, consultez [écriture de filtres de transformation](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="33db7-109">For information on how to write a copy transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="33db7-110">Les encodeurs logiciels peuvent être implémentés en tant que filtres de transformation ou DMOs.</span><span class="sxs-lookup"><span data-stu-id="33db7-110">Software encoders can be implemented as either transform filters or DMOs.</span></span> <span data-ttu-id="33db7-111">Les encodeurs n’utilisent pas DirectX VA, car DirectX VA est actuellement utilisé uniquement pour la décompression.</span><span class="sxs-lookup"><span data-stu-id="33db7-111">Encoders do not use DirectX VA, since DirectX VA currently is only used for decompression.</span></span> <span data-ttu-id="33db7-112">La spécification de l’API d’encodeur décrite dans cette section s’applique aux encodeurs matériels et logiciels.</span><span class="sxs-lookup"><span data-stu-id="33db7-112">The Encoder API specification described in this section is relevant for both hardware and software encoders.</span></span>

<span data-ttu-id="33db7-113">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="33db7-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="33db7-114">API d’encodeur</span><span class="sxs-lookup"><span data-stu-id="33db7-114">Encoder API</span></span>](encoder-api.md)
-   [<span data-ttu-id="33db7-115">Interfaces et spécifications du décodeur</span><span class="sxs-lookup"><span data-stu-id="33db7-115">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
-   [<span data-ttu-id="33db7-116">Paramètres du décodeur pour Windows Media Center Edition</span><span class="sxs-lookup"><span data-stu-id="33db7-116">Decoder Settings for Windows Media Center Edition</span></span>](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a><span data-ttu-id="33db7-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33db7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33db7-118">Utilisation de VMR pour les développeurs de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="33db7-118">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



