---
description: La méthode GetNextTrans récupère la première transition qui apparaît à l’heure spécifiée ou une version ultérieure.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'IAMTimelineTransable :: GetNextTrans, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc8f7c88dab2b8c0dfece6f2799b6648c0b9da2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543780"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a><span data-ttu-id="dcfa8-103">IAMTimelineTransable :: GetNextTrans, méthode</span><span class="sxs-lookup"><span data-stu-id="dcfa8-103">IAMTimelineTransable::GetNextTrans method</span></span>

> [!Note]  
> <span data-ttu-id="dcfa8-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="dcfa8-104">\[Deprecated.</span></span> <span data-ttu-id="dcfa8-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dcfa8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dcfa8-106">La `GetNextTrans` méthode récupère la première transition qui apparaît à l’heure spécifiée ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="dcfa8-106">The `GetNextTrans` method retrieves the first transition that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcfa8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcfa8-107">Syntax</span></span>


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="dcfa8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcfa8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcfa8-109">*ppTrans* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dcfa8-109">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcfa8-110">Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet de transition.</span><span class="sxs-lookup"><span data-stu-id="dcfa8-110">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="dcfa8-111">*pInOut*</span><span class="sxs-lookup"><span data-stu-id="dcfa8-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="dcfa8-112">Pointeur vers une variable qui spécifie le temps en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="dcfa8-112">Pointer to a variable that specifies the time in 100-nanosecond units.</span></span> <span data-ttu-id="dcfa8-113">En entrée, cette valeur spécifie l’heure à partir de laquelle la transition doit être trouvée.</span><span class="sxs-lookup"><span data-stu-id="dcfa8-113">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="dcfa8-114">En sortie, si une transition est récupérée, cette valeur est définie sur l’heure d’arrêt de la transition.</span><span class="sxs-lookup"><span data-stu-id="dcfa8-114">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcfa8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dcfa8-115">Return value</span></span>

<span data-ttu-id="dcfa8-116">Retourne \_ la valeur OK si la méthode récupère une transition ou la \_ valeur false si elle ne trouve pas de transition.</span><span class="sxs-lookup"><span data-stu-id="dcfa8-116">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="dcfa8-117">Sinon, retourne une valeur **HRESULT** indiquant la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="dcfa8-117">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcfa8-118">Notes</span><span class="sxs-lookup"><span data-stu-id="dcfa8-118">Remarks</span></span>

<span data-ttu-id="dcfa8-119">L’heure de début de la transition peut être inférieure à l’heure que vous spécifiez dans *pInOut*, si la transition s’étend sur l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dcfa8-119">The start time of the transition might be less than the time that you specify in *pInOut*, if the transition spans the specified time.</span></span>

<span data-ttu-id="dcfa8-120">Si la méthode retourne la valeur \_ OK, l’interface [**IAMTimelineObj**](iamtimelineobj.md) qu’elle retourne a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="dcfa8-120">If the method returns S\_OK, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="dcfa8-121">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="dcfa8-121">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="dcfa8-122">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="dcfa8-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dcfa8-123">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dcfa8-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dcfa8-124">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="dcfa8-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dcfa8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcfa8-125">Requirements</span></span>



| <span data-ttu-id="dcfa8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcfa8-126">Requirement</span></span> | <span data-ttu-id="dcfa8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcfa8-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcfa8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcfa8-128">Header</span></span><br/>  | <dl> <span data-ttu-id="dcfa8-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcfa8-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dcfa8-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dcfa8-130">Library</span></span><br/> | <dl> <span data-ttu-id="dcfa8-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcfa8-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcfa8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcfa8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcfa8-133">**Interface IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="dcfa8-133">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="dcfa8-134">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="dcfa8-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




