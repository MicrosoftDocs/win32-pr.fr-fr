---
description: La méthode GetTimelineObject récupère la chronologie que le moteur de rendu utilise actuellement.
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: 'IRenderEngine :: GetTimelineObject, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aab8e9a5f77affc464763b1c5a5045eaa4fc042a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545943"
---
# <a name="irenderenginegettimelineobject-method"></a><span data-ttu-id="d09ac-103">IRenderEngine :: GetTimelineObject, méthode</span><span class="sxs-lookup"><span data-stu-id="d09ac-103">IRenderEngine::GetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="d09ac-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d09ac-104">\[Deprecated.</span></span> <span data-ttu-id="d09ac-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d09ac-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d09ac-106">La `GetTimelineObject` méthode récupère la chronologie que le moteur de rendu utilise actuellement.</span><span class="sxs-lookup"><span data-stu-id="d09ac-106">The `GetTimelineObject` method retrieves the timeline that the render engine is currently using.</span></span>

## <a name="syntax"></a><span data-ttu-id="d09ac-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d09ac-107">Syntax</span></span>


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="d09ac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d09ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d09ac-109">*ppTimeline* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d09ac-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d09ac-110">Reçoit un pointeur vers l’interface [**IAMTimeline**](iamtimeline.md) de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="d09ac-110">Receives a pointer to the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="d09ac-111">Elle reçoit la valeur **null** s’il n’y a pas de chronologie.</span><span class="sxs-lookup"><span data-stu-id="d09ac-111">It receives the value **NULL** if there is no timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d09ac-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d09ac-112">Return value</span></span>

<span data-ttu-id="d09ac-113">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="d09ac-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="d09ac-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d09ac-114">Return code</span></span>                                                                                            | <span data-ttu-id="d09ac-115">Description</span><span class="sxs-lookup"><span data-stu-id="d09ac-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="d09ac-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d09ac-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="d09ac-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="d09ac-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="d09ac-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="d09ac-118"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="d09ac-119">Pointeur non valide.</span><span class="sxs-lookup"><span data-stu-id="d09ac-119">Invalid pointer.</span></span><br/>                    |
| <dl> <span data-ttu-id="d09ac-120"><dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt></span><span class="sxs-lookup"><span data-stu-id="d09ac-120"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="d09ac-121">Le moteur de rendu n’a pas pu s’initialiser.</span><span class="sxs-lookup"><span data-stu-id="d09ac-121">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d09ac-122">Notes</span><span class="sxs-lookup"><span data-stu-id="d09ac-122">Remarks</span></span>

<span data-ttu-id="d09ac-123">En cas de retour, si la valeur de *\* ppTimeline* est non **null**, l’interface **IAMTimeline** a un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="d09ac-123">On return, if the value of *\*ppTimeline* is non-**NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="d09ac-124">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="d09ac-124">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="d09ac-125">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="d09ac-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d09ac-126">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d09ac-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d09ac-127">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d09ac-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d09ac-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d09ac-128">Requirements</span></span>



| <span data-ttu-id="d09ac-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d09ac-129">Requirement</span></span> | <span data-ttu-id="d09ac-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="d09ac-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d09ac-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="d09ac-131">Header</span></span><br/>  | <dl> <span data-ttu-id="d09ac-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d09ac-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d09ac-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d09ac-133">Library</span></span><br/> | <dl> <span data-ttu-id="d09ac-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d09ac-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d09ac-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d09ac-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d09ac-136">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="d09ac-136">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="d09ac-137">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="d09ac-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




