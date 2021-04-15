---
description: 'Cette section contient des informations sur les interfaces de nuanceur suivantes :'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Interfaces de nuanceur (graphiques Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a65d263533d0b2225515664e21c2d93114495
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483400"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a><span data-ttu-id="629ca-103">Interfaces de nuanceur (graphiques Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="629ca-103">Shader Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="629ca-104">Cette section contient des informations sur les interfaces de nuanceur suivantes :</span><span class="sxs-lookup"><span data-stu-id="629ca-104">This section contains information about the following shader interfaces:</span></span>

<span data-ttu-id="629ca-105">Chacune de ces interfaces de nuanceur gère un nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="629ca-105">Each of these shader interfaces manages a compiled shader.</span></span> <span data-ttu-id="629ca-106">L’interface est créée lors de la compilation d’un nuanceur et est ensuite transmise à différentes API qui doivent accéder à un nuanceur compilé ; par exemple, lors de la liaison d’un nuanceur à une phase de pipeline ou de l’obtention d’une signature de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="629ca-106">The interface is created when a shader is compiled, and is then passed to various APIs that need access to a compiled shader; such as when binding a shader to a pipeline stage or getting a shader signature.</span></span>



| <span data-ttu-id="629ca-107">Interfaces Pipeline-Stage</span><span class="sxs-lookup"><span data-stu-id="629ca-107">Pipeline-Stage Interfaces</span></span>                                      | <span data-ttu-id="629ca-108">Description</span><span class="sxs-lookup"><span data-stu-id="629ca-108">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="629ca-109">**Interface ID3D10GeometryShader**</span><span class="sxs-lookup"><span data-stu-id="629ca-109">**ID3D10GeometryShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | <span data-ttu-id="629ca-110">Un nuanceur Geometry implémente un traitement par primitive dans l' [étape Geometry-Shader](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="629ca-110">A geometry-shader implements per-primitive processing in the [geometry-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> |
| [<span data-ttu-id="629ca-111">**Interface ID3D10PixelShader**</span><span class="sxs-lookup"><span data-stu-id="629ca-111">**ID3D10PixelShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | <span data-ttu-id="629ca-112">Un nuanceur de pixels implémente le traitement par pixel dans l' [étape nuanceur de pixels](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="629ca-112">A pixel-shader implements per-pixel processing in the [pixel-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>           |
| [<span data-ttu-id="629ca-113">**Interface ID3D10VertexShader**</span><span class="sxs-lookup"><span data-stu-id="629ca-113">**ID3D10VertexShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | <span data-ttu-id="629ca-114">Un nuanceur de sommets implémente le traitement par vertex dans l' [étape de nuanceur de sommets](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="629ca-114">A vertex-shader implements per-vertex processing in the [vertex-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>        |



 

<span data-ttu-id="629ca-115">Les interfaces de nuanceur-réflexion permettent à une application d’inspecter le contenu d’un nuanceur au moment de la conception ou de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="629ca-115">Shader-reflection interfaces allow an application to inspect the contents of a shader at design/author time.</span></span> <span data-ttu-id="629ca-116">La réflexion du nuanceur n’est pas utile pour définir des variables au moment de l’exécution, car il s’agit d’un miroir des données du nuanceur et ne prend donc pas en charge les méthodes de définition des données.</span><span class="sxs-lookup"><span data-stu-id="629ca-116">Shader reflection is not useful for setting variables at runtime as it is a mirror of the shader data, and therefore supports no methods for setting data.</span></span>



| <span data-ttu-id="629ca-117">Interfaces Shader-Reflection</span><span class="sxs-lookup"><span data-stu-id="629ca-117">Shader-Reflection Interfaces</span></span>                                                                   | <span data-ttu-id="629ca-118">Description</span><span class="sxs-lookup"><span data-stu-id="629ca-118">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="629ca-119">**Interface ID3D10ShaderReflection**</span><span class="sxs-lookup"><span data-stu-id="629ca-119">**ID3D10ShaderReflection Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | <span data-ttu-id="629ca-120">Interface COM pour lire des informations à partir d’un nuanceur compilé au moment de l’édition.</span><span class="sxs-lookup"><span data-stu-id="629ca-120">A COM interface for reading information from a compiled shader at author time.</span></span>     |
| [<span data-ttu-id="629ca-121">**Interface ID3D10ShaderReflectionConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="629ca-121">**ID3D10ShaderReflectionConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | <span data-ttu-id="629ca-122">Une interface d’assistance pour obtenir une interface de mémoire tampon de nuanceur-réflexion.</span><span class="sxs-lookup"><span data-stu-id="629ca-122">A helper interface for getting a shader-reflection constant-buffer interface.</span></span>      |
| [<span data-ttu-id="629ca-123">**Interface ID3D10ShaderReflectionType**</span><span class="sxs-lookup"><span data-stu-id="629ca-123">**ID3D10ShaderReflectionType Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | <span data-ttu-id="629ca-124">Interface d’assistance pour l’obtention d’une interface de type nuanceur-réflexion.</span><span class="sxs-lookup"><span data-stu-id="629ca-124">A helper interface for getting a shader-reflection-type interface.</span></span>                 |
| [<span data-ttu-id="629ca-125">**Interface ID3D10ShaderReflectionVariable**</span><span class="sxs-lookup"><span data-stu-id="629ca-125">**ID3D10ShaderReflectionVariable Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | <span data-ttu-id="629ca-126">Interface d’assistance pour l’obtention d’une interface de nuanceur-réflexion-variable.</span><span class="sxs-lookup"><span data-stu-id="629ca-126">A helper interface for getting a shader-reflection-variable interface.</span></span>             |
| [<span data-ttu-id="629ca-127">**Interface ID3D10ShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="629ca-127">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | <span data-ttu-id="629ca-128">Interface de nuanceur-réflexion permettant de lire des informations à partir d’un affichage des ressources de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="629ca-128">A shader-reflection interface for reading information from a shader-resource view.</span></span> |



 

<span data-ttu-id="629ca-129">Les API de réflexion de nuanceur implémentent une interface de réflexion de nuanceur COM ([**ID3D10ShaderReflection interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) et plusieurs interfaces d’assistance non com (le reste des interfaces).</span><span class="sxs-lookup"><span data-stu-id="629ca-129">Shader reflection APIs implement one COM shader reflection interface ([**ID3D10ShaderReflection Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) and several non-COM helper interfaces (the rest of the interfaces).</span></span> <span data-ttu-id="629ca-130">L' **interface ID3D10ShaderReflection** est créée lors de la création d’un objet de réflexion de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="629ca-130">**ID3D10ShaderReflection Interface** is created when a shader reflection object is created.</span></span> <span data-ttu-id="629ca-131">Il suit les règles COM standard ; la création de l’interface augmente le nombre de références et l’interface doit être libérée lorsqu’elle n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="629ca-131">It follows standard COM rules; creating the interface increases a reference count and the interface must be released when it is no longer needed.</span></span> <span data-ttu-id="629ca-132">Les interfaces de nuanceur-réflexion restantes sont des interfaces d’assistance qui n’héritent pas de IUnknown.</span><span class="sxs-lookup"><span data-stu-id="629ca-132">The remaining shader-reflection interfaces are helper interfaces that do not inherit from IUnknown.</span></span> <span data-ttu-id="629ca-133">Cela signifie qu’ils ne modifient aucun nombre de références lors de leur création, et qu’ils n’ont pas besoin d’être détruits lorsque vous en avez terminé avec eux.</span><span class="sxs-lookup"><span data-stu-id="629ca-133">This means that they do not change any reference count when they are created, and they do not need to be destroyed when you are finished with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="629ca-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="629ca-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="629ca-135">Référence du nuanceur</span><span class="sxs-lookup"><span data-stu-id="629ca-135">Shader Reference</span></span>](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
