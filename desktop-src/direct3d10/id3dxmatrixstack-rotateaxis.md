---
description: 'ID3DXMATRIXStack :: RotateAxis, méthode (D3DX10. h) : pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.'
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
ms.openlocfilehash: 0a2e52eed1c1957de9a0fcfed4ba3d3d05f89cb9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107908"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx10h"></a><span data-ttu-id="d1208-103">ID3DXMATRIXStack :: RotateAxis, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="d1208-103">ID3DXMATRIXStack::RotateAxis method (D3DX10.h)</span></span>

<span data-ttu-id="d1208-104">Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="d1208-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1208-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1208-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="d1208-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1208-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1208-107">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d1208-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1208-108">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d1208-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d1208-109">Pointeur vers l’axe arbitraire de la rotation.</span><span class="sxs-lookup"><span data-stu-id="d1208-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="d1208-110">Consultez [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="d1208-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1208-111">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d1208-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1208-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1208-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1208-113">Angle de rotation autour de l’axe arbitraire, en radians.</span><span class="sxs-lookup"><span data-stu-id="d1208-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="d1208-114">Les angles sont mesurés dans le sens inverse des aiguilles d’une consiste à Rechercher l’origine dans l’axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="d1208-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1208-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d1208-115">Return value</span></span>

<span data-ttu-id="d1208-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1208-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1208-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d1208-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d1208-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d1208-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1208-119">Notes </span><span class="sxs-lookup"><span data-stu-id="d1208-119">Remarks</span></span>

<span data-ttu-id="d1208-120">Cette méthode ajoute la rotation à la pile de matrice avec la matrice de rotation calculée similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="d1208-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="d1208-121">Étant donné que la rotation est multipliée à droite à la pile de matrices, la rotation est relative à l’espace de coordonnées universel.</span><span class="sxs-lookup"><span data-stu-id="d1208-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1208-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1208-122">Requirements</span></span>



| <span data-ttu-id="d1208-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1208-123">Requirement</span></span> | <span data-ttu-id="d1208-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1208-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1208-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1208-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d1208-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1208-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1208-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1208-127">Library</span></span><br/> | <dl> <span data-ttu-id="d1208-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1208-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1208-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1208-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1208-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="d1208-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d1208-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d1208-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
