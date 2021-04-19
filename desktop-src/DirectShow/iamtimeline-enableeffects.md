---
description: La méthode EnableEffects active ou désactive tous les effets de la chronologie. Si les effets sont désactivés, ils restent dans la chronologie, mais ne sont pas rendus.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: 'IAMTimeline :: EnableEffects, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e090f115083e2d1433e60d7a8707ded9b89ba433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532239"
---
# <a name="iamtimelineenableeffects-method"></a><span data-ttu-id="65aa5-104">IAMTimeline :: EnableEffects, méthode</span><span class="sxs-lookup"><span data-stu-id="65aa5-104">IAMTimeline::EnableEffects method</span></span>

> [!Note]  
> <span data-ttu-id="65aa5-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="65aa5-105">\[Deprecated.</span></span> <span data-ttu-id="65aa5-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="65aa5-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="65aa5-107">La `EnableEffects` méthode active ou désactive tous les effets de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="65aa5-107">The `EnableEffects` method enables or disables all effects in the timeline.</span></span> <span data-ttu-id="65aa5-108">Si les effets sont désactivés, ils restent dans la chronologie, mais ne sont pas rendus.</span><span class="sxs-lookup"><span data-stu-id="65aa5-108">If effects are disabled, they remain in the timeline but are not rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="65aa5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65aa5-109">Syntax</span></span>


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="65aa5-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65aa5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65aa5-111">*fEnabled*</span><span class="sxs-lookup"><span data-stu-id="65aa5-111">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="65aa5-112">Valeur booléenne qui spécifie s’il faut activer ou désactiver les effets.</span><span class="sxs-lookup"><span data-stu-id="65aa5-112">Boolean value that specifies whether to enable or disable effects.</span></span> <span data-ttu-id="65aa5-113">Si la **valeur est true**, les effets sont activés.</span><span class="sxs-lookup"><span data-stu-id="65aa5-113">If **TRUE**, effects are enabled.</span></span> <span data-ttu-id="65aa5-114">Si la **valeur est false**, les effets sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="65aa5-114">If **FALSE**, effects are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65aa5-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65aa5-115">Return value</span></span>

<span data-ttu-id="65aa5-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="65aa5-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65aa5-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65aa5-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65aa5-118">Notes</span><span class="sxs-lookup"><span data-stu-id="65aa5-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="65aa5-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="65aa5-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="65aa5-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="65aa5-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="65aa5-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="65aa5-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65aa5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65aa5-122">Requirements</span></span>



| <span data-ttu-id="65aa5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65aa5-123">Requirement</span></span> | <span data-ttu-id="65aa5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="65aa5-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65aa5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="65aa5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="65aa5-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="65aa5-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="65aa5-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="65aa5-127">Library</span></span><br/> | <dl> <span data-ttu-id="65aa5-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65aa5-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65aa5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65aa5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65aa5-130">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="65aa5-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="65aa5-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="65aa5-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




