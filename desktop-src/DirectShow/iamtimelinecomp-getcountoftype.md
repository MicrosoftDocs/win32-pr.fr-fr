---
description: La méthode GetCountOfType récupère le nombre d’objets d’un type donné contenu dans cette composition et toutes ses pistes virtuelles, de manière récursive.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: 'IAMTimelineComp :: GetCountOfType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 69c4c582a3883feedec962bfb88b4a833be3750b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543306"
---
# <a name="iamtimelinecompgetcountoftype-method"></a><span data-ttu-id="3135d-103">IAMTimelineComp :: GetCountOfType, méthode</span><span class="sxs-lookup"><span data-stu-id="3135d-103">IAMTimelineComp::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="3135d-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3135d-104">\[Deprecated.</span></span> <span data-ttu-id="3135d-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3135d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3135d-106">La `GetCountOfType` méthode récupère le nombre d’objets d’un type donné contenu dans cette composition et toutes ses pistes virtuelles, de manière récursive.</span><span class="sxs-lookup"><span data-stu-id="3135d-106">The `GetCountOfType` method retrieves the number of objects of a given type contained in this composition and all its virtual tracks, recursively.</span></span>

## <a name="syntax"></a><span data-ttu-id="3135d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3135d-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="3135d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3135d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3135d-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="3135d-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="3135d-110">Reçoit le nombre d’objets du type spécifié contenus dans cette composition et toutes ses pistes virtuelles, de manière récursive.</span><span class="sxs-lookup"><span data-stu-id="3135d-110">Receives the number of objects of the specified type contained in this composition and all its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="3135d-111">*pValWithComps*</span><span class="sxs-lookup"><span data-stu-id="3135d-111">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="3135d-112">Reçoit le nombre renvoyé dans *pval* plus le nombre de compositions recherchées, y compris celui-ci.</span><span class="sxs-lookup"><span data-stu-id="3135d-112">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="3135d-113">*MajorType*</span><span class="sxs-lookup"><span data-stu-id="3135d-113">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="3135d-114">Membre du type énuméré de la [**chronologie \_ principale \_**](timeline-major-type.md) , en spécifiant le type d’objet à compter.</span><span class="sxs-lookup"><span data-stu-id="3135d-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3135d-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3135d-115">Return value</span></span>

<span data-ttu-id="3135d-116">Retourne S \_ OK en cas de réussite, ou un pointeur E dans le \_ cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3135d-116">Returns S\_OK if successful, or E\_POINTER otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3135d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3135d-117">Remarks</span></span>

<span data-ttu-id="3135d-118">En règle générale, une application n’appelle pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3135d-118">Typically, an application will not call this method.</span></span> <span data-ttu-id="3135d-119">Elle est appelée par le moteur de rendu.</span><span class="sxs-lookup"><span data-stu-id="3135d-119">It is called by the render engine.</span></span>

<span data-ttu-id="3135d-120">Si vous comptez des compositions, la valeur retournée dans *pval* est égale à zéro et la valeur retournée dans *pValWithComps* est le nombre de compositions.</span><span class="sxs-lookup"><span data-stu-id="3135d-120">If you count compositions, the value returned in *pVal* is zero and the value returned in *pValWithComps* is the number of compositions.</span></span> <span data-ttu-id="3135d-121">La valeur de *\* pValWithComps* comprend la composition sur laquelle vous appelez la méthode.</span><span class="sxs-lookup"><span data-stu-id="3135d-121">The value of *\*pValWithComps* includes the composition on which you call the method.</span></span> <span data-ttu-id="3135d-122">Par exemple, si vous appelez cette méthode sur une composition vide, *\* pValWithComps* est égal à 1.</span><span class="sxs-lookup"><span data-stu-id="3135d-122">For example, if you call this method on an empty composition, *\*pValWithComps* equals 1.</span></span>

<span data-ttu-id="3135d-123">Les groupes ne peuvent pas résider dans les compositions. vous ne pouvez donc pas utiliser cette méthode pour compter les groupes.</span><span class="sxs-lookup"><span data-stu-id="3135d-123">Groups cannot reside inside compositions, so you cannot use this method to count groups.</span></span> <span data-ttu-id="3135d-124">(Le nombre retourné sera toujours égal à zéro.) Pour compter les groupes, appelez la méthode [**IAMTimeline :: GetGroupCount**](iamtimeline-getgroupcount.md) .</span><span class="sxs-lookup"><span data-stu-id="3135d-124">(The returned count will always be zero.) To count groups, call the [**IAMTimeline::GetGroupCount**](iamtimeline-getgroupcount.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="3135d-125">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="3135d-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3135d-126">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3135d-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3135d-127">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3135d-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3135d-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3135d-128">Requirements</span></span>



| <span data-ttu-id="3135d-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3135d-129">Requirement</span></span> | <span data-ttu-id="3135d-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="3135d-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3135d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="3135d-131">Header</span></span><br/>  | <dl> <span data-ttu-id="3135d-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3135d-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3135d-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3135d-133">Library</span></span><br/> | <dl> <span data-ttu-id="3135d-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3135d-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3135d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3135d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3135d-136">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="3135d-136">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="3135d-137">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="3135d-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




