---
description: Détermine le produit de la matrice actuelle et la matrice de translation calculée déterminée par les facteurs donnés (x, y et z).
ms.assetid: d6e347a5-bb66-451d-b66e-49ea8eff70b3
title: 'ID3DXMATRIXStack :: translate, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 159e1dc6b3dabeb92b32798cbe318f6c72c01d70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535210"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx10h"></a><span data-ttu-id="4634e-103">ID3DXMATRIXStack :: translate, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="4634e-103">ID3DXMATRIXStack::Translate method (D3DX10.h)</span></span>

<span data-ttu-id="4634e-104">Détermine le produit de la matrice actuelle et la matrice de translation calculée déterminée par les facteurs donnés (x, y et z).</span><span class="sxs-lookup"><span data-stu-id="4634e-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="4634e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4634e-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="4634e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4634e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4634e-107">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4634e-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4634e-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4634e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4634e-109">Facteur de translation sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="4634e-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="4634e-110">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4634e-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4634e-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4634e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4634e-112">Facteur de translation sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="4634e-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="4634e-113">*z* \[\]</span><span class="sxs-lookup"><span data-stu-id="4634e-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4634e-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4634e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4634e-115">Facteur de translation dans l’axe z.</span><span class="sxs-lookup"><span data-stu-id="4634e-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4634e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4634e-116">Return value</span></span>

<span data-ttu-id="4634e-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4634e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4634e-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4634e-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4634e-119">Notes</span><span class="sxs-lookup"><span data-stu-id="4634e-119">Remarks</span></span>

<span data-ttu-id="4634e-120">Cette méthode multiplie la matrice actuelle par la matrice de traduction calculée (la transformation concerne l’origine mondiale active).</span><span class="sxs-lookup"><span data-stu-id="4634e-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="4634e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4634e-121">Requirements</span></span>



| <span data-ttu-id="4634e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4634e-122">Requirement</span></span> | <span data-ttu-id="4634e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4634e-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4634e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4634e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4634e-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4634e-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4634e-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4634e-126">Library</span></span><br/> | <dl> <span data-ttu-id="4634e-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4634e-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4634e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4634e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4634e-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="4634e-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="4634e-130">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="4634e-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
