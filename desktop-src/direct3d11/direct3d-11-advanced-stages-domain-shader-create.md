---
title: Comment créer un nuanceur de domaine
description: Cette rubrique montre comment créer un nuanceur de domaine.
ms.assetid: 7d02fee4-2d7c-434b-86ab-e5ee615ae93b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89b7f3d7ec6cf801432a5745520fcbd924d139
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028735"
---
# <a name="how-to-create-a-domain-shader"></a><span data-ttu-id="b7dbd-103">Comment : créer un nuanceur de domaine</span><span class="sxs-lookup"><span data-stu-id="b7dbd-103">How To: Create a Domain Shader</span></span>

<span data-ttu-id="b7dbd-104">Un nuanceur de domaine est le troisième des trois étapes qui fonctionnent ensemble pour implémenter le [pavage](direct3d-11-advanced-stages-tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="b7dbd-104">A domain shader is the third of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="b7dbd-105">Les entrées de l’étape de nuanceur de domaine proviennent d’un nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="b7dbd-105">The inputs for the domain-shader stage come from a hull shader.</span></span> <span data-ttu-id="b7dbd-106">Cette rubrique montre comment créer un nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="b7dbd-106">This topic shows how to create a domain shader.</span></span>

<span data-ttu-id="b7dbd-107">Un nuanceur de domaine transforme la géométrie de surface (créée par l’étape du paveur de la fonction fixe) à l’aide des points de contrôle de sortie de nuanceur de coque, des données de correction de sortie de nuanceur de coque et un ensemble unique de coordonnées UV du paveur.</span><span class="sxs-lookup"><span data-stu-id="b7dbd-107">A domain shader transforms surface geometry (created by the fixed-function tessellator stage) using hull shader output-control points, hull shader output patch-constant data, and a single set of tessellator uv coordinates.</span></span>

<span data-ttu-id="b7dbd-108">**Pour créer un nuanceur de domaine**</span><span class="sxs-lookup"><span data-stu-id="b7dbd-108">**To create a domain shader**</span></span>

1.  <span data-ttu-id="b7dbd-109">Concevoir un nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="b7dbd-109">Design a domain shader.</span></span> <span data-ttu-id="b7dbd-110">Consultez [Comment : concevoir un nuanceur de domaine](direct3d-11-advanced-stages-domain-shader-design.md).</span><span class="sxs-lookup"><span data-stu-id="b7dbd-110">See [How To: Design a Domain Shader](direct3d-11-advanced-stages-domain-shader-design.md).</span></span>
2.  <span data-ttu-id="b7dbd-111">Compilez le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="b7dbd-111">Compile the shader code.</span></span>
3.  <span data-ttu-id="b7dbd-112">Créez un objet de nuanceur de domaine à l’aide de [**ID3D11Device :: CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span><span class="sxs-lookup"><span data-stu-id="b7dbd-112">Create a domain-shader object using [**ID3D11Device::CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span></span>
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  <span data-ttu-id="b7dbd-113">Initialisez l’étape de pipeline à l’aide de [**ID3D11DeviceContext ::D ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).</span><span class="sxs-lookup"><span data-stu-id="b7dbd-113">Initialize the pipeline stage using [**ID3D11DeviceContext::DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).</span></span>
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="b7dbd-114">Un nuanceur de domaine doit être lié au pipeline si un nuanceur de coque est lié.</span><span class="sxs-lookup"><span data-stu-id="b7dbd-114">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="b7dbd-115">En particulier, il n’est pas valide de diffuser directement en continu des points de contrôle de nuanceur de coque avec le nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="b7dbd-115">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7dbd-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7dbd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7dbd-117">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="b7dbd-117">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="b7dbd-118">Vue d’ensemble de la polygonalisation</span><span class="sxs-lookup"><span data-stu-id="b7dbd-118">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




