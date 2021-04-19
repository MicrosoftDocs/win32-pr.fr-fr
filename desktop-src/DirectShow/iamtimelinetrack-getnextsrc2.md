---
description: 'La méthode GetNextSrc2 recherche dans le suivi la source suivante qui apparaît à l’heure spécifiée ou ultérieurement. Cette méthode est équivalente à IAMTimelineTrack :: GetNextSrc, mais prend une valeur REFTIME.'
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: 'IAMTimelineTrack :: GetNextSrc2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543592"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a><span data-ttu-id="8c04b-104">IAMTimelineTrack :: GetNextSrc2, méthode</span><span class="sxs-lookup"><span data-stu-id="8c04b-104">IAMTimelineTrack::GetNextSrc2 method</span></span>

> [!Note]  
> <span data-ttu-id="8c04b-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8c04b-105">\[Deprecated.</span></span> <span data-ttu-id="8c04b-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8c04b-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8c04b-107">La `GetNextSrc2` méthode recherche la source suivante qui apparaît à l’heure spécifiée ou une version ultérieure dans le suivi.</span><span class="sxs-lookup"><span data-stu-id="8c04b-107">The `GetNextSrc2` method searches the track for the next source that appears at the specified time or later.</span></span> <span data-ttu-id="8c04b-108">Cette méthode est équivalente à [**IAMTimelineTrack :: GetNextSrc**](iamtimelinetrack-getnextsrc.md), mais prend une valeur [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="8c04b-108">This method is equivalent to [**IAMTimelineTrack::GetNextSrc**](iamtimelinetrack-getnextsrc.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c04b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c04b-109">Syntax</span></span>


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="8c04b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c04b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c04b-111">*ppSrc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8c04b-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c04b-112">Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="8c04b-112">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8c04b-113">*pInOut*</span><span class="sxs-lookup"><span data-stu-id="8c04b-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="8c04b-114">En entrée, contient l’heure de début de la recherche, en secondes.</span><span class="sxs-lookup"><span data-stu-id="8c04b-114">On input, contains the start time for the search, in seconds.</span></span> <span data-ttu-id="8c04b-115">Si la méthode récupère une source, elle définit la valeur sur l’heure d’arrêt de la source.</span><span class="sxs-lookup"><span data-stu-id="8c04b-115">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="8c04b-116">Si la méthode ne récupère pas de source, la valeur devient non valide et l’application ne doit pas l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="8c04b-116">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c04b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c04b-117">Return value</span></span>

<span data-ttu-id="8c04b-118">Retourne \_ la valeur OK si la méthode récupère une source, ou la \_ valeur false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8c04b-118">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c04b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="8c04b-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8c04b-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="8c04b-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8c04b-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c04b-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8c04b-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8c04b-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8c04b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c04b-123">Requirements</span></span>



| <span data-ttu-id="8c04b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c04b-124">Requirement</span></span> | <span data-ttu-id="8c04b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c04b-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c04b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c04b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8c04b-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c04b-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8c04b-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8c04b-128">Library</span></span><br/> | <dl> <span data-ttu-id="8c04b-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c04b-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c04b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c04b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c04b-131">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="8c04b-131">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="8c04b-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="8c04b-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




