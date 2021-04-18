---
description: La méthode VTrackSwapPriorities bascule les niveaux de priorité de deux pistes.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: 'IAMTimelineComp :: VTrackSwapPriorities, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df90fe3f4c481f454c6cc743f09de9538a2c892d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533327"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a><span data-ttu-id="3961b-103">IAMTimelineComp :: VTrackSwapPriorities, méthode</span><span class="sxs-lookup"><span data-stu-id="3961b-103">IAMTimelineComp::VTrackSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="3961b-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3961b-104">\[Deprecated.</span></span> <span data-ttu-id="3961b-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3961b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3961b-106">La `VTrackSwapPriorities` méthode change les niveaux de priorité de deux pistes.</span><span class="sxs-lookup"><span data-stu-id="3961b-106">The `VTrackSwapPriorities` method switches the priority levels of two tracks.</span></span>

<span data-ttu-id="3961b-107">Étant donné deux niveaux de priorité, cette méthode bascule les pistes virtuelles à ces priorités.</span><span class="sxs-lookup"><span data-stu-id="3961b-107">Given two priority levels, this method switches the virtual tracks at those priorities.</span></span> <span data-ttu-id="3961b-108">Lorsque la méthode retourne, la piste qui était au premier niveau de priorité est désormais au deuxième niveau de priorité, et vice versa.</span><span class="sxs-lookup"><span data-stu-id="3961b-108">When the method returns, the track that was at the first priority level is now at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="3961b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3961b-109">Syntax</span></span>


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a><span data-ttu-id="3961b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3961b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3961b-111">*VirtualTrackA*</span><span class="sxs-lookup"><span data-stu-id="3961b-111">*VirtualTrackA*</span></span> 
</dt> <dd>

<span data-ttu-id="3961b-112">Premier niveau de priorité auquel permuter les pistes virtuelles.</span><span class="sxs-lookup"><span data-stu-id="3961b-112">First priority level at which to swap virtual tracks.</span></span>

</dd> <dt>

<span data-ttu-id="3961b-113">*VirtualTrackB*</span><span class="sxs-lookup"><span data-stu-id="3961b-113">*VirtualTrackB*</span></span> 
</dt> <dd>

<span data-ttu-id="3961b-114">Deuxième niveau de priorité auquel permuter les pistes virtuelles.</span><span class="sxs-lookup"><span data-stu-id="3961b-114">Second priority level at which to swap virtual tracks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3961b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3961b-115">Return value</span></span>

<span data-ttu-id="3961b-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3961b-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3961b-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3961b-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3961b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="3961b-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3961b-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="3961b-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3961b-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3961b-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3961b-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3961b-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3961b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3961b-122">Requirements</span></span>



| <span data-ttu-id="3961b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3961b-123">Requirement</span></span> | <span data-ttu-id="3961b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3961b-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3961b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="3961b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3961b-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3961b-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3961b-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3961b-127">Library</span></span><br/> | <dl> <span data-ttu-id="3961b-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3961b-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3961b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3961b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3961b-130">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="3961b-130">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="3961b-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="3961b-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




