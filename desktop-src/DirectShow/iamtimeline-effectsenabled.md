---
description: La méthode EffectsEnabled détermine si les effets sont activés. Si les effets sont désactivés, ils restent dans la chronologie, mais ne sont pas rendus.
ms.assetid: fd8bb2aa-9c10-4a85-9e9d-1b342fbce03b
title: 'IAMTimeline :: EffectsEnabled, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EffectsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d988e8a4c10dc6dba52269c6729b8d7fea1f090e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540240"
---
# <a name="iamtimelineeffectsenabled-method"></a><span data-ttu-id="6739f-104">IAMTimeline :: EffectsEnabled, méthode</span><span class="sxs-lookup"><span data-stu-id="6739f-104">IAMTimeline::EffectsEnabled method</span></span>

> [!Note]  
> <span data-ttu-id="6739f-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="6739f-105">\[Deprecated.</span></span> <span data-ttu-id="6739f-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6739f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6739f-107">La `EffectsEnabled` méthode détermine si les effets sont activés.</span><span class="sxs-lookup"><span data-stu-id="6739f-107">The `EffectsEnabled` method determines whether effects are enabled.</span></span> <span data-ttu-id="6739f-108">Si les effets sont désactivés, ils restent dans la chronologie, mais ne sont pas rendus.</span><span class="sxs-lookup"><span data-stu-id="6739f-108">If effects are disabled, they remain in the timeline but are not rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="6739f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6739f-109">Syntax</span></span>


```C++
HRESULT EffectsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="6739f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6739f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6739f-111">*pfEnabled*</span><span class="sxs-lookup"><span data-stu-id="6739f-111">*pfEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="6739f-112">Reçoit une valeur booléenne indiquant si les effets sont activés.</span><span class="sxs-lookup"><span data-stu-id="6739f-112">Receives a Boolean value indicating whether effects are enabled.</span></span> <span data-ttu-id="6739f-113">Si la **valeur est true**, les effets sont activés.</span><span class="sxs-lookup"><span data-stu-id="6739f-113">If **TRUE**, effects are enabled.</span></span> <span data-ttu-id="6739f-114">Si la **valeur est false**, les effets sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="6739f-114">If **FALSE**, effects are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6739f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6739f-115">Return value</span></span>

<span data-ttu-id="6739f-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6739f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6739f-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6739f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6739f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="6739f-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6739f-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="6739f-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6739f-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6739f-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6739f-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6739f-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6739f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6739f-122">Requirements</span></span>



| <span data-ttu-id="6739f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6739f-123">Requirement</span></span> | <span data-ttu-id="6739f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6739f-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6739f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6739f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6739f-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6739f-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6739f-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6739f-127">Library</span></span><br/> | <dl> <span data-ttu-id="6739f-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6739f-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6739f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6739f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6739f-130">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="6739f-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="6739f-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="6739f-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




