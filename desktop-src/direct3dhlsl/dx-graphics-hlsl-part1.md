---
title: Compilation des nuanceurs
description: Examinons à présent les différentes façons de compiler le code et les conventions de votre nuanceur pour les extensions de fichier pour le code du nuanceur.
ms.assetid: a4e6b7cd-c5cc-4165-ba73-205155e449c9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03e5b23f5186111719e45b8e3c0b1b5bd0227065f28489996524ffca3b38d2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090986"
---
# <a name="compiling-shaders"></a>Compilation des nuanceurs

> [!NOTE]
> Cette rubrique couvre le `FXC.EXE` compilateur utilisé pour les modèles de nuanceur 2 à 5,1. Pour le nuancier modèle 6, vous utilisez `DXC.EXE` à la place, qui est documenté dans [utilisation de dxc.exe et dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).

Microsoft Visual Studio 2012 peut maintenant compiler du code de nuanceur à partir de \* fichiers. hlsl que vous incluez dans votre projet C++.

dans le cadre du processus de génération, Visual Studio 2012 utilise le compilateur de code [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL pour compiler les fichiers. hlsl dans des fichiers objets de nuanceur binaire ou dans des tableaux d’octets définis dans des fichiers d’en-tête. La façon dont le compilateur de code HLSL compile chaque fichier. HLSL dans votre projet dépend de la manière dont vous spécifiez la propriété **fichiers de sortie** pour ce fichier. Pour plus d’informations sur les pages de propriétés HLSL, consultez [HLSL Property pages](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).

La méthode de compilation que vous utilisez en général dépend de la taille de votre \* fichier. HLSL. Si vous incluez une grande quantité de code d’octet dans un en-tête, vous augmentez la taille et le temps de chargement initial de votre application. Vous forcez également tous les codes d’octet à résider en mémoire même après la création du nuanceur, ce qui gaspille les ressources. Toutefois, lorsque vous incluez le code d’octet dans un en-tête, vous pouvez réduire la complexité du code et simplifier la création de nuanceur.

Examinons à présent les différentes façons de compiler le code et les conventions de votre nuanceur pour les extensions de fichier pour le code du nuanceur.

-   [Utilisation des extensions de fichier de code du nuanceur](#using-shader-code-file-extensions)
-   [Compiler au moment de la génération dans des fichiers objets](#compiling-at-build-time-to-object-files)
-   [Compiler au moment de la génération dans des fichiers d’en-tête](#compiling-at-build-time-to-header-files)
-   [Compilation avec D3DCompileFromFile](#compiling-with-d3dcompilefromfile)
-   [Rubriques connexes](#related-topics)
-   [Rubriques connexes](#related-topics)

## <a name="using-shader-code-file-extensions"></a>Utilisation des extensions de fichier de code du nuanceur

Pour se conformer à la Convention Microsoft, utilisez les extensions de fichier suivantes pour votre code de nuanceur :

-   Un fichier avec l’extension. HLSL contient le code source[HLSL](dx-graphics-hlsl-reference.md)(High Level Shading Language).
-   Un fichier avec l’extension. CSO contient un objet de nuanceur compilé.
-   Un fichier avec l’extension. h est un fichier d’en-tête, mais dans un contexte de code de nuanceur, ce fichier d’en-tête définit un tableau d’octets qui contient les données de nuanceur.

## <a name="compiling-at-build-time-to-object-files"></a>Compiler au moment de la génération dans des fichiers objets

Si vous compilez vos fichiers. HLSL dans des fichiers objets nuanceur binaires, votre application doit lire les données de ces fichiers objets (. CSO est l’extension par défaut pour ces fichiers objets), assigner les données aux tableaux d’octets et créer des objets nuanceur à partir de ces tableaux d’octets. Par exemple, pour créer un nuanceur de sommets ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader) \* \* ), appelez la méthode [**ID3D11Device :: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) avec un tableau d’octets qui contient le code d’octet du nuanceur de sommets compilé. L' [exemple de didacticiel Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) montre comment créer des objets nuanceur à partir de tableaux d’octets qu’il a obtenus à partir de fichiers objets de nuanceur binaire. CSO. Dans cet exemple de code de l' [exemple de didacticiel Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), la propriété **fichiers de sortie** pour le fichier SimpleVertexShader. HLSL spécifie de compiler dans le fichier objet SimpleVertexShader. CSO.

```cpp
        auto vertexShaderBytecode = reader->ReadData("SimpleVertexShader.cso");
        ComPtr<ID3D11VertexShader> vertexShader;
        DX::ThrowIfFailed(
            m_d3dDevice->CreateVertexShader(
                vertexShaderBytecode->Data,
                vertexShaderBytecode->Length,
                nullptr,
                &vertexShader
                )
```

## <a name="compiling-at-build-time-to-header-files"></a>Compiler au moment de la génération dans des fichiers d’en-tête

Si vous compilez vos fichiers. HLSL dans des tableaux d’octets qui sont définis dans des fichiers d’en-tête, vous devez inclure ces fichiers d’en-tête dans votre code. L' [exemple Media extensions](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) indique comment créer des objets nuanceur à partir de tableaux d’octets qui sont définis dans des fichiers d’en-tête et que vous incluez dans votre projet au moment de la compilation. Dans cet exemple de code de l' [exemple Media extensions](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample), la propriété **fichiers de sortie** pour le fichier PixelShader. HLSL spécifie de compiler dans le tableau d’octets *g \_ psshader* défini dans le fichier d’en-tête PixelShader. h.


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a>Compilation avec D3DCompileFromFile

Vous pouvez également utiliser la fonction [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) au moment de l’exécution pour compiler le code du nuanceur. Pour plus d’informations sur la façon de procéder, consultez [Comment : compiler un nuanceur](/windows/desktop/direct3d11/how-to--compile-a-shader).

> [!Note]  
> Windows Les applications du Store prennent en charge l’utilisation de [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) pour le développement, mais pas pour le déploiement.

 

## <a name="related-topics"></a>Rubriques connexes

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 