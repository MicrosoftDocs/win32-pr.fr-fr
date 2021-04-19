---
description: 'La méthode GetSrcAtTime2 récupère l’objet source le plus proche de l’heure spécifiée, en fonction des conditions limites spécifiées. Cette méthode est équivalente à IAMTimelineTrack :: GetSrcAtTime, mais prend une valeur REFTIME.'
ms.assetid: 11f6545b-478b-4ffd-8344-2bf8585db2a5
title: 'IAMTimelineTrack :: GetSrcAtTime2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7140644f64c66b204d6a50cb8e88cb5beca41dae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532961"
---
# <a name="iamtimelinetrackgetsrcattime2-method"></a><span data-ttu-id="60bac-104">IAMTimelineTrack :: GetSrcAtTime2, méthode</span><span class="sxs-lookup"><span data-stu-id="60bac-104">IAMTimelineTrack::GetSrcAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="60bac-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="60bac-105">\[Deprecated.</span></span> <span data-ttu-id="60bac-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="60bac-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="60bac-107">La `GetSrcAtTime2` méthode récupère l’objet source le plus proche de l’heure spécifiée, en fonction des conditions limites spécifiées.</span><span class="sxs-lookup"><span data-stu-id="60bac-107">The `GetSrcAtTime2` method retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="60bac-108">Cette méthode est équivalente à [**IAMTimelineTrack :: GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), mais prend une valeur [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="60bac-108">This method is equivalent to [**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="60bac-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60bac-109">Syntax</span></span>


```C++
HRESULT GetSrcAtTime2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="60bac-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60bac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60bac-111">*ppSrc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="60bac-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60bac-112">Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="60bac-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="60bac-113">*Time*</span><span class="sxs-lookup"><span data-stu-id="60bac-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="60bac-114">Heure de début de la recherche, en secondes.</span><span class="sxs-lookup"><span data-stu-id="60bac-114">Start time for the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="60bac-115">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="60bac-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="60bac-116">Membre du type [**d' \_ \_ \_ indicateur de recherche DEXTERF Track**](dexterf-track-search-flags.md) qui spécifie les conditions limites pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="60bac-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60bac-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60bac-117">Return value</span></span>

<span data-ttu-id="60bac-118">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="60bac-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="60bac-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="60bac-119">Return code</span></span>                                                                                  | <span data-ttu-id="60bac-120">Description</span><span class="sxs-lookup"><span data-stu-id="60bac-120">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="60bac-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="60bac-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="60bac-122">L’objet source n’a pas été trouvé.</span><span class="sxs-lookup"><span data-stu-id="60bac-122">Did not locate a source object.</span></span><br/> |
| <dl> <span data-ttu-id="60bac-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="60bac-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="60bac-124">A trouvé un objet source.</span><span class="sxs-lookup"><span data-stu-id="60bac-124">Located a source object.</span></span><br/>        |
| <dl> <span data-ttu-id="60bac-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="60bac-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="60bac-126">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="60bac-126">Invalid argument.</span></span><br/>               |
| <dl> <span data-ttu-id="60bac-127"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="60bac-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="60bac-128">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="60bac-128">**NULL** pointer argument.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="60bac-129">Notes</span><span class="sxs-lookup"><span data-stu-id="60bac-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="60bac-130">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="60bac-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="60bac-131">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="60bac-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="60bac-132">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="60bac-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="60bac-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60bac-133">Requirements</span></span>



| <span data-ttu-id="60bac-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60bac-134">Requirement</span></span> | <span data-ttu-id="60bac-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="60bac-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60bac-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="60bac-136">Header</span></span><br/>  | <dl> <span data-ttu-id="60bac-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="60bac-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="60bac-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60bac-138">Library</span></span><br/> | <dl> <span data-ttu-id="60bac-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60bac-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60bac-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60bac-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60bac-141">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="60bac-141">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="60bac-142">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="60bac-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




