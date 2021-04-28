---
description: 'ID3DXMATRIXStack :: translate, méthode (D3dx9math. h)-détermine le produit de la matrice actuelle et la matrice de traduction calculée déterminée par les facteurs donnés (x, y et z).'
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
ms.openlocfilehash: 7fadad95e8e72691a0e030ed89eedc745de2be43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093337"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a><span data-ttu-id="04a7e-103">ID3DXMATRIXStack :: translate, méthode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="04a7e-103">ID3DXMATRIXStack::Translate method (D3dx9math.h)</span></span>

<span data-ttu-id="04a7e-104">Détermine le produit de la matrice actuelle et la matrice de translation calculée déterminée par les facteurs donnés (x, y et z).</span><span class="sxs-lookup"><span data-stu-id="04a7e-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="04a7e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04a7e-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="04a7e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04a7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04a7e-107">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04a7e-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04a7e-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04a7e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04a7e-109">Facteur de translation sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="04a7e-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="04a7e-110">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04a7e-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04a7e-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04a7e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04a7e-112">Facteur de translation sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="04a7e-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="04a7e-113">*z* \[\]</span><span class="sxs-lookup"><span data-stu-id="04a7e-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04a7e-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04a7e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04a7e-115">Facteur de translation dans l’axe z.</span><span class="sxs-lookup"><span data-stu-id="04a7e-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04a7e-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04a7e-116">Return value</span></span>

<span data-ttu-id="04a7e-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04a7e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04a7e-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="04a7e-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="04a7e-119">Notes </span><span class="sxs-lookup"><span data-stu-id="04a7e-119">Remarks</span></span>

<span data-ttu-id="04a7e-120">Cette méthode multiplie la matrice actuelle par la matrice de traduction calculée (la transformation concerne l’origine mondiale active).</span><span class="sxs-lookup"><span data-stu-id="04a7e-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="04a7e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04a7e-121">Requirements</span></span>



| <span data-ttu-id="04a7e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04a7e-122">Requirement</span></span> | <span data-ttu-id="04a7e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="04a7e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04a7e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="04a7e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="04a7e-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="04a7e-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="04a7e-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="04a7e-126">Library</span></span><br/> | <dl> <span data-ttu-id="04a7e-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04a7e-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="04a7e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04a7e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04a7e-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="04a7e-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="04a7e-130">**ID3DXMATRIXStack::TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="04a7e-130">**ID3DXMATRIXStack::TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
