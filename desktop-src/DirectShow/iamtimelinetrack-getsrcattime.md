---
description: La méthode GetSrcAtTime récupère l’objet source le plus proche de l’heure spécifiée, en fonction des conditions limites spécifiées.
ms.assetid: 0469c0c2-13df-49f7-95b2-15d3069c5b1c
title: 'IAMTimelineTrack :: GetSrcAtTime, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b726d26efd0550df364200a27d536d60d38274a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537393"
---
# <a name="iamtimelinetrackgetsrcattime-method"></a><span data-ttu-id="d39ff-103">IAMTimelineTrack :: GetSrcAtTime, méthode</span><span class="sxs-lookup"><span data-stu-id="d39ff-103">IAMTimelineTrack::GetSrcAtTime method</span></span>

> [!Note]  
> <span data-ttu-id="d39ff-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d39ff-104">\[Deprecated.</span></span> <span data-ttu-id="d39ff-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d39ff-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d39ff-106">La `GetSrcAtTime` méthode récupère l’objet source le plus proche de l’heure spécifiée, en fonction des conditions limites spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d39ff-106">The `GetSrcAtTime` method retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d39ff-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d39ff-107">Syntax</span></span>


```C++
HRESULT GetSrcAtTime(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="d39ff-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d39ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d39ff-109">*ppSrc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d39ff-109">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d39ff-110">Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="d39ff-110">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="d39ff-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="d39ff-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="d39ff-112">Heure de début de la recherche, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="d39ff-112">Start time for the search, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="d39ff-113">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="d39ff-113">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="d39ff-114">Membre du type [**d' \_ \_ \_ indicateur de recherche DEXTERF Track**](dexterf-track-search-flags.md) qui spécifie les conditions limites pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="d39ff-114">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d39ff-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d39ff-115">Return value</span></span>

<span data-ttu-id="d39ff-116">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="d39ff-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="d39ff-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d39ff-117">Return code</span></span>                                                                                  | <span data-ttu-id="d39ff-118">Description</span><span class="sxs-lookup"><span data-stu-id="d39ff-118">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="d39ff-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="d39ff-119"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="d39ff-120">L’objet source n’a pas été trouvé.</span><span class="sxs-lookup"><span data-stu-id="d39ff-120">Did not locate a source object.</span></span><br/> |
| <dl> <span data-ttu-id="d39ff-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d39ff-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d39ff-122">A trouvé un objet source.</span><span class="sxs-lookup"><span data-stu-id="d39ff-122">Located a source object.</span></span><br/>        |
| <dl> <span data-ttu-id="d39ff-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d39ff-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d39ff-124">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="d39ff-124">Invalid argument.</span></span><br/>               |
| <dl> <span data-ttu-id="d39ff-125"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="d39ff-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="d39ff-126">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="d39ff-126">**NULL** pointer argument.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="d39ff-127">Notes</span><span class="sxs-lookup"><span data-stu-id="d39ff-127">Remarks</span></span>

<span data-ttu-id="d39ff-128">Si la méthode retourne la valeur \_ OK, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="d39ff-128">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="d39ff-129">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="d39ff-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="d39ff-130">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="d39ff-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d39ff-131">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d39ff-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d39ff-132">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d39ff-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d39ff-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d39ff-133">Requirements</span></span>



| <span data-ttu-id="d39ff-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d39ff-134">Requirement</span></span> | <span data-ttu-id="d39ff-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d39ff-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d39ff-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="d39ff-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d39ff-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d39ff-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d39ff-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d39ff-138">Library</span></span><br/> | <dl> <span data-ttu-id="d39ff-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d39ff-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d39ff-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d39ff-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d39ff-141">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="d39ff-141">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="d39ff-142">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="d39ff-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




