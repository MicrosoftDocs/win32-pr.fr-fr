---
description: 'ID3DXMATRIXStack :: RotateAxisLocal, méthode (D3dx9math. h) : pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.'
ms.assetid: c7ef11e9-f4c4-4801-8f25-190066baeb52
title: 'ID3DXMATRIXStack :: RotateAxisLocal, méthode (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0bfcfd7301f90dcf49b03e7bbb3fd7e3b0de6c3e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093467"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a><span data-ttu-id="bab78-103">ID3DXMATRIXStack :: RotateAxisLocal, méthode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="bab78-103">ID3DXMATRIXStack::RotateAxisLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="bab78-104">Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="bab78-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab78-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bab78-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="bab78-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bab78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab78-107">*PV* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bab78-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab78-108">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bab78-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bab78-109">Pointeur vers l’axe arbitraire de la rotation.</span><span class="sxs-lookup"><span data-stu-id="bab78-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="bab78-110">Consultez [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="bab78-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab78-111">*Angle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bab78-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab78-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bab78-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bab78-113">Angle de rotation autour de l’axe arbitraire, en radians.</span><span class="sxs-lookup"><span data-stu-id="bab78-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="bab78-114">Les angles sont mesurés dans le sens inverse des aiguilles d’une consiste à Rechercher l’origine dans l’axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="bab78-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bab78-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bab78-115">Return value</span></span>

<span data-ttu-id="bab78-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bab78-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bab78-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bab78-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bab78-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bab78-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bab78-119">Notes </span><span class="sxs-lookup"><span data-stu-id="bab78-119">Remarks</span></span>

<span data-ttu-id="bab78-120">Cette méthode ajoute la rotation à la pile de matrice avec la matrice de rotation calculée similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="bab78-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="bab78-121">Étant donné que la rotation est multipliée à gauche à la pile de matrices, la rotation est relative à l’espace de coordonnées local de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bab78-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="bab78-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bab78-122">Requirements</span></span>



| <span data-ttu-id="bab78-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bab78-123">Requirement</span></span> | <span data-ttu-id="bab78-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="bab78-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bab78-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="bab78-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bab78-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bab78-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bab78-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bab78-127">Library</span></span><br/> | <dl> <span data-ttu-id="bab78-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bab78-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bab78-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bab78-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab78-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="bab78-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="bab78-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="bab78-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="bab78-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="bab78-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="bab78-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="bab78-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="bab78-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="bab78-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
