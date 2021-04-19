---
description: La méthode SetSwapInputs spécifie si les entrées de transition sont échangées.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: 'IAMTimelineTrans :: SetSwapInputs, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b2deecb393d6532015cf1490aacd1bd50501920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541496"
---
# <a name="iamtimelinetranssetswapinputs-method"></a><span data-ttu-id="16f1b-103">IAMTimelineTrans :: SetSwapInputs, méthode</span><span class="sxs-lookup"><span data-stu-id="16f1b-103">IAMTimelineTrans::SetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="16f1b-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="16f1b-104">\[Deprecated.</span></span> <span data-ttu-id="16f1b-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="16f1b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="16f1b-106">La `SetSwapInputs` méthode spécifie si les entrées de transition sont échangées.</span><span class="sxs-lookup"><span data-stu-id="16f1b-106">The `SetSwapInputs` method specifies whether the transition inputs are swapped.</span></span>

<span data-ttu-id="16f1b-107">Par défaut, une transition va du composite de toutes les couches de faible priorité à la couche où la transition réside.</span><span class="sxs-lookup"><span data-stu-id="16f1b-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="16f1b-108">Vous pouvez inverser cette progression, de sorte que la transition va de la couche où elle réside vers l’composite des couches de faible priorité.</span><span class="sxs-lookup"><span data-stu-id="16f1b-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span> <span data-ttu-id="16f1b-109">Pour plus d’informations, consultez [direction de transition](transition-direction.md).</span><span class="sxs-lookup"><span data-stu-id="16f1b-109">For more information, see [Transition Direction](transition-direction.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="16f1b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16f1b-110">Syntax</span></span>


```C++
HRESULT SetSwapInputs(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="16f1b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16f1b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16f1b-112">*Val*</span><span class="sxs-lookup"><span data-stu-id="16f1b-112">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="16f1b-113">Spécifie si les entrées sont échangées.</span><span class="sxs-lookup"><span data-stu-id="16f1b-113">Specifies whether the inputs are swapped.</span></span> <span data-ttu-id="16f1b-114">Si la **valeur est false**, la transition passe de l’composite de toutes les couches de faible priorité à la couche de transition.</span><span class="sxs-lookup"><span data-stu-id="16f1b-114">If **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="16f1b-115">Si la **valeur est true**, la transition passe dans la direction opposée.</span><span class="sxs-lookup"><span data-stu-id="16f1b-115">If **TRUE**, the transition goes in the opposite direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16f1b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16f1b-116">Return value</span></span>

<span data-ttu-id="16f1b-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="16f1b-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="16f1b-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="16f1b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="16f1b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="16f1b-119">Remarks</span></span>

<span data-ttu-id="16f1b-120">Cette méthode ne modifie pas la direction de l’effet visuel.</span><span class="sxs-lookup"><span data-stu-id="16f1b-120">This method does not change the direction of the visual effect.</span></span> <span data-ttu-id="16f1b-121">Par exemple, une réinitialisation de gauche à droite sera toujours de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="16f1b-121">For example, a left-to-right wipe will still go from left to right.</span></span> <span data-ttu-id="16f1b-122">Pour modifier la direction, définissez la propriété **Progress** à l’aide de l’interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="16f1b-122">To change the direction, set the **Progress** property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="16f1b-123">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="16f1b-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="16f1b-124">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="16f1b-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="16f1b-125">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="16f1b-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16f1b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16f1b-126">Requirements</span></span>



| <span data-ttu-id="16f1b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16f1b-127">Requirement</span></span> | <span data-ttu-id="16f1b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="16f1b-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16f1b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="16f1b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="16f1b-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="16f1b-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="16f1b-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="16f1b-131">Library</span></span><br/> | <dl> <span data-ttu-id="16f1b-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16f1b-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16f1b-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16f1b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16f1b-134">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="16f1b-134">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="16f1b-135">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="16f1b-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




