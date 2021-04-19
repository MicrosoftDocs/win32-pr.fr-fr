---
title: VIDEO. fullScreen
description: L’attribut fullScreen spécifie ou récupère une valeur indiquant si la vidéo est affichée en mode plein écran.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- VIDEO. fullScreen Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c27fa1bde6437b55689494751410145995862d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533375"
---
# <a name="videofullscreen"></a><span data-ttu-id="5af0c-104">VIDEO. fullScreen</span><span class="sxs-lookup"><span data-stu-id="5af0c-104">VIDEO.fullScreen</span></span>

<span data-ttu-id="5af0c-105">L’attribut **fullscreen** spécifie ou récupère une valeur indiquant si la vidéo est affichée en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="5af0c-105">The **fullScreen** attribute specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="5af0c-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="5af0c-106">Possible Values</span></span>

<span data-ttu-id="5af0c-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5af0c-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="5af0c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="5af0c-108">Value</span></span> | <span data-ttu-id="5af0c-109">Description</span><span class="sxs-lookup"><span data-stu-id="5af0c-109">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="5af0c-110">true</span><span class="sxs-lookup"><span data-stu-id="5af0c-110">true</span></span>  | <span data-ttu-id="5af0c-111">La vidéo s’affiche en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="5af0c-111">Video displays in full-screen mode.</span></span>                  |
| <span data-ttu-id="5af0c-112">false</span><span class="sxs-lookup"><span data-stu-id="5af0c-112">false</span></span> | <span data-ttu-id="5af0c-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="5af0c-113">Default.</span></span> <span data-ttu-id="5af0c-114">La vidéo ne s’affiche pas en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="5af0c-114">Video does not display in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5af0c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5af0c-115">Remarks</span></span>

<span data-ttu-id="5af0c-116">Cette propriété ne peut être spécifiée qu’au moment de l’exécution, une fois qu’un fichier a été chargé.</span><span class="sxs-lookup"><span data-stu-id="5af0c-116">This property can be specified only at run time, after a file has been loaded.</span></span> <span data-ttu-id="5af0c-117">Il doit donc être défini dans un gestionnaire d’événements de script.</span><span class="sxs-lookup"><span data-stu-id="5af0c-117">It must therefore be set within a script event handler.</span></span> <span data-ttu-id="5af0c-118">Le bouton d’échappement est utilisé pour revenir à un affichage normal.</span><span class="sxs-lookup"><span data-stu-id="5af0c-118">The escape button is used to return to normal viewing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5af0c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5af0c-119">Requirements</span></span>



| <span data-ttu-id="5af0c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5af0c-120">Requirement</span></span> | <span data-ttu-id="5af0c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5af0c-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5af0c-122">Version</span><span class="sxs-lookup"><span data-stu-id="5af0c-122">Version</span></span><br/> | <span data-ttu-id="5af0c-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="5af0c-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5af0c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5af0c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af0c-125">**Élément VIDEO**</span><span class="sxs-lookup"><span data-stu-id="5af0c-125">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="5af0c-126">**VIDÉO. maintainAspectRatio**</span><span class="sxs-lookup"><span data-stu-id="5af0c-126">**VIDEO.maintainAspectRatio**</span></span>](video-maintainaspectratio.md)
</dt> <dt>

[<span data-ttu-id="5af0c-127">**VIDÉO. shrinkToFit**</span><span class="sxs-lookup"><span data-stu-id="5af0c-127">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> <dt>

[<span data-ttu-id="5af0c-128">**VIDÉO. stretchToFit**</span><span class="sxs-lookup"><span data-stu-id="5af0c-128">**VIDEO.stretchToFit**</span></span>](video-stretchtofit.md)
</dt> </dl>

 

 





