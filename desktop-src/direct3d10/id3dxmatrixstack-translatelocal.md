---
description: Détermine le produit de la matrice de traduction calculée, déterminé par les facteurs donnés (x, y et z) et la matrice actuelle.
ms.assetid: 96399801-dd80-4e9a-a5c3-c5d41eb9368a
title: 'ID3DXMATRIXStack :: TranslateLocal, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65a627141f552107d88c3f43988daa0d316a0bef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538749"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx10h"></a><span data-ttu-id="cbab2-103">ID3DXMATRIXStack :: TranslateLocal, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="cbab2-103">ID3DXMATRIXStack::TranslateLocal method (D3DX10.h)</span></span>

<span data-ttu-id="cbab2-104">Détermine le produit de la matrice de traduction calculée, déterminé par les facteurs donnés (x, y et z) et la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="cbab2-104">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbab2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbab2-105">Syntax</span></span>


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="cbab2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbab2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbab2-107">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbab2-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbab2-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cbab2-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cbab2-109">Facteur de translation sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="cbab2-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="cbab2-110">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbab2-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbab2-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cbab2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cbab2-112">Facteur de translation sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="cbab2-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="cbab2-113">*z* \[\]</span><span class="sxs-lookup"><span data-stu-id="cbab2-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbab2-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cbab2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cbab2-115">Facteur de translation dans l’axe z.</span><span class="sxs-lookup"><span data-stu-id="cbab2-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbab2-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cbab2-116">Return value</span></span>

<span data-ttu-id="cbab2-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cbab2-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cbab2-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cbab2-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbab2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="cbab2-119">Remarks</span></span>

<span data-ttu-id="cbab2-120">Cette méthode multiplie la matrice actuelle par la matrice de traduction calculée (la transformation concerne l’origine locale de l’objet).</span><span class="sxs-lookup"><span data-stu-id="cbab2-120">This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation(&tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="cbab2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbab2-121">Requirements</span></span>



| <span data-ttu-id="cbab2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbab2-122">Requirement</span></span> | <span data-ttu-id="cbab2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbab2-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cbab2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="cbab2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cbab2-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbab2-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="cbab2-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cbab2-126">Library</span></span><br/> | <dl> <span data-ttu-id="cbab2-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbab2-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbab2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbab2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbab2-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="cbab2-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="cbab2-130">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="cbab2-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
