---
title: Construction d’un graphique de fonctions de liaison de fonction et de son lien au code compilé
description: Ici, nous vous montrons comment construire des graphiques à fonctions de liaison de fonction (FLGs) pour les nuanceurs et comment lier ces nuanceurs à une bibliothèque de nuanceurs pour produire des objets BLOB de nuanceur que le runtime Direct3D peut utiliser.
ms.assetid: 82C3109E-8571-49D2-A8BF-298E30E1281B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c037e7ea111d11d24df173ffba7e56c8f486af82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842562"
---
# <a name="constructing-a-function-linking-graph-and-linking-it-to-compiled-code"></a><span data-ttu-id="2696a-103">Construction d’un graphique de fonctions de liaison de fonction et de son lien au code compilé</span><span class="sxs-lookup"><span data-stu-id="2696a-103">Constructing a function-linking-graph and linking it to compiled code</span></span>

<span data-ttu-id="2696a-104">Ici, nous vous montrons comment construire des graphiques à fonctions de liaison de fonction (FLGs) pour les nuanceurs et comment lier ces nuanceurs à une bibliothèque de nuanceurs pour produire des objets BLOB de nuanceur que le runtime Direct3D peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="2696a-104">Here we show you how to construct function-linking-graphs (FLGs) for shaders and how to link those shaders with a shader library to produce shader blobs that the Direct3D runtime can use.</span></span>

<span data-ttu-id="2696a-105">**Objectif :** Pour construire une fonction-Linking-Graph et la lier au code compilé.</span><span class="sxs-lookup"><span data-stu-id="2696a-105">**Objective:** To construct a function-linking-graph and link it to compiled code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2696a-106">Prérequis</span><span class="sxs-lookup"><span data-stu-id="2696a-106">Prerequisites</span></span>

<span data-ttu-id="2696a-107">Nous partons du principe que vous êtes familiarisé avec C++.</span><span class="sxs-lookup"><span data-stu-id="2696a-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="2696a-108">Vous avez également besoin d’une expérience de base dans les concepts de programmation graphique.</span><span class="sxs-lookup"><span data-stu-id="2696a-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="2696a-109">Nous partons également du principe que vous avez parcouru [une bibliothèque de nuanceur](pachaging-a-shader-library.md).</span><span class="sxs-lookup"><span data-stu-id="2696a-109">We also assume that you went through [Packaging a shader library](pachaging-a-shader-library.md).</span></span>

<span data-ttu-id="2696a-110">**Durée d’exécution :** 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="2696a-110">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="2696a-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="2696a-111">Instructions</span></span>

### <a name="1-construct-a-function-linking-graph-for-the-vertex-shader"></a><span data-ttu-id="2696a-112">1. construisez une fonction-Linking-Graph pour le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="2696a-112">1. Construct a function-linking-graph for the vertex shader.</span></span>

<span data-ttu-id="2696a-113">Appelez la fonction [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) pour créer une fonction-Linking-Graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) pour représenter le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="2696a-113">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the vertex shader.</span></span>

<span data-ttu-id="2696a-114">Utilisez un tableau de [**structures \_ \_ desc de paramètre d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) pour définir les paramètres d’entrée pour le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="2696a-114">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the vertex shader.</span></span> <span data-ttu-id="2696a-115">L' [étape assembleur d’entrée](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) alimente les paramètres d’entrée dans le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="2696a-115">The [Input-Assembler Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) feeds the input parameters to the vertex shader.</span></span> <span data-ttu-id="2696a-116">La disposition des paramètres d’entrée du nuanceur vertex correspond à la disposition du nuanceur de sommets dans le code compilé.</span><span class="sxs-lookup"><span data-stu-id="2696a-116">The layout of the vertex shader’s input parameters matches the layout of the vertex shader in the compiled code.</span></span> <span data-ttu-id="2696a-117">Après avoir défini les paramètres d’entrée, appelez la méthode [**ID3D11FunctionLinkingGraph :: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) pour définir le nœud d’entrée ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) pour le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="2696a-117">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


```C++
            ComPtr<ID3D11FunctionLinkingGraph> vertexShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &vertexShaderGraph));

            // Define the main input node which will be fed by the Input Assembler pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderInputParameters[] =
            {
                {"inputPos",  "POSITION0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputTex",  "TEXCOORD0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderInputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetInputSignature(vertexShaderInputParameters, ARRAYSIZE(vertexShaderInputParameters), 
                &vertexShaderInputNode), vertexShaderGraph.Get());
```



