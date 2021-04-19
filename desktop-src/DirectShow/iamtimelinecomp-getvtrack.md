---
description: La méthode GetVTrack récupère la piste virtuelle à la priorité spécifiée.
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: 'IAMTimelineComp :: GetVTrack, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 06c205f700cbdb98fdc5f45bdd2ca7727e2456f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543305"
---
# <a name="iamtimelinecompgetvtrack-method"></a><span data-ttu-id="272de-103">IAMTimelineComp :: GetVTrack, méthode</span><span class="sxs-lookup"><span data-stu-id="272de-103">IAMTimelineComp::GetVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="272de-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="272de-104">\[Deprecated.</span></span> <span data-ttu-id="272de-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="272de-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="272de-106">La `GetVTrack` méthode récupère la piste virtuelle à la priorité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="272de-106">The `GetVTrack` method retrieves the virtual track at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="272de-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="272de-107">Syntax</span></span>


```C++
HRESULT GetVTrack(
  [out] IAMTimelineObj **ppVirtualTrack,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="272de-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="272de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="272de-109">*ppVirtualTrack* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="272de-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="272de-110">Reçoit l’interface [**IAMTimelineObj**](iamtimelineobj.md) de la piste virtuelle.</span><span class="sxs-lookup"><span data-stu-id="272de-110">Receives the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="272de-111">*Et*</span><span class="sxs-lookup"><span data-stu-id="272de-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="272de-112">Priorité de la piste virtuelle à récupérer.</span><span class="sxs-lookup"><span data-stu-id="272de-112">Priority of the virtual track to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="272de-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="272de-113">Return value</span></span>

<span data-ttu-id="272de-114">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="272de-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="272de-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="272de-115">Return code</span></span>                                                                                  | <span data-ttu-id="272de-116">Description</span><span class="sxs-lookup"><span data-stu-id="272de-116">Description</span></span>                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="272de-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="272de-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="272de-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="272de-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="272de-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="272de-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="272de-120">Aucune piste virtuelle avec la priorité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="272de-120">No virtual track with the specified priority.</span></span><br/> |
| <dl> <span data-ttu-id="272de-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="272de-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="272de-122">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="272de-122">**NULL** pointer argument.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="272de-123">Notes</span><span class="sxs-lookup"><span data-stu-id="272de-123">Remarks</span></span>

<span data-ttu-id="272de-124">Si la méthode est réussie, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="272de-124">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="272de-125">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="272de-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="272de-126">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="272de-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="272de-127">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="272de-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="272de-128">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="272de-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="272de-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="272de-129">Requirements</span></span>



| <span data-ttu-id="272de-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="272de-130">Requirement</span></span> | <span data-ttu-id="272de-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="272de-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="272de-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="272de-132">Header</span></span><br/>  | <dl> <span data-ttu-id="272de-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="272de-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="272de-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="272de-134">Library</span></span><br/> | <dl> <span data-ttu-id="272de-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="272de-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="272de-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="272de-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="272de-137">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="272de-137">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="272de-138">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="272de-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




