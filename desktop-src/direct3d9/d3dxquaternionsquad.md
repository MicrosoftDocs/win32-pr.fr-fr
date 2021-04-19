---
description: Interpole entre les quaternions, à l’aide de l’interpolation sphérique Quadrangle.
ms.assetid: afce9afb-64cc-4059-90f5-7ed1aca9b3cb
title: D3DXQuaternionSquad, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e4fa980d551ac43f66035c1dcaa46d1c1c590a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538324"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a><span data-ttu-id="557e0-103">D3DXQuaternionSquad, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="557e0-103">D3DXQuaternionSquad function (D3dx9math.h)</span></span>

<span data-ttu-id="557e0-104">Interpole entre les quaternions, à l’aide de l’interpolation sphérique Quadrangle.</span><span class="sxs-lookup"><span data-stu-id="557e0-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="557e0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="557e0-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="557e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="557e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="557e0-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="557e0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="557e0-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="557e0-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="557e0-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="557e0-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="557e0-110">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="557e0-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="557e0-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="557e0-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="557e0-112">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="557e0-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="557e0-113">*PA* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="557e0-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="557e0-114">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="557e0-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="557e0-115">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="557e0-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="557e0-116">*PB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="557e0-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="557e0-117">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="557e0-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="557e0-118">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="557e0-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="557e0-119">*ordinateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="557e0-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="557e0-120">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="557e0-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="557e0-121">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="557e0-121">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="557e0-122">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="557e0-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="557e0-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="557e0-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="557e0-124">Paramètre qui indique la distance à interpoler entre les quaternions.</span><span class="sxs-lookup"><span data-stu-id="557e0-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="557e0-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="557e0-125">Return value</span></span>

<span data-ttu-id="557e0-126">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="557e0-126">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="557e0-127">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’interpolation sphérique Quadrangle.</span><span class="sxs-lookup"><span data-stu-id="557e0-127">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="557e0-128">Notes</span><span class="sxs-lookup"><span data-stu-id="557e0-128">Remarks</span></span>

<span data-ttu-id="557e0-129">Cette fonction utilise la séquence suivante d’opérations d’interpolation linéaire sphérique :</span><span class="sxs-lookup"><span data-stu-id="557e0-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="557e0-130">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="557e0-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="557e0-131">De cette façon, la fonction **D3DXQuaternionSquad** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="557e0-131">In this way, the **D3DXQuaternionSquad** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="557e0-132">Pour obtenir un exemple d’interpolation entre les quaternions, consultez l’exemple SkinnedMesh.</span><span class="sxs-lookup"><span data-stu-id="557e0-132">For an example of interpolating between quaternions, see the SkinnedMesh Sample.</span></span> <span data-ttu-id="557e0-133">Vous pouvez obtenir cet exemple et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="557e0-133">You can get this sample and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="557e0-134">Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="557e0-134">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="557e0-135">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="557e0-135">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="557e0-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="557e0-136">Requirements</span></span>



| <span data-ttu-id="557e0-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="557e0-137">Requirement</span></span> | <span data-ttu-id="557e0-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="557e0-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="557e0-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="557e0-139">Header</span></span><br/>  | <dl> <span data-ttu-id="557e0-140"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="557e0-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="557e0-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="557e0-141">Library</span></span><br/> | <dl> <span data-ttu-id="557e0-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="557e0-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="557e0-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="557e0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="557e0-144">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="557e0-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="557e0-145">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="557e0-145">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="557e0-146">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="557e0-146">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="557e0-147">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="557e0-147">**D3DXQuaternionSquadSetup**</span></span>](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
