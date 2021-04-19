---
description: 'Non pris en charge. Appelez la méthode IAMTimelineComp :: GetRecursiveLayerOfType à la place.'
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: 'IAMTimelineComp :: GetRecursiveLayerOfTypeI, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfTypeI
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8aded93aa0753ee8dddf173262c80678e28037a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532214"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a><span data-ttu-id="70e09-104">IAMTimelineComp :: GetRecursiveLayerOfTypeI, méthode</span><span class="sxs-lookup"><span data-stu-id="70e09-104">IAMTimelineComp::GetRecursiveLayerOfTypeI method</span></span>

> [!Note]  
> <span data-ttu-id="70e09-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="70e09-105">\[Deprecated.</span></span> <span data-ttu-id="70e09-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="70e09-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="70e09-107">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="70e09-107">Not supported.</span></span> <span data-ttu-id="70e09-108">Appelez la méthode [**IAMTimelineComp :: GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="70e09-108">Call the [**IAMTimelineComp::GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="70e09-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70e09-109">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfTypeI(
   IAMTimelineObj      **ppVirtualTrack,
   long                **pWhichLayer,
   TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="70e09-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70e09-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70e09-111">*ppVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="70e09-111">*ppVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="70e09-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="70e09-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="70e09-113">*pWhichLayer*</span><span class="sxs-lookup"><span data-stu-id="70e09-113">*pWhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="70e09-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="70e09-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="70e09-115">*Type*</span><span class="sxs-lookup"><span data-stu-id="70e09-115">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="70e09-116">Réservé.</span><span class="sxs-lookup"><span data-stu-id="70e09-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70e09-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70e09-117">Return value</span></span>

<span data-ttu-id="70e09-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="70e09-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="70e09-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="70e09-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="70e09-120">Notes</span><span class="sxs-lookup"><span data-stu-id="70e09-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="70e09-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="70e09-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="70e09-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="70e09-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="70e09-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="70e09-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70e09-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70e09-124">Requirements</span></span>



| <span data-ttu-id="70e09-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70e09-125">Requirement</span></span> | <span data-ttu-id="70e09-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="70e09-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70e09-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="70e09-127">Header</span></span><br/>  | <dl> <span data-ttu-id="70e09-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="70e09-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="70e09-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="70e09-129">Library</span></span><br/> | <dl> <span data-ttu-id="70e09-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70e09-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70e09-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70e09-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70e09-132">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="70e09-132">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> </dl>

 

 




