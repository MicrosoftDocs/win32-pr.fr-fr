---
description: La méthode TrackGetPriority récupère le niveau de priorité de l’objet.
ms.assetid: f9a138e8-e9ad-4703-bdcc-c64aea4fbad0
title: 'IAMTimelineVirtualTrack :: TrackGetPriority, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack.TrackGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08b43fa34848e5dac41d22281c08d25ee9065831
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541714"
---
# <a name="iamtimelinevirtualtracktrackgetpriority-method"></a><span data-ttu-id="6b9b0-103">IAMTimelineVirtualTrack :: TrackGetPriority, méthode</span><span class="sxs-lookup"><span data-stu-id="6b9b0-103">IAMTimelineVirtualTrack::TrackGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="6b9b0-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="6b9b0-104">\[Deprecated.</span></span> <span data-ttu-id="6b9b0-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6b9b0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6b9b0-106">La `TrackGetPriority` méthode récupère le niveau de priorité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6b9b0-106">The `TrackGetPriority` method retrieves the object's priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b9b0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b9b0-107">Syntax</span></span>


```C++
HRESULT TrackGetPriority(
   long *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="6b9b0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b9b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b9b0-109">*pPriority*</span><span class="sxs-lookup"><span data-stu-id="6b9b0-109">*pPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="6b9b0-110">Pointeur vers une variable qui reçoit le niveau de priorité.</span><span class="sxs-lookup"><span data-stu-id="6b9b0-110">Pointer to a variable that receives the priority level.</span></span> <span data-ttu-id="6b9b0-111">Si l’objet ne fait pas partie d’une chronologie, la valeur est définie sur – 1.</span><span class="sxs-lookup"><span data-stu-id="6b9b0-111">If the object is not part of a timeline, the value is set to –1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b9b0-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b9b0-112">Return value</span></span>

<span data-ttu-id="6b9b0-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6b9b0-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6b9b0-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6b9b0-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b9b0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="6b9b0-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6b9b0-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="6b9b0-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6b9b0-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6b9b0-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6b9b0-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6b9b0-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6b9b0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b9b0-119">Requirements</span></span>



| <span data-ttu-id="6b9b0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b9b0-120">Requirement</span></span> | <span data-ttu-id="6b9b0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b9b0-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b9b0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b9b0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6b9b0-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b9b0-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6b9b0-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6b9b0-124">Library</span></span><br/> | <dl> <span data-ttu-id="6b9b0-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b9b0-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b9b0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b9b0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b9b0-127">**Interface IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="6b9b0-127">**IAMTimelineVirtualTrack Interface**</span></span>](iamtimelinevirtualtrack.md)
</dt> <dt>

[<span data-ttu-id="6b9b0-128">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="6b9b0-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




