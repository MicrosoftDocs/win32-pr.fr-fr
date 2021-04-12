---
description: 'Cette section contient des informations sur les fonctions de nuanceur suivantes :'
ms.assetid: c8b33c08-7b3f-4b33-9b3c-4aa2b45b8f32
title: Fonctions du nuanceur (Direct3D 10 Graphics)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac0136eee8648512287eb146bbae02256fb223
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317909"
---
# <a name="shader-functions-direct3d-10-graphics"></a><span data-ttu-id="dea15-103">Fonctions du nuanceur (Direct3D 10 Graphics)</span><span class="sxs-lookup"><span data-stu-id="dea15-103">Shader Functions (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="dea15-104">Cette section contient des informations sur les fonctions de nuanceur suivantes :</span><span class="sxs-lookup"><span data-stu-id="dea15-104">This section contains information about the following shader functions:</span></span>



| <span data-ttu-id="dea15-105">Fonctions</span><span class="sxs-lookup"><span data-stu-id="dea15-105">Functions</span></span>                                                                          | <span data-ttu-id="dea15-106">Description</span><span class="sxs-lookup"><span data-stu-id="dea15-106">Description</span></span>                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="dea15-107">**D3D10CompileShader**</span><span class="sxs-lookup"><span data-stu-id="dea15-107">**D3D10CompileShader**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10compileshader)                                   | <span data-ttu-id="dea15-108">Compilez un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="dea15-108">Compile a shader.</span></span>                                                           |
| [<span data-ttu-id="dea15-109">**D3D10DisassembleShader**</span><span class="sxs-lookup"><span data-stu-id="dea15-109">**D3D10DisassembleShader**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10disassembleshader)                           | <span data-ttu-id="dea15-110">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="dea15-110">Deprecated.</span></span> <span data-ttu-id="dea15-111">Consultez [**D3DX10DisassembleShader**](d3dx10disassembleshader.md).</span><span class="sxs-lookup"><span data-stu-id="dea15-111">See [**D3DX10DisassembleShader**](d3dx10disassembleshader.md).</span></span> |
| [<span data-ttu-id="dea15-112">**D3D10GetGeometryShaderProfile**</span><span class="sxs-lookup"><span data-stu-id="dea15-112">**D3D10GetGeometryShaderProfile**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getgeometryshaderprofile)             | <span data-ttu-id="dea15-113">Obtenir le profil de nuanceur Geometry le mieux adapté à un appareil donné.</span><span class="sxs-lookup"><span data-stu-id="dea15-113">Get the geometry-shader profile best suited to a given device.</span></span>              |
| [<span data-ttu-id="dea15-114">**D3D10GetInputAndOutputSignatureBlob**</span><span class="sxs-lookup"><span data-stu-id="dea15-114">**D3D10GetInputAndOutputSignatureBlob**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getinputandoutputsignatureblob) | <span data-ttu-id="dea15-115">Obtient une mémoire tampon qui contient des signatures de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="dea15-115">Get a buffer that contains shader signatures.</span></span>                               |
| [<span data-ttu-id="dea15-116">**D3D10GetInputSignatureBlob**</span><span class="sxs-lookup"><span data-stu-id="dea15-116">**D3D10GetInputSignatureBlob**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getinputsignatureblob)                   | <span data-ttu-id="dea15-117">Obtient une mémoire tampon qui contient des signatures d’entrée de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="dea15-117">Get a buffer that contains shader input signatures.</span></span>                         |
| [<span data-ttu-id="dea15-118">**D3D10GetOutputSignatureBlob**</span><span class="sxs-lookup"><span data-stu-id="dea15-118">**D3D10GetOutputSignatureBlob**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getoutputsignatureblob)                 | <span data-ttu-id="dea15-119">Obtient une mémoire tampon qui contient les signatures de sortie du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="dea15-119">Get a buffer that contains shader output signatures.</span></span>                        |
| [<span data-ttu-id="dea15-120">**D3D10GetPixelShaderProfile**</span><span class="sxs-lookup"><span data-stu-id="dea15-120">**D3D10GetPixelShaderProfile**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getpixelshaderprofile)                   | <span data-ttu-id="dea15-121">Obtenir le profil de nuanceur de pixels le mieux adapté à un appareil donné.</span><span class="sxs-lookup"><span data-stu-id="dea15-121">Get the pixel-shader profile best suited to a given device.</span></span>                 |
| [<span data-ttu-id="dea15-122">**D3D10GetShaderDebugInfo**</span><span class="sxs-lookup"><span data-stu-id="dea15-122">**D3D10GetShaderDebugInfo**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getshaderdebuginfo)                         | <span data-ttu-id="dea15-123">Obtenir les informations de débogage du nuanceur à partir d’un nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="dea15-123">Get shader debug info from a compiled shader.</span></span>                               |
| [<span data-ttu-id="dea15-124">**D3D10GetVertexShaderProfile**</span><span class="sxs-lookup"><span data-stu-id="dea15-124">**D3D10GetVertexShaderProfile**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getvertexshaderprofile)                 | <span data-ttu-id="dea15-125">Obtenir le profil de nuanceur de vertex le mieux adapté à un appareil donné.</span><span class="sxs-lookup"><span data-stu-id="dea15-125">Get the vertex-shader profile best suited to a given device.</span></span>                |
| [<span data-ttu-id="dea15-126">**D3D10PreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="dea15-126">**D3D10PreprocessShader**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10preprocessshader)                             | <span data-ttu-id="dea15-127">Générez une chaîne de texte qui contient le flux de jetons du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="dea15-127">Generate a text string that contains the shader token stream.</span></span>               |
| [<span data-ttu-id="dea15-128">**D3D10ReflectShader**</span><span class="sxs-lookup"><span data-stu-id="dea15-128">**D3D10ReflectShader**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10reflectshader)                                   | <span data-ttu-id="dea15-129">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="dea15-129">Deprecated.</span></span> <span data-ttu-id="dea15-130">Consultez [**D3DX10ReflectShader**](d3dx10reflectshader.md).</span><span class="sxs-lookup"><span data-stu-id="dea15-130">See [**D3DX10ReflectShader**](d3dx10reflectshader.md).</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="dea15-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dea15-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dea15-132">Référence du nuanceur</span><span class="sxs-lookup"><span data-stu-id="dea15-132">Shader Reference</span></span>](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 



