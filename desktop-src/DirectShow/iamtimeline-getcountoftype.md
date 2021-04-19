---
description: La méthode GetCountOfType récupère le nombre d’objets du type spécifié qui sont contenus dans un groupe spécifié et tous ses enfants.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: 'IAMTimeline :: GetCountOfType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f0636eac7c651ed003c618e258f7dbf2bdd60996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542304"
---
# <a name="iamtimelinegetcountoftype-method"></a><span data-ttu-id="3f33c-103">IAMTimeline :: GetCountOfType, méthode</span><span class="sxs-lookup"><span data-stu-id="3f33c-103">IAMTimeline::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="3f33c-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3f33c-104">\[Deprecated.</span></span> <span data-ttu-id="3f33c-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3f33c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3f33c-106">La `GetCountOfType` méthode récupère le nombre d’objets du type spécifié qui sont contenus dans un groupe spécifié et tous ses enfants.</span><span class="sxs-lookup"><span data-stu-id="3f33c-106">The `GetCountOfType` method retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f33c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f33c-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="3f33c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f33c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f33c-109">*Groupe*</span><span class="sxs-lookup"><span data-stu-id="3f33c-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="3f33c-110">Numéro d’index du groupe pour lequel le nombre doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="3f33c-110">Index number of the group for which to retrieve the count.</span></span>

</dd> <dt>

<span data-ttu-id="3f33c-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="3f33c-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="3f33c-112">Reçoit le nombre d’objets du type spécifié contenus dans le groupe et toutes ses pistes virtuelles, de manière récursive.</span><span class="sxs-lookup"><span data-stu-id="3f33c-112">Receives the number of objects of the specified type contained in the group and all of its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="3f33c-113">*pValWithComps*</span><span class="sxs-lookup"><span data-stu-id="3f33c-113">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="3f33c-114">Reçoit le nombre renvoyé dans *pval* plus le nombre de compositions recherchées, y compris celui-ci.</span><span class="sxs-lookup"><span data-stu-id="3f33c-114">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="3f33c-115">*MajorType*</span><span class="sxs-lookup"><span data-stu-id="3f33c-115">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="3f33c-116">Membre du type énuméré de la [**chronologie \_ principale \_**](timeline-major-type.md) , en spécifiant le type d’objet à compter.</span><span class="sxs-lookup"><span data-stu-id="3f33c-116">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f33c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3f33c-117">Return value</span></span>

<span data-ttu-id="3f33c-118">Retourne l’une des valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="3f33c-118">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="3f33c-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3f33c-119">Return code</span></span>                                                                                  | <span data-ttu-id="3f33c-120">Description</span><span class="sxs-lookup"><span data-stu-id="3f33c-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3f33c-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3f33c-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3f33c-122">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="3f33c-122">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="3f33c-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3f33c-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3f33c-124">Numéro de groupe non valide.</span><span class="sxs-lookup"><span data-stu-id="3f33c-124">Invalid group number.</span></span><br/>      |
| <dl> <span data-ttu-id="3f33c-125"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="3f33c-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="3f33c-126">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="3f33c-126">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3f33c-127">Notes</span><span class="sxs-lookup"><span data-stu-id="3f33c-127">Remarks</span></span>

<span data-ttu-id="3f33c-128">L’appel de cette méthode équivaut à appeler [**IAMTimelineComp :: GetCountOfType**](iamtimelinecomp-getcountoftype.md) sur le groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="3f33c-128">Calling this method is equivalent to calling [**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md) on the specified group.</span></span> <span data-ttu-id="3f33c-129">Pour plus d’informations, consultez la section Notes de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3f33c-129">See the Remarks section of that method for more information.</span></span>

<span data-ttu-id="3f33c-130">En règle générale, une application n’appelle pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3f33c-130">Typically, an application will not call this method.</span></span> <span data-ttu-id="3f33c-131">Elle est appelée en interne par le moteur de rendu.</span><span class="sxs-lookup"><span data-stu-id="3f33c-131">It is called internally by the render engine.</span></span>

> [!Note]  
> <span data-ttu-id="3f33c-132">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="3f33c-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3f33c-133">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f33c-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3f33c-134">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3f33c-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3f33c-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f33c-135">Requirements</span></span>



| <span data-ttu-id="3f33c-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f33c-136">Requirement</span></span> | <span data-ttu-id="3f33c-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f33c-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f33c-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f33c-138">Header</span></span><br/>  | <dl> <span data-ttu-id="3f33c-139"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f33c-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3f33c-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3f33c-140">Library</span></span><br/> | <dl> <span data-ttu-id="3f33c-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f33c-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f33c-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f33c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f33c-143">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="3f33c-143">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="3f33c-144">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="3f33c-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




