---
title: Attribut PLAYERAPPLICATION. playerDocked
description: L’attribut playerDocked récupère une valeur indiquant si le lecteur Windows Media est dans un état d’ancrage.
ms.assetid: 8b95da72-037b-4179-a564-fc9bc63368ac
keywords:
- Lecteur Windows Media PLAYERAPPLICATION. playerDocked
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.playerDocked
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21abe3dd5cb14906db39e8eb50a1d18302a92ff6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533072"
---
# <a name="playerapplicationplayerdocked"></a><span data-ttu-id="7f374-104">PLAYERAPPLICATION.playerDocked</span><span class="sxs-lookup"><span data-stu-id="7f374-104">PLAYERAPPLICATION.playerDocked</span></span>

<span data-ttu-id="7f374-105">L’attribut **playerDocked** récupère une valeur indiquant si le lecteur Windows Media est dans un état d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="7f374-105">The **playerDocked** attribute retrieves a value indicating whether Windows Media Player is in a docked state.</span></span>

``` syntax
        elementID.playerDocked
```

## <a name="possible-values"></a><span data-ttu-id="7f374-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="7f374-106">Possible Values</span></span>

<span data-ttu-id="7f374-107">Cet attribut est une **valeur booléenne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7f374-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="7f374-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f374-108">Value</span></span> | <span data-ttu-id="7f374-109">Description</span><span class="sxs-lookup"><span data-stu-id="7f374-109">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="7f374-110">True</span><span class="sxs-lookup"><span data-stu-id="7f374-110">True</span></span>  | <span data-ttu-id="7f374-111">Le lecteur Windows Media est ancré.</span><span class="sxs-lookup"><span data-stu-id="7f374-111">Windows Media Player is docked.</span></span>   |
| <span data-ttu-id="7f374-112">Faux</span><span class="sxs-lookup"><span data-stu-id="7f374-112">False</span></span> | <span data-ttu-id="7f374-113">Le lecteur Windows Media n’est pas ancré.</span><span class="sxs-lookup"><span data-stu-id="7f374-113">Windows Media Player is undocked.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7f374-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7f374-114">Remarks</span></span>

<span data-ttu-id="7f374-115">Cet attribut est utilisé uniquement lors de la communication à distance du contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7f374-115">This attribute is used only when remoting the Windows Media Player control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f374-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f374-116">Requirements</span></span>



| <span data-ttu-id="7f374-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f374-117">Requirement</span></span> | <span data-ttu-id="7f374-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f374-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="7f374-119">Version</span><span class="sxs-lookup"><span data-stu-id="7f374-119">Version</span></span><br/> | <span data-ttu-id="7f374-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7f374-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7f374-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f374-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f374-122">**Élément PLAYERAPPLICATION**</span><span class="sxs-lookup"><span data-stu-id="7f374-122">**PLAYERAPPLICATION Element**</span></span>](playerapplication-element.md)
</dt> <dt>

[<span data-ttu-id="7f374-123">**Utilisation à distance du contrôle Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="7f374-123">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