<span data-ttu-id="2696a-118">Appelez la méthode [**ID3D11FunctionLinkingGraph :: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) pour créer un nœud pour la fonction principale du nuanceur de sommets et effectuer des appels à [**ID3D11FunctionLinkingGraph ::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) pour passer des valeurs du nœud d’entrée au nœud pour la fonction de nuanceur vertex principale.</span><span class="sxs-lookup"><span data-stu-id="2696a-118">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main vertex shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main vertex shader function.</span></span>


```C++
            // Create a node for the main VertexFunction call using the output of the helper functions.
            ComPtr<ID3D11LinkingNode> vertexFunctionCallNode;
            LinkingThrowIfFailed(vertexShaderGraph->CallFunction("", shaderLibrary.Get(), "VertexFunction", &vertexFunctionCallNode), 
                vertexShaderGraph.Get());

            // Define the graph edges from the input node and helper function nodes.
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForPos.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 0), vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexShaderInputNode.Get(), 1, vertexFunctionCallNode.Get(), 1), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForNorm.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 2), vertexShaderGraph.Get());
```



<span data-ttu-id="2696a-119">Utilisez un tableau de [**structures \_ \_ desc de paramètre d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) pour définir les paramètres de sortie du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="2696a-119">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the vertex shader.</span></span> <span data-ttu-id="2696a-120">Le nuanceur de sommets alimente ses paramètres de sortie vers le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="2696a-120">The vertex shader feeds its output parameters to the pixel shader.</span></span> <span data-ttu-id="2696a-121">La disposition des paramètres de sortie du nuanceur de sommets correspond à la disposition du nuanceur de pixels dans le code compilé.</span><span class="sxs-lookup"><span data-stu-id="2696a-121">The layout of the vertex shader’s output parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="2696a-122">Après avoir défini les paramètres de sortie, appelez la méthode [**ID3D11FunctionLinkingGraph :: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) pour définir le nœud de sortie ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) pour le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="2696a-122">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


```C++
            // Define the main output node which will feed the Pixel Shader pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderOutputParameters[] =
            {
                {"outputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderOutputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetOutputSignature(vertexShaderOutputParameters, ARRAYSIZE(vertexShaderOutputParameters), 
                &vertexShaderOutputNode), vertexShaderGraph.Get());
```



<span data-ttu-id="2696a-123">Effectuez des appels à [**ID3D11FunctionLinkingGraph ::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) pour passer des valeurs du nœud pour la fonction de nuanceur vertex principale au nœud de sortie.</span><span class="sxs-lookup"><span data-stu-id="2696a-123">Make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the node for the main vertex shader function to the output node.</span></span>


```C++
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 0, vertexShaderOutputNode.Get(), 2), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 1, vertexShaderOutputNode.Get(), 0), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 2, vertexShaderOutputNode.Get(), 1), 
                vertexShaderGraph.Get());
```



<span data-ttu-id="2696a-124">Appelez la méthode [**ID3D11FunctionLinkingGraph :: CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) pour finaliser le graphique du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="2696a-124">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the vertex shader graph.</span></span>


```C++
            // Finalize the vertex shader graph.
            ComPtr<ID3D11ModuleInstance> vertexShaderGraphInstance;
            LinkingThrowIfFailed(vertexShaderGraph->CreateModuleInstance(&vertexShaderGraphInstance, nullptr), vertexShaderGraph.Get());
```



### <a name="2-link-the-vertex-shader"></a><span data-ttu-id="2696a-125">2. lier le nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="2696a-125">2. Link the vertex shader</span></span>

