---
title: CounterItem. Width, propriété
description: Récupère ou définit la largeur de ligne utilisée pour représenter sous forme de graphique la valeur de compteur.
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Propriété Width SysMon
- Propriété Width SysMon, classe CounterItem
- Classe CounterItem SysMon, propriété Width
topic_type:
- apiref
api_name:
- CounterItem.Width
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67892f9e4cf6799f1b9311bb2cd47ec02744cb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741788"
---
# <a name="counteritemwidth-property"></a><span data-ttu-id="6634c-106">CounterItem. Width, propriété</span><span class="sxs-lookup"><span data-stu-id="6634c-106">CounterItem.Width property</span></span>

<span data-ttu-id="6634c-107">Récupère ou définit la largeur de ligne utilisée pour représenter sous forme de graphique la valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="6634c-107">Retrieves or sets the line width used to graph the counter value.</span></span>

<span data-ttu-id="6634c-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6634c-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6634c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6634c-109">Syntax</span></span>


```VB
Property Width As Long
```



## <a name="property-value"></a><span data-ttu-id="6634c-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6634c-110">Property value</span></span>

<span data-ttu-id="6634c-111">Largeur de ligne utilisée dans un graphique linéaire.</span><span class="sxs-lookup"><span data-stu-id="6634c-111">Line width used in a line graph.</span></span> <span data-ttu-id="6634c-112">Les valeurs valides sont comprises entre 1 et 3, où 1 (la valeur par défaut) est la largeur la plus étroite.</span><span class="sxs-lookup"><span data-stu-id="6634c-112">Valid values range from 1 to 3, where 1 (the default value) is the narrowest width.</span></span>

<span data-ttu-id="6634c-113">**Avant Windows Vista :** Les valeurs valides sont comprises entre 1 et 9.</span><span class="sxs-lookup"><span data-stu-id="6634c-113">**Prior to Windows Vista:** Valid values range from 1 to 9.</span></span> <span data-ttu-id="6634c-114">N’utilisez pas une valeur de largeur supérieure à 3 Si votre application est exécutée sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6634c-114">Do not use a width value greater than 3 if your application will be run on Windows Vista.</span></span>

## <a name="exceptions"></a><span data-ttu-id="6634c-115">Exceptions</span><span class="sxs-lookup"><span data-stu-id="6634c-115">Exceptions</span></span>



| <span data-ttu-id="6634c-116">Type d'exception</span><span class="sxs-lookup"><span data-stu-id="6634c-116">Exception type</span></span>               | <span data-ttu-id="6634c-117">Condition</span><span class="sxs-lookup"><span data-stu-id="6634c-117">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="6634c-118">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="6634c-118">**System.ArgumentException**</span></span> | <span data-ttu-id="6634c-119">La largeur de ligne spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6634c-119">The specified line width is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6634c-120">Notes</span><span class="sxs-lookup"><span data-stu-id="6634c-120">Remarks</span></span>

<span data-ttu-id="6634c-121">La largeur de ligne par défaut pour les seize premiers compteurs que vous ajoutez est 1.</span><span class="sxs-lookup"><span data-stu-id="6634c-121">The default line width for the first sixteen counters that you add is 1.</span></span> <span data-ttu-id="6634c-122">La largeur de ligne par défaut pour les seize compteurs suivants (compteurs 17-32) que vous ajoutez est 2.</span><span class="sxs-lookup"><span data-stu-id="6634c-122">The default line width for the next sixteen counters (counters 17 - 32) that you add is 2.</span></span> <span data-ttu-id="6634c-123">La largeur de ligne par défaut pour les seize compteurs suivants (compteurs 33-48) que vous ajoutez est 3.</span><span class="sxs-lookup"><span data-stu-id="6634c-123">The default line width for the next sixteen counters (counters 33 - 48) that you add is 3.</span></span> <span data-ttu-id="6634c-124">Après cela, SYSMON choisit de façon aléatoire la largeur de ligne.</span><span class="sxs-lookup"><span data-stu-id="6634c-124">After that, SYSMON randomly chooses the line width.</span></span> <span data-ttu-id="6634c-125">Pour plus d’informations, consultez [**CounterItem. Color**](counteritem-color.md).</span><span class="sxs-lookup"><span data-stu-id="6634c-125">For details, see [**CounterItem.Color**](counteritem-color.md).</span></span>

<span data-ttu-id="6634c-126">Pour spécifier un [**style de ligne**](counteritem-linestyle.md) autre que Solid, la largeur doit être 1.</span><span class="sxs-lookup"><span data-stu-id="6634c-126">To specify a [**line style**](counteritem-linestyle.md) other than solid, the width must be 1.</span></span> <span data-ttu-id="6634c-127">Si vous spécifiez une valeur supérieure à 1 et spécifiez un style de ligne non plein, SYSMON ignore la largeur de ligne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6634c-127">If you specify a value greater than 1 and specify a non-solid line style, SYSMON ignores the specified line width.</span></span>

## <a name="requirements"></a><span data-ttu-id="6634c-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6634c-128">Requirements</span></span>



| <span data-ttu-id="6634c-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6634c-129">Requirement</span></span> | <span data-ttu-id="6634c-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="6634c-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6634c-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6634c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6634c-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6634c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6634c-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6634c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6634c-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6634c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6634c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6634c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6634c-136"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6634c-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6634c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6634c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6634c-138">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="6634c-138">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





