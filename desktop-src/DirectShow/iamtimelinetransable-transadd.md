---
description: La méthode TransAdd ajoute une transition à l’objet. Un objet peut avoir plusieurs transitions, mais il ne doit pas se chevaucher dans le temps. Les transitions doivent se situer dans les limites de temps de l’objet.
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: 'IAMTimelineTransable :: TransAdd, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2636922549635c4a1c5e6e0b36f308f62328dc60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526457"
---
# <a name="iamtimelinetransabletransadd-method"></a><span data-ttu-id="470f4-105">IAMTimelineTransable :: TransAdd, méthode</span><span class="sxs-lookup"><span data-stu-id="470f4-105">IAMTimelineTransable::TransAdd method</span></span>

> [!Note]  
> <span data-ttu-id="470f4-106">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="470f4-106">\[Deprecated.</span></span> <span data-ttu-id="470f4-107">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="470f4-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="470f4-108">La `TransAdd` méthode ajoute une transition à l’objet.</span><span class="sxs-lookup"><span data-stu-id="470f4-108">The `TransAdd` method adds a transition to the object.</span></span> <span data-ttu-id="470f4-109">Un objet peut avoir plusieurs transitions, mais il ne doit pas se chevaucher dans le temps.</span><span class="sxs-lookup"><span data-stu-id="470f4-109">An object can have multiple transitions, but they must not overlap in time.</span></span> <span data-ttu-id="470f4-110">Les transitions doivent se situer dans les limites de temps de l’objet.</span><span class="sxs-lookup"><span data-stu-id="470f4-110">Transitions must fall within the time boundaries of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="470f4-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="470f4-111">Syntax</span></span>


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a><span data-ttu-id="470f4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="470f4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="470f4-113">*pTrans*</span><span class="sxs-lookup"><span data-stu-id="470f4-113">*pTrans*</span></span> 
</dt> <dd>

<span data-ttu-id="470f4-114">Pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de la transition à ajouter.</span><span class="sxs-lookup"><span data-stu-id="470f4-114">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the transition to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="470f4-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="470f4-115">Return value</span></span>

<span data-ttu-id="470f4-116">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="470f4-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="470f4-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="470f4-117">Return code</span></span>                                                                                   | <span data-ttu-id="470f4-118">Description</span><span class="sxs-lookup"><span data-stu-id="470f4-118">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="470f4-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="470f4-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="470f4-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="470f4-120">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="470f4-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="470f4-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="470f4-122">Impossible d’insérer la transition.</span><span class="sxs-lookup"><span data-stu-id="470f4-122">Cannot insert the transition.</span></span><br/>              |
| <dl> <span data-ttu-id="470f4-123"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="470f4-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="470f4-124">*pTrans* n’est pas un pointeur vers une transition.</span><span class="sxs-lookup"><span data-stu-id="470f4-124">*pTrans* is not a pointer to a transition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="470f4-125">Notes</span><span class="sxs-lookup"><span data-stu-id="470f4-125">Remarks</span></span>

<span data-ttu-id="470f4-126">Si la transition chevauche une transition existante, la méthode retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="470f4-126">If the transition overlaps an existing transition, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="470f4-127">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="470f4-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="470f4-128">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="470f4-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="470f4-129">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="470f4-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="470f4-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="470f4-130">Requirements</span></span>



| <span data-ttu-id="470f4-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="470f4-131">Requirement</span></span> | <span data-ttu-id="470f4-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="470f4-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="470f4-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="470f4-133">Header</span></span><br/>  | <dl> <span data-ttu-id="470f4-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="470f4-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="470f4-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="470f4-135">Library</span></span><br/> | <dl> <span data-ttu-id="470f4-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="470f4-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="470f4-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="470f4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="470f4-138">**Interface IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="470f4-138">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="470f4-139">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="470f4-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




