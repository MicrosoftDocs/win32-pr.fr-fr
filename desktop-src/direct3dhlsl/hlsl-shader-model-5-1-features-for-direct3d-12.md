---
title: Modèle de nuanceur HLSL 5,1
description: Cette section décrit les fonctionnalités du modèle de nuanceur 5,1 telles qu’elles s’appliquent dans la pratique à D3D12 et à D3D 11.3. Tout le matériel DirectX 12 prend en charge le modèle de nuanceur 5,1.
ms.assetid: 6EF38EB9-71CB-4591-AAE2-F3FFC23E73B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e13620fe81f3c1e7d3de1589f82171667834a26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463250"
---
# <a name="hlsl-shader-model-51"></a><span data-ttu-id="5acbf-104">Modèle de nuanceur HLSL 5,1</span><span class="sxs-lookup"><span data-stu-id="5acbf-104">HLSL Shader Model 5.1</span></span>

<span data-ttu-id="5acbf-105">Cette section décrit les fonctionnalités du modèle de nuanceur 5,1 telles qu’elles s’appliquent dans la pratique à D3D12.</span><span class="sxs-lookup"><span data-stu-id="5acbf-105">This section describes the features of Shader Model 5.1 as they apply in practice to D3D12.</span></span> <span data-ttu-id="5acbf-106">Tout le matériel DirectX 12 prend en charge le modèle de nuanceur 5,1.</span><span class="sxs-lookup"><span data-stu-id="5acbf-106">All DirectX 12 hardware supports Shader Model 5.1.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5acbf-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="5acbf-107">In this section</span></span>



| <span data-ttu-id="5acbf-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="5acbf-108">Topic</span></span>                                                                         | <span data-ttu-id="5acbf-109">Description</span><span class="sxs-lookup"><span data-stu-id="5acbf-109">Description</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5acbf-110">Changements de bytecode dans SM 5.1</span><span class="sxs-lookup"><span data-stu-id="5acbf-110">Bytecode changes in SM5.1</span></span>](bytecode-changes-in-sm5-1.md)<br/>         | <span data-ttu-id="5acbf-111">SM 5.1 change la façon dont les registres de ressources sont déclarés et référencés dans les instructions.</span><span class="sxs-lookup"><span data-stu-id="5acbf-111">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <br/>                                                            |
| [<span data-ttu-id="5acbf-112">Signature racine spécifiée par HLSL</span><span class="sxs-lookup"><span data-stu-id="5acbf-112">HLSL Specified Root Signature</span></span>](hlsl-specified-root-signature.md)<br/> | <span data-ttu-id="5acbf-113">Une [signature racine](/windows/desktop/direct3d12/root-signatures) (une table de clés de ressources et d’autres éléments pour D3D12) peut être spécifiée en langage HLSL en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="5acbf-113">A [Root Signature](/windows/desktop/direct3d12/root-signatures) (a key table of resources and other elements for D3D12) can be specified in HLSL as a string.</span></span> <br/> |



 

<span data-ttu-id="5acbf-114">Pour plus d’informations sur les modifications apportées à la syntaxe du nuanceur, reportez-vous au [nuancier Model 5,1](shader-model-5-1.md).</span><span class="sxs-lookup"><span data-stu-id="5acbf-114">For details of the syntax changes to the shader language, refer to [Shader Model 5.1](shader-model-5-1.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5acbf-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5acbf-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5acbf-116">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="5acbf-116">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

