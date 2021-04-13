---
description: Définit une clé d’événement qui modifie l’heure locale d’une piste d’animation.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: 'ID3DXAnimationController :: KeyTrackPosition, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d027069efa9fb49cad3d2344da593eae4c3c844c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323181"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a><span data-ttu-id="ed188-103">ID3DXAnimationController :: KeyTrackPosition, méthode</span><span class="sxs-lookup"><span data-stu-id="ed188-103">ID3DXAnimationController::KeyTrackPosition method</span></span>

<span data-ttu-id="ed188-104">Définit une clé d’événement qui modifie l’heure locale d’une piste d’animation.</span><span class="sxs-lookup"><span data-stu-id="ed188-104">Sets an event key that changes the local time of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed188-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed188-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE NewPosition,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="ed188-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed188-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed188-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed188-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed188-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed188-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed188-109">Identificateur de la piste à modifier.</span><span class="sxs-lookup"><span data-stu-id="ed188-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="ed188-110">*NewPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed188-110">*NewPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed188-111">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed188-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed188-112">Nouvelle heure locale de la piste d’animation.</span><span class="sxs-lookup"><span data-stu-id="ed188-112">New local time of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="ed188-113">*StartTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed188-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed188-114">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed188-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed188-115">Clé de temps globale.</span><span class="sxs-lookup"><span data-stu-id="ed188-115">Global time key.</span></span> <span data-ttu-id="ed188-116">Spécifie l’heure globale à laquelle la modification doit avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="ed188-116">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed188-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed188-117">Return value</span></span>

<span data-ttu-id="ed188-118">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="ed188-118">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="ed188-119">Descripteur d’événement pour l’événement Priority Blend.</span><span class="sxs-lookup"><span data-stu-id="ed188-119">Event handle to the priority blend event.</span></span> <span data-ttu-id="ed188-120">La **valeur null** est retournée si Track n’est pas valide ou si aucun événement libre n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="ed188-120">**NULL** is returned if Track is invalid, or if no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed188-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed188-121">Requirements</span></span>



| <span data-ttu-id="ed188-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed188-122">Requirement</span></span> | <span data-ttu-id="ed188-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed188-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed188-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed188-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ed188-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed188-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ed188-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ed188-126">Library</span></span><br/> | <dl> <span data-ttu-id="ed188-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed188-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ed188-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed188-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed188-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ed188-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
