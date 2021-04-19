---
description: La méthode GetDefaultEffect récupère l’effet par défaut. Si le moteur de rendu ne peut pas restituer un effet, il remplace l’effet par défaut.
ms.assetid: 27eec6e8-702f-4e56-8d81-aa0633b8ec68
title: 'IAMTimeline :: GetDefaultEffect, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a0b1cf356a9c067ccae246814d2e1f381d7f78e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537812"
---
# <a name="iamtimelinegetdefaulteffect-method"></a><span data-ttu-id="788bb-104">IAMTimeline :: GetDefaultEffect, méthode</span><span class="sxs-lookup"><span data-stu-id="788bb-104">IAMTimeline::GetDefaultEffect method</span></span>

> [!Note]  
> <span data-ttu-id="788bb-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="788bb-105">\[Deprecated.</span></span> <span data-ttu-id="788bb-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="788bb-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="788bb-107">La `GetDefaultEffect` méthode récupère l’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="788bb-107">The `GetDefaultEffect` method retrieves the default effect.</span></span> <span data-ttu-id="788bb-108">Si le moteur de rendu ne peut pas restituer un effet, il remplace l’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="788bb-108">If the render engine cannot render an effect, it substitutes the default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="788bb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="788bb-109">Syntax</span></span>


```C++
HRESULT GetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="788bb-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="788bb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="788bb-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="788bb-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="788bb-112">Reçoit l’identificateur global unique (GUID) de l’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="788bb-112">Receives the globally unique identifier (GUID) of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="788bb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="788bb-113">Return value</span></span>

<span data-ttu-id="788bb-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="788bb-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="788bb-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="788bb-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="788bb-116">Notes</span><span class="sxs-lookup"><span data-stu-id="788bb-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="788bb-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="788bb-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="788bb-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="788bb-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="788bb-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="788bb-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="788bb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="788bb-120">Requirements</span></span>



| <span data-ttu-id="788bb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="788bb-121">Requirement</span></span> | <span data-ttu-id="788bb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="788bb-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="788bb-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="788bb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="788bb-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="788bb-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="788bb-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="788bb-125">Library</span></span><br/> | <dl> <span data-ttu-id="788bb-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="788bb-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="788bb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="788bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="788bb-128">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="788bb-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="788bb-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="788bb-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




