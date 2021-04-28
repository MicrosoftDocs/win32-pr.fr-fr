---
description: 'ID3DXMATRIXStack :: translate, méthode (D3DX10. h)-détermine le produit de la matrice actuelle et la matrice de traduction calculée déterminée par les facteurs donnés (x, y et z).'
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
ms.openlocfilehash: 41e84b62c077da03806a5e781498c05ee3c8ee67
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107767"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx10h"></a><span data-ttu-id="f9361-103">ID3DXMATRIXStack :: translate, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="f9361-103">ID3DXMATRIXStack::Translate method (D3DX10.h)</span></span>

<span data-ttu-id="f9361-104">Détermine le produit de la matrice actuelle et la matrice de translation calculée déterminée par les facteurs donnés (x, y et z).</span><span class="sxs-lookup"><span data-stu-id="f9361-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9361-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9361-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="f9361-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9361-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9361-107">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9361-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9361-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9361-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f9361-109">Facteur de translation sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="f9361-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="f9361-110">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9361-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9361-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9361-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f9361-112">Facteur de translation sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="f9361-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="f9361-113">*z* \[\]</span><span class="sxs-lookup"><span data-stu-id="f9361-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9361-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9361-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f9361-115">Facteur de translation dans l’axe z.</span><span class="sxs-lookup"><span data-stu-id="f9361-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9361-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f9361-116">Return value</span></span>

<span data-ttu-id="f9361-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f9361-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f9361-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f9361-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9361-119">Notes </span><span class="sxs-lookup"><span data-stu-id="f9361-119">Remarks</span></span>

<span data-ttu-id="f9361-120">Cette méthode multiplie la matrice actuelle par la matrice de traduction calculée (la transformation concerne l’origine mondiale active).</span><span class="sxs-lookup"><span data-stu-id="f9361-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="f9361-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9361-121">Requirements</span></span>



| <span data-ttu-id="f9361-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9361-122">Requirement</span></span> | <span data-ttu-id="f9361-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9361-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9361-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9361-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f9361-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9361-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9361-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f9361-126">Library</span></span><br/> | <dl> <span data-ttu-id="f9361-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9361-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9361-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9361-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9361-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="f9361-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="f9361-130">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="f9361-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
