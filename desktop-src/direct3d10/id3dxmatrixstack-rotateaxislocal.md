---
description: 'ID3DXMATRIXStack :: RotateAxisLocal, méthode (D3DX10. h) : pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.'
ms.assetid: 90837762-9bfe-4065-94b3-1ca61184a78e
title: 'ID3DXMATRIXStack :: RotateAxisLocal, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a81a4c4bd9a2f738274f98ce925799b34986fbb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107877"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx10h"></a><span data-ttu-id="1174b-103">ID3DXMATRIXStack :: RotateAxisLocal, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="1174b-103">ID3DXMATRIXStack::RotateAxisLocal method (D3DX10.h)</span></span>

<span data-ttu-id="1174b-104">Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="1174b-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="1174b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1174b-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="1174b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1174b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1174b-107">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1174b-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1174b-108">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1174b-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1174b-109">Pointeur vers l’axe arbitraire de la rotation.</span><span class="sxs-lookup"><span data-stu-id="1174b-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="1174b-110">Consultez [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="1174b-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="1174b-111">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1174b-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1174b-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1174b-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1174b-113">Angle de rotation autour de l’axe arbitraire, en radians.</span><span class="sxs-lookup"><span data-stu-id="1174b-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="1174b-114">Les angles sont mesurés dans le sens inverse des aiguilles d’une consiste à Rechercher l’origine dans l’axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="1174b-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1174b-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1174b-115">Return value</span></span>

<span data-ttu-id="1174b-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1174b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1174b-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1174b-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1174b-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1174b-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1174b-119">Notes </span><span class="sxs-lookup"><span data-stu-id="1174b-119">Remarks</span></span>

<span data-ttu-id="1174b-120">Cette méthode ajoute la rotation à la pile de matrice avec la matrice de rotation calculée similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="1174b-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="1174b-121">Étant donné que la rotation est multipliée à gauche à la pile de matrices, la rotation est relative à l’espace de coordonnées local de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1174b-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="1174b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1174b-122">Requirements</span></span>



| <span data-ttu-id="1174b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1174b-123">Requirement</span></span> | <span data-ttu-id="1174b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1174b-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1174b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="1174b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1174b-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1174b-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1174b-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1174b-127">Library</span></span><br/> | <dl> <span data-ttu-id="1174b-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1174b-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1174b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1174b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1174b-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="1174b-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="1174b-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="1174b-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
