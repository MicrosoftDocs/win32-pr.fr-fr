---
description: 'La méthode GetTransAtTime2 récupère la transition la plus proche de l’heure spécifiée, en fonction des conditions limites spécifiées. Cette méthode est équivalente à IAMTimelineTransable :: GetTransAtTime, mais prend un paramètre REFTIME.'
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: 'IAMTimelineTransable :: GetTransAtTime2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541512"
---
# <a name="iamtimelinetransablegettransattime2-method"></a><span data-ttu-id="25970-104">IAMTimelineTransable :: GetTransAtTime2, méthode</span><span class="sxs-lookup"><span data-stu-id="25970-104">IAMTimelineTransable::GetTransAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="25970-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="25970-105">\[Deprecated.</span></span> <span data-ttu-id="25970-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="25970-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="25970-107">La `GetTransAtTime2` méthode récupère la transition la plus proche du temps spécifié, en fonction des conditions limites spécifiées.</span><span class="sxs-lookup"><span data-stu-id="25970-107">The `GetTransAtTime2` method retrieves the transition nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="25970-108">Cette méthode est équivalente à [**IAMTimelineTransable :: GetTransAtTime**](iamtimelinetransable-gettransattime.md), mais prend un paramètre [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="25970-108">This method is equivalent to [**IAMTimelineTransable::GetTransAtTime**](iamtimelinetransable-gettransattime.md), but takes a [**REFTIME**](reftime.md) parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="25970-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25970-109">Syntax</span></span>


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="25970-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25970-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25970-111">*ppObj* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="25970-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25970-112">Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de la transition.</span><span class="sxs-lookup"><span data-stu-id="25970-112">Receives a pointer to the transition's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="25970-113">*Time*</span><span class="sxs-lookup"><span data-stu-id="25970-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="25970-114">Heure à partir de laquelle commencer la recherche, en secondes.</span><span class="sxs-lookup"><span data-stu-id="25970-114">Time from which to begin the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="25970-115">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="25970-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="25970-116">Membre du type [**d' \_ \_ \_ indicateur de recherche DEXTERF Track**](dexterf-track-search-flags.md) qui spécifie les conditions limites pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="25970-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25970-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25970-117">Return value</span></span>

<span data-ttu-id="25970-118">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="25970-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="25970-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="25970-119">Return code</span></span>                                                                                  | <span data-ttu-id="25970-120">Description</span><span class="sxs-lookup"><span data-stu-id="25970-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="25970-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="25970-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="25970-122">Aucune transition n’a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="25970-122">No transition was found.</span></span><br/>   |
| <dl> <span data-ttu-id="25970-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25970-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="25970-124">La transition a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="25970-124">Transition was found.</span></span><br/>      |
| <dl> <span data-ttu-id="25970-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="25970-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="25970-126">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="25970-126">Invalid argument.</span></span><br/>          |
| <dl> <span data-ttu-id="25970-127"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="25970-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="25970-128">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="25970-128">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="25970-129">Notes</span><span class="sxs-lookup"><span data-stu-id="25970-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="25970-130">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="25970-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="25970-131">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="25970-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="25970-132">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="25970-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="25970-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25970-133">Requirements</span></span>



| <span data-ttu-id="25970-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25970-134">Requirement</span></span> | <span data-ttu-id="25970-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="25970-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25970-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="25970-136">Header</span></span><br/>  | <dl> <span data-ttu-id="25970-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="25970-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="25970-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="25970-138">Library</span></span><br/> | <dl> <span data-ttu-id="25970-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25970-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25970-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25970-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25970-141">**Interface IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="25970-141">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="25970-142">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="25970-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