<span data-ttu-id="2696a-126">Appelez la fonction [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) pour créer un éditeur de liens ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) que vous pouvez utiliser pour lier l’instance de la bibliothèque de nuanceur que vous avez créée lors de l' [empaquetage d’une bibliothèque de nuanceur](pachaging-a-shader-library.md) avec l’instance du graphique de nuanceur de sommets que vous avez créée à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="2696a-126">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the vertex shader graph that you created in the preceding step.</span></span> <span data-ttu-id="2696a-127">Appelez la méthode [**ID3D11Linker :: UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) pour spécifier la bibliothèque de nuanceur à utiliser pour la liaison.</span><span class="sxs-lookup"><span data-stu-id="2696a-127">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="2696a-128">Appelez la méthode [**ID3D11Linker :: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) pour lier la bibliothèque du nuanceur au graphique du nuanceur de sommets et pour produire un pointeur vers l’interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que vous pouvez utiliser pour accéder au code du nuanceur de sommets compilé.</span><span class="sxs-lookup"><span data-stu-id="2696a-128">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the vertex shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled vertex shader code.</span></span> <span data-ttu-id="2696a-129">Vous pouvez ensuite passer ce code de nuanceur de vertex compilé à la méthode [**ID3D11Device :: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) pour créer l’objet de nuanceur de sommets et à la méthode [**ID3D11Device :: CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) pour créer l’objet de disposition d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2696a-129">You can then pass this compiled vertex shader code to the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method to create the vertex shader object and to the [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) method to create the input-layout object.</span></span>


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the vertex shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(vertexShaderGraphInstance.Get(), "main", ("vs" + m_shaderModelSuffix).c_str(), 0, &vertexShaderBlob, 
                &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11VertexShader> vertexShader;
    DX::ThrowIfFailed(
        device->CreateVertexShader(
            vertexShaderBlob->GetBufferPointer(),
            vertexShaderBlob->GetBufferSize(),
            nullptr,
            &vertexShader
            )
        );
    context->VSSetShader(vertexShader.Get(), nullptr, 0);
    D3D11_INPUT_ELEMENT_DESC inputLayoutDesc[] =
    {
        { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0,  D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT,    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "NORMAL",   0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, D3D11_INPUT_PER_VERTEX_DATA, 0 }
    };
    ComPtr<ID3D11InputLayout> inputLayout;
    DX::ThrowIfFailed(device->CreateInputLayout(inputLayoutDesc, ARRAYSIZE(inputLayoutDesc), vertexShaderBlob->GetBufferPointer(), vertexShaderBlob->GetBufferSize(), &inputLayout));
    context->IASetInputLayout(inputLayout.Get());
```



### <a name="3-construct-a-function-linking-graph-for-the-pixel-shader"></a><span data-ttu-id="2696a-130">3. Créez une fonction-Linking-Graph pour le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="2696a-130">3. Construct a function-linking-graph for the pixel shader.</span></span>

<span data-ttu-id="2696a-131">Appelez la fonction [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) pour créer une fonction-Linking-Graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) pour représenter le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="2696a-131">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the pixel shader.</span></span>

<span data-ttu-id="2696a-132">Utilisez un tableau de [**structures \_ \_ desc de paramètre d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) pour définir les paramètres d’entrée pour le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="2696a-132">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the pixel shader.</span></span> <span data-ttu-id="2696a-133">L’étape du nuanceur de sommets alimente les paramètres d’entrée dans le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="2696a-133">The vertex shader stage feeds the input parameters to the pixel shader.</span></span> <span data-ttu-id="2696a-134">La disposition des paramètres d’entrée du nuanceur de pixels correspond à la disposition du nuanceur de pixels dans le code compilé.</span><span class="sxs-lookup"><span data-stu-id="2696a-134">The layout of the pixel shader’s input parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="2696a-135">Après avoir défini les paramètres d’entrée, appelez la méthode [**ID3D11FunctionLinkingGraph :: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) pour définir le nœud d’entrée ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) pour le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="2696a-135">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader.</span></span>


```C++
            ComPtr<ID3D11FunctionLinkingGraph> pixelShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &pixelShaderGraph));

            // Define the main input node which will be fed by the vertex shader pipeline stage.
            static const D3D11_PARAMETER_DESC pixelShaderInputParameters[] =
            {
                {"inputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderInputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetInputSignature(pixelShaderInputParameters, ARRAYSIZE(pixelShaderInputParameters), 
                &pixelShaderInputNode), pixelShaderGraph.Get());
