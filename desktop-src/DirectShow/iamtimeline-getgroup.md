---
description: La méthode GetGroup récupère un groupe spécifié.
ms.assetid: 4ff651e5-a3aa-4da9-af23-a3a2bdbf7c5b
title: 'IAMTimeline :: GetGroup, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1241a125698cf78c1138d9264ecd8c73ff78056c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532544"
---
# <a name="iamtimelinegetgroup-method"></a><span data-ttu-id="3809d-103">IAMTimeline :: GetGroup, méthode</span><span class="sxs-lookup"><span data-stu-id="3809d-103">IAMTimeline::GetGroup method</span></span>

> [!Note]  
> <span data-ttu-id="3809d-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3809d-104">\[Deprecated.</span></span> <span data-ttu-id="3809d-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3809d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3809d-106">La `GetGroup` méthode récupère un groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="3809d-106">The `GetGroup` method retrieves a specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="3809d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3809d-107">Syntax</span></span>


```C++
HRESULT GetGroup(
  [out] IAMTimelineObj **ppGroup,
        long           WhichGroup
);
```



## <a name="parameters"></a><span data-ttu-id="3809d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3809d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3809d-109">*ppGroup* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3809d-109">*ppGroup* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3809d-110">Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) du groupe.</span><span class="sxs-lookup"><span data-stu-id="3809d-110">Receives a pointer to the group's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="3809d-111">*WhichGroup*</span><span class="sxs-lookup"><span data-stu-id="3809d-111">*WhichGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="3809d-112">Index du groupe à récupérer, en fonction de l’ordre dans lequel les groupes ont été ajoutés à la chronologie.</span><span class="sxs-lookup"><span data-stu-id="3809d-112">Index of the group to retrieve, based on the order in which the groups were added to the timeline.</span></span> <span data-ttu-id="3809d-113">Le premier groupe ajouté à la chronologie a un index de 0.</span><span class="sxs-lookup"><span data-stu-id="3809d-113">The first group added to the timeline has an index of 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3809d-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3809d-114">Return value</span></span>

<span data-ttu-id="3809d-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3809d-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3809d-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3809d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3809d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3809d-117">Remarks</span></span>

<span data-ttu-id="3809d-118">Si la méthode est réussie, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="3809d-118">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="3809d-119">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="3809d-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="3809d-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="3809d-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3809d-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3809d-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3809d-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3809d-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3809d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3809d-123">Requirements</span></span>



| <span data-ttu-id="3809d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3809d-124">Requirement</span></span> | <span data-ttu-id="3809d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3809d-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3809d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="3809d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3809d-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3809d-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3809d-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3809d-128">Library</span></span><br/> | <dl> <span data-ttu-id="3809d-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3809d-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3809d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3809d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3809d-131">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="3809d-131">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="3809d-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="3809d-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




