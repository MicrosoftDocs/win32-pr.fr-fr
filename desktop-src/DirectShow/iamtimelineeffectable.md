---
description: L’interface IAMTimelineEffectable fournit des méthodes pour ajouter des effets à un objet Timeline dans les services de modification DirectShow (DES) et pour manipuler les effets sur un objet.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: Interface IAMTimelineEffectable (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc67483f44515c2ce18825de5b6657d51e2c3826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539273"
---
# <a name="iamtimelineeffectable-interface"></a><span data-ttu-id="a0792-103">Interface IAMTimelineEffectable</span><span class="sxs-lookup"><span data-stu-id="a0792-103">IAMTimelineEffectable interface</span></span>

> [!Note]  
> <span data-ttu-id="a0792-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="a0792-104">\[Deprecated.</span></span> <span data-ttu-id="a0792-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a0792-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a0792-106">L' `IAMTimelineEffectable` interface fournit des méthodes pour ajouter des effets à un objet Timeline dans les [services de modification DirectShow](directshow-editing-services.md) (des) et pour manipuler les effets sur un objet.</span><span class="sxs-lookup"><span data-stu-id="a0792-106">The `IAMTimelineEffectable` interface provides methods for adding effects to a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES), and for manipulating the effects on an object.</span></span> <span data-ttu-id="a0792-107">Tous les objets qui peuvent avoir des effets appliqués implémentent cette interface ; Cela comprend les sources, les pistes et les compositions.</span><span class="sxs-lookup"><span data-stu-id="a0792-107">All objects that can have effects applied to them implement this interface; this includes sources, tracks, and compositions.</span></span>

<span data-ttu-id="a0792-108">Un objet qui implémente cette interface peut avoir n’importe quel nombre d’effets.</span><span class="sxs-lookup"><span data-stu-id="a0792-108">An object that implements this interface can have any number of effects.</span></span> <span data-ttu-id="a0792-109">Pour chaque objet, le moteur de rendu applique ses effets par ordre de priorité, en commençant par le niveau de priorité 0.</span><span class="sxs-lookup"><span data-stu-id="a0792-109">For each object, the render engine applies its effects in order of priority, starting with priority level 0.</span></span>

## <a name="members"></a><span data-ttu-id="a0792-110">Membres</span><span class="sxs-lookup"><span data-stu-id="a0792-110">Members</span></span>

<span data-ttu-id="a0792-111">L’interface **IAMTimelineEffectable** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a0792-111">The **IAMTimelineEffectable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a0792-112">**IAMTimelineEffectable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a0792-112">**IAMTimelineEffectable** also has these types of members:</span></span>

-   [<span data-ttu-id="a0792-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a0792-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a0792-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a0792-114">Methods</span></span>

<span data-ttu-id="a0792-115">L’interface **IAMTimelineEffectable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a0792-115">The **IAMTimelineEffectable** interface has these methods.</span></span>



| <span data-ttu-id="a0792-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="a0792-116">Method</span></span>                                                                     | <span data-ttu-id="a0792-117">Description</span><span class="sxs-lookup"><span data-stu-id="a0792-117">Description</span></span>                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="a0792-118">**EffectGetCount**</span><span class="sxs-lookup"><span data-stu-id="a0792-118">**EffectGetCount**</span></span>](iamtimelineeffectable-effectgetcount.md)             | <span data-ttu-id="a0792-119">Récupère le nombre d’effets sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="a0792-119">Retrieves the number of effects on this object.</span></span><br/>                    |
| [<span data-ttu-id="a0792-120">**EffectInsBefore**</span><span class="sxs-lookup"><span data-stu-id="a0792-120">**EffectInsBefore**</span></span>](iamtimelineeffectable-effectinsbefore.md)           | <span data-ttu-id="a0792-121">Insère un effet dans l’objet au niveau de priorité spécifié.</span><span class="sxs-lookup"><span data-stu-id="a0792-121">Inserts an effect into the object at the specified priority level.</span></span><br/> |
| [<span data-ttu-id="a0792-122">**EffectSwapPriorities**</span><span class="sxs-lookup"><span data-stu-id="a0792-122">**EffectSwapPriorities**</span></span>](iamtimelineeffectable-effectswappriorities.md) | <span data-ttu-id="a0792-123">Change les niveaux de priorité de deux effets.</span><span class="sxs-lookup"><span data-stu-id="a0792-123">Switches the priority levels of two effects.</span></span><br/>                       |
| [<span data-ttu-id="a0792-124">**GetEffect**</span><span class="sxs-lookup"><span data-stu-id="a0792-124">**GetEffect**</span></span>](iamtimelineeffectable-geteffect.md)                       | <span data-ttu-id="a0792-125">Récupère l’effet au niveau de priorité spécifié.</span><span class="sxs-lookup"><span data-stu-id="a0792-125">Retrieves the effect at the specified priority level.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="a0792-126">Notes</span><span class="sxs-lookup"><span data-stu-id="a0792-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a0792-127">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="a0792-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a0792-128">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a0792-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a0792-129">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a0792-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a0792-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0792-130">Requirements</span></span>



| <span data-ttu-id="a0792-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0792-131">Requirement</span></span> | <span data-ttu-id="a0792-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0792-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0792-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0792-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a0792-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0792-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a0792-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a0792-135">Library</span></span><br/> | <dl> <span data-ttu-id="a0792-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0792-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
