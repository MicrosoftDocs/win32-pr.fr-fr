---
title: Construction d’un graphique de fonctions de liaison de fonction et de son lien au code compilé
description: Ici, nous vous montrons comment construire des graphiques à fonctions de liaison de fonction (FLGs) pour les nuanceurs et comment lier ces nuanceurs à une bibliothèque de nuanceurs pour produire des objets BLOB de nuanceur que le runtime Direct3D peut utiliser.
ms.assetid: 82C3109E-8571-49D2-A8BF-298E30E1281B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c037e7ea111d11d24df173ffba7e56c8f486af82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232601"
---
# <a name="constructing-a-function-linking-graph-and-linking-it-to-compiled-code"></a>Construction d’un graphique de fonctions de liaison de fonction et de son lien au code compilé

Ici, nous vous montrons comment construire des graphiques à fonctions de liaison de fonction (FLGs) pour les nuanceurs et comment lier ces nuanceurs à une bibliothèque de nuanceurs pour produire des objets BLOB de nuanceur que le runtime Direct3D peut utiliser.

**Objectif :** Pour construire une fonction-Linking-Graph et la lier au code compilé.

## <a name="prerequisites"></a>Prérequis

Nous partons du principe que vous êtes familiarisé avec C++. Vous avez également besoin d’une expérience de base dans les concepts de programmation graphique.

Nous partons également du principe que vous avez parcouru [une bibliothèque de nuanceur](pachaging-a-shader-library.md).

**Durée d’exécution :** 30 minutes.

## <a name="instructions"></a>Instructions

### <a name="1-construct-a-function-linking-graph-for-the-vertex-shader"></a>1. construisez une fonction-Linking-Graph pour le nuanceur de sommets.

Appelez la fonction [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) pour créer une fonction-Linking-Graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) pour représenter le nuanceur de sommets.

Utilisez un tableau de [**structures \_ \_ desc de paramètre d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) pour définir les paramètres d’entrée pour le nuanceur de sommets. L' [étape assembleur d’entrée](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) alimente les paramètres d’entrée dans le nuanceur de sommets. La disposition des paramètres d’entrée du nuanceur vertex correspond à la disposition du nuanceur de sommets dans le code compilé. Après avoir défini les paramètres d’entrée, appelez la méthode [**ID3D11FunctionLinkingGraph :: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) pour définir le nœud d’entrée ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) pour le nuanceur de sommets.


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



Appelez la méthode [**ID3D11FunctionLinkingGraph :: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) pour créer un nœud pour la fonction principale du nuanceur de sommets et effectuer des appels à [**ID3D11FunctionLinkingGraph ::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) pour passer des valeurs du nœud d’entrée au nœud pour la fonction de nuanceur vertex principale.


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



Utilisez un tableau de [**structures \_ \_ desc de paramètre d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) pour définir les paramètres de sortie du nuanceur de sommets. Le nuanceur de sommets alimente ses paramètres de sortie vers le nuanceur de pixels. La disposition des paramètres de sortie du nuanceur de sommets correspond à la disposition du nuanceur de pixels dans le code compilé. Après avoir défini les paramètres de sortie, appelez la méthode [**ID3D11FunctionLinkingGraph :: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) pour définir le nœud de sortie ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) pour le nuanceur de sommets.


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



Effectuez des appels à [**ID3D11FunctionLinkingGraph ::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) pour passer des valeurs du nœud pour la fonction de nuanceur vertex principale au nœud de sortie.


```C++
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 0, vertexShaderOutputNode.Get(), 2), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 1, vertexShaderOutputNode.Get(), 0), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 2, vertexShaderOutputNode.Get(), 1), 
                vertexShaderGraph.Get());
```



Appelez la méthode [**ID3D11FunctionLinkingGraph :: CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) pour finaliser le graphique du nuanceur de sommets.


```C++
            // Finalize the vertex shader graph.
            ComPtr<ID3D11ModuleInstance> vertexShaderGraphInstance;
            LinkingThrowIfFailed(vertexShaderGraph->CreateModuleInstance(&vertexShaderGraphInstance, nullptr), vertexShaderGraph.Get());
```



### <a name="2-link-the-vertex-shader"></a>2. lier le nuanceur de sommets

Appelez la fonction [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) pour créer un éditeur de liens ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) que vous pouvez utiliser pour lier l’instance de la bibliothèque de nuanceur que vous avez créée lors de l' [empaquetage d’une bibliothèque de nuanceur](pachaging-a-shader-library.md) avec l’instance du graphique de nuanceur de sommets que vous avez créée à l’étape précédente. Appelez la méthode [**ID3D11Linker :: UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) pour spécifier la bibliothèque de nuanceur à utiliser pour la liaison. Appelez la méthode [**ID3D11Linker :: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) pour lier la bibliothèque du nuanceur au graphique du nuanceur de sommets et pour produire un pointeur vers l’interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que vous pouvez utiliser pour accéder au code du nuanceur de sommets compilé. Vous pouvez ensuite passer ce code de nuanceur de vertex compilé à la méthode [**ID3D11Device :: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) pour créer l’objet de nuanceur de sommets et à la méthode [**ID3D11Device :: CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) pour créer l’objet de disposition d’entrée.


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



