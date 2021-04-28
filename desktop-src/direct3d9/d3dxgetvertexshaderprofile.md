---
description: D3DXGetVertexShaderProfile fonction-retourne le nom du profil HLSL (High-Level Shader Language) le plus élevé pris en charge par un appareil donné.
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: D3DXGetVertexShaderProfile, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70d6cdf79fdd91e819d54702682515aa3e4810b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114457"
---
# <a name="d3dxgetvertexshaderprofile-function"></a><span data-ttu-id="d980e-103">D3DXGetVertexShaderProfile fonction)</span><span class="sxs-lookup"><span data-stu-id="d980e-103">D3DXGetVertexShaderProfile function</span></span>

<span data-ttu-id="d980e-104">Retourne le nom du profil HLSL (High-Level Shader Language) le plus élevé pris en charge par un appareil donné.</span><span class="sxs-lookup"><span data-stu-id="d980e-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d980e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d980e-105">Syntax</span></span>


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="d980e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d980e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d980e-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d980e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d980e-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d980e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d980e-109">Pointeur vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d980e-109">Pointer to the device.</span></span> <span data-ttu-id="d980e-110">Consultez [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="d980e-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d980e-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d980e-111">Return value</span></span>

<span data-ttu-id="d980e-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d980e-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d980e-113">Nom du profil HLSL.</span><span class="sxs-lookup"><span data-stu-id="d980e-113">The HLSL profile name.</span></span>

<span data-ttu-id="d980e-114">Si l’appareil ne prend pas en charge les nuanceurs vertex, la fonction retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d980e-114">If the device does not support vertex shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d980e-115">Notes </span><span class="sxs-lookup"><span data-stu-id="d980e-115">Remarks</span></span>

<span data-ttu-id="d980e-116">Un profil de nuanceur spécifie la version du nuanceur d’assembly à utiliser et les fonctionnalités disponibles pour le compilateur HLSL lors de la compilation d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="d980e-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="d980e-117">Le tableau suivant répertorie les profils de nuanceur de sommets pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d980e-117">The following table lists the vertex shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d980e-118">Profil de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d980e-118">Shader Profile</span></span></th>
<th><span data-ttu-id="d980e-119">Description</span><span class="sxs-lookup"><span data-stu-id="d980e-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d980e-120">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="d980e-120">vs_1_1</span></span></td>
<td><span data-ttu-id="d980e-121">Compilez sur vs_1_1 version.</span><span class="sxs-lookup"><span data-stu-id="d980e-121">Compile to vs_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d980e-122">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="d980e-122">vs_2_0</span></span></td>
<td><span data-ttu-id="d980e-123">Compilez sur vs_2_0 version.</span><span class="sxs-lookup"><span data-stu-id="d980e-123">Compile to vs_2_0 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d980e-124">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="d980e-124">vs_2_a</span></span></td>
<td><span data-ttu-id="d980e-125">Identique au profil de vs_2_0, avec les fonctionnalités supplémentaires suivantes disponibles pour que le compilateur cible :</span><span class="sxs-lookup"><span data-stu-id="d980e-125">Same as the vs_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="d980e-126">Le nombre de registres temporaires (r #) est supérieur ou égal à 13.</span><span class="sxs-lookup"><span data-stu-id="d980e-126">Number of Temporary Registers (r#) is greater than or equal to 13.</span></span></li>
<li><span data-ttu-id="d980e-127">Instruction de contrôle de Flow dynamique.</span><span class="sxs-lookup"><span data-stu-id="d980e-127">Dynamic flow control instruction.</span></span></li>
<li><span data-ttu-id="d980e-128">Prédication.</span><span class="sxs-lookup"><span data-stu-id="d980e-128">Predication.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d980e-129">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="d980e-129">vs_3_0</span></span></td>
<td><span data-ttu-id="d980e-130">Compilez sur vs_3_0 version.</span><span class="sxs-lookup"><span data-stu-id="d980e-130">Compile to vs_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d980e-131">Pour plus d’informations sur les différences entre les versions de nuanceur, consultez [différences de nuanceur de sommets](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d980e-131">For more information about the differences between shader versions, see [Vertex Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d980e-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d980e-132">Requirements</span></span>



| <span data-ttu-id="d980e-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d980e-133">Requirement</span></span> | <span data-ttu-id="d980e-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="d980e-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d980e-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="d980e-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d980e-136"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d980e-136"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d980e-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d980e-137">Library</span></span><br/> | <dl> <span data-ttu-id="d980e-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d980e-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d980e-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d980e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d980e-140">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d980e-140">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
