---
title: Type de texture
description: Utilisez la syntaxe suivante pour déclarer une variable de texture.
ms.assetid: 54db5432-dab8-4a4d-a4de-93c6fa640535
keywords:
- Type de texture HLSL
topic_type:
- apiref
api_name:
- Texture type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89568dc5cf24af38f916375795eea052c8b39200
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "103723985"
---
# <a name="texture-type"></a><span data-ttu-id="15ea7-104">Type de texture</span><span class="sxs-lookup"><span data-stu-id="15ea7-104">Texture type</span></span>

<span data-ttu-id="15ea7-105">Utilisez la syntaxe suivante pour déclarer une variable de texture.</span><span class="sxs-lookup"><span data-stu-id="15ea7-105">Use the following syntax to declare a texture variable.</span></span>

|                |
|----------------|
| <span data-ttu-id="15ea7-106">**Nom de type ;**</span><span class="sxs-lookup"><span data-stu-id="15ea7-106">**Type Name;**</span></span> |

## <a name="parameters"></a><span data-ttu-id="15ea7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15ea7-107">Parameters</span></span>
| <span data-ttu-id="15ea7-108">Élément</span><span class="sxs-lookup"><span data-stu-id="15ea7-108">Item</span></span>                                                                                     | <span data-ttu-id="15ea7-109">Description</span><span class="sxs-lookup"><span data-stu-id="15ea7-109">Description</span></span>                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15ea7-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Entrer**</span><span class="sxs-lookup"><span data-stu-id="15ea7-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/> | <span data-ttu-id="15ea7-111">L’un des types suivants : texture (non typée, pour la compatibilité descendante), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube.</span><span class="sxs-lookup"><span data-stu-id="15ea7-111">One of the following types: texture (untyped, for backwards compatibility), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube.</span></span> <span data-ttu-id="15ea7-112">La taille de l’élément doit être contenue dans des quantités de 4 32 bits.</span><span class="sxs-lookup"><span data-stu-id="15ea7-112">The element size must fit into 4 32-bit quantities.</span></span><br/> |
| <span data-ttu-id="15ea7-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**</span><span class="sxs-lookup"><span data-stu-id="15ea7-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/> | <span data-ttu-id="15ea7-114">Chaîne ASCII qui identifie de façon unique le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="15ea7-114">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                   |
## <a name="remarks"></a><span data-ttu-id="15ea7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="15ea7-115">Remarks</span></span>

<span data-ttu-id="15ea7-116">Il existe trois parties à l’utilisation d’une texture.</span><span class="sxs-lookup"><span data-stu-id="15ea7-116">There are three parts to using a texture.</span></span>

1.  <span data-ttu-id="15ea7-117">Déclaration d’une variable de texture.</span><span class="sxs-lookup"><span data-stu-id="15ea7-117">Declaring a texture variable.</span></span> <span data-ttu-id="15ea7-118">Cette opération s’effectue à l’aide de la syntaxe indiquée ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="15ea7-118">This is done with the syntax shown above.</span></span> <span data-ttu-id="15ea7-119">Par exemple, il s’agit de déclarations valides.</span><span class="sxs-lookup"><span data-stu-id="15ea7-119">For example, these are valid declarations.</span></span>

    ```
    texture g_MeshTexture;
    ```

    <span data-ttu-id="15ea7-120">\- ou -</span><span class="sxs-lookup"><span data-stu-id="15ea7-120">\- or -</span></span>

    ```
    Texture2D g_MeshTexture;
    ```

2.  <span data-ttu-id="15ea7-121">Déclaration et initialisation d’un objet d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="15ea7-121">Declaring and initializing a sampler object.</span></span> <span data-ttu-id="15ea7-122">Cette opération est effectuée avec une syntaxe légèrement différente dans Direct3D 9 et Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="15ea7-122">This is done with slightly different syntax in Direct3D 9 and Direct3D 10.</span></span> <span data-ttu-id="15ea7-123">Pour plus d’informations sur la syntaxe des objets d’échantillonnage, consultez [type d’échantillonneur (DirectX HLSL)](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="15ea7-123">For details about sampler object syntax, see [Sampler Type (DirectX HLSL)](dx-graphics-hlsl-sampler.md).</span></span>
3.  <span data-ttu-id="15ea7-124">Appel d’une fonction de texture dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="15ea7-124">Invoking a texture function in a shader.</span></span>

<span data-ttu-id="15ea7-125">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="15ea7-125">Differences between Direct3D 9 and Direct3D 10:</span></span>

<span data-ttu-id="15ea7-126">Direct3D 9 utilise des [fonctions de texture intrinsèques](dx-graphics-hlsl-intrinsic-functions.md) pour effectuer des opérations de texture.</span><span class="sxs-lookup"><span data-stu-id="15ea7-126">Direct3D 9 uses [intrinsic texture functions](dx-graphics-hlsl-intrinsic-functions.md) to perform texture operations.</span></span> <span data-ttu-id="15ea7-127">Cet exemple provient de l' [exemple BasicHLSL](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) et utilise [tex2D (s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) pour effectuer l’échantillonnage de texture.</span><span class="sxs-lookup"><span data-stu-id="15ea7-127">This example is from the [BasicHLSL Sample](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) and uses [tex2D(s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) to perform texture sampling.</span></span>

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

<span data-ttu-id="15ea7-128">Direct3D 10 utilise à la place des [objets de texture basés](dx-graphics-hlsl-to-type.md) sur des modèles.</span><span class="sxs-lookup"><span data-stu-id="15ea7-128">Direct3D 10 uses [templated texture objects](dx-graphics-hlsl-to-type.md) instead.</span></span> <span data-ttu-id="15ea7-129">Voici un exemple de l’opération de texture équivalente.</span><span class="sxs-lookup"><span data-stu-id="15ea7-129">Here is an example of the equivalent texture operation.</span></span>

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a><span data-ttu-id="15ea7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15ea7-130">See also</span></span>

[<span data-ttu-id="15ea7-131">Types de données (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15ea7-131">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
