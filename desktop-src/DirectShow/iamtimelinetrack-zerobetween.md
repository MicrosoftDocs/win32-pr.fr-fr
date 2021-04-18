---
description: La méthode ZeroBetween supprime tous les éléments de la piste entre les heures spécifiées. Cette méthode fractionne tous les objets qui s’étendent sur la plage de temps spécifiée et supprime les parties qui se trouvent dans la plage.
ms.assetid: df173a3c-147b-4f2d-9bcb-a8c2873f5420
title: 'IAMTimelineTrack :: ZeroBetween, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bef669bae5e5e5c4c31a49b545fcfc7f58285f97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532775"
---
# <a name="iamtimelinetrackzerobetween-method"></a><span data-ttu-id="0e76a-104">IAMTimelineTrack :: ZeroBetween, méthode</span><span class="sxs-lookup"><span data-stu-id="0e76a-104">IAMTimelineTrack::ZeroBetween method</span></span>

> [!Note]  
> <span data-ttu-id="0e76a-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0e76a-105">\[Deprecated.</span></span> <span data-ttu-id="0e76a-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0e76a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0e76a-107">La `ZeroBetween` méthode supprime tous les éléments de la piste entre les heures spécifiées.</span><span class="sxs-lookup"><span data-stu-id="0e76a-107">The `ZeroBetween` method removes everything from the track between the specified times.</span></span> <span data-ttu-id="0e76a-108">Cette méthode fractionne tous les objets qui s’étendent sur la plage de temps spécifiée et supprime les parties qui se trouvent dans la plage.</span><span class="sxs-lookup"><span data-stu-id="0e76a-108">This method splits any objects that span the specified time range and removes the pieces that fall within the range.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e76a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e76a-109">Syntax</span></span>


```C++
HRESULT ZeroBetween(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="0e76a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e76a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e76a-111">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="0e76a-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="0e76a-112">Début de la plage à effacer, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="0e76a-112">Beginning of the range to clear, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="0e76a-113">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="0e76a-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0e76a-114">Fin de la plage à effacer, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="0e76a-114">End of the range to clear, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e76a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e76a-115">Return value</span></span>

<span data-ttu-id="0e76a-116">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0e76a-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0e76a-117">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e76a-117">Possible values include the following.</span></span>



| <span data-ttu-id="0e76a-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0e76a-118">Return code</span></span>                                                                             | <span data-ttu-id="0e76a-119">Description</span><span class="sxs-lookup"><span data-stu-id="0e76a-119">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0e76a-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="0e76a-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="0e76a-121">L’intervalle de temps dépasse tous les éléments de la piste.</span><span class="sxs-lookup"><span data-stu-id="0e76a-121">The time range falls beyond everything in the track.</span></span><br/> |
| <dl> <span data-ttu-id="0e76a-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0e76a-122"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="0e76a-123">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="0e76a-123">Success.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="0e76a-124">Notes</span><span class="sxs-lookup"><span data-stu-id="0e76a-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0e76a-125">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="0e76a-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0e76a-126">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0e76a-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0e76a-127">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0e76a-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e76a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e76a-128">Requirements</span></span>



| <span data-ttu-id="0e76a-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e76a-129">Requirement</span></span> | <span data-ttu-id="0e76a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e76a-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e76a-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e76a-131">Header</span></span><br/>  | <dl> <span data-ttu-id="0e76a-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e76a-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0e76a-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0e76a-133">Library</span></span><br/> | <dl> <span data-ttu-id="0e76a-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e76a-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e76a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e76a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e76a-136">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="0e76a-136">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="0e76a-137">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="0e76a-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




