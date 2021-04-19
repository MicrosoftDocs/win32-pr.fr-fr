---
description: 'La méthode ZeroBetween2 supprime tous les éléments de la piste entre les heures spécifiées. Cette méthode est équivalente à IAMTimelineTrack :: ZeroBetween, mais prend des valeurs REFTIME.'
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: 'IAMTimelineTrack :: ZeroBetween2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 27e3ab5cc2a631cb54c926824c2f3410413cd981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542482"
---
# <a name="iamtimelinetrackzerobetween2-method"></a><span data-ttu-id="b4997-104">IAMTimelineTrack :: ZeroBetween2, méthode</span><span class="sxs-lookup"><span data-stu-id="b4997-104">IAMTimelineTrack::ZeroBetween2 method</span></span>

> [!Note]  
> <span data-ttu-id="b4997-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b4997-105">\[Deprecated.</span></span> <span data-ttu-id="b4997-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b4997-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b4997-107">La `ZeroBetween2` méthode supprime tous les éléments de la piste entre les heures spécifiées.</span><span class="sxs-lookup"><span data-stu-id="b4997-107">The `ZeroBetween2` method removes everything from the track between the specified times.</span></span> <span data-ttu-id="b4997-108">Cette méthode est équivalente à [**IAMTimelineTrack :: ZeroBetween**](iamtimelinetrack-zerobetween.md), mais prend des valeurs [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="b4997-108">This method is equivalent to [**IAMTimelineTrack::ZeroBetween**](iamtimelinetrack-zerobetween.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4997-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4997-109">Syntax</span></span>


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="b4997-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4997-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4997-111">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="b4997-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="b4997-112">Début de la plage à effacer, en secondes.</span><span class="sxs-lookup"><span data-stu-id="b4997-112">Beginning of the range to clear, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="b4997-113">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="b4997-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b4997-114">Fin de la plage à effacer, en secondes.</span><span class="sxs-lookup"><span data-stu-id="b4997-114">End of the range to clear, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4997-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4997-115">Return value</span></span>

<span data-ttu-id="b4997-116">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4997-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b4997-117">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4997-117">Possible values include the following.</span></span>



| <span data-ttu-id="b4997-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b4997-118">Return code</span></span>                                                                             | <span data-ttu-id="b4997-119">Description</span><span class="sxs-lookup"><span data-stu-id="b4997-119">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b4997-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b4997-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="b4997-121">L’intervalle de temps dépasse tous les éléments de la piste.</span><span class="sxs-lookup"><span data-stu-id="b4997-121">The time range falls beyond everything in the track.</span></span><br/> |
| <dl> <span data-ttu-id="b4997-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4997-122"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="b4997-123">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="b4997-123">Success.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="b4997-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b4997-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b4997-125">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="b4997-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b4997-126">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b4997-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b4997-127">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b4997-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b4997-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4997-128">Requirements</span></span>



| <span data-ttu-id="b4997-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4997-129">Requirement</span></span> | <span data-ttu-id="b4997-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4997-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4997-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4997-131">Header</span></span><br/>  | <dl> <span data-ttu-id="b4997-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4997-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b4997-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b4997-133">Library</span></span><br/> | <dl> <span data-ttu-id="b4997-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4997-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4997-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4997-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4997-136">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="b4997-136">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="b4997-137">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="b4997-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




