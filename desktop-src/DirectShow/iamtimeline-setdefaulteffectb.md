---
description: 'La méthode SetDefaultEffectB définit l’effet par défaut. Cette méthode est équivalente à IAMTimeline :: SetDefaultEffect, mais prend une valeur BSTR plutôt qu’un pointeur vers un GUID.'
ms.assetid: ffee9728-f69e-48a4-ac0a-d41347a20deb
title: 'IAMTimeline :: SetDefaultEffectB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a8722a195078cb032285e4ea2ac449ad045d54f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525206"
---
# <a name="iamtimelinesetdefaulteffectb-method"></a><span data-ttu-id="59a84-104">IAMTimeline :: SetDefaultEffectB, méthode</span><span class="sxs-lookup"><span data-stu-id="59a84-104">IAMTimeline::SetDefaultEffectB method</span></span>

> [!Note]  
> <span data-ttu-id="59a84-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="59a84-105">\[Deprecated.</span></span> <span data-ttu-id="59a84-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="59a84-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="59a84-107">La `SetDefaultEffectB` méthode définit l’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="59a84-107">The `SetDefaultEffectB` method sets the default effect.</span></span> <span data-ttu-id="59a84-108">Cette méthode est équivalente à [**IAMTimeline :: SetDefaultEffect**](iamtimeline-setdefaulteffect.md), mais prend une valeur BSTR plutôt qu’un pointeur vers un GUID.</span><span class="sxs-lookup"><span data-stu-id="59a84-108">This method is equivalent to [**IAMTimeline::SetDefaultEffect**](iamtimeline-setdefaulteffect.md), but takes a BSTR value, rather than a pointer to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="59a84-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59a84-109">Syntax</span></span>


```C++
HRESULT SetDefaultEffectB(
   BSTR pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="59a84-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59a84-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59a84-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="59a84-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="59a84-112">Valeur BSTR représentant le GUID de l’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="59a84-112">BSTR value representing the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59a84-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59a84-113">Return value</span></span>

<span data-ttu-id="59a84-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="59a84-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="59a84-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="59a84-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="59a84-116">Notes</span><span class="sxs-lookup"><span data-stu-id="59a84-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="59a84-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="59a84-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="59a84-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="59a84-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="59a84-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="59a84-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="59a84-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59a84-120">Requirements</span></span>



| <span data-ttu-id="59a84-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59a84-121">Requirement</span></span> | <span data-ttu-id="59a84-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="59a84-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59a84-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="59a84-123">Header</span></span><br/>  | <dl> <span data-ttu-id="59a84-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="59a84-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="59a84-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59a84-125">Library</span></span><br/> | <dl> <span data-ttu-id="59a84-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59a84-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59a84-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59a84-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a84-128">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="59a84-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="59a84-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="59a84-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




