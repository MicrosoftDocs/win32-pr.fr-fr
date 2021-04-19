---
description: La méthode SetRenderRange définit la plage de temps à restituer sur la chronologie. Les objets qui se trouvent en dehors de la plage spécifiée ne sont pas rendus, et les ressources ne sont pas allouées pour eux.
ms.assetid: 2dcdca6b-2bae-4a27-bfbc-19a9b2ea633a
title: 'IRenderEngine :: SetRenderRange, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e715c2c0077a890948cfd5f5026afe98633325ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530337"
---
# <a name="irenderenginesetrenderrange-method"></a><span data-ttu-id="25ad8-104">IRenderEngine :: SetRenderRange, méthode</span><span class="sxs-lookup"><span data-stu-id="25ad8-104">IRenderEngine::SetRenderRange method</span></span>

> [!Note]  
> <span data-ttu-id="25ad8-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="25ad8-105">\[Deprecated.</span></span> <span data-ttu-id="25ad8-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="25ad8-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="25ad8-107">La `SetRenderRange` méthode définit la plage de temps de la chronologie à restituer.</span><span class="sxs-lookup"><span data-stu-id="25ad8-107">The `SetRenderRange` method sets the range of time on the timeline to be rendered.</span></span> <span data-ttu-id="25ad8-108">Les objets qui se trouvent en dehors de la plage spécifiée ne sont pas rendus, et les ressources ne sont pas allouées pour eux.</span><span class="sxs-lookup"><span data-stu-id="25ad8-108">Objects that lie outside the specified range are not rendered, and resources are not allocated for them.</span></span>

## <a name="syntax"></a><span data-ttu-id="25ad8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25ad8-109">Syntax</span></span>


```C++
HRESULT SetRenderRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="25ad8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25ad8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25ad8-111">*Start*</span><span class="sxs-lookup"><span data-stu-id="25ad8-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="25ad8-112">Heure de début, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="25ad8-112">Start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="25ad8-113">*Stop*</span><span class="sxs-lookup"><span data-stu-id="25ad8-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="25ad8-114">Heure d’arrêt, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="25ad8-114">Stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25ad8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25ad8-115">Return value</span></span>

<span data-ttu-id="25ad8-116">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="25ad8-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="25ad8-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="25ad8-117">Return code</span></span>                                                                                            | <span data-ttu-id="25ad8-118">Description</span><span class="sxs-lookup"><span data-stu-id="25ad8-118">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="25ad8-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25ad8-119"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="25ad8-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="25ad8-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="25ad8-121"><dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt></span><span class="sxs-lookup"><span data-stu-id="25ad8-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="25ad8-122">Le moteur de rendu n’a pas pu s’initialiser.</span><span class="sxs-lookup"><span data-stu-id="25ad8-122">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="25ad8-123">Notes</span><span class="sxs-lookup"><span data-stu-id="25ad8-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="25ad8-124">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="25ad8-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="25ad8-125">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="25ad8-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="25ad8-126">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="25ad8-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="25ad8-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25ad8-127">Requirements</span></span>



| <span data-ttu-id="25ad8-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25ad8-128">Requirement</span></span> | <span data-ttu-id="25ad8-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="25ad8-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25ad8-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="25ad8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="25ad8-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="25ad8-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="25ad8-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="25ad8-132">Library</span></span><br/> | <dl> <span data-ttu-id="25ad8-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25ad8-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25ad8-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25ad8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ad8-135">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="25ad8-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="25ad8-136">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="25ad8-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




