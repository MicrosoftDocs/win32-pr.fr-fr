---
description: 'La méthode GetNextTrans2 récupère la première transition qui apparaît à l’heure spécifiée ou une version ultérieure. Cette méthode est équivalente à IAMTimelineTransable :: GetNextTrans, mais prend une valeur REFTIME.'
ms.assetid: e6910e94-f289-4a5d-9976-1e8f7373c882
title: 'IAMTimelineTransable :: GetNextTrans2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c5f79ff20507247fbcac3badceaf2c3e28f0303
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543339"
---
# <a name="iamtimelinetransablegetnexttrans2-method"></a><span data-ttu-id="51414-104">IAMTimelineTransable :: GetNextTrans2, méthode</span><span class="sxs-lookup"><span data-stu-id="51414-104">IAMTimelineTransable::GetNextTrans2 method</span></span>

> [!Note]  
> <span data-ttu-id="51414-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="51414-105">\[Deprecated.</span></span> <span data-ttu-id="51414-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51414-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="51414-107">La `GetNextTrans2` méthode récupère la première transition qui apparaît à l’heure spécifiée ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="51414-107">The `GetNextTrans2` method retrieves the first transition that appears at the specified time or later.</span></span> <span data-ttu-id="51414-108">Cette méthode est équivalente à [**IAMTimelineTransable :: GetNextTrans**](iamtimelinetransable-getnexttrans.md), mais prend une valeur [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="51414-108">This method is equivalent to [**IAMTimelineTransable::GetNextTrans**](iamtimelinetransable-getnexttrans.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="51414-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51414-109">Syntax</span></span>


```C++
HRESULT GetNextTrans2(
  [out] IAMTimelineObj **ppTrans,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="51414-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51414-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51414-111">*ppTrans* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="51414-111">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51414-112">Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet de transition.</span><span class="sxs-lookup"><span data-stu-id="51414-112">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="51414-113">*pInOut*</span><span class="sxs-lookup"><span data-stu-id="51414-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="51414-114">Pointeur vers une variable qui spécifie la durée en secondes.</span><span class="sxs-lookup"><span data-stu-id="51414-114">Pointer to a variable that specifies the time in seconds.</span></span> <span data-ttu-id="51414-115">En entrée, cette valeur spécifie l’heure à partir de laquelle la transition doit être trouvée.</span><span class="sxs-lookup"><span data-stu-id="51414-115">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="51414-116">En sortie, si une transition est récupérée, cette valeur est définie sur l’heure d’arrêt de la transition.</span><span class="sxs-lookup"><span data-stu-id="51414-116">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51414-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51414-117">Return value</span></span>

<span data-ttu-id="51414-118">Retourne \_ la valeur OK si la méthode récupère une transition ou la \_ valeur false si elle ne trouve pas de transition.</span><span class="sxs-lookup"><span data-stu-id="51414-118">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="51414-119">Sinon, retourne une valeur **HRESULT** indiquant la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="51414-119">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="51414-120">Notes</span><span class="sxs-lookup"><span data-stu-id="51414-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="51414-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="51414-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="51414-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="51414-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="51414-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="51414-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="51414-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51414-124">Requirements</span></span>



| <span data-ttu-id="51414-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51414-125">Requirement</span></span> | <span data-ttu-id="51414-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="51414-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51414-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="51414-127">Header</span></span><br/>  | <dl> <span data-ttu-id="51414-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="51414-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="51414-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="51414-129">Library</span></span><br/> | <dl> <span data-ttu-id="51414-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51414-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51414-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51414-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51414-132">**Interface IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="51414-132">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="51414-133">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="51414-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




