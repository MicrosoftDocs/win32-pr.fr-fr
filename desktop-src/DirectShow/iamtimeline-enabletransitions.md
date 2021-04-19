---
description: La méthode EnableTransitions active ou désactive toutes les transitions dans la chronologie.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'IAMTimeline :: EnableTransitions, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530956"
---
# <a name="iamtimelineenabletransitions-method"></a><span data-ttu-id="430f8-103">IAMTimeline :: EnableTransitions, méthode</span><span class="sxs-lookup"><span data-stu-id="430f8-103">IAMTimeline::EnableTransitions method</span></span>

> [!Note]  
> <span data-ttu-id="430f8-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="430f8-104">\[Deprecated.</span></span> <span data-ttu-id="430f8-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="430f8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="430f8-106">La `EnableTransitions` méthode active ou désactive toutes les transitions dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="430f8-106">The `EnableTransitions` method enables or disables all transitions in the timeline.</span></span> <span data-ttu-id="430f8-107">Si les transitions sont désactivées, les moteurs de rendu les traitent comme des coupes. autrement dit, la sortie rendue passe instantanément d’une piste à la suivante.</span><span class="sxs-lookup"><span data-stu-id="430f8-107">If transitions are disabled, the render engines treats them as cuts; that is, the rendered output jumps instantly from one track to the next.</span></span> <span data-ttu-id="430f8-108">Le point de coupe par défaut est à mi-chemin dans la durée de la transition.</span><span class="sxs-lookup"><span data-stu-id="430f8-108">The default cut point is halfway through the duration of the transition.</span></span> <span data-ttu-id="430f8-109">Vous pouvez modifier le point de coupe en appelant la méthode [**IAMTimelineTrans :: SetCutPoint**](iamtimelinetrans-setcutpoint.md) sur la transition.</span><span class="sxs-lookup"><span data-stu-id="430f8-109">You can change the cut point by calling the [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md) method on the transition.</span></span> <span data-ttu-id="430f8-110">Les transitions désactivées ne sont pas supprimées de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="430f8-110">Disabled transitions are not removed from the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="430f8-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="430f8-111">Syntax</span></span>


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="430f8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="430f8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="430f8-113">*fEnabled*</span><span class="sxs-lookup"><span data-stu-id="430f8-113">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="430f8-114">Valeur booléenne qui spécifie s’il faut activer ou désactiver les transitions.</span><span class="sxs-lookup"><span data-stu-id="430f8-114">Boolean value that specifies whether to enable or disable transitions.</span></span> <span data-ttu-id="430f8-115">Si la **valeur est true**, les transitions sont activées.</span><span class="sxs-lookup"><span data-stu-id="430f8-115">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="430f8-116">Si la **valeur est false**, les transitions sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="430f8-116">If **FALSE**, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="430f8-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="430f8-117">Return value</span></span>

<span data-ttu-id="430f8-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="430f8-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="430f8-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="430f8-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="430f8-120">Notes</span><span class="sxs-lookup"><span data-stu-id="430f8-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="430f8-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="430f8-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="430f8-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="430f8-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="430f8-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="430f8-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="430f8-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="430f8-124">Requirements</span></span>



| <span data-ttu-id="430f8-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="430f8-125">Requirement</span></span> | <span data-ttu-id="430f8-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="430f8-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="430f8-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="430f8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="430f8-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="430f8-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="430f8-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="430f8-129">Library</span></span><br/> | <dl> <span data-ttu-id="430f8-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="430f8-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="430f8-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="430f8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="430f8-132">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="430f8-132">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="430f8-133">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="430f8-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




