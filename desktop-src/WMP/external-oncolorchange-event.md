---
title: External. OnColorChange, événement
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. OnColorChange, événement
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- Événement External. OnColorChange lecteur Windows Media
topic_type:
- apiref
api_name:
- External.OnColorChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029c8bb860443ed026737c7413be2bed8862c6d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542398"
---
# <a name="externaloncolorchange-event"></a><span data-ttu-id="c9250-105">External. OnColorChange, événement</span><span class="sxs-lookup"><span data-stu-id="c9250-105">External.OnColorChange Event</span></span>

> [!Note]  
> <span data-ttu-id="c9250-106">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="c9250-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c9250-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c9250-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c9250-108">L’événement **OnColorChange** se produit lorsque la couleur de l’interface utilisateur du lecteur Windows Media change.</span><span class="sxs-lookup"><span data-stu-id="c9250-108">The **OnColorChange** event occurs when the color of the Windows Media Player user interface changes.</span></span>

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="c9250-109">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c9250-109">Possible Values</span></span>

<span data-ttu-id="c9250-110">Il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que le lecteur Windows Media appelle lorsque l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="c9250-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9250-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9250-111">Parameters</span></span>

<span data-ttu-id="c9250-112">La fonction qui gère cet événement n’accepte aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c9250-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9250-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c9250-113">Remarks</span></span>

<span data-ttu-id="c9250-114">Les utilisateurs peuvent modifier la couleur de l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c9250-114">Users can change the color of the Windows Media Player user interface.</span></span> <span data-ttu-id="c9250-115">Vous pouvez utiliser cet événement pour personnaliser l’apparence de votre page Web hébergée en fonction du lecteur.</span><span class="sxs-lookup"><span data-stu-id="c9250-115">You can use this event to customize the appearance of your hosted webpage to match the Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9250-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9250-116">Requirements</span></span>



| <span data-ttu-id="c9250-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9250-117">Requirement</span></span> | <span data-ttu-id="c9250-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9250-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9250-119">Version</span><span class="sxs-lookup"><span data-stu-id="c9250-119">Version</span></span><br/> | <span data-ttu-id="c9250-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c9250-120">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="c9250-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c9250-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="c9250-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9250-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9250-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9250-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9250-124">**Objet externe pour les magasins de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="c9250-124">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





