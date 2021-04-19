---
title: Événement External. OnColorChange (type 1)
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Événement External. OnColorChange (type 1)
ms.assetid: 45e6ec4a-e680-4d50-8fb7-410f12383eef
keywords:
- External. OnColorChange, événement (type 1) lecteur Windows Media
topic_type:
- apiref
api_name:
- External.OnColorChange Event (Type 1)
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11805cc154c60b8a765f46041f74d40929df418d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541302"
---
# <a name="externaloncolorchange-event-type-1"></a><span data-ttu-id="8f2ba-105">Événement External. OnColorChange (type 1)</span><span class="sxs-lookup"><span data-stu-id="8f2ba-105">External.OnColorChange Event (Type 1)</span></span>

> [!Note]  
> <span data-ttu-id="8f2ba-106">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="8f2ba-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="8f2ba-108">L’événement **OnColorChange** se produit lorsque la couleur de l’interface utilisateur du lecteur Windows Media change.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-108">The **OnColorChange** event occurs when the color of the Windows Media Player user interface changes.</span></span>

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="8f2ba-109">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="8f2ba-109">Possible Values</span></span>

<span data-ttu-id="8f2ba-110">Il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que le lecteur Windows Media appelle lorsque l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f2ba-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f2ba-111">Parameters</span></span>

<span data-ttu-id="8f2ba-112">La fonction qui gère cet événement n’accepte aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f2ba-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8f2ba-113">Remarks</span></span>

<span data-ttu-id="8f2ba-114">Les utilisateurs peuvent modifier la couleur de l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-114">Users can change the color of the Windows Media Player user interface.</span></span> <span data-ttu-id="8f2ba-115">Vous pouvez utiliser cet événement pour personnaliser l’apparence de votre page Web hébergée en fonction du lecteur.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-115">You can use this event to customize the appearance of your hosted webpage to match the Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f2ba-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f2ba-116">Requirements</span></span>



| <span data-ttu-id="8f2ba-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f2ba-117">Requirement</span></span> | <span data-ttu-id="8f2ba-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f2ba-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2ba-119">Version</span><span class="sxs-lookup"><span data-stu-id="8f2ba-119">Version</span></span><br/> | <span data-ttu-id="8f2ba-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8f2ba-120">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="8f2ba-121">DLL</span><span class="sxs-lookup"><span data-stu-id="8f2ba-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="8f2ba-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f2ba-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f2ba-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f2ba-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f2ba-124">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="8f2ba-124">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





