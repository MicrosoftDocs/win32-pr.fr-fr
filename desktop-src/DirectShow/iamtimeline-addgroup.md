---
description: La méthode AddGroup ajoute un groupe à la chronologie.
ms.assetid: c7fc3b59-5852-4a3c-b9bf-f87e659819b5
title: 'IAMTimeline :: AddGroup, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.AddGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0de10defd5e7aa840322599fb32104f1dc5bb5a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525207"
---
# <a name="iamtimelineaddgroup-method"></a><span data-ttu-id="0b49e-103">IAMTimeline :: AddGroup, méthode</span><span class="sxs-lookup"><span data-stu-id="0b49e-103">IAMTimeline::AddGroup method</span></span>

> [!Note]  
> <span data-ttu-id="0b49e-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0b49e-104">\[Deprecated.</span></span> <span data-ttu-id="0b49e-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0b49e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0b49e-106">La `AddGroup` méthode ajoute un groupe à la chronologie.</span><span class="sxs-lookup"><span data-stu-id="0b49e-106">The `AddGroup` method adds a group to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b49e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b49e-107">Syntax</span></span>


```C++
HRESULT AddGroup(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a><span data-ttu-id="0b49e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b49e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b49e-109">*pGroup*</span><span class="sxs-lookup"><span data-stu-id="0b49e-109">*pGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="0b49e-110">Pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) du groupe.</span><span class="sxs-lookup"><span data-stu-id="0b49e-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b49e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b49e-111">Return value</span></span>

<span data-ttu-id="0b49e-112">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b49e-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="0b49e-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0b49e-113">Return code</span></span>                                                                                   | <span data-ttu-id="0b49e-114">Description</span><span class="sxs-lookup"><span data-stu-id="0b49e-114">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="0b49e-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0b49e-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0b49e-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="0b49e-116">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="0b49e-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0b49e-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0b49e-118">Le nombre maximal de groupes est dépassé.</span><span class="sxs-lookup"><span data-stu-id="0b49e-118">Maximum number of groups exceeded.</span></span><br/> |
| <dl> <span data-ttu-id="0b49e-119"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="0b49e-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="0b49e-120">L’objet n’est pas un groupe.</span><span class="sxs-lookup"><span data-stu-id="0b49e-120">The object is not a group.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="0b49e-121">Notes</span><span class="sxs-lookup"><span data-stu-id="0b49e-121">Remarks</span></span>

<span data-ttu-id="0b49e-122">Actuellement, les chronologies prennent en charge un maximum de 32 groupes.</span><span class="sxs-lookup"><span data-stu-id="0b49e-122">Currently, timelines support a maximum of 32 groups.</span></span>

> [!Note]  
> <span data-ttu-id="0b49e-123">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="0b49e-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0b49e-124">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0b49e-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0b49e-125">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0b49e-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0b49e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b49e-126">Requirements</span></span>



| <span data-ttu-id="0b49e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b49e-127">Requirement</span></span> | <span data-ttu-id="0b49e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b49e-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b49e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b49e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0b49e-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b49e-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0b49e-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0b49e-131">Library</span></span><br/> | <dl> <span data-ttu-id="0b49e-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b49e-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b49e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b49e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b49e-134">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="0b49e-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="0b49e-135">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="0b49e-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




