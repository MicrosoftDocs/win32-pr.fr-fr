---
title: Objet Propriétés du média d’entrée
description: Objet Propriétés du média d’entrée
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- SDK Windows Media format, objets de propriétés de média d’entrée
- ASF (Advanced Systems Format), objets de propriétés de média d’entrée
- ASF (format de systèmes avancés), objets de propriétés de média d’entrée
- objets, objets de propriétés de média d’entrée
- objets de propriétés de média d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841881"
---
# <a name="input-media-properties-object"></a><span data-ttu-id="cdfcf-108">Objet Propriétés du média d’entrée</span><span class="sxs-lookup"><span data-stu-id="cdfcf-108">Input Media Properties Object</span></span>

<span data-ttu-id="cdfcf-109">Un objet de propriétés de média d’entrée créé par l’objet Writer prend en charge les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="cdfcf-109">An input media properties object created by the writer object supports the following interfaces.</span></span> <span data-ttu-id="cdfcf-110">Ces interfaces sont accessibles par un appel à **QueryInterface** sur l’une des interfaces de l’objet Writer.</span><span class="sxs-lookup"><span data-stu-id="cdfcf-110">These interfaces are accessed by a call to **QueryInterface** on one of the interfaces of the writer object.</span></span>



| <span data-ttu-id="cdfcf-111">Interface</span><span class="sxs-lookup"><span data-stu-id="cdfcf-111">Interface</span></span>                                        | <span data-ttu-id="cdfcf-112">Description</span><span class="sxs-lookup"><span data-stu-id="cdfcf-112">Description</span></span>                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdfcf-113">**IWMInputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="cdfcf-113">**IWMInputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | <span data-ttu-id="cdfcf-114">Récupère les propriétés d’un flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cdfcf-114">Retrieves the properties of an input stream.</span></span>                                                               |
| [<span data-ttu-id="cdfcf-115">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="cdfcf-115">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="cdfcf-116">Utilisé comme interface de base pour les autres interfaces de propriété de média (entrée, sortie et vidéo).</span><span class="sxs-lookup"><span data-stu-id="cdfcf-116">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="cdfcf-117">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="cdfcf-117">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="cdfcf-118">Gère les propriétés d’un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="cdfcf-118">Manages the properties of a video stream.</span></span> <span data-ttu-id="cdfcf-119">Il s’agit d’une interface facultative, disponible uniquement pour les flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="cdfcf-119">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cdfcf-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cdfcf-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdfcf-121">**Objets**</span><span class="sxs-lookup"><span data-stu-id="cdfcf-121">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="cdfcf-122">**Auteur, objet**</span><span class="sxs-lookup"><span data-stu-id="cdfcf-122">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




