---
description: La méthode SetTimelineObject définit la chronologie à utiliser par le moteur de rendu.
ms.assetid: 9b60b148-9768-43ba-a986-a96838c4d2bb
title: 'IRenderEngine :: SetTimelineObject, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 954fab15e92e6111439abb66d53d53525a5afdb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541298"
---
# <a name="irenderenginesettimelineobject-method"></a><span data-ttu-id="ea721-103">IRenderEngine :: SetTimelineObject, méthode</span><span class="sxs-lookup"><span data-stu-id="ea721-103">IRenderEngine::SetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="ea721-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="ea721-104">\[Deprecated.</span></span> <span data-ttu-id="ea721-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ea721-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ea721-106">La `SetTimelineObject` méthode définit la chronologie que le moteur de rendu utilise.</span><span class="sxs-lookup"><span data-stu-id="ea721-106">The `SetTimelineObject` method sets the timeline for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea721-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea721-107">Syntax</span></span>


```C++
HRESULT SetTimelineObject(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="ea721-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea721-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea721-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="ea721-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="ea721-110">Pointeur vers l’interface [**IAMTimeline**](iamtimeline.md) de l’objet Timeline.</span><span class="sxs-lookup"><span data-stu-id="ea721-110">Pointer to the timeline object's [**IAMTimeline**](iamtimeline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea721-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea721-111">Return value</span></span>

<span data-ttu-id="ea721-112">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea721-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="ea721-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ea721-113">Return code</span></span>                                                                                            | <span data-ttu-id="ea721-114">Description</span><span class="sxs-lookup"><span data-stu-id="ea721-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="ea721-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ea721-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="ea721-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="ea721-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="ea721-117"><dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt></span><span class="sxs-lookup"><span data-stu-id="ea721-117"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="ea721-118">Le moteur de rendu n’a pas pu s’initialiser.</span><span class="sxs-lookup"><span data-stu-id="ea721-118">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="ea721-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="ea721-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="ea721-120">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="ea721-120">Insufficient memory.</span></span><br/>                |
| <dl> <span data-ttu-id="ea721-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="ea721-121"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="ea721-122">Pointeur non valide.</span><span class="sxs-lookup"><span data-stu-id="ea721-122">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="ea721-123">Notes</span><span class="sxs-lookup"><span data-stu-id="ea721-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ea721-124">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="ea721-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ea721-125">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ea721-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ea721-126">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ea721-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea721-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea721-127">Requirements</span></span>



| <span data-ttu-id="ea721-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea721-128">Requirement</span></span> | <span data-ttu-id="ea721-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea721-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea721-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea721-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ea721-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea721-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ea721-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ea721-132">Library</span></span><br/> | <dl> <span data-ttu-id="ea721-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea721-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea721-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea721-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea721-135">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="ea721-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="ea721-136">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="ea721-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




