---
description: L’interface IAMTimelineEffect fournit des méthodes pour manipuler les effets audio et vidéo dans les services de modification DirectShow (DES).
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Interface IAMTimelineEffect (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8b9936616b9c4487849053d36c6a63290bd16b5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537917"
---
# <a name="iamtimelineeffect-interface"></a><span data-ttu-id="309a5-103">Interface IAMTimelineEffect</span><span class="sxs-lookup"><span data-stu-id="309a5-103">IAMTimelineEffect interface</span></span>

> [!Note]  
> <span data-ttu-id="309a5-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="309a5-104">\[Deprecated.</span></span> <span data-ttu-id="309a5-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="309a5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="309a5-106">L' `IAMTimelineEffect` interface fournit des méthodes pour manipuler les effets audio et vidéo dans les [services de modification DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="309a5-106">The `IAMTimelineEffect` interface provides methods for manipulating audio and video effects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="309a5-107">Un effet peut être ajouté à n’importe quel objet Timeline qui expose l’interface [**IAMTimelineEffectable**](iamtimelineeffectable.md) .</span><span class="sxs-lookup"><span data-stu-id="309a5-107">An effect can be added to any timeline object that exposes the [**IAMTimelineEffectable**](iamtimelineeffectable.md) interface.</span></span> <span data-ttu-id="309a5-108">Pour définir des propriétés sur un effet, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="309a5-108">To set properties on an effect, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="309a5-109">L’objet DES EFFETS DES est en fait un wrapper pour l’un des deux autres objets :</span><span class="sxs-lookup"><span data-stu-id="309a5-109">The DES effect object is actually a wrapper for one of two other objects:</span></span>

-   <span data-ttu-id="309a5-110">Pour les effets audio, n’importe quel filtre d’effet audio DirectShow.</span><span class="sxs-lookup"><span data-stu-id="309a5-110">For audio effects, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="309a5-111">Pour les effets vidéo, et 1-entrée de l’objet de transformation DirectX.</span><span class="sxs-lookup"><span data-stu-id="309a5-111">For video effects, and 1-input DirectX Transform object.</span></span>

<span data-ttu-id="309a5-112">Microsoft ne prend plus en charge le développement d’objets de transformation DirectX tiers.</span><span class="sxs-lookup"><span data-stu-id="309a5-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span>

<span data-ttu-id="309a5-113">Pour spécifier le filtre ou l’objet de transformation DirectX pour un effet, appelez la méthode [**IAMTimelineObj :: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="309a5-113">To specify the filter or DirectX Transform object for an effect, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="309a5-114">Pour créer un objet Effect, appelez [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) avec l’effet de type principal de chronologie des valeurs \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="309a5-114">To create an effect object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_EFFECT.</span></span> <span data-ttu-id="309a5-115">Vous pouvez interroger le pointeur [**IAMTimelineObj**](iamtimelineobj.md) retourné pour l' `IAMTimelineEffect` interface.</span><span class="sxs-lookup"><span data-stu-id="309a5-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineEffect` interface.</span></span>

## <a name="members"></a><span data-ttu-id="309a5-116">Membres</span><span class="sxs-lookup"><span data-stu-id="309a5-116">Members</span></span>

<span data-ttu-id="309a5-117">L’interface **IAMTimelineEffect** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="309a5-117">The **IAMTimelineEffect** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="309a5-118">**IAMTimelineEffect** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="309a5-118">**IAMTimelineEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="309a5-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="309a5-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="309a5-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="309a5-120">Methods</span></span>

<span data-ttu-id="309a5-121">L’interface **IAMTimelineEffect** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="309a5-121">The **IAMTimelineEffect** interface has these methods.</span></span>



| <span data-ttu-id="309a5-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="309a5-122">Method</span></span>                                                           | <span data-ttu-id="309a5-123">Description</span><span class="sxs-lookup"><span data-stu-id="309a5-123">Description</span></span>                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="309a5-124">**EffectGetPriority**</span><span class="sxs-lookup"><span data-stu-id="309a5-124">**EffectGetPriority**</span></span>](iamtimelineeffect-effectgetpriority.md) | <span data-ttu-id="309a5-125">Récupère le niveau de priorité de l’effet.</span><span class="sxs-lookup"><span data-stu-id="309a5-125">Retrieves the effect's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="309a5-126">Notes</span><span class="sxs-lookup"><span data-stu-id="309a5-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="309a5-127">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="309a5-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="309a5-128">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="309a5-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="309a5-129">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="309a5-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="309a5-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="309a5-130">Requirements</span></span>



| <span data-ttu-id="309a5-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="309a5-131">Requirement</span></span> | <span data-ttu-id="309a5-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="309a5-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="309a5-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="309a5-133">Header</span></span><br/>  | <dl> <span data-ttu-id="309a5-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="309a5-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="309a5-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="309a5-135">Library</span></span><br/> | <dl> <span data-ttu-id="309a5-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="309a5-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="309a5-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="309a5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="309a5-138">Utilisation des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="309a5-138">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
