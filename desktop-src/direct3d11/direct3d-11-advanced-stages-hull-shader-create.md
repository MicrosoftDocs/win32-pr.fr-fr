---
title: Comment créer un nuanceur de coque
description: Cette rubrique montre comment créer un nuanceur de coque.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a1eea7d2e6e70377028976f9576790ce3b64ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671654"
---
# <a name="how-to-create-a-hull-shader"></a><span data-ttu-id="06b82-103">Comment : créer un nuanceur de coque</span><span class="sxs-lookup"><span data-stu-id="06b82-103">How To: Create a Hull Shader</span></span>

<span data-ttu-id="06b82-104">Un nuanceur de coque est le premier des trois étapes qui fonctionnent ensemble pour implémenter le [pavage](direct3d-11-advanced-stages-tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="06b82-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="06b82-105">Les sorties de nuanceur de coque désignent l’étape du paveur, ainsi que l’étape de nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="06b82-105">The hull-shader outputs drive the tessellator stage, as well as the domain-shader stage.</span></span> <span data-ttu-id="06b82-106">Cette rubrique montre comment créer un nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="06b82-106">This topic shows how to create a hull shader.</span></span>

<span data-ttu-id="06b82-107">Un nuanceur de coque transforme un ensemble de points de contrôle d’entrée (à partir d’un nuanceur de sommets) en un ensemble de points de contrôle de sortie.</span><span class="sxs-lookup"><span data-stu-id="06b82-107">A hull shader transforms a set of input control points (from a vertex shader) into a set of output control points.</span></span> <span data-ttu-id="06b82-108">Le nombre de points d’entrée et de sortie peut varier en fonction du contenu et du nombre selon la transformation (une transformation classique est une transformation de base).</span><span class="sxs-lookup"><span data-stu-id="06b82-108">The number of input and output points can vary in contents and number depending on the transform (a typical transformation would be a basis transformation).</span></span>

<span data-ttu-id="06b82-109">Un nuanceur de coque génère également des informations sur les constantes correctifs, telles que les facteurs de pavage, pour un nuanceur de domaine et le du paveur.</span><span class="sxs-lookup"><span data-stu-id="06b82-109">A hull shader also outputs patch constant information, such as tessellation factors, for a domain shader and the tessellator.</span></span> <span data-ttu-id="06b82-110">L’étape du paveur de la fonction fixe utilise les facteurs de pavage ainsi que les autres États déclarés dans un nuanceur de coque pour déterminer la quantité à paver.</span><span class="sxs-lookup"><span data-stu-id="06b82-110">The fixed-function tessellator stage uses the tessellation factors as well as other state declared in a hull shader to determine how much to tessellate.</span></span>

<span data-ttu-id="06b82-111">**Pour créer un nuanceur de coque**</span><span class="sxs-lookup"><span data-stu-id="06b82-111">**To create a hull shader**</span></span>

1.  <span data-ttu-id="06b82-112">Concevoir un nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="06b82-112">Design a hull shader.</span></span> <span data-ttu-id="06b82-113">Consultez [Comment : concevoir un nuanceur de coque](direct3d-11-advanced-stages-hull-shader-design.md).</span><span class="sxs-lookup"><span data-stu-id="06b82-113">See [How To: Design a Hull Shader](direct3d-11-advanced-stages-hull-shader-design.md).</span></span>
2.  <span data-ttu-id="06b82-114">Compiler le code du nuanceur</span><span class="sxs-lookup"><span data-stu-id="06b82-114">Compile the shader code</span></span>
3.  <span data-ttu-id="06b82-115">Créez un objet de nuanceur de coque à l’aide de [**ID3D11Device :: CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).</span><span class="sxs-lookup"><span data-stu-id="06b82-115">Create a hull-shader object using [**ID3D11Device::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).</span></span>
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  <span data-ttu-id="06b82-116">Initialisez l’étape de pipeline à l’aide de [**ID3D11DeviceContext :: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span><span class="sxs-lookup"><span data-stu-id="06b82-116">Initialize the pipeline stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="06b82-117">Un nuanceur de domaine doit être lié au pipeline si un nuanceur de coque est lié.</span><span class="sxs-lookup"><span data-stu-id="06b82-117">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="06b82-118">En particulier, il n’est pas valide de diffuser directement en continu des points de contrôle de nuanceur de coque avec le nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="06b82-118">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06b82-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="06b82-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06b82-120">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="06b82-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="06b82-121">Vue d’ensemble de la polygonalisation</span><span class="sxs-lookup"><span data-stu-id="06b82-121">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




