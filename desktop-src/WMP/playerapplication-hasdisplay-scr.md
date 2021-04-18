---
title: Attribut PLAYERAPPLICATION. hasDisplay
description: L’attribut hasDisplay récupère une valeur indiquant si la vidéo peut s’afficher via le contrôle du lecteur Windows Media distant.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- Lecteur Windows Media PLAYERAPPLICATION. hasDisplay
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7579c724496ee2f36ce12adb01c2f13a0962e7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533030"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="10e64-104">PLAYERAPPLICATION.hasDisplay</span><span class="sxs-lookup"><span data-stu-id="10e64-104">PLAYERAPPLICATION.hasDisplay</span></span>

<span data-ttu-id="10e64-105">L’attribut **hasDisplay** récupère une valeur indiquant si la vidéo peut s’afficher via le contrôle du lecteur Windows Media distant.</span><span class="sxs-lookup"><span data-stu-id="10e64-105">The **hasDisplay** attribute retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span>

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a><span data-ttu-id="10e64-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="10e64-106">Possible Values</span></span>

<span data-ttu-id="10e64-107">Cet attribut est une **valeur booléenne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="10e64-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="10e64-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="10e64-108">Value</span></span> | <span data-ttu-id="10e64-109">Description</span><span class="sxs-lookup"><span data-stu-id="10e64-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="10e64-110">True</span><span class="sxs-lookup"><span data-stu-id="10e64-110">True</span></span>  | <span data-ttu-id="10e64-111">La vidéo peut être affichée.</span><span class="sxs-lookup"><span data-stu-id="10e64-111">The video can display.</span></span>    |
| <span data-ttu-id="10e64-112">Faux</span><span class="sxs-lookup"><span data-stu-id="10e64-112">False</span></span> | <span data-ttu-id="10e64-113">La vidéo ne peut pas être affichée.</span><span class="sxs-lookup"><span data-stu-id="10e64-113">The video cannot display.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="10e64-114">Notes</span><span class="sxs-lookup"><span data-stu-id="10e64-114">Remarks</span></span>

<span data-ttu-id="10e64-115">Cet attribut est utilisé uniquement lors de la communication à distance du contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="10e64-115">This attribute is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="10e64-116">Plusieurs contrôles de lecteur Windows Media peuvent s’exécuter à distance en même temps, mais la vidéo ne peut s’afficher qu’à un seul emplacement à la fois, soit en mode complet du lecteur, soit dans l’un des contrôles distants.</span><span class="sxs-lookup"><span data-stu-id="10e64-116">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted controls.</span></span> <span data-ttu-id="10e64-117">Utilisez cette propriété pour déterminer si le contrôle actuel est celui par le biais duquel la vidéo peut être affichée.</span><span class="sxs-lookup"><span data-stu-id="10e64-117">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="10e64-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10e64-118">Requirements</span></span>



| <span data-ttu-id="10e64-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10e64-119">Requirement</span></span> | <span data-ttu-id="10e64-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="10e64-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="10e64-121">Version</span><span class="sxs-lookup"><span data-stu-id="10e64-121">Version</span></span><br/> | <span data-ttu-id="10e64-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="10e64-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10e64-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10e64-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10e64-124">**Élément PLAYERAPPLICATION**</span><span class="sxs-lookup"><span data-stu-id="10e64-124">**PLAYERAPPLICATION Element**</span></span>](playerapplication-element.md)
</dt> <dt>

[<span data-ttu-id="10e64-125">**Utilisation à distance du contrôle Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="10e64-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





