---
description: Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.
ms.assetid: da023816-5176-460d-ab6b-909b89cc46cd
title: 'ID3DXMATRIXStack :: RotateYawPitchRollLocal, méthode (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a7b9e08adb7e66f78b3823c71e07fadfd561201
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762368"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx10h"></a><span data-ttu-id="6a77b-103">ID3DXMATRIXStack :: RotateYawPitchRollLocal, méthode (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="6a77b-103">ID3DXMATRIXStack::RotateYawPitchRollLocal method (D3DX10.h)</span></span>

<span data-ttu-id="6a77b-104">Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="6a77b-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a77b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a77b-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRollLocal(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="6a77b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a77b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a77b-107">*Lacet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a77b-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a77b-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a77b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a77b-109">Lacet autour de l’axe y en radians.</span><span class="sxs-lookup"><span data-stu-id="6a77b-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="6a77b-110">*Espacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a77b-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a77b-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a77b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a77b-112">La hauteur autour de l’axe x en radians.</span><span class="sxs-lookup"><span data-stu-id="6a77b-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="6a77b-113">*Roll* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a77b-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a77b-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a77b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a77b-115">Roulement autour de l’axe z en radians.</span><span class="sxs-lookup"><span data-stu-id="6a77b-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a77b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a77b-116">Return value</span></span>

<span data-ttu-id="6a77b-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a77b-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a77b-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6a77b-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a77b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="6a77b-119">Remarks</span></span>

<span data-ttu-id="6a77b-120">Cette méthode ajoute la rotation à la pile de matrice avec la matrice de rotation calculée similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="6a77b-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="6a77b-121">Étant donné que la rotation est multipliée à gauche à la pile de matrices, la rotation est relative à l’espace de coordonnées local de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6a77b-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a77b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a77b-122">Requirements</span></span>



| <span data-ttu-id="6a77b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a77b-123">Requirement</span></span> | <span data-ttu-id="6a77b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a77b-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a77b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a77b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6a77b-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a77b-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a77b-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6a77b-127">Library</span></span><br/> | <dl> <span data-ttu-id="6a77b-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a77b-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a77b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a77b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a77b-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="6a77b-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="6a77b-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="6a77b-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
