---
description: Détermine le produit de la matrice actuelle et la matrice de translation calculée déterminée par les facteurs donnés (x, y et z).
ms.assetid: e0ac72a2-9970-433e-9026-aa79edc8261c
title: 'ID3DXMATRIXStack :: translate, méthode (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 228b4302a512e96d5c009edcb3f0b673ee61e047
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531583"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a><span data-ttu-id="7f85e-103">ID3DXMATRIXStack :: translate, méthode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7f85e-103">ID3DXMATRIXStack::Translate method (D3dx9math.h)</span></span>

<span data-ttu-id="7f85e-104">Détermine le produit de la matrice actuelle et la matrice de translation calculée déterminée par les facteurs donnés (x, y et z).</span><span class="sxs-lookup"><span data-stu-id="7f85e-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f85e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f85e-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="7f85e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f85e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f85e-107">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f85e-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f85e-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f85e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f85e-109">Facteur de translation sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="7f85e-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="7f85e-110">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f85e-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f85e-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f85e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f85e-112">Facteur de translation sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="7f85e-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="7f85e-113">*z* \[\]</span><span class="sxs-lookup"><span data-stu-id="7f85e-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f85e-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f85e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f85e-115">Facteur de translation dans l’axe z.</span><span class="sxs-lookup"><span data-stu-id="7f85e-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f85e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f85e-116">Return value</span></span>

<span data-ttu-id="7f85e-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7f85e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7f85e-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7f85e-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f85e-119">Notes</span><span class="sxs-lookup"><span data-stu-id="7f85e-119">Remarks</span></span>

<span data-ttu-id="7f85e-120">Cette méthode multiplie la matrice actuelle par la matrice de traduction calculée (la transformation concerne l’origine mondiale active).</span><span class="sxs-lookup"><span data-stu-id="7f85e-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="7f85e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f85e-121">Requirements</span></span>



| <span data-ttu-id="7f85e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f85e-122">Requirement</span></span> | <span data-ttu-id="7f85e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f85e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f85e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f85e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7f85e-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f85e-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7f85e-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7f85e-126">Library</span></span><br/> | <dl> <span data-ttu-id="7f85e-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f85e-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7f85e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f85e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f85e-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="7f85e-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="7f85e-130">**ID3DXMATRIXStack::TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="7f85e-130">**ID3DXMATRIXStack::TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