```



<span data-ttu-id="2696a-136">Appelez la méthode [**ID3D11FunctionLinkingGraph :: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) pour créer un nœud pour la fonction de nuanceur de pixels principale et effectuer des appels à [**ID3D11FunctionLinkingGraph ::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) pour passer des valeurs du nœud d’entrée au nœud pour la fonction de nuanceur de pixels principale.</span><span class="sxs-lookup"><span data-stu-id="2696a-136">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main pixel shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main pixel shader function.</span></span>


```C++
            // Create a node for the main ColorFunction call and connect it to the pixel shader inputs.
            ComPtr<ID3D11LinkingNode> colorValueNode;
            LinkingThrowIfFailed(pixelShaderGraph->CallFunction("", shaderLibrary.Get(), "ColorFunction", &colorValueNode), 
                pixelShaderGraph.Get());

            // Define the graph edges from the input node.
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 0, colorValueNode.Get(), 0), 
                pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 1, colorValueNode.Get(), 1), 
                pixelShaderGraph.Get());
```



<span data-ttu-id="2696a-137">Utilisez un tableau de [**structures \_ \_ desc de paramètre d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) pour définir les paramètres de sortie pour le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="2696a-137">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the pixel shader.</span></span> <span data-ttu-id="2696a-138">Le nuanceur de pixels passe ses paramètres de sortie à l' [étape de fusion de sortie](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage).</span><span class="sxs-lookup"><span data-stu-id="2696a-138">The pixel shader feeds its output parameters to the [Output-Merger Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage).</span></span> <span data-ttu-id="2696a-139">Après avoir défini les paramètres de sortie, appelez la méthode [**ID3D11FunctionLinkingGraph :: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) pour définir le nœud de sortie ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) pour le nuanceur de pixels et effectuer des appels à [**ID3D11FunctionLinkingGraph ::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) pour passer des valeurs d’un nœud de fonction de nuanceur de pixels au nœud de sortie.</span><span class="sxs-lookup"><span data-stu-id="2696a-139">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from a pixel shader function node to the output node.</span></span>


```C++
            // Define the main output node which will feed the Output Merger pipeline stage.
            D3D11_PARAMETER_DESC pixelShaderOutputParameters[] =
            {
                {"outputColor", "SV_TARGET", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderOutputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetOutputSignature(pixelShaderOutputParameters, ARRAYSIZE(pixelShaderOutputParameters), 
                &pixelShaderOutputNode), pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(fillAlphaCallNode.Get(), D3D_RETURN_PARAMETER_INDEX, pixelShaderOutputNode.Get(), 0), 
                pixelShaderGraph.Get());
```



<span data-ttu-id="2696a-140">Appelez la méthode [**ID3D11FunctionLinkingGraph :: CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) pour finaliser le graphique de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="2696a-140">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the pixel shader graph.</span></span>


```C++
            // Finalize the pixel shader graph.
            ComPtr<ID3D11ModuleInstance> pixelShaderGraphInstance;
            LinkingThrowIfFailed(pixelShaderGraph->CreateModuleInstance(&pixelShaderGraphInstance, nullptr), pixelShaderGraph.Get());
```



### <a name="4-link-the-pixel-shader"></a><span data-ttu-id="2696a-141">4. lier le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="2696a-141">4. Link the pixel shader</span></span>

<span data-ttu-id="2696a-142">Appelez la fonction [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) pour créer un éditeur de liens ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) que vous pouvez utiliser pour lier l’instance de la bibliothèque de nuanceur que vous avez créée lors de l' [empaquetage d’une bibliothèque de nuanceur](pachaging-a-shader-library.md) avec l’instance du graphique de nuanceur de pixels que vous avez créée à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="2696a-142">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the pixel shader graph that you created in the preceding step.</span></span> <span data-ttu-id="2696a-143">Appelez la méthode [**ID3D11Linker :: UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) pour spécifier la bibliothèque de nuanceur à utiliser pour la liaison.</span><span class="sxs-lookup"><span data-stu-id="2696a-143">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="2696a-144">Appelez la méthode [**ID3D11Linker :: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) pour lier la bibliothèque de nuanceur au graphique de nuanceur de pixels et produire un pointeur vers l’interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que vous pouvez utiliser pour accéder au code du nuanceur de pixels compilé.</span><span class="sxs-lookup"><span data-stu-id="2696a-144">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the pixel shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled pixel shader code.</span></span> <span data-ttu-id="2696a-145">Vous pouvez ensuite passer ce code de nuanceur de pixels compilé à la méthode [**ID3D11Device :: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) pour créer l’objet nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="2696a-145">You can then pass this compiled pixel shader code to the [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) method to create the pixel shader object.</span></span>


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the pixel shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(pixelShaderGraphInstance.Get(), "main", ("ps" + m_shaderModelSuffix).c_str(), 0, &pixelShaderBlob, &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11PixelShader> pixelShader;
    DX::ThrowIfFailed(
        device->CreatePixelShader(
            pixelShaderBlob->GetBufferPointer(),
            pixelShaderBlob->GetBufferSize(),
            nullptr,
            &pixelShader
            )
        );
    context->PSSetShader(pixelShader.Get(), nullptr, 0);
```



## <a name="summary"></a><span data-ttu-id="2696a-146">Résumé</span><span class="sxs-lookup"><span data-stu-id="2696a-146">Summary</span></span>

<span data-ttu-id="2696a-147">Nous avons utilisé les méthodes [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) pour construire les graphiques de nuanceur vertex et de pixels et pour spécifier la structure de nuanceur par programmation.</span><span class="sxs-lookup"><span data-stu-id="2696a-147">We used the [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) methods to construct the vertex and pixel shader graphs and to specify the shader structure programmatically.</span></span>

<span data-ttu-id="2696a-148">Ces constructions graphiques se composent de séquences d’appels de fonctions précompilées qui passent des valeurs les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="2696a-148">These graph constructions consist of sequences of precompiled function calls that pass values to each other.</span></span> <span data-ttu-id="2696a-149">Les nœuds FLG ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) représentent les nœuds du nuanceur d’entrée et de sortie et les appels des fonctions de bibliothèque précompilées.</span><span class="sxs-lookup"><span data-stu-id="2696a-149">FLG nodes ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) represent input and output shader nodes and invocations of precompiled library functions.</span></span> <span data-ttu-id="2696a-150">L’ordre dans lequel vous inscrivez les nœuds d’appel de fonction définit la séquence d’appels.</span><span class="sxs-lookup"><span data-stu-id="2696a-150">The order in which you register the function-call nodes defines the sequence of invocations.</span></span> <span data-ttu-id="2696a-151">Vous devez d’abord spécifier le nœud d’entrée ([**ID3D11FunctionLinkingGraph :: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) et le nœud de sortie ([**ID3D11FunctionLinkingGraph :: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)).</span><span class="sxs-lookup"><span data-stu-id="2696a-151">You must specify the input node ([**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) first and the output node last ([**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)).</span></span> <span data-ttu-id="2696a-152">Les bords FLG définissent la façon dont les valeurs sont passées d’un nœud à un autre.</span><span class="sxs-lookup"><span data-stu-id="2696a-152">FLG edges define how values are passed from one node to another.</span></span> <span data-ttu-id="2696a-153">Les types de données des valeurs passées doivent être identiques ; Il n’existe pas de conversion de type implicite.</span><span class="sxs-lookup"><span data-stu-id="2696a-153">The data types of passed values must be the same; there is no implicit type conversion.</span></span> <span data-ttu-id="2696a-154">Les règles de forme et swizzling suivent le comportement HLSL.</span><span class="sxs-lookup"><span data-stu-id="2696a-154">Shape and swizzling rules follow the HLSL behavior.</span></span> <span data-ttu-id="2696a-155">Les valeurs peuvent uniquement être transmises par progression dans cette séquence.</span><span class="sxs-lookup"><span data-stu-id="2696a-155">Values can only be passed forward in this sequence.</span></span>

<span data-ttu-id="2696a-156">Nous avons également utilisé les méthodes [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) pour lier la bibliothèque de nuanceurs aux graphiques de nuanceur et pour produire des objets BLOB de nuanceur à utiliser par le runtime Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2696a-156">We also used [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) methods to link the shader library with the shader graphs and to produce shader blobs for the Direct3D runtime to use.</span></span>

<span data-ttu-id="2696a-157">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="2696a-157">Congratulations!</span></span> <span data-ttu-id="2696a-158">Vous êtes maintenant prêt à utiliser la liaison de nuanceur dans vos propres applications.</span><span class="sxs-lookup"><span data-stu-id="2696a-158">You are now ready to use shader linking in your own apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2696a-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2696a-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2696a-160">Utilisation de la liaison de nuanceur</span><span class="sxs-lookup"><span data-stu-id="2696a-160">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 