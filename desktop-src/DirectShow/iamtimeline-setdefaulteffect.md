---
description: La méthode SetDefaultEffect définit l’effet par défaut. Si le moteur de rendu ne peut pas restituer un effet, il remplace l’effet par défaut.
ms.assetid: 6ee94d86-c27f-4378-9a10-f3993a3ae657
title: 'IAMTimeline :: SetDefaultEffect, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 33e23070a7bb10dd040d08c145bfe1e0111026d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544082"
---
# <a name="iamtimelinesetdefaulteffect-method"></a><span data-ttu-id="07cb2-104">IAMTimeline :: SetDefaultEffect, méthode</span><span class="sxs-lookup"><span data-stu-id="07cb2-104">IAMTimeline::SetDefaultEffect method</span></span>

> [!Note]  
> <span data-ttu-id="07cb2-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="07cb2-105">\[Deprecated.</span></span> <span data-ttu-id="07cb2-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="07cb2-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="07cb2-107">La `SetDefaultEffect` méthode définit l’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="07cb2-107">The `SetDefaultEffect` method sets the default effect.</span></span> <span data-ttu-id="07cb2-108">Si le moteur de rendu ne peut pas restituer un effet, il remplace l’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="07cb2-108">If the render engine cannot render an effect, it substitutes the default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="07cb2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07cb2-109">Syntax</span></span>


```C++
HRESULT SetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="07cb2-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07cb2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07cb2-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="07cb2-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="07cb2-112">Pointeur vers le GUID de l’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="07cb2-112">Pointer to the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07cb2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07cb2-113">Return value</span></span>

<span data-ttu-id="07cb2-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="07cb2-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="07cb2-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07cb2-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="07cb2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="07cb2-116">Remarks</span></span>

<span data-ttu-id="07cb2-117">Si vous ne définissez pas d’effet par défaut ou si l’effet que vous spécifiez comme valeur par défaut provoque une erreur, l’algorithme DES utilise son propre effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="07cb2-117">If you do not set a default effect, or if the effect that you specify as a default causes an error, DES uses its own default effect.</span></span>

> [!Note]  
> <span data-ttu-id="07cb2-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="07cb2-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="07cb2-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="07cb2-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="07cb2-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="07cb2-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="07cb2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07cb2-121">Requirements</span></span>



| <span data-ttu-id="07cb2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07cb2-122">Requirement</span></span> | <span data-ttu-id="07cb2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="07cb2-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07cb2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="07cb2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="07cb2-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="07cb2-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="07cb2-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="07cb2-126">Library</span></span><br/> | <dl> <span data-ttu-id="07cb2-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07cb2-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07cb2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07cb2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07cb2-129">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="07cb2-129">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="07cb2-130">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="07cb2-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




