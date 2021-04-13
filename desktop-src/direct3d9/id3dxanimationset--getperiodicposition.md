---
description: Retourne la position de l’heure dans la plage locale d’un ensemble d’animations.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'ID3DXAnimationSet :: GetPeriodicPosition, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3c4f2e8e57efdfe0681b8ae691e0b5de42624e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323350"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a><span data-ttu-id="c1a43-103">ID3DXAnimationSet :: GetPeriodicPosition, méthode</span><span class="sxs-lookup"><span data-stu-id="c1a43-103">ID3DXAnimationSet::GetPeriodicPosition method</span></span>

<span data-ttu-id="c1a43-104">Retourne la position de l’heure dans la plage locale d’un ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="c1a43-104">Returns time position in the local timeframe of an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a43-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1a43-105">Syntax</span></span>


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a><span data-ttu-id="c1a43-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1a43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a43-107">*Position* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1a43-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a43-108">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1a43-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1a43-109">Heure locale de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="c1a43-109">Local time of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a43-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1a43-110">Return value</span></span>

<span data-ttu-id="c1a43-111">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1a43-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1a43-112">Position temporelle telle que mesurée dans le laps de temps de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="c1a43-112">Time position as measured in the timeframe of the animation set.</span></span> <span data-ttu-id="c1a43-113">Cette valeur est limitée par la période de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="c1a43-113">This value will be bounded by the period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1a43-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c1a43-114">Remarks</span></span>

<span data-ttu-id="c1a43-115">La position d’heure retournée par cette méthode peut être utilisée en tant que paramètre PeriodicPosition de [**ID3DXAnimationSet :: GetSRT**](id3dxanimationset--getsrt.md).</span><span class="sxs-lookup"><span data-stu-id="c1a43-115">The time position returned by this method can be used as the PeriodicPosition parameter of [**ID3DXAnimationSet::GetSRT**](id3dxanimationset--getsrt.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1a43-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1a43-116">Requirements</span></span>



| <span data-ttu-id="c1a43-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1a43-117">Requirement</span></span> | <span data-ttu-id="c1a43-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1a43-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a43-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1a43-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c1a43-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1a43-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c1a43-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c1a43-121">Library</span></span><br/> | <dl> <span data-ttu-id="c1a43-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1a43-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1a43-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1a43-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a43-124">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="c1a43-124">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
