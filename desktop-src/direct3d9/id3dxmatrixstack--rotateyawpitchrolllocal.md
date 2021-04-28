---
description: 'ID3DXMATRIXStack :: RotateYawPitchRollLocal, méthode (D3dx9math. h) : pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.'
ms.assetid: c69f5ea7-5d14-4187-9405-1ceff8230185
title: 'ID3DXMATRIXStack :: RotateYawPitchRollLocal, méthode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRollLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1d104676b6d346afd527552dbfba4bac23ed09cd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093447"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx9mathh"></a><span data-ttu-id="d5fdc-103">ID3DXMATRIXStack :: RotateYawPitchRollLocal, méthode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d5fdc-103">ID3DXMATRIXStack::RotateYawPitchRollLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="d5fdc-104">Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="d5fdc-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5fdc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5fdc-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRollLocal(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="d5fdc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5fdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5fdc-107">*Lacet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5fdc-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5fdc-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5fdc-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5fdc-109">Lacet autour de l’axe y en radians.</span><span class="sxs-lookup"><span data-stu-id="d5fdc-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="d5fdc-110">*Espacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5fdc-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5fdc-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5fdc-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5fdc-112">La hauteur autour de l’axe x en radians.</span><span class="sxs-lookup"><span data-stu-id="d5fdc-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="d5fdc-113">*Roll* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5fdc-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5fdc-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5fdc-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5fdc-115">Roulement autour de l’axe z en radians.</span><span class="sxs-lookup"><span data-stu-id="d5fdc-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5fdc-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d5fdc-116">Return value</span></span>

<span data-ttu-id="d5fdc-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5fdc-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5fdc-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d5fdc-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5fdc-119">Notes </span><span class="sxs-lookup"><span data-stu-id="d5fdc-119">Remarks</span></span>

<span data-ttu-id="d5fdc-120">Cette méthode ajoute la rotation à la pile de matrice avec la matrice de rotation calculée similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="d5fdc-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="d5fdc-121">Étant donné que la rotation est multipliée à gauche à la pile de matrices, la rotation est relative à l’espace de coordonnées local de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d5fdc-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5fdc-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5fdc-122">Requirements</span></span>



| <span data-ttu-id="d5fdc-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5fdc-123">Requirement</span></span> | <span data-ttu-id="d5fdc-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5fdc-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5fdc-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5fdc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d5fdc-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5fdc-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d5fdc-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d5fdc-127">Library</span></span><br/> | <dl> <span data-ttu-id="d5fdc-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5fdc-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d5fdc-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5fdc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5fdc-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="d5fdc-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d5fdc-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="d5fdc-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="d5fdc-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="d5fdc-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="d5fdc-133">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="d5fdc-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="d5fdc-134">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="d5fdc-134">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> </dl>

 

 
