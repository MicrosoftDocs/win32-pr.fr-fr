---
title: 'TextureCube :: Sample (S, float, float, uint), fonction'
description: 'Échantillonne une texture avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération. | TextureCube :: Sample (S, float, float, uint), fonction'
ms.assetid: 8FA17583-9002-4DEC-A6D5-85B25DEA19B7
keywords:
- Exemple de fonction HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a91e9a3dcc2df617f50175eb0872398bc564103
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974254"
---
# <a name="texturecubesamplesfloatfloatuint-function"></a><span data-ttu-id="d0639-105">TextureCube :: Sample (S, float, float, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="d0639-105">TextureCube::Sample(S,float,float,uint) function</span></span>

<span data-ttu-id="d0639-106">Échantillonne une texture avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d0639-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0639-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0639-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="d0639-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0639-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0639-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="d0639-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0639-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="d0639-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="d0639-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="d0639-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="d0639-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d0639-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0639-113">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="d0639-113">The texture coordinates.</span></span> <span data-ttu-id="d0639-114">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="d0639-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d0639-115">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d0639-115">Texture-Object Type</span></span>                    | <span data-ttu-id="d0639-116">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="d0639-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="d0639-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d0639-117">Texture1D</span></span>                              | <span data-ttu-id="d0639-118">float</span><span class="sxs-lookup"><span data-stu-id="d0639-118">float</span></span>          |
| <span data-ttu-id="d0639-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="d0639-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="d0639-120">float2</span><span class="sxs-lookup"><span data-stu-id="d0639-120">float2</span></span>         |
| <span data-ttu-id="d0639-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="d0639-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="d0639-122">float3</span><span class="sxs-lookup"><span data-stu-id="d0639-122">float3</span></span>         |
| <span data-ttu-id="d0639-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d0639-123">TextureCubeArray</span></span>                       | <span data-ttu-id="d0639-124">float4</span><span class="sxs-lookup"><span data-stu-id="d0639-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="d0639-125">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d0639-125">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0639-126">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="d0639-126">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="d0639-127">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="d0639-127">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="d0639-128">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d0639-128">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0639-129">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d0639-129">The status of the operation.</span></span> <span data-ttu-id="d0639-130">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="d0639-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="d0639-131">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="d0639-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="d0639-132">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="d0639-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0639-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0639-133">Return value</span></span>

<span data-ttu-id="d0639-134">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="d0639-134">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="d0639-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0639-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0639-136">Exemples de méthodes</span><span class="sxs-lookup"><span data-stu-id="d0639-136">Sample methods</span></span>](texturecube-sample.md)
</dt> <dt>

[<span data-ttu-id="d0639-137">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="d0639-137">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
