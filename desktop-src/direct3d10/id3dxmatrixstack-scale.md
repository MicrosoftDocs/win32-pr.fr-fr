---
description: Mettre à l’échelle la matrice actuelle sur l’origine de la coordonnée universelle.
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
ms.openlocfilehash: 361c1fcbdc3f793bcf3e21d569eee740ca0b4ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527959"
---
# <a name="id3dxmatrixstackscale-method-d3dx10h"></a><span data-ttu-id="f009e-103">ID3DXMATRIXStack :: Scale, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="f009e-103">ID3DXMATRIXStack::Scale method (D3DX10.h)</span></span>

<span data-ttu-id="f009e-104">Mettre à l’échelle la matrice actuelle sur l’origine de la coordonnée universelle.</span><span class="sxs-lookup"><span data-stu-id="f009e-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="f009e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f009e-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="f009e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f009e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f009e-107">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f009e-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f009e-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f009e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f009e-109">Composant de mise à l’échelle sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="f009e-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="f009e-110">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f009e-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f009e-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f009e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f009e-112">Composant de mise à l’échelle sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="f009e-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="f009e-113">*z* \[\]</span><span class="sxs-lookup"><span data-stu-id="f009e-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f009e-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f009e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f009e-115">Composant de mise à l’échelle dans l’axe z.</span><span class="sxs-lookup"><span data-stu-id="f009e-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f009e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f009e-116">Return value</span></span>

<span data-ttu-id="f009e-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f009e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f009e-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f009e-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f009e-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f009e-119">Remarks</span></span>

<span data-ttu-id="f009e-120">Cette méthode multiplie la matrice actuelle par la matrice de mise à l’échelle calculée.</span><span class="sxs-lookup"><span data-stu-id="f009e-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="f009e-121">La transformation concerne l’origine du monde actuel.</span><span class="sxs-lookup"><span data-stu-id="f009e-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="f009e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f009e-122">Requirements</span></span>



| <span data-ttu-id="f009e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f009e-123">Requirement</span></span> | <span data-ttu-id="f009e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f009e-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f009e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f009e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f009e-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f009e-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f009e-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f009e-127">Library</span></span><br/> | <dl> <span data-ttu-id="f009e-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f009e-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f009e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f009e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f009e-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="f009e-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="f009e-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="f009e-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
