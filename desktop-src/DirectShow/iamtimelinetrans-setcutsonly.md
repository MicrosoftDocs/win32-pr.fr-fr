---
description: La méthode SetCutsOnly spécifie si la transition est rendue sous la forme d’une coupe. Si c’est le cas, la transition se produit instantanément au point de coupe. Si le rendu d’une transition prend beaucoup de temps, vous souhaiterez peut-être l’afficher en mode d’affichage couper pour accélérer l’affichage.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: 'IAMTimelineTrans :: SetCutsOnly, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b2944d652bffac5bf3bfa72a1e2372f734645bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528841"
---
# <a name="iamtimelinetranssetcutsonly-method"></a><span data-ttu-id="5460f-105">IAMTimelineTrans :: SetCutsOnly, méthode</span><span class="sxs-lookup"><span data-stu-id="5460f-105">IAMTimelineTrans::SetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="5460f-106">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5460f-106">\[Deprecated.</span></span> <span data-ttu-id="5460f-107">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5460f-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5460f-108">La `SetCutsOnly` méthode spécifie si la transition est rendue sous la forme d’une coupe.</span><span class="sxs-lookup"><span data-stu-id="5460f-108">The `SetCutsOnly` method specifies whether the transition is rendered as a cut.</span></span> <span data-ttu-id="5460f-109">Si c’est le cas, la transition se produit instantanément au point de coupe.</span><span class="sxs-lookup"><span data-stu-id="5460f-109">If so, the transition occurs instantly at the cut point.</span></span> <span data-ttu-id="5460f-110">Si le rendu d’une transition prend beaucoup de temps, vous souhaiterez peut-être l’afficher en mode d’affichage couper pour accélérer l’affichage.</span><span class="sxs-lookup"><span data-stu-id="5460f-110">If a transition takes a long time to render, you might want to preview it as a cut to speed preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="5460f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5460f-111">Syntax</span></span>


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="5460f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5460f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5460f-113">*Val*</span><span class="sxs-lookup"><span data-stu-id="5460f-113">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="5460f-114">Spécifie s’il faut restituer la transition comme une coupe.</span><span class="sxs-lookup"><span data-stu-id="5460f-114">Specifies whether to render the transition as a cut.</span></span> <span data-ttu-id="5460f-115">Si la **valeur est true**, la transition est rendue sous la forme d’une coupe instantanée.</span><span class="sxs-lookup"><span data-stu-id="5460f-115">If **TRUE**, the transition is rendered as an instantaneous cut.</span></span> <span data-ttu-id="5460f-116">Si la **valeur est false**, la transition est rendue sur sa durée normale.</span><span class="sxs-lookup"><span data-stu-id="5460f-116">If **FALSE**, the transition renders over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5460f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5460f-117">Return value</span></span>

<span data-ttu-id="5460f-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5460f-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5460f-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5460f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5460f-120">Notes</span><span class="sxs-lookup"><span data-stu-id="5460f-120">Remarks</span></span>

<span data-ttu-id="5460f-121">Le rendu d’une transition en tant que coupe n’est pas compatible avec la permutation des entrées.</span><span class="sxs-lookup"><span data-stu-id="5460f-121">Rendering a transition as a cut is not compatible with swapping the inputs.</span></span> <span data-ttu-id="5460f-122">(Voir [**IAMTimelineTrans :: SetSwapInputs**](iamtimelinetrans-setswapinputs.md).) Si vous appelez `SetCutsOnly` avec la valeur **true**, il remplace temporairement le paramètre **SetSwapInputs** .</span><span class="sxs-lookup"><span data-stu-id="5460f-122">(See [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md).) If you call `SetCutsOnly` with a value of **TRUE**, it temporarily overrides the **SetSwapInputs** setting.</span></span> <span data-ttu-id="5460f-123">Toutefois, le paramètre de coupe uniquement est prévu pour l’aperçu. par conséquent, cette limitation n’affecte pas la sortie du fichier. n’oubliez pas d’appeler `SetCutsOnly` avec la valeur **false** avant d’écrire le fichier.</span><span class="sxs-lookup"><span data-stu-id="5460f-123">The cuts-only setting is intended for preview, however, so this limitation does not affect file output—just remember to call `SetCutsOnly` with the value **FALSE** before writing the file.</span></span>

> [!Note]  
> <span data-ttu-id="5460f-124">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="5460f-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5460f-125">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5460f-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5460f-126">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5460f-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5460f-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5460f-127">Requirements</span></span>



| <span data-ttu-id="5460f-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5460f-128">Requirement</span></span> | <span data-ttu-id="5460f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="5460f-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5460f-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="5460f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5460f-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5460f-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5460f-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5460f-132">Library</span></span><br/> | <dl> <span data-ttu-id="5460f-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5460f-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5460f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5460f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5460f-135">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="5460f-135">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="5460f-136">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="5460f-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




