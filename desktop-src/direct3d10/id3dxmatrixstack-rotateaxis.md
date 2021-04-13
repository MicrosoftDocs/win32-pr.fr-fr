---
description: Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.
ms.assetid: 7c842bf6-2d13-422e-8136-0506a76ce9fe
title: 'ID3DXMATRIXStack :: RotateAxis, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxis
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: badd26d61fa6580b0193039e29a8fceedabe2d3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323377"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx10h"></a><span data-ttu-id="ca544-103">ID3DXMATRIXStack :: RotateAxis, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="ca544-103">ID3DXMATRIXStack::RotateAxis method (D3DX10.h)</span></span>

<span data-ttu-id="ca544-104">Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="ca544-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca544-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca544-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="ca544-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca544-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca544-107">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca544-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca544-108">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ca544-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ca544-109">Pointeur vers l’axe arbitraire de la rotation.</span><span class="sxs-lookup"><span data-stu-id="ca544-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="ca544-110">Consultez [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="ca544-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca544-111">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca544-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca544-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca544-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca544-113">Angle de rotation autour de l’axe arbitraire, en radians.</span><span class="sxs-lookup"><span data-stu-id="ca544-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="ca544-114">Les angles sont mesurés dans le sens inverse des aiguilles d’une consiste à Rechercher l’origine dans l’axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="ca544-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca544-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca544-115">Return value</span></span>

<span data-ttu-id="ca544-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca544-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca544-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca544-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ca544-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ca544-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca544-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ca544-119">Remarks</span></span>

<span data-ttu-id="ca544-120">Cette méthode ajoute la rotation à la pile de matrice avec la matrice de rotation calculée similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="ca544-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="ca544-121">Étant donné que la rotation est multipliée à droite à la pile de matrices, la rotation est relative à l’espace de coordonnées universel.</span><span class="sxs-lookup"><span data-stu-id="ca544-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca544-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca544-122">Requirements</span></span>



| <span data-ttu-id="ca544-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca544-123">Requirement</span></span> | <span data-ttu-id="ca544-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca544-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca544-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca544-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ca544-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca544-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca544-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ca544-127">Library</span></span><br/> | <dl> <span data-ttu-id="ca544-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca544-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca544-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca544-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca544-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="ca544-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="ca544-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="ca544-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
