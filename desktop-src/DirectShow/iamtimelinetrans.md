---
description: L’interface IAMTimelineTrans fournit des méthodes de manipulation des transitions dans les services de modification DirectShow (DES).
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: Interface IAMTimelineTrans (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cd3c39d0a5434befdd5607b340fef936644bf48e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541748"
---
# <a name="iamtimelinetrans-interface"></a><span data-ttu-id="e4061-103">Interface IAMTimelineTrans</span><span class="sxs-lookup"><span data-stu-id="e4061-103">IAMTimelineTrans interface</span></span>

> [!Note]  
> <span data-ttu-id="e4061-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e4061-104">\[Deprecated.</span></span> <span data-ttu-id="e4061-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e4061-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e4061-106">L' `IAMTimelineTrans` interface fournit des méthodes pour la manipulation des transitions dans les [services de modification DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="e4061-106">The `IAMTimelineTrans` interface provides methods for manipulating transitions in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="e4061-107">Une transition est une progression entre une couche vidéo et le rendu composite de toutes les couches vidéo avec une priorité plus faible.</span><span class="sxs-lookup"><span data-stu-id="e4061-107">A transition is a progression between one video layer and the rendered composite of all video layers with a lower priority.</span></span> <span data-ttu-id="e4061-108">Une transition peut être ajoutée à n’importe quel objet Timeline qui expose l’interface [**IAMTimelineTransable**](iamtimelinetransable.md) .</span><span class="sxs-lookup"><span data-stu-id="e4061-108">A transition can be added to any timeline object that exposes the [**IAMTimelineTransable**](iamtimelinetransable.md) interface.</span></span> <span data-ttu-id="e4061-109">Pour définir les propriétés d’une transition, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="e4061-109">To set properties on a transition, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="e4061-110">L’objet de transition DES est en fait un wrapper pour un objet de transformation DirectX.</span><span class="sxs-lookup"><span data-stu-id="e4061-110">The DES transition object is actually a wrapper for a DirectX Transform object.</span></span> <span data-ttu-id="e4061-111">Tout objet de transformation DirectX à 2 entrées peut être utilisé pour implémenter l’effet visuel de la transition.</span><span class="sxs-lookup"><span data-stu-id="e4061-111">Any 2-input DirectX Transform object can be used to implement the visual effect for the transition.</span></span> <span data-ttu-id="e4061-112">Microsoft ne prend plus en charge le développement d’objets de transformation DirectX tiers.</span><span class="sxs-lookup"><span data-stu-id="e4061-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="e4061-113">Pour spécifier l’objet de transformation DirectX pour une transition, appelez la méthode [**IAMTimelineObj :: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="e4061-113">To specify the DirectX Transform object for a transition, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="e4061-114">Pour créer un objet de transition, appelez [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) avec la \_ transition de type principale de la valeur Timeline \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e4061-114">To create a transition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRANSITION.</span></span> <span data-ttu-id="e4061-115">Vous pouvez interroger le pointeur [**IAMTimelineObj**](iamtimelineobj.md) retourné pour l' `IAMTimelineTrans` interface.</span><span class="sxs-lookup"><span data-stu-id="e4061-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineTrans` interface.</span></span>

## <a name="members"></a><span data-ttu-id="e4061-116">Membres</span><span class="sxs-lookup"><span data-stu-id="e4061-116">Members</span></span>

<span data-ttu-id="e4061-117">L’interface **IAMTimelineTrans** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e4061-117">The **IAMTimelineTrans** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e4061-118">**IAMTimelineTrans** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e4061-118">**IAMTimelineTrans** also has these types of members:</span></span>

-   [<span data-ttu-id="e4061-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e4061-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e4061-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e4061-120">Methods</span></span>

<span data-ttu-id="e4061-121">L’interface **IAMTimelineTrans** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e4061-121">The **IAMTimelineTrans** interface has these methods.</span></span>



| <span data-ttu-id="e4061-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="e4061-122">Method</span></span>                                                  | <span data-ttu-id="e4061-123">Description</span><span class="sxs-lookup"><span data-stu-id="e4061-123">Description</span></span>                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4061-124">**GetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="e4061-124">**GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)     | <span data-ttu-id="e4061-125">Récupère le point de coupe.</span><span class="sxs-lookup"><span data-stu-id="e4061-125">Retrieves the cut point.</span></span><br/>                                                    |
| [<span data-ttu-id="e4061-126">**GetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="e4061-126">**GetCutPoint2**</span></span>](iamtimelinetrans-getcutpoint2.md)   | <span data-ttu-id="e4061-127">Récupère le point de coupe, en tant que valeur [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="e4061-127">Retrieves the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>             |
| [<span data-ttu-id="e4061-128">**GetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="e4061-128">**GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)     | <span data-ttu-id="e4061-129">Détermine si la transition est rendue sous la forme d’une coupe.</span><span class="sxs-lookup"><span data-stu-id="e4061-129">Determines whether the transition is rendered as a cut.</span></span><br/>                     |
| [<span data-ttu-id="e4061-130">**GetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="e4061-130">**GetSwapInputs**</span></span>](iamtimelinetrans-getswapinputs.md) | <span data-ttu-id="e4061-131">Récupère une valeur qui indique si les entrées de transition sont échangées.</span><span class="sxs-lookup"><span data-stu-id="e4061-131">Retrieves a value that indicates whether the transition inputs are swapped.</span></span><br/> |
| [<span data-ttu-id="e4061-132">**SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="e4061-132">**SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)     | <span data-ttu-id="e4061-133">Définit le point de coupe.</span><span class="sxs-lookup"><span data-stu-id="e4061-133">Sets the cut point.</span></span><br/>                                                         |
| [<span data-ttu-id="e4061-134">**SetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="e4061-134">**SetCutPoint2**</span></span>](iamtimelinetrans-setcutpoint2.md)   | <span data-ttu-id="e4061-135">Définit le point de coupe comme valeur [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="e4061-135">Sets the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>                  |
| [<span data-ttu-id="e4061-136">**SetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="e4061-136">**SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)     | <span data-ttu-id="e4061-137">Spécifie si la transition est rendue sous la forme d’une coupe.</span><span class="sxs-lookup"><span data-stu-id="e4061-137">Specifies whether the transition is rendered as a cut.</span></span><br/>                      |
| [<span data-ttu-id="e4061-138">**SetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="e4061-138">**SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md) | <span data-ttu-id="e4061-139">Spécifie si les entrées de transition sont échangées.</span><span class="sxs-lookup"><span data-stu-id="e4061-139">Specifies whether the transition inputs are swapped.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="e4061-140">Notes</span><span class="sxs-lookup"><span data-stu-id="e4061-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e4061-141">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="e4061-141">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e4061-142">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e4061-142">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e4061-143">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e4061-143">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e4061-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4061-144">Requirements</span></span>



| <span data-ttu-id="e4061-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4061-145">Requirement</span></span> | <span data-ttu-id="e4061-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4061-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4061-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4061-147">Header</span></span><br/>  | <dl> <span data-ttu-id="e4061-148"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4061-148"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e4061-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e4061-149">Library</span></span><br/> | <dl> <span data-ttu-id="e4061-150"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4061-150"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4061-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4061-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4061-152">Utilisation des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="e4061-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
