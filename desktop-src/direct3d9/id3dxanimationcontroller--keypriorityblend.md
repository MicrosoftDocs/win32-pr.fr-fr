---
description: Définit les clés d’événement de fusion pour la piste d’animation spécifiée.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'ID3DXAnimationController :: KeyPriorityBlend, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31778da9b26ddd79b5f05c69c822ed62a5b5281e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322681"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a><span data-ttu-id="e00b0-103">ID3DXAnimationController :: KeyPriorityBlend, méthode</span><span class="sxs-lookup"><span data-stu-id="e00b0-103">ID3DXAnimationController::KeyPriorityBlend method</span></span>

<span data-ttu-id="e00b0-104">Définit les clés d’événement de fusion pour la piste d’animation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e00b0-104">Sets blending event keys for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="e00b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e00b0-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="e00b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e00b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e00b0-107">*NewBlendWeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e00b0-107">*NewBlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e00b0-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e00b0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e00b0-109">Nombre compris entre 0 et 1 qui est utilisé pour fusionner les pistes.</span><span class="sxs-lookup"><span data-stu-id="e00b0-109">Number between 0 and 1 that is used to blend tracks together.</span></span>

</dd> <dt>

<span data-ttu-id="e00b0-110">*StartTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e00b0-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e00b0-111">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e00b0-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e00b0-112">Heure globale de démarrage de la fusion.</span><span class="sxs-lookup"><span data-stu-id="e00b0-112">Global time to start the blend.</span></span>

</dd> <dt>

<span data-ttu-id="e00b0-113">*Durée* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e00b0-113">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e00b0-114">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e00b0-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e00b0-115">Durée globale de la fusion.</span><span class="sxs-lookup"><span data-stu-id="e00b0-115">Global time duration of the blend.</span></span>

</dd> <dt>

<span data-ttu-id="e00b0-116">*Transition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e00b0-116">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e00b0-117">Type : **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="e00b0-117">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="e00b0-118">Spécifie le type de transition utilisé pour la durée du Blend.</span><span class="sxs-lookup"><span data-stu-id="e00b0-118">Specifies the transition type used for the duration of the blend.</span></span> <span data-ttu-id="e00b0-119">Consultez [**\_ type D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="e00b0-119">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e00b0-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e00b0-120">Return value</span></span>

<span data-ttu-id="e00b0-121">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="e00b0-121">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="e00b0-122">Descripteur d’événement pour l’événement Priority Blend.</span><span class="sxs-lookup"><span data-stu-id="e00b0-122">Event handle to the priority blend event.</span></span> <span data-ttu-id="e00b0-123">La **valeur null** est retournée si un ou plusieurs des paramètres d’entrée ne sont pas valides ou si aucun événement libre n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="e00b0-123">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="e00b0-124">Notes</span><span class="sxs-lookup"><span data-stu-id="e00b0-124">Remarks</span></span>

<span data-ttu-id="e00b0-125">Le contrôleur d’animation se mélange en trois phases : les pistes de faible priorité sont fusionnées en premier, les pistes haute priorité sont fusionnées en second, puis les résultats des deux sont fusionnés.</span><span class="sxs-lookup"><span data-stu-id="e00b0-125">The animation controller blends in three phases: low priority tracks are blended first, high priority tracks are blended second, and then the results of both are blended.</span></span>

## <a name="requirements"></a><span data-ttu-id="e00b0-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e00b0-126">Requirements</span></span>



| <span data-ttu-id="e00b0-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e00b0-127">Requirement</span></span> | <span data-ttu-id="e00b0-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e00b0-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e00b0-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="e00b0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e00b0-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e00b0-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e00b0-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e00b0-131">Library</span></span><br/> | <dl> <span data-ttu-id="e00b0-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e00b0-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e00b0-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e00b0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00b0-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="e00b0-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="e00b0-135">**SetPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="e00b0-135">**SetPriorityBlend**</span></span>](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
