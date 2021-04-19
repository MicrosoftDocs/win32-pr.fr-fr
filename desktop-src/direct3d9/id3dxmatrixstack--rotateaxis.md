---
description: Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.
ms.assetid: b7ae5195-a2af-429f-9a0d-51cd7e955362
title: 'ID3DXMATRIXStack :: RotateAxis, méthode (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 476b8e01da6265e9bdf4642d24647d0e804949d6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523809"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx9mathh"></a><span data-ttu-id="56f69-103">ID3DXMATRIXStack :: RotateAxis, méthode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="56f69-103">ID3DXMATRIXStack::RotateAxis method (D3dx9math.h)</span></span>

<span data-ttu-id="56f69-104">Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="56f69-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="56f69-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56f69-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="56f69-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56f69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56f69-107">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56f69-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56f69-108">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="56f69-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="56f69-109">Pointeur vers l’axe arbitraire de la rotation.</span><span class="sxs-lookup"><span data-stu-id="56f69-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="56f69-110">Consultez [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="56f69-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f69-111">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56f69-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56f69-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56f69-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="56f69-113">Angle de rotation autour de l’axe arbitraire, en radians.</span><span class="sxs-lookup"><span data-stu-id="56f69-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="56f69-114">Les angles sont mesurés dans le sens inverse des aiguilles d’une consiste à Rechercher l’origine dans l’axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="56f69-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56f69-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56f69-115">Return value</span></span>

<span data-ttu-id="56f69-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="56f69-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="56f69-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="56f69-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="56f69-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="56f69-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="56f69-119">Notes</span><span class="sxs-lookup"><span data-stu-id="56f69-119">Remarks</span></span>

<span data-ttu-id="56f69-120">Cette méthode ajoute la rotation à la pile de matrice avec la matrice de rotation calculée similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="56f69-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="56f69-121">Étant donné que la rotation est multipliée à droite à la pile de matrices, la rotation est relative à l’espace de coordonnées universel.</span><span class="sxs-lookup"><span data-stu-id="56f69-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="56f69-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56f69-122">Requirements</span></span>



| <span data-ttu-id="56f69-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56f69-123">Requirement</span></span> | <span data-ttu-id="56f69-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="56f69-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56f69-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="56f69-125">Header</span></span><br/>  | <dl> <span data-ttu-id="56f69-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="56f69-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="56f69-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="56f69-127">Library</span></span><br/> | <dl> <span data-ttu-id="56f69-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56f69-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="56f69-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56f69-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56f69-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="56f69-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="56f69-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="56f69-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="56f69-132">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="56f69-132">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="56f69-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="56f69-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="56f69-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="56f69-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
