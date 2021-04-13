---
description: Définit une clé d’événement qui active ou désactive une piste d’animation.
ms.assetid: de81e646-0b94-40d3-89c2-060d118d17b2
title: 'ID3DXAnimationController :: KeyTrackEnable, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f22c732ff57e948ebcc2e89d790d352e4dc057ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322678"
---
# <a name="id3dxanimationcontrollerkeytrackenable-method"></a><span data-ttu-id="be729-103">ID3DXAnimationController :: KeyTrackEnable, méthode</span><span class="sxs-lookup"><span data-stu-id="be729-103">ID3DXAnimationController::KeyTrackEnable method</span></span>

<span data-ttu-id="be729-104">Définit une clé d’événement qui active ou désactive une piste d’animation.</span><span class="sxs-lookup"><span data-stu-id="be729-104">Sets an event key that enables or disables an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="be729-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be729-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackEnable(
  [in] UINT   Track,
  [in] BOOL   NewEnable,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="be729-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be729-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be729-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be729-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be729-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be729-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be729-109">Identificateur de la piste d’animation à modifier.</span><span class="sxs-lookup"><span data-stu-id="be729-109">Identifier of the animation track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="be729-110">*NewEnable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be729-110">*NewEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be729-111">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be729-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be729-112">Activer l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="be729-112">Enable flag.</span></span> <span data-ttu-id="be729-113">Affectez la valeur **true** pour activer la piste d’animation, ou la **valeur false** pour désactiver la piste.</span><span class="sxs-lookup"><span data-stu-id="be729-113">Set this to **TRUE** to enable the animation track, or to **FALSE** to disable the track.</span></span>

</dd> <dt>

<span data-ttu-id="be729-114">*StartTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be729-114">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be729-115">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be729-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be729-116">Clé de temps globale.</span><span class="sxs-lookup"><span data-stu-id="be729-116">Global time key.</span></span> <span data-ttu-id="be729-117">Spécifie l’heure globale à laquelle la modification doit avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="be729-117">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be729-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be729-118">Return value</span></span>

<span data-ttu-id="be729-119">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="be729-119">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="be729-120">Descripteur d’événement pour l’événement Priority Blend.</span><span class="sxs-lookup"><span data-stu-id="be729-120">Event handle to the priority blend event.</span></span> <span data-ttu-id="be729-121">La **valeur null** est retournée si Track n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="be729-121">**NULL** is returned if Track is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="be729-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be729-122">Requirements</span></span>



| <span data-ttu-id="be729-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be729-123">Requirement</span></span> | <span data-ttu-id="be729-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="be729-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be729-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="be729-125">Header</span></span><br/>  | <dl> <span data-ttu-id="be729-126"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="be729-126"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="be729-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be729-127">Library</span></span><br/> | <dl> <span data-ttu-id="be729-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be729-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be729-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be729-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be729-130">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="be729-130">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
