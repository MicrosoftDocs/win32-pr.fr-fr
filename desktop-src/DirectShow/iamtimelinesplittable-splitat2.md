---
description: 'La méthode SplitAt2 fractionne l’objet à l’heure spécifiée. Cette méthode est équivalente à IAMTimelineSplittable :: SplitAt, mais prend une valeur REFTIME.'
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: 'IAMTimelineSplittable :: SplitAt2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0f941469983f2eaebf0363797fb54a81388bc51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542254"
---
# <a name="iamtimelinesplittablesplitat2-method"></a><span data-ttu-id="9ae86-104">IAMTimelineSplittable :: SplitAt2, méthode</span><span class="sxs-lookup"><span data-stu-id="9ae86-104">IAMTimelineSplittable::SplitAt2 method</span></span>

> [!Note]  
> <span data-ttu-id="9ae86-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="9ae86-105">\[Deprecated.</span></span> <span data-ttu-id="9ae86-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9ae86-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9ae86-107">La `SplitAt2` méthode fractionne l’objet à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9ae86-107">The `SplitAt2` method splits the object at the specified time.</span></span> <span data-ttu-id="9ae86-108">Cette méthode est équivalente à [**IAMTimelineSplittable :: SplitAt**](iamtimelinesplittable-splitat.md), mais prend une valeur [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="9ae86-108">This method is equivalent to [**IAMTimelineSplittable::SplitAt**](iamtimelinesplittable-splitat.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae86-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ae86-109">Syntax</span></span>


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="9ae86-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ae86-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ae86-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="9ae86-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="9ae86-112">Heure à laquelle fractionner l’objet, en secondes, par rapport au début de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="9ae86-112">Time at which to split the object, relative to the start of the timeline, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ae86-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ae86-113">Return value</span></span>

<span data-ttu-id="9ae86-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ae86-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9ae86-115">Il peut prendre les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ae86-115">Possible values include the following:</span></span>



| <span data-ttu-id="9ae86-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9ae86-116">Return code</span></span>                                                                                   | <span data-ttu-id="9ae86-117">Description</span><span class="sxs-lookup"><span data-stu-id="9ae86-117">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="9ae86-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9ae86-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="9ae86-119">Rien à fractionner.</span><span class="sxs-lookup"><span data-stu-id="9ae86-119">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="9ae86-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9ae86-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9ae86-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="9ae86-121">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="9ae86-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9ae86-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9ae86-123">L’objet n’existe pas pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="9ae86-123">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="9ae86-124"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="9ae86-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9ae86-125">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="9ae86-125">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9ae86-126">Notes</span><span class="sxs-lookup"><span data-stu-id="9ae86-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9ae86-127">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="9ae86-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9ae86-128">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ae86-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9ae86-129">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9ae86-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9ae86-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ae86-130">Requirements</span></span>



| <span data-ttu-id="9ae86-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ae86-131">Requirement</span></span> | <span data-ttu-id="9ae86-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ae86-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae86-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ae86-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9ae86-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ae86-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9ae86-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ae86-135">Library</span></span><br/> | <dl> <span data-ttu-id="9ae86-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ae86-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ae86-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ae86-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ae86-138">**Interface IAMTimelineSplittable**</span><span class="sxs-lookup"><span data-stu-id="9ae86-138">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="9ae86-139">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="9ae86-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




