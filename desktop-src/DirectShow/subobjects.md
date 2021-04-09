---
description: Sous-objets
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Sous-objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8b427a315231577f1608a168629bc8b77d2cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867082"
---
# <a name="subobjects"></a><span data-ttu-id="6637a-103">Sous-objets</span><span class="sxs-lookup"><span data-stu-id="6637a-103">Subobjects</span></span>

<span data-ttu-id="6637a-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="6637a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="6637a-105">Les sources, les effets et les transitions ont des pointeurs internes vers d’autres objets COM, appelés sous- *objets*.</span><span class="sxs-lookup"><span data-stu-id="6637a-105">Sources, effects, and transitions have internal pointers to other COM objects, called *subobjects*.</span></span> <span data-ttu-id="6637a-106">Le sous-objet effectue le travail réel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6637a-106">The subobject performs the actual work of the object.</span></span> <span data-ttu-id="6637a-107">Le sous-objet d’une source est le composant qui crée les données vidéo ou audio.</span><span class="sxs-lookup"><span data-stu-id="6637a-107">The subobject of a source is the component that creates the video or audio data.</span></span> <span data-ttu-id="6637a-108">Le sous-objet d’un effet ou d’une transition est le composant qui transforme les données ; par exemple, dans un effet vidéo, il crée l’effet visuel dans le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="6637a-108">The subobject of an effect or transition is the component that transforms the data; for example, in a video effect, it creates the visual effect in the video stream.</span></span>

<span data-ttu-id="6637a-109">Le type de sous-objet dépend du type d’objet :</span><span class="sxs-lookup"><span data-stu-id="6637a-109">The type of subobject depends on the type of object:</span></span>

-   <span data-ttu-id="6637a-110">Source : tout filtre de filtre ou d’analyseur source DirectShow qui prend en charge la recherche et produit un format pris en charge par.</span><span class="sxs-lookup"><span data-stu-id="6637a-110">Source: Any DirectShow source filter or parser filter that supports seeking and produces a format that DES supports.</span></span> <span data-ttu-id="6637a-111">Il peut s’agir d’un format compressé si des filtres DirectShow existent pour le décoder.</span><span class="sxs-lookup"><span data-stu-id="6637a-111">It can be a compressed format if DirectShow filters exist to decode it.</span></span>
-   <span data-ttu-id="6637a-112">Effet : pour la vidéo, n’importe quel objet de transformation Microsoft® DirectX® à un seul entré.</span><span class="sxs-lookup"><span data-stu-id="6637a-112">Effect: For video, any 2-D one-input Microsoft® DirectX® Transform object.</span></span> <span data-ttu-id="6637a-113">Pour l’audio, tout filtre d’effet audio DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6637a-113">For audio, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="6637a-114">Transition : pour la vidéo, tout objet de transformation DirectX à deux entrées 2D.</span><span class="sxs-lookup"><span data-stu-id="6637a-114">Transition: For video, any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="6637a-115">L’audio ne prend pas en charge les transitions.</span><span class="sxs-lookup"><span data-stu-id="6637a-115">Audio does not support transitions.</span></span>

<span data-ttu-id="6637a-116">Les groupes, les compositions et les suivis n’ont pas de sous-objets.</span><span class="sxs-lookup"><span data-stu-id="6637a-116">Groups, compositions, and tracks do not have subobjects.</span></span>

<span data-ttu-id="6637a-117">L’application ne définit pas directement le pointeur de sous-objet.</span><span class="sxs-lookup"><span data-stu-id="6637a-117">The application does not directly set the subobject pointer.</span></span> <span data-ttu-id="6637a-118">Pour les effets et les transitions, l’application appelle la méthode [**IAMTimelineObj :: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) pour spécifier le GUID du sous-objet.</span><span class="sxs-lookup"><span data-stu-id="6637a-118">For effects and transitions, the application calls the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method to specify the GUID of the subobject.</span></span> <span data-ttu-id="6637a-119">Pour les objets sources, une application appelle généralement [**IAMTimelineSrc :: SetMediaName**](iamtimelinesrc-setmedianame.md) pour spécifier le nom d’un fichier source.</span><span class="sxs-lookup"><span data-stu-id="6637a-119">For source objects, an application typically calls the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) to specify the name of a source file.</span></span> <span data-ttu-id="6637a-120">Toutefois, la méthode **SetSubObjectGUID** peut également être utilisée pour les objets sources, pour spécifier l’identificateur de classe (CLSID) d’un filtre.</span><span class="sxs-lookup"><span data-stu-id="6637a-120">However, the **SetSubObjectGUID** method can also be used for source objects, to specify the class identifier (CLSID) of a filter.</span></span>

<span data-ttu-id="6637a-121">Pour plus d’informations, consultez [utilisation des sources](working-with-sources.md) et [utilisation des effets et des transitions](working-with-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="6637a-121">For more information, see [Working with Sources](working-with-sources.md) and [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6637a-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6637a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6637a-123">Vue d’ensemble des composants de la chronologie</span><span class="sxs-lookup"><span data-stu-id="6637a-123">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



