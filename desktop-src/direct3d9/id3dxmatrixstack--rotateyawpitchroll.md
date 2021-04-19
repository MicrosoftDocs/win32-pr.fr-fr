---
description: Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.
ms.assetid: 25a7eff4-a575-4ddb-85eb-ef3fa2d6ae3b
title: 'ID3DXMATRIXStack :: RotateYawPitchRoll, méthode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRoll
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5020cb6ff3af41b9ef32ef77bb71607f6cd5ea6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539430"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx9mathh"></a><span data-ttu-id="de872-103">ID3DXMATRIXStack :: RotateYawPitchRoll, méthode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="de872-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3dx9math.h)</span></span>

<span data-ttu-id="de872-104">Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="de872-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="de872-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de872-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="de872-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de872-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de872-107">*Lacet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="de872-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de872-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="de872-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="de872-109">Lacet autour de l’axe y en radians.</span><span class="sxs-lookup"><span data-stu-id="de872-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="de872-110">*Espacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="de872-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de872-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="de872-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="de872-112">La hauteur autour de l’axe x en radians.</span><span class="sxs-lookup"><span data-stu-id="de872-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="de872-113">*Roll* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="de872-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de872-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="de872-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="de872-115">Roulement autour de l’axe z en radians.</span><span class="sxs-lookup"><span data-stu-id="de872-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de872-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de872-116">Return value</span></span>

<span data-ttu-id="de872-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="de872-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="de872-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="de872-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="de872-119">Notes</span><span class="sxs-lookup"><span data-stu-id="de872-119">Remarks</span></span>

<span data-ttu-id="de872-120">Cette méthode ajoute la rotation à la pile de matrice avec la matrice de rotation calculée similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="de872-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="de872-121">Étant donné que la rotation est multipliée à droite à la pile de matrices, la rotation est relative à l’espace de coordonnées universel.</span><span class="sxs-lookup"><span data-stu-id="de872-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="de872-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de872-122">Requirements</span></span>



| <span data-ttu-id="de872-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de872-123">Requirement</span></span> | <span data-ttu-id="de872-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="de872-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de872-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="de872-125">Header</span></span><br/>  | <dl> <span data-ttu-id="de872-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="de872-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="de872-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="de872-127">Library</span></span><br/> | <dl> <span data-ttu-id="de872-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de872-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="de872-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de872-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de872-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="de872-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="de872-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="de872-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="de872-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="de872-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="de872-133">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="de872-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="de872-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="de872-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
