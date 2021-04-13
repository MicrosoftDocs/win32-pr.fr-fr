---
description: Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.
ms.assetid: 35e237f6-40f2-4001-adb0-f489d61f64e7
title: 'ID3DXMATRIXStack :: RotateYawPitchRoll, méthode (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8d57af31e9944c718419a3a90863c9960d0bdb36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323374"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx10h"></a><span data-ttu-id="ed64b-103">ID3DXMATRIXStack :: RotateYawPitchRoll, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="ed64b-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3DX10.h)</span></span>

<span data-ttu-id="ed64b-104">Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="ed64b-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed64b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed64b-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="ed64b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed64b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed64b-107">*Lacet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed64b-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed64b-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed64b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed64b-109">Lacet autour de l’axe y en radians.</span><span class="sxs-lookup"><span data-stu-id="ed64b-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="ed64b-110">*Espacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed64b-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed64b-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed64b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed64b-112">La hauteur autour de l’axe x en radians.</span><span class="sxs-lookup"><span data-stu-id="ed64b-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="ed64b-113">*Roll* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed64b-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed64b-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed64b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed64b-115">Roulement autour de l’axe z en radians.</span><span class="sxs-lookup"><span data-stu-id="ed64b-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed64b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed64b-116">Return value</span></span>

<span data-ttu-id="ed64b-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed64b-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed64b-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed64b-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed64b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ed64b-119">Remarks</span></span>

<span data-ttu-id="ed64b-120">Cette méthode ajoute la rotation à la pile de matrice avec la matrice de rotation calculée similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="ed64b-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="ed64b-121">Étant donné que la rotation est multipliée à droite à la pile de matrices, la rotation est relative à l’espace de coordonnées universel.</span><span class="sxs-lookup"><span data-stu-id="ed64b-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed64b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed64b-122">Requirements</span></span>



| <span data-ttu-id="ed64b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed64b-123">Requirement</span></span> | <span data-ttu-id="ed64b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed64b-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed64b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed64b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ed64b-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed64b-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed64b-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ed64b-127">Library</span></span><br/> | <dl> <span data-ttu-id="ed64b-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed64b-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed64b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed64b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed64b-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="ed64b-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="ed64b-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="ed64b-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
