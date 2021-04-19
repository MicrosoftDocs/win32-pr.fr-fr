---
description: La méthode GetCutsOnly détermine si la transition est rendue sous la forme d’une coupe. Si c’est le cas, la transition se produit instantanément au point de coupe.
ms.assetid: d7959816-1152-4bc4-b3f8-bed69b450530
title: 'IAMTimelineTrans :: GetCutsOnly, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d3bbec55ddfe77c053135054fde9b64efce516a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537688"
---
# <a name="iamtimelinetransgetcutsonly-method"></a><span data-ttu-id="41fbd-104">IAMTimelineTrans :: GetCutsOnly, méthode</span><span class="sxs-lookup"><span data-stu-id="41fbd-104">IAMTimelineTrans::GetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="41fbd-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="41fbd-105">\[Deprecated.</span></span> <span data-ttu-id="41fbd-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="41fbd-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="41fbd-107">La `GetCutsOnly` méthode détermine si la transition est rendue sous la forme d’une coupe.</span><span class="sxs-lookup"><span data-stu-id="41fbd-107">The `GetCutsOnly` method determines whether the transition is rendered as a cut.</span></span> <span data-ttu-id="41fbd-108">Si c’est le cas, la transition se produit instantanément au point de coupe.</span><span class="sxs-lookup"><span data-stu-id="41fbd-108">If so, the transition occurs instantaneously at the cut point.</span></span>

## <a name="syntax"></a><span data-ttu-id="41fbd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41fbd-109">Syntax</span></span>


```C++
HRESULT GetCutsOnly(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="41fbd-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41fbd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41fbd-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="41fbd-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="41fbd-112">Reçoit une valeur booléenne spécifiant si la transition est rendue sous la forme d’une coupe.</span><span class="sxs-lookup"><span data-stu-id="41fbd-112">Receives a Boolean value specifying whether the transition is rendered as a cut.</span></span> <span data-ttu-id="41fbd-113">Si la **valeur est true**, la transition est une coupe instantanée.</span><span class="sxs-lookup"><span data-stu-id="41fbd-113">If **TRUE**, the transition is an instantaneous cut.</span></span> <span data-ttu-id="41fbd-114">Si la **valeur est false**, la transition se produit sur sa durée normale.</span><span class="sxs-lookup"><span data-stu-id="41fbd-114">If **FALSE**, the transition occurs over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41fbd-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41fbd-115">Return value</span></span>

<span data-ttu-id="41fbd-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="41fbd-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41fbd-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="41fbd-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="41fbd-118">Notes</span><span class="sxs-lookup"><span data-stu-id="41fbd-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="41fbd-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="41fbd-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="41fbd-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="41fbd-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="41fbd-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="41fbd-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="41fbd-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41fbd-122">Requirements</span></span>



| <span data-ttu-id="41fbd-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41fbd-123">Requirement</span></span> | <span data-ttu-id="41fbd-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="41fbd-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41fbd-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="41fbd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="41fbd-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="41fbd-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="41fbd-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="41fbd-127">Library</span></span><br/> | <dl> <span data-ttu-id="41fbd-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41fbd-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41fbd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41fbd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41fbd-130">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="41fbd-130">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="41fbd-131">**IAMTimelineTrans::SetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="41fbd-131">**IAMTimelineTrans::SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)
</dt> <dt>

[<span data-ttu-id="41fbd-132">**IAMTimelineTrans::GetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="41fbd-132">**IAMTimelineTrans::GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)
</dt> <dt>

[<span data-ttu-id="41fbd-133">**IAMTimeline::TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="41fbd-133">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="41fbd-134">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="41fbd-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




