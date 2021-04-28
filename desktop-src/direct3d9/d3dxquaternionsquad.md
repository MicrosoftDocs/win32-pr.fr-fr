---
description: 'Fonction D3DXQuaternionSquad (D3dx9math. h) : interpole entre les quaternions, à l’aide de l’interpolation Quadrangle sphérique.'
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
ms.openlocfilehash: c7bef8671b38ec2e8208a6de0ec7542cf28ffa44
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117987"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a><span data-ttu-id="0a209-103">D3DXQuaternionSquad, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0a209-103">D3DXQuaternionSquad function (D3dx9math.h)</span></span>

<span data-ttu-id="0a209-104">Interpole entre les quaternions, à l’aide de l’interpolation sphérique Quadrangle.</span><span class="sxs-lookup"><span data-stu-id="0a209-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a209-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a209-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0a209-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a209-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a209-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0a209-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a209-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a209-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0a209-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0a209-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0a209-110">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a209-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a209-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0a209-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0a209-112">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="0a209-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0a209-113">*PA* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a209-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a209-114">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0a209-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0a209-115">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="0a209-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0a209-116">*PB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a209-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a209-117">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0a209-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0a209-118">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="0a209-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0a209-119">*ordinateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a209-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a209-120">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0a209-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0a209-121">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="0a209-121">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0a209-122">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a209-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a209-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a209-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a209-124">Paramètre qui indique la distance à interpoler entre les quaternions.</span><span class="sxs-lookup"><span data-stu-id="0a209-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a209-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0a209-125">Return value</span></span>

<span data-ttu-id="0a209-126">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a209-126">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0a209-127">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’interpolation sphérique Quadrangle.</span><span class="sxs-lookup"><span data-stu-id="0a209-127">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a209-128">Notes </span><span class="sxs-lookup"><span data-stu-id="0a209-128">Remarks</span></span>

<span data-ttu-id="0a209-129">Cette fonction utilise la séquence suivante d’opérations d’interpolation linéaire sphérique :</span><span class="sxs-lookup"><span data-stu-id="0a209-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="0a209-130">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="0a209-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0a209-131">De cette façon, la fonction **D3DXQuaternionSquad** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="0a209-131">In this way, the **D3DXQuaternionSquad** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0a209-132">Pour obtenir un exemple d’interpolation entre les quaternions, consultez l’exemple SkinnedMesh.</span><span class="sxs-lookup"><span data-stu-id="0a209-132">For an example of interpolating between quaternions, see the SkinnedMesh Sample.</span></span> <span data-ttu-id="0a209-133">Vous pouvez obtenir cet exemple et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="0a209-133">You can get this sample and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="0a209-134">Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="0a209-134">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="0a209-135">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="0a209-135">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a209-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a209-136">Requirements</span></span>



| <span data-ttu-id="0a209-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a209-137">Requirement</span></span> | <span data-ttu-id="0a209-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a209-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a209-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a209-139">Header</span></span><br/>  | <dl> <span data-ttu-id="0a209-140"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a209-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0a209-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0a209-141">Library</span></span><br/> | <dl> <span data-ttu-id="0a209-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a209-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0a209-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a209-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a209-144">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="0a209-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0a209-145">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="0a209-145">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="0a209-146">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="0a209-146">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="0a209-147">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="0a209-147">**D3DXQuaternionSquadSetup**</span></span>](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
