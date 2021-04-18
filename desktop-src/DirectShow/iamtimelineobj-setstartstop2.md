---
description: 'La méthode SetStartStop2 définit les heures de début et de fin de l’objet par rapport au parent de l’objet. Cette méthode est équivalente à IAMTimelineObj :: SetStartStop, mais prend des valeurs REFTIME.'
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: 'IAMTimelineObj :: SetStartStop2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 190e47d2ccee00d202dc16e20704b545447d844f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526583"
---
# <a name="iamtimelineobjsetstartstop2-method"></a><span data-ttu-id="cc067-104">IAMTimelineObj :: SetStartStop2, méthode</span><span class="sxs-lookup"><span data-stu-id="cc067-104">IAMTimelineObj::SetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="cc067-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="cc067-105">\[Deprecated.</span></span> <span data-ttu-id="cc067-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cc067-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cc067-107">La `SetStartStop2` méthode définit les heures de début et de fin de l’objet par rapport au parent de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cc067-107">The `SetStartStop2` method sets the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="cc067-108">Cette méthode est équivalente à [**IAMTimelineObj :: SetStartStop**](iamtimelineobj-setstartstop.md), mais prend des valeurs [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="cc067-108">This method is equivalent to [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc067-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc067-109">Syntax</span></span>


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="cc067-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc067-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc067-111">*Start*</span><span class="sxs-lookup"><span data-stu-id="cc067-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="cc067-112">Nouvelle heure de début, en secondes, ou-1 pour conserver l’heure de début existante.</span><span class="sxs-lookup"><span data-stu-id="cc067-112">New start time, in seconds, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="cc067-113">*Stop*</span><span class="sxs-lookup"><span data-stu-id="cc067-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="cc067-114">Nouvelle heure d’arrêt, en secondes, ou-1 pour conserver l’heure d’arrêt existante.</span><span class="sxs-lookup"><span data-stu-id="cc067-114">New stop time, in seconds, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc067-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc067-115">Return value</span></span>

<span data-ttu-id="cc067-116">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="cc067-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="cc067-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cc067-117">Return code</span></span>                                                                                  | <span data-ttu-id="cc067-118">Description</span><span class="sxs-lookup"><span data-stu-id="cc067-118">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="cc067-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cc067-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="cc067-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="cc067-120">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="cc067-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cc067-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="cc067-122">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="cc067-122">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="cc067-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="cc067-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="cc067-124">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="cc067-124">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="cc067-125">Notes</span><span class="sxs-lookup"><span data-stu-id="cc067-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cc067-126">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="cc067-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cc067-127">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cc067-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cc067-128">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="cc067-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cc067-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc067-129">Requirements</span></span>



| <span data-ttu-id="cc067-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc067-130">Requirement</span></span> | <span data-ttu-id="cc067-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc067-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc067-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc067-132">Header</span></span><br/>  | <dl> <span data-ttu-id="cc067-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc067-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cc067-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cc067-134">Library</span></span><br/> | <dl> <span data-ttu-id="cc067-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc067-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc067-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc067-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc067-137">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="cc067-137">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="cc067-138">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="cc067-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




