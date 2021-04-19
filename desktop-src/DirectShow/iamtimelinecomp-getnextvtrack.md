---
description: La méthode GetNextVTrack récupère la piste virtuelle suivante après une piste virtuelle spécifiée.
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: 'IAMTimelineComp :: GetNextVTrack, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e5a4500c2b53703a13b509f112453e65c954f96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531086"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a><span data-ttu-id="dccbd-103">IAMTimelineComp :: GetNextVTrack, méthode</span><span class="sxs-lookup"><span data-stu-id="dccbd-103">IAMTimelineComp::GetNextVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="dccbd-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="dccbd-104">\[Deprecated.</span></span> <span data-ttu-id="dccbd-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dccbd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dccbd-106">La `GetNextVTrack` méthode récupère la piste virtuelle suivante après une piste virtuelle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dccbd-106">The `GetNextVTrack` method retrieves the next virtual track after a specified virtual track.</span></span>

## <a name="syntax"></a><span data-ttu-id="dccbd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dccbd-107">Syntax</span></span>


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a><span data-ttu-id="dccbd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dccbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dccbd-109">*pVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="dccbd-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="dccbd-110">Pointeur vers la piste virtuelle précédente, ou **null** pour récupérer la première piste virtuelle dans la composition.</span><span class="sxs-lookup"><span data-stu-id="dccbd-110">Pointer to the previous virtual track, or **NULL** to retrieve the first virtual track in the composition.</span></span>

</dd> <dt>

<span data-ttu-id="dccbd-111">*ppNextVirtualTrack* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dccbd-111">*ppNextVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dccbd-112">Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de la piste virtuelle suivante, par ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="dccbd-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the next virtual track, in order of priority.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dccbd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dccbd-113">Return value</span></span>

<span data-ttu-id="dccbd-114">Retourne S \_ OK si la méthode récupère une piste virtuelle, ou la \_ valeur false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="dccbd-114">Returns S\_OK if the method retrieves a virtual track, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dccbd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="dccbd-115">Remarks</span></span>

<span data-ttu-id="dccbd-116">Si la méthode est réussie, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="dccbd-116">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="dccbd-117">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="dccbd-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="dccbd-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="dccbd-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dccbd-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dccbd-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dccbd-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="dccbd-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dccbd-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dccbd-121">Requirements</span></span>



| <span data-ttu-id="dccbd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dccbd-122">Requirement</span></span> | <span data-ttu-id="dccbd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="dccbd-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dccbd-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="dccbd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="dccbd-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dccbd-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dccbd-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dccbd-126">Library</span></span><br/> | <dl> <span data-ttu-id="dccbd-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dccbd-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dccbd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dccbd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dccbd-129">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="dccbd-129">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="dccbd-130">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="dccbd-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




