---
description: Retourne le nom du profil HLSL (High-Level Shader Language) le plus élevé pris en charge par un appareil donné.
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: D3DXGetPixelShaderProfile, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ad1f430a95b1ff2173dceb1e0561dccf3d0ee88d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953848"
---
# <a name="d3dxgetpixelshaderprofile-function"></a><span data-ttu-id="0cf0f-103">D3DXGetPixelShaderProfile fonction)</span><span class="sxs-lookup"><span data-stu-id="0cf0f-103">D3DXGetPixelShaderProfile function</span></span>

<span data-ttu-id="0cf0f-104">Retourne le nom du profil HLSL (High-Level Shader Language) le plus élevé pris en charge par un appareil donné.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf0f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cf0f-105">Syntax</span></span>


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="0cf0f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cf0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cf0f-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0cf0f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf0f-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0cf0f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0cf0f-109">Pointeur vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-109">Pointer to the device.</span></span> <span data-ttu-id="0cf0f-110">Consultez [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="0cf0f-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cf0f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0cf0f-111">Return value</span></span>

<span data-ttu-id="0cf0f-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cf0f-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cf0f-113">Nom du profil HLSL.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-113">The HLSL profile name.</span></span>

<span data-ttu-id="0cf0f-114">Si l’appareil ne prend pas en charge les nuanceurs de pixels, la fonction retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-114">If the device does not support pixel shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cf0f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0cf0f-115">Remarks</span></span>

<span data-ttu-id="0cf0f-116">Un profil de nuanceur spécifie la version du nuanceur d’assembly à utiliser et les fonctionnalités disponibles pour le compilateur HLSL lors de la compilation d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="0cf0f-117">Le tableau suivant répertorie les profils de nuanceur de pixels pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-117">The following table lists the pixel shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0cf0f-118">Profil de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0cf0f-118">Shader Profile</span></span></th>
<th><span data-ttu-id="0cf0f-119">Description</span><span class="sxs-lookup"><span data-stu-id="0cf0f-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0cf0f-120">ps_1_1</span><span class="sxs-lookup"><span data-stu-id="0cf0f-120">ps_1_1</span></span></td>
<td><span data-ttu-id="0cf0f-121">Compilez sur ps_1_1 version.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-121">Compile to ps_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0cf0f-122">ps_1_2</span><span class="sxs-lookup"><span data-stu-id="0cf0f-122">ps_1_2</span></span></td>
<td><span data-ttu-id="0cf0f-123">Compilez sur ps_1_2 version.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-123">Compile to ps_1_2 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0cf0f-124">ps_1_3</span><span class="sxs-lookup"><span data-stu-id="0cf0f-124">ps_1_3</span></span></td>
<td><span data-ttu-id="0cf0f-125">Compilez sur ps_1_3 version.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-125">Compile to ps_1_3 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0cf0f-126">ps_1_4</span><span class="sxs-lookup"><span data-stu-id="0cf0f-126">ps_1_4</span></span></td>
<td><span data-ttu-id="0cf0f-127">Compilez sur ps_1_4 version.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-127">Compile to ps_1_4 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0cf0f-128">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="0cf0f-128">ps_2_0</span></span></td>
<td><span data-ttu-id="0cf0f-129">Compilez sur ps_2_0 version.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-129">Compile to ps_2_0 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0cf0f-130">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="0cf0f-130">ps_2_a</span></span></td>
<td><span data-ttu-id="0cf0f-131">Identique au profil de ps_2_0, avec les fonctionnalités supplémentaires suivantes disponibles pour que le compilateur cible :</span><span class="sxs-lookup"><span data-stu-id="0cf0f-131">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="0cf0f-132">Le nombre de registres temporaires (r #) est supérieur ou égal à 22.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-132">Number of Temporary Registers (r#) is greater than or equal to 22.</span></span></li>
<li><span data-ttu-id="0cf0f-133">Swizzle source arbitraire.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-133">Arbitrary source swizzle.</span></span></li>
<li><span data-ttu-id="0cf0f-134">Instructions de dégradé : DSX, DSY.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-134">Gradient instructions: dsx, dsy.</span></span></li>
<li><span data-ttu-id="0cf0f-135">Prédication.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-135">Predication.</span></span></li>
<li><span data-ttu-id="0cf0f-136">Aucune limite de lecture de texture dépendante.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-136">No dependent texture read limit.</span></span></li>
<li><span data-ttu-id="0cf0f-137">Aucune limite pour le nombre d’instructions de texture.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-137">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0cf0f-138">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="0cf0f-138">ps_2_b</span></span></td>
<td><span data-ttu-id="0cf0f-139">Identique au profil de ps_2_0, avec les fonctionnalités supplémentaires suivantes disponibles pour que le compilateur cible :</span><span class="sxs-lookup"><span data-stu-id="0cf0f-139">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="0cf0f-140">Le nombre de registres temporaires (r #) est supérieur ou égal à 32.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-140">Number of Temporary Registers (r#) is greater than or equal to 32.</span></span></li>
<li><span data-ttu-id="0cf0f-141">Aucune limite pour le nombre d’instructions de texture.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-141">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0cf0f-142">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="0cf0f-142">ps_3_0</span></span></td>
<td><span data-ttu-id="0cf0f-143">Compilez sur ps_3_0 version.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-143">Compile to ps_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0cf0f-144">Pour plus d’informations sur les différences entre les versions de nuanceur, consultez [différences de nuanceur de pixels](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0cf0f-144">For more information about the differences between shader versions, see [Pixel Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cf0f-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cf0f-145">Requirements</span></span>



| <span data-ttu-id="0cf0f-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cf0f-146">Requirement</span></span> | <span data-ttu-id="0cf0f-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cf0f-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf0f-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="0cf0f-148">Header</span></span><br/>  | <dl> <span data-ttu-id="0cf0f-149"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cf0f-149"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0cf0f-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0cf0f-150">Library</span></span><br/> | <dl> <span data-ttu-id="0cf0f-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cf0f-151"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0cf0f-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cf0f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf0f-153">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0cf0f-153">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
