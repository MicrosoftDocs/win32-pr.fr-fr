---
description: La méthode GetRecursiveLayerOfType effectue un classement à profondeur prioritaire des pistes virtuelles contenues dans cette composition, puis récupère la nième piste virtuelle à partir de ce classement.
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: 'IAMTimelineComp :: GetRecursiveLayerOfType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541601"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a><span data-ttu-id="299ca-103">IAMTimelineComp :: GetRecursiveLayerOfType, méthode</span><span class="sxs-lookup"><span data-stu-id="299ca-103">IAMTimelineComp::GetRecursiveLayerOfType method</span></span>

> [!Note]  
> <span data-ttu-id="299ca-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="299ca-104">\[Deprecated.</span></span> <span data-ttu-id="299ca-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="299ca-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="299ca-106">La `GetRecursiveLayerOfType` méthode effectue un classement à profondeur prioritaire des pistes virtuelles contenues dans cette composition, et récupère la *n* ième piste virtuelle à partir de ce classement.</span><span class="sxs-lookup"><span data-stu-id="299ca-106">The `GetRecursiveLayerOfType` method performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span>

## <a name="syntax"></a><span data-ttu-id="299ca-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="299ca-107">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="299ca-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="299ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="299ca-109">*ppVirtualTrack* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="299ca-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="299ca-110">Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de la piste virtuelle.</span><span class="sxs-lookup"><span data-stu-id="299ca-110">Receives a pointer to the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="299ca-111">*WhichLayer*</span><span class="sxs-lookup"><span data-stu-id="299ca-111">*WhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="299ca-112">Spécifie la piste virtuelle à récupérer, indexée à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="299ca-112">Specifies which virtual track to retrieve, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="299ca-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="299ca-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="299ca-114">Membre du type énuméré de la [**chronologie \_ principale \_**](timeline-major-type.md) qui spécifie s’il faut inclure les suivis dans la recherche.</span><span class="sxs-lookup"><span data-stu-id="299ca-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type that specifies whether to include tracks in the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="299ca-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="299ca-115">Return value</span></span>

<span data-ttu-id="299ca-116">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="299ca-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="299ca-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="299ca-117">Return code</span></span>                                                                                  | <span data-ttu-id="299ca-118">Description</span><span class="sxs-lookup"><span data-stu-id="299ca-118">Description</span></span>                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="299ca-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="299ca-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="299ca-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="299ca-120">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="299ca-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="299ca-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="299ca-122">Aucun objet du type spécifié.</span><span class="sxs-lookup"><span data-stu-id="299ca-122">No object of the specified type.</span></span><br/> |
| <dl> <span data-ttu-id="299ca-123"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="299ca-123"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="299ca-124">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="299ca-124">**NULL** pointer argument.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="299ca-125">Notes</span><span class="sxs-lookup"><span data-stu-id="299ca-125">Remarks</span></span>

<span data-ttu-id="299ca-126">En règle générale, une application n’a pas besoin d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="299ca-126">Typically, an application will not need to call this method.</span></span>

<span data-ttu-id="299ca-127">Si le paramètre de *type* est \_ une \_ piste de type principal de chronologie \_ , le classement à profondeur prioritaire comprend des pistes.</span><span class="sxs-lookup"><span data-stu-id="299ca-127">If the *Type* parameter is TIMELINE\_MAJOR\_TYPE\_TRACK, the depth-first ordering includes tracks.</span></span> <span data-ttu-id="299ca-128">Si ce n’est pas le cas, il comprend uniquement des compositions et des groupes.</span><span class="sxs-lookup"><span data-stu-id="299ca-128">If not, it includes only compositions and groups.</span></span> <span data-ttu-id="299ca-129">L’objet lui-même est inclus dans le classement.</span><span class="sxs-lookup"><span data-stu-id="299ca-129">The object itself is included in the ordering.</span></span>

<span data-ttu-id="299ca-130">Par exemple, dans l’organisation suivante, à partir de la composition A, le classement serait B, C, F, D, E, A.</span><span class="sxs-lookup"><span data-stu-id="299ca-130">For example, in the following arrangement, starting from Composition A, the ordering would be B, C, F, D, E, A.</span></span>

![getrecursivelayeroftype](images/composition.png)

<span data-ttu-id="299ca-132">Si la méthode est réussie, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="299ca-132">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="299ca-133">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="299ca-133">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="299ca-134">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="299ca-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="299ca-135">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="299ca-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="299ca-136">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="299ca-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="299ca-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="299ca-137">Requirements</span></span>



| <span data-ttu-id="299ca-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="299ca-138">Requirement</span></span> | <span data-ttu-id="299ca-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="299ca-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="299ca-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="299ca-140">Header</span></span><br/>  | <dl> <span data-ttu-id="299ca-141"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="299ca-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="299ca-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="299ca-142">Library</span></span><br/> | <dl> <span data-ttu-id="299ca-143"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="299ca-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="299ca-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="299ca-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="299ca-145">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="299ca-145">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="299ca-146">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="299ca-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




