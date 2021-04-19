---
description: La méthode EffectSwapPriorities bascule les niveaux de priorité de deux effets.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: 'IAMTimelineEffectable :: EffectSwapPriorities, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fb6a7dbee2d7f90da8f32e2a034e82df485f1ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545696"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a><span data-ttu-id="05bed-103">IAMTimelineEffectable :: EffectSwapPriorities, méthode</span><span class="sxs-lookup"><span data-stu-id="05bed-103">IAMTimelineEffectable::EffectSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="05bed-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="05bed-104">\[Deprecated.</span></span> <span data-ttu-id="05bed-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="05bed-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="05bed-106">La `EffectSwapPriorities` méthode bascule les niveaux de priorité de deux effets.</span><span class="sxs-lookup"><span data-stu-id="05bed-106">The `EffectSwapPriorities` method switches the priority levels of two effects.</span></span>

<span data-ttu-id="05bed-107">Étant donné deux valeurs de priorité, cette méthode permute les effets à ces priorités.</span><span class="sxs-lookup"><span data-stu-id="05bed-107">Given two priority values, this method swaps the effects at those priorities.</span></span> <span data-ttu-id="05bed-108">Lorsque la méthode retourne, l’effet qui se trouvait au premier niveau de priorité est le deuxième niveau de priorité, et vice versa.</span><span class="sxs-lookup"><span data-stu-id="05bed-108">When the method returns, the effect that was at the first priority level is at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="05bed-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05bed-109">Syntax</span></span>


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a><span data-ttu-id="05bed-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05bed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05bed-111">*Prioritéa*</span><span class="sxs-lookup"><span data-stu-id="05bed-111">*PriorityA*</span></span> 
</dt> <dd>

<span data-ttu-id="05bed-112">Premier niveau de priorité auquel permuter les effets.</span><span class="sxs-lookup"><span data-stu-id="05bed-112">First priority level at which to swap effects.</span></span>

</dd> <dt>

<span data-ttu-id="05bed-113">*PriorityB*</span><span class="sxs-lookup"><span data-stu-id="05bed-113">*PriorityB*</span></span> 
</dt> <dd>

<span data-ttu-id="05bed-114">Deuxième niveau de priorité auquel permuter les effets.</span><span class="sxs-lookup"><span data-stu-id="05bed-114">Second priority level at which to swap effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05bed-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05bed-115">Return value</span></span>

<span data-ttu-id="05bed-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="05bed-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="05bed-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="05bed-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="05bed-118">Notes</span><span class="sxs-lookup"><span data-stu-id="05bed-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="05bed-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="05bed-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="05bed-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="05bed-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="05bed-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="05bed-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="05bed-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05bed-122">Requirements</span></span>



| <span data-ttu-id="05bed-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05bed-123">Requirement</span></span> | <span data-ttu-id="05bed-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="05bed-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05bed-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="05bed-125">Header</span></span><br/>  | <dl> <span data-ttu-id="05bed-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="05bed-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="05bed-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="05bed-127">Library</span></span><br/> | <dl> <span data-ttu-id="05bed-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05bed-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05bed-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05bed-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05bed-130">**Interface IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="05bed-130">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="05bed-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="05bed-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




