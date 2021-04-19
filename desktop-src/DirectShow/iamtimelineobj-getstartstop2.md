---
description: 'La méthode GetStartStop2 récupère les heures de début et de fin de l’objet par rapport au parent de l’objet. Cette méthode est équivalente à IAMTimelineObj :: GetStartStop, mais prend des valeurs REFTIME.'
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: 'IAMTimelineObj :: GetStartStop2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 211bd54ee755a08d3e592a856c792eba6e3d4e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528087"
---
# <a name="iamtimelineobjgetstartstop2-method"></a><span data-ttu-id="f9191-104">IAMTimelineObj :: GetStartStop2, méthode</span><span class="sxs-lookup"><span data-stu-id="f9191-104">IAMTimelineObj::GetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="f9191-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f9191-105">\[Deprecated.</span></span> <span data-ttu-id="f9191-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f9191-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f9191-107">La `GetStartStop2` méthode récupère les heures de début et de fin de l’objet par rapport au parent de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f9191-107">The `GetStartStop2` method retrieves the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="f9191-108">Cette méthode est équivalente à [**IAMTimelineObj :: GetStartStop**](iamtimelineobj-getstartstop.md), mais prend des valeurs [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="f9191-108">This method is equivalent to [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9191-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9191-109">Syntax</span></span>


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="f9191-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9191-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9191-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="f9191-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="f9191-112">Reçoit l’heure de début, en secondes.</span><span class="sxs-lookup"><span data-stu-id="f9191-112">Receives the start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="f9191-113">*pStop*</span><span class="sxs-lookup"><span data-stu-id="f9191-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="f9191-114">Reçoit l’heure d’arrêt, en secondes.</span><span class="sxs-lookup"><span data-stu-id="f9191-114">Receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9191-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9191-115">Return value</span></span>

<span data-ttu-id="f9191-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f9191-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f9191-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f9191-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9191-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f9191-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f9191-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="f9191-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f9191-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f9191-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f9191-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f9191-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f9191-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9191-122">Requirements</span></span>



| <span data-ttu-id="f9191-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9191-123">Requirement</span></span> | <span data-ttu-id="f9191-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9191-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9191-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9191-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f9191-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9191-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f9191-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f9191-127">Library</span></span><br/> | <dl> <span data-ttu-id="f9191-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9191-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9191-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9191-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9191-130">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="f9191-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="f9191-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="f9191-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




