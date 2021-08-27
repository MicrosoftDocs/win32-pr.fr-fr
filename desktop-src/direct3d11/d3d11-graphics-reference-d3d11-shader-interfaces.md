---
title: Interfaces de nuanceur (graphisme Direct3D 11)
description: Cette section contient des informations sur les interfaces de nuanceur.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- interfaces, nuanceur Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fcecdff6f35b634ecbbeca0b85bc5ba42fd1e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479455"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a>Interfaces de nuanceur (graphisme Direct3D 11)

Cette section contient des informations sur les interfaces de nuanceur.

Chacune de ces interfaces de nuanceur gère un nuanceur compilé. L’interface est créée lors de la compilation d’un nuanceur et est ensuite transmise à différentes API qui doivent accéder à un nuanceur compilé ; par exemple, lors de la liaison d’un nuanceur à une phase de pipeline ou de l’obtention d’une signature de nuanceur.


## <a name="in-this-section"></a>Contenu de cette section




| Rubrique | Description | 
|-------|-------------|
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a><br /> | Cette interface encapsule une classe HLSL.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a><br /> | Cette interface encapsule une liaison dynamique HLSL.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a><br /> | Une interface de nuanceur de calcul gère un programme exécutable (un nuanceur de calcul) qui contrôle l’étape de nuanceur de calcul.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a><br /> | Une interface de nuanceur de domaine gère un programme exécutable (un nuanceur de domaine) qui contrôle l’étape du nuanceur de domaine.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a><br /> | Une interface de graphe de liaison de fonction est utilisée pour construire des nuanceurs qui se composent d’une séquence d’appels de fonctions précompilées qui passent des valeurs les unes aux autres. <br /><blockquote>[!Note]<br />Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a><br /> | Une interface de réflexion de fonction accède aux informations de la fonction. <br /><blockquote>[!Note]<br />Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a><br /> | Une interface de fonction-paramètre-Reflection accède aux informations sur les paramètres de fonction. <br /><blockquote>[!Note]<br />Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a><br /> | Une interface Geometry-Shader gère un programme exécutable (un nuanceur Geometry) qui contrôle l’étape Geometry-Shader.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a><br /> | Une interface de nuanceur de coque gère un programme exécutable (un nuanceur de coque) qui contrôle l’étape de nuanceur de coque.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a><br /> | Une interface de réflexion de bibliothèque accède aux informations de la bibliothèque. <br /><blockquote>[!Note]<br />Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a><br /> | Une interface de l’éditeur de liens est utilisée pour lier un module de nuanceur. <br /><blockquote>[!Note]<br />Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a><br /> | Une interface de nœud de liaison est utilisée pour la liaison de nuanceur. <br /><blockquote>[!Note]<br />Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a><br /> | Une interface de module crée une instance d’un module utilisé pour la reliaison des ressources. <br /><blockquote>[!Note]<br />Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a><br /> | Une interface de module-instance est utilisée pour la reliaison des ressources. <br /><blockquote>[!Note]<br />Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a><br /> | Une interface de nuanceur de pixels gère un programme exécutable (un nuanceur de pixels) qui contrôle l’étape de nuanceur de pixels.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a><br /> | Une interface de nuanceur-réflexion accède à des informations de nuanceur.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a><br /> | Cette interface de nuanceur-réflexion fournit l’accès à une mémoire tampon constante.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a><br /> | Cette interface de nuanceur-réflexion donne accès au type de variable.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a><br /> | Cette interface de nuanceur-réflexion donne accès à une variable.<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a><br /> | Une interface <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> implémente des méthodes pour obtenir des traces d’exécutions de nuanceur.<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a><br /> | Une interface <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> implémente une méthode pour générer des objets d’informations de trace de nuanceur.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a><br /> | Une interface de nuanceur de sommets gère un programme exécutable (un nuanceur de sommets) qui contrôle l’étape de nuanceur de sommets.<br /> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du nuanceur](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