### <a name="3-construct-a-function-linking-graph-for-the-pixel-shader"></a>3. Créez une fonction-Linking-Graph pour le nuanceur de pixels.

Appelez la fonction [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) pour créer une fonction-Linking-Graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) pour représenter le nuanceur de pixels.

Utilisez un tableau de [**structures \_ \_ desc de paramètre d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) pour définir les paramètres d’entrée pour le nuanceur de pixels. L’étape du nuanceur de sommets alimente les paramètres d’entrée dans le nuanceur de pixels. La disposition des paramètres d’entrée du nuanceur de pixels correspond à la disposition du nuanceur de pixels dans le code compilé. Après avoir défini les paramètres d’entrée, appelez la méthode [**ID3D11FunctionLinkingGraph :: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) pour définir le nœud d’entrée ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) pour le nuanceur de pixels.


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



Appelez la méthode [**ID3D11FunctionLinkingGraph :: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) pour créer un nœud pour la fonction de nuanceur de pixels principale et effectuer des appels à [**ID3D11FunctionLinkingGraph ::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) pour passer des valeurs du nœud d’entrée au nœud pour la fonction de nuanceur de pixels principale.


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



Utilisez un tableau de [**structures \_ \_ desc de paramètre d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) pour définir les paramètres de sortie pour le nuanceur de pixels. Le nuanceur de pixels passe ses paramètres de sortie à l' [étape de fusion de sortie](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage). Après avoir défini les paramètres de sortie, appelez la méthode [**ID3D11FunctionLinkingGraph :: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) pour définir le nœud de sortie ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) pour le nuanceur de pixels et effectuer des appels à [**ID3D11FunctionLinkingGraph ::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) pour passer des valeurs d’un nœud de fonction de nuanceur de pixels au nœud de sortie.


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



Appelez la méthode [**ID3D11FunctionLinkingGraph :: CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) pour finaliser le graphique de nuanceur de pixels.


```C++
            // Finalize the pixel shader graph.
            ComPtr<ID3D11ModuleInstance> pixelShaderGraphInstance;
            LinkingThrowIfFailed(pixelShaderGraph->CreateModuleInstance(&pixelShaderGraphInstance, nullptr), pixelShaderGraph.Get());
```



### <a name="4-link-the-pixel-shader"></a>4. lier le nuanceur de pixels

Appelez la fonction [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) pour créer un éditeur de liens ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) que vous pouvez utiliser pour lier l’instance de la bibliothèque de nuanceur que vous avez créée lors de l' [empaquetage d’une bibliothèque de nuanceur](pachaging-a-shader-library.md) avec l’instance du graphique de nuanceur de pixels que vous avez créée à l’étape précédente. Appelez la méthode [**ID3D11Linker :: UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) pour spécifier la bibliothèque de nuanceur à utiliser pour la liaison. Appelez la méthode [**ID3D11Linker :: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) pour lier la bibliothèque de nuanceur au graphique de nuanceur de pixels et produire un pointeur vers l’interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que vous pouvez utiliser pour accéder au code du nuanceur de pixels compilé. Vous pouvez ensuite passer ce code de nuanceur de pixels compilé à la méthode [**ID3D11Device :: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) pour créer l’objet nuanceur de pixels.


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



## <a name="summary"></a>Résumé

Nous avons utilisé les méthodes [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) pour construire les graphiques de nuanceur vertex et de pixels et pour spécifier la structure de nuanceur par programmation.

Ces constructions graphiques se composent de séquences d’appels de fonctions précompilées qui passent des valeurs les unes aux autres. Les nœuds FLG ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) représentent les nœuds du nuanceur d’entrée et de sortie et les appels des fonctions de bibliothèque précompilées. L’ordre dans lequel vous inscrivez les nœuds d’appel de fonction définit la séquence d’appels. Vous devez d’abord spécifier le nœud d’entrée ([**ID3D11FunctionLinkingGraph :: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) et le nœud de sortie ([**ID3D11FunctionLinkingGraph :: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)). Les bords FLG définissent la façon dont les valeurs sont passées d’un nœud à un autre. Les types de données des valeurs passées doivent être identiques ; Il n’existe pas de conversion de type implicite. Les règles de forme et swizzling suivent le comportement HLSL. Les valeurs peuvent uniquement être transmises par progression dans cette séquence.

Nous avons également utilisé les méthodes [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) pour lier la bibliothèque de nuanceurs aux graphiques de nuanceur et pour produire des objets BLOB de nuanceur à utiliser par le runtime Direct3D.

Félicitations ! Vous êtes maintenant prêt à utiliser la liaison de nuanceur dans vos propres applications.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la liaison de nuanceur](using-shader-linking.md)
</dt> </dl>

 

 