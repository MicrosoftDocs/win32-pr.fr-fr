---
description: 'ID3DXMATRIXStack :: Scale, méthode (D3DX10. h)-mettre à l’échelle la matrice actuelle à propos de l’origine de la coordonnée universelle.'
ms.assetid: d0f4b341-b3b6-42e4-84df-78f203c3728e
title: 'ID3DXMATRIXStack :: Scale, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Scale
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a7b4aceb53659fc2b1a4a95f964d068e6d7d2554
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107787"
---
# <a name="id3dxmatrixstackscale-method-d3dx10h"></a><span data-ttu-id="443f5-103">ID3DXMATRIXStack :: Scale, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="443f5-103">ID3DXMATRIXStack::Scale method (D3DX10.h)</span></span>

<span data-ttu-id="443f5-104">Mettre à l’échelle la matrice actuelle sur l’origine de la coordonnée universelle.</span><span class="sxs-lookup"><span data-stu-id="443f5-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="443f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="443f5-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="443f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="443f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="443f5-107">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="443f5-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="443f5-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="443f5-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="443f5-109">Composant de mise à l’échelle sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="443f5-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="443f5-110">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="443f5-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="443f5-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="443f5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="443f5-112">Composant de mise à l’échelle sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="443f5-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="443f5-113">*z* \[\]</span><span class="sxs-lookup"><span data-stu-id="443f5-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="443f5-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="443f5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="443f5-115">Composant de mise à l’échelle dans l’axe z.</span><span class="sxs-lookup"><span data-stu-id="443f5-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="443f5-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="443f5-116">Return value</span></span>

<span data-ttu-id="443f5-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="443f5-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="443f5-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="443f5-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="443f5-119">Notes </span><span class="sxs-lookup"><span data-stu-id="443f5-119">Remarks</span></span>

<span data-ttu-id="443f5-120">Cette méthode multiplie la matrice actuelle par la matrice de mise à l’échelle calculée.</span><span class="sxs-lookup"><span data-stu-id="443f5-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="443f5-121">La transformation concerne l’origine du monde actuel.</span><span class="sxs-lookup"><span data-stu-id="443f5-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="443f5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="443f5-122">Requirements</span></span>



| <span data-ttu-id="443f5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="443f5-123">Requirement</span></span> | <span data-ttu-id="443f5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="443f5-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="443f5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="443f5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="443f5-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="443f5-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="443f5-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="443f5-127">Library</span></span><br/> | <dl> <span data-ttu-id="443f5-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="443f5-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="443f5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="443f5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="443f5-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="443f5-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="443f5-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="443f5-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
