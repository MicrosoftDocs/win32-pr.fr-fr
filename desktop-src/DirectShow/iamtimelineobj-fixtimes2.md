---
description: 'La méthode FixTimes2 arrondit les heures de démarrage et d’arrêt spécifiées aux limites de frame les plus proches, comme défini par le paramètre de fréquence d’images du groupe parent. Cette méthode est équivalente à IAMTimelineObj :: FixTimes, mais prend des valeurs REFTIME.'
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: 'IAMTimelineObj :: FixTimes2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48b487d8dc17d6b815ea9dff79fc58af953b0bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545692"
---
# <a name="iamtimelineobjfixtimes2-method"></a><span data-ttu-id="fbeaf-104">IAMTimelineObj :: FixTimes2, méthode</span><span class="sxs-lookup"><span data-stu-id="fbeaf-104">IAMTimelineObj::FixTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="fbeaf-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="fbeaf-105">\[Deprecated.</span></span> <span data-ttu-id="fbeaf-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fbeaf-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fbeaf-107">La `FixTimes2` méthode arrondit les heures de démarrage et d’arrêt spécifiées aux limites de frame les plus proches, comme défini par le paramètre de fréquence d’images du groupe parent.</span><span class="sxs-lookup"><span data-stu-id="fbeaf-107">The `FixTimes2` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span> <span data-ttu-id="fbeaf-108">Cette méthode est équivalente à [**IAMTimelineObj :: FixTimes**](iamtimelineobj-fixtimes.md), mais prend des valeurs [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="fbeaf-108">This method is equivalent to [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbeaf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbeaf-109">Syntax</span></span>


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="fbeaf-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbeaf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbeaf-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="fbeaf-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="fbeaf-112">Pointeur vers une variable qui contient l’heure de début, en secondes.</span><span class="sxs-lookup"><span data-stu-id="fbeaf-112">Pointer to a variable that contains the start time, in seconds.</span></span> <span data-ttu-id="fbeaf-113">Si l’appel a échoué, cette variable est définie sur le temps arrondi.</span><span class="sxs-lookup"><span data-stu-id="fbeaf-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="fbeaf-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="fbeaf-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="fbeaf-115">Pointeur vers une variable qui contient l’heure d’arrêt, en secondes.</span><span class="sxs-lookup"><span data-stu-id="fbeaf-115">Pointer to a variable that contains the stop time, in seconds.</span></span> <span data-ttu-id="fbeaf-116">Si l’appel a échoué, cette variable est définie sur le temps arrondi.</span><span class="sxs-lookup"><span data-stu-id="fbeaf-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbeaf-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbeaf-117">Return value</span></span>

<span data-ttu-id="fbeaf-118">Retourne S \_ OK en cas de réussite, ou E \_ NOTINTREE si l’objet ne fait pas partie d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="fbeaf-118">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbeaf-119">Notes</span><span class="sxs-lookup"><span data-stu-id="fbeaf-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fbeaf-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="fbeaf-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fbeaf-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fbeaf-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fbeaf-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fbeaf-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fbeaf-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbeaf-123">Requirements</span></span>



| <span data-ttu-id="fbeaf-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbeaf-124">Requirement</span></span> | <span data-ttu-id="fbeaf-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbeaf-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbeaf-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="fbeaf-126">Header</span></span><br/>  | <dl> <span data-ttu-id="fbeaf-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbeaf-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fbeaf-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fbeaf-128">Library</span></span><br/> | <dl> <span data-ttu-id="fbeaf-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbeaf-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbeaf-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbeaf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbeaf-131">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="fbeaf-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="fbeaf-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="fbeaf-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




