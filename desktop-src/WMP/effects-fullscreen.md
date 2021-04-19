---
title: EFFECTs. fullScreen
description: L’attribut fullScreen spécifie ou récupère une valeur indiquant si la visualisation en cours est affichée en mode plein écran. Cet attribut ne peut être défini qu’au moment de l’exécution.
ms.assetid: 319b46a4-b6c2-4dda-8285-f12af6836b25
keywords:
- EFFECTs. fullScreen Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e1824e35793a083eb88ea42de0eb8858a4b76f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528830"
---
# <a name="effectsfullscreen"></a><span data-ttu-id="b9d17-105">EFFECTs. fullScreen</span><span class="sxs-lookup"><span data-stu-id="b9d17-105">EFFECTS.fullScreen</span></span>

<span data-ttu-id="b9d17-106">L’attribut **fullscreen** spécifie ou récupère une valeur indiquant si la visualisation en cours est affichée en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="b9d17-106">The **fullScreen** attribute specifies or retrieves a value indicating whether the current visualization is displayed full-screen.</span></span> <span data-ttu-id="b9d17-107">Cet attribut ne peut être défini qu’au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="b9d17-107">This attribute can only be set at run time.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="b9d17-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="b9d17-108">Possible Values</span></span>

<span data-ttu-id="b9d17-109">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b9d17-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="b9d17-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9d17-110">Value</span></span> | <span data-ttu-id="b9d17-111">Description</span><span class="sxs-lookup"><span data-stu-id="b9d17-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="b9d17-112">true</span><span class="sxs-lookup"><span data-stu-id="b9d17-112">true</span></span>  | <span data-ttu-id="b9d17-113">La visualisation s’affiche en plein écran.</span><span class="sxs-lookup"><span data-stu-id="b9d17-113">Visualization is displayed full-screen.</span></span>              |
| <span data-ttu-id="b9d17-114">false</span><span class="sxs-lookup"><span data-stu-id="b9d17-114">false</span></span> | <span data-ttu-id="b9d17-115">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="b9d17-115">Default.</span></span> <span data-ttu-id="b9d17-116">La visualisation n’est pas affichée en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="b9d17-116">Visualization is not displayed full-screen.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b9d17-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b9d17-117">Remarks</span></span>

<span data-ttu-id="b9d17-118">Une visualisation peut être placée en mode plein écran uniquement pendant que le média est en cours de diffusion ou en pause.</span><span class="sxs-lookup"><span data-stu-id="b9d17-118">A visualization can be put into full-screen mode only while media is playing or paused.</span></span> <span data-ttu-id="b9d17-119">Si *Player*. **currentMedia** est une vidéo, un plug-in vidéo doit être présent.</span><span class="sxs-lookup"><span data-stu-id="b9d17-119">If *Player*.**currentMedia** is video, a video plug-in must be present.</span></span> <span data-ttu-id="b9d17-120">S’il s’agit d’un fichier audio, un plug-in de visualisation qui prend en charge l’affichage plein écran doit être présent.</span><span class="sxs-lookup"><span data-stu-id="b9d17-120">If it is audio, a visualization plug-in that supports full-screen display must be present.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9d17-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9d17-121">Requirements</span></span>



| <span data-ttu-id="b9d17-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9d17-122">Requirement</span></span> | <span data-ttu-id="b9d17-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9d17-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b9d17-124">Version</span><span class="sxs-lookup"><span data-stu-id="b9d17-124">Version</span></span><br/> | <span data-ttu-id="b9d17-125">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="b9d17-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9d17-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9d17-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9d17-127">**Élément EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="b9d17-127">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





