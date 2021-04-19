---
description: La méthode GetTimeline récupère la chronologie à laquelle appartient ce groupe.
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: 'IAMTimelineGroup :: GetTimeline, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b85b0c6f1730c2946134a36d33537f311b6603f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542384"
---
# <a name="iamtimelinegroupgettimeline-method"></a><span data-ttu-id="69532-103">IAMTimelineGroup :: GetTimeline, méthode</span><span class="sxs-lookup"><span data-stu-id="69532-103">IAMTimelineGroup::GetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="69532-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="69532-104">\[Deprecated.</span></span> <span data-ttu-id="69532-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="69532-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="69532-106">La `GetTimeline` méthode récupère la chronologie à laquelle appartient ce groupe.</span><span class="sxs-lookup"><span data-stu-id="69532-106">The `GetTimeline` method retrieves the timeline to which this group belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="69532-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69532-107">Syntax</span></span>


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="69532-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69532-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69532-109">*ppTimeline* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="69532-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69532-110">Reçoit l’interface [**IAMTimeline**](iamtimeline.md) de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="69532-110">Receives the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="69532-111">Si le groupe ne fait pas partie d’une chronologie, la valeur est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="69532-111">If the group is not part of a timeline, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69532-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69532-112">Return value</span></span>

<span data-ttu-id="69532-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="69532-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="69532-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="69532-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="69532-115">Notes</span><span class="sxs-lookup"><span data-stu-id="69532-115">Remarks</span></span>

<span data-ttu-id="69532-116">Si la valeur retournée dans *ppTimeline* n’est pas **null**, l’interface **IAMTimeline** a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="69532-116">If the value returned in *ppTimeline* is not **NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="69532-117">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="69532-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="69532-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="69532-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="69532-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="69532-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="69532-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="69532-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="69532-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69532-121">Requirements</span></span>



| <span data-ttu-id="69532-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69532-122">Requirement</span></span> | <span data-ttu-id="69532-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="69532-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69532-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="69532-124">Header</span></span><br/>  | <dl> <span data-ttu-id="69532-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="69532-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="69532-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="69532-126">Library</span></span><br/> | <dl> <span data-ttu-id="69532-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69532-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69532-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69532-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69532-129">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="69532-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="69532-130">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="69532-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




