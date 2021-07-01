---
title: CalculateLevelOfDetail (objet texture HLSL DirectX)
description: Calcule le niveau de détail.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e307527f93c153f0f78ce58b4d70ead4f7c1bc4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120554"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a><span data-ttu-id="9d7ef-103">CalculateLevelOfDetail (objet texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="9d7ef-103">CalculateLevelOfDetail (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="9d7ef-104">Calcule le niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="9d7ef-104">Calculates the level of detail.</span></span>

<span data-ttu-id="9d7ef-105">RET Object. CalculateLevelOfDetail (état de l’échantillonneur \_ S, float x);</span><span class="sxs-lookup"><span data-stu-id="9d7ef-105">ret Object.CalculateLevelOfDetail( sampler\_state S, float x );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="9d7ef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d7ef-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d7ef-107">Élément</span><span class="sxs-lookup"><span data-stu-id="9d7ef-107">Item</span></span></th>
<th><span data-ttu-id="9d7ef-108">Description</span><span class="sxs-lookup"><span data-stu-id="9d7ef-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d7ef-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Dessin</em></span><span class="sxs-lookup"><span data-stu-id="9d7ef-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="9d7ef-110">Tout type d' <a href="dx-graphics-hlsl-to-type.md">objet texture</a> (sauf Texture2DMS et Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="9d7ef-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d7ef-111"><span id="S"></span><span id="s"></span><em>X</em></span><span class="sxs-lookup"><span data-stu-id="9d7ef-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="9d7ef-112">dans État de l' <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">échantillonneur</a>.</span><span class="sxs-lookup"><span data-stu-id="9d7ef-112">[in] A <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Sampler state</a>.</span></span> <span data-ttu-id="9d7ef-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="9d7ef-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d7ef-114"><span id="x"></span><span id="X"></span><em>x</em></span><span class="sxs-lookup"><span data-stu-id="9d7ef-114"><span id="x"></span><span id="X"></span><em>x</em></span></span><br/></td>
<td><span data-ttu-id="9d7ef-115">dans Valeur ou valeurs d’interpolation linéaire, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus.</span><span class="sxs-lookup"><span data-stu-id="9d7ef-115">[in] The linear interpolation value or values, which is a floating-point number between 0.0 and 1.0 inclusive.</span></span> <span data-ttu-id="9d7ef-116">Le nombre de composants dépend du type d’objet texture.</span><span class="sxs-lookup"><span data-stu-id="9d7ef-116">The number of components is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d7ef-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="9d7ef-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="9d7ef-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="9d7ef-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d7ef-119">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="9d7ef-119">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="9d7ef-120">float1</span><span class="sxs-lookup"><span data-stu-id="9d7ef-120">float1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d7ef-121">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="9d7ef-121">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="9d7ef-122">float2</span><span class="sxs-lookup"><span data-stu-id="9d7ef-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d7ef-123">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="9d7ef-123">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="9d7ef-124">float3</span><span class="sxs-lookup"><span data-stu-id="9d7ef-124">float3</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="9d7ef-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9d7ef-125">Return Value</span></span>

<span data-ttu-id="9d7ef-126">Retourne le LOD calculé, une valeur à virgule flottante unique.</span><span class="sxs-lookup"><span data-stu-id="9d7ef-126">Returns the calculated LOD, a single floating-point value.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="9d7ef-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9d7ef-127">Minimum Shader Model</span></span>

<span data-ttu-id="9d7ef-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="9d7ef-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9d7ef-129">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9d7ef-129">vs\_4\_0</span></span> | <span data-ttu-id="9d7ef-130">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9d7ef-130">vs\_4\_1</span></span>  | <span data-ttu-id="9d7ef-131">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9d7ef-131">ps\_4\_0</span></span> | <span data-ttu-id="9d7ef-132">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9d7ef-132">ps\_4\_1</span></span>  | <span data-ttu-id="9d7ef-133">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9d7ef-133">gs\_4\_0</span></span> | <span data-ttu-id="9d7ef-134">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9d7ef-134">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | <span data-ttu-id="9d7ef-135">x</span><span class="sxs-lookup"><span data-stu-id="9d7ef-135">x</span></span>         |          |           |



 

1.  <span data-ttu-id="9d7ef-136">TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9d7ef-136">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="9d7ef-137">Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9d7ef-137">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d7ef-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d7ef-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d7ef-139">Texture-objet</span><span class="sxs-lookup"><span data-stu-id="9d7ef-139">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

