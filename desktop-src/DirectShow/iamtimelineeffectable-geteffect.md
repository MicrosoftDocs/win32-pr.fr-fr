---
description: La méthode GetEffect récupère l’effet au niveau de priorité spécifié.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: 'IAMTimelineEffectable :: GetEffect, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7a769fca28ea1f8f698b23de7df6b7c15f05234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523456"
---
# <a name="iamtimelineeffectablegeteffect-method"></a><span data-ttu-id="21778-103">IAMTimelineEffectable :: GetEffect, méthode</span><span class="sxs-lookup"><span data-stu-id="21778-103">IAMTimelineEffectable::GetEffect method</span></span>

> [!Note]  
> <span data-ttu-id="21778-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="21778-104">\[Deprecated.</span></span> <span data-ttu-id="21778-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="21778-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="21778-106">La méthode **GetEffect** récupère l’effet au niveau de priorité spécifié.</span><span class="sxs-lookup"><span data-stu-id="21778-106">The **GetEffect** method retrieves the effect at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="21778-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21778-107">Syntax</span></span>


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="21778-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21778-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21778-109">*ppFX* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="21778-109">*ppFX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21778-110">Reçoit l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’effet.</span><span class="sxs-lookup"><span data-stu-id="21778-110">Receives the effect's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="21778-111">*Et*</span><span class="sxs-lookup"><span data-stu-id="21778-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="21778-112">Niveau de priorité de l’effet à récupérer.</span><span class="sxs-lookup"><span data-stu-id="21778-112">Priority level of the effect to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21778-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21778-113">Return value</span></span>

<span data-ttu-id="21778-114">Retourne une valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="21778-114">Returns an HRESULT value.</span></span> <span data-ttu-id="21778-115">Il peut prendre les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="21778-115">Possible values include the following:</span></span>



| <span data-ttu-id="21778-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="21778-116">Return code</span></span>                                                                               | <span data-ttu-id="21778-117">Description</span><span class="sxs-lookup"><span data-stu-id="21778-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="21778-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="21778-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="21778-119">Aucun effet à la priorité spécifiée</span><span class="sxs-lookup"><span data-stu-id="21778-119">No effect at the specified priority,</span></span><br/> |
| <dl> <span data-ttu-id="21778-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="21778-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="21778-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="21778-121">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="21778-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="21778-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="21778-123">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="21778-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="21778-124">Notes</span><span class="sxs-lookup"><span data-stu-id="21778-124">Remarks</span></span>

<span data-ttu-id="21778-125">Si la méthode retourne la valeur \_ OK, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="21778-125">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="21778-126">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="21778-126">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="21778-127">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="21778-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="21778-128">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="21778-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="21778-129">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="21778-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="21778-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21778-130">Requirements</span></span>



| <span data-ttu-id="21778-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21778-131">Requirement</span></span> | <span data-ttu-id="21778-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="21778-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21778-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="21778-133">Header</span></span><br/>  | <dl> <span data-ttu-id="21778-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="21778-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="21778-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="21778-135">Library</span></span><br/> | <dl> <span data-ttu-id="21778-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21778-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21778-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21778-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21778-138">**Interface IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="21778-138">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="21778-139">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="21778-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




