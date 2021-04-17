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
ms.openlocfilehash: 3ea71da99dd68769324b07d3fc76a0c5ca00009d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315527"
---
# <a name="compiling-shaders"></a><span data-ttu-id="694f3-103">Compilation des nuanceurs</span><span class="sxs-lookup"><span data-stu-id="694f3-103">Compiling shaders</span></span>

> [!NOTE]
> <span data-ttu-id="694f3-104">Cette rubrique couvre le `FXC.EXE` compilateur utilisé pour les modèles de nuanceur 2 à 5,1.</span><span class="sxs-lookup"><span data-stu-id="694f3-104">This topic covers the `FXC.EXE` compiler used for Shader Models 2 through 5.1.</span></span> <span data-ttu-id="694f3-105">Pour le nuancier modèle 6, vous utilisez `DXC.EXE` à la place, qui est documenté dans [utilisation de dxc.exe et dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).</span><span class="sxs-lookup"><span data-stu-id="694f3-105">For Shader Model 6, you use `DXC.EXE` instead, which is documented in [Using dxc.exe and dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).</span></span>

<span data-ttu-id="694f3-106">Microsoft Visual Studio 2012 peut maintenant compiler du code de nuanceur à partir de \* fichiers. HLSL que vous incluez dans votre projet C++.</span><span class="sxs-lookup"><span data-stu-id="694f3-106">Microsoft Visual Studio 2012 can now compile shader code from \*.hlsl files that you include in your C++ project.</span></span>

<span data-ttu-id="694f3-107">Dans le cadre du processus de génération, Visual Studio 2012 utilise le compilateur de code [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL pour compiler les fichiers. HLSL dans des fichiers objets de nuanceur binaire ou dans des tableaux d’octets définis dans des fichiers d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="694f3-107">As part of the build process, Visual Studio 2012 uses the [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL code compiler to compile the .hlsl files into binary shader object files or into byte arrays that are defined in header files.</span></span> <span data-ttu-id="694f3-108">La façon dont le compilateur de code HLSL compile chaque fichier. HLSL dans votre projet dépend de la manière dont vous spécifiez la propriété **fichiers de sortie** pour ce fichier.</span><span class="sxs-lookup"><span data-stu-id="694f3-108">How the HLSL code compiler compiles each .hlsl file in your project depends on how you specify the **Ouput Files** property for that file.</span></span> <span data-ttu-id="694f3-109">Pour plus d’informations sur les pages de propriétés HLSL, consultez [HLSL Property pages](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).</span><span class="sxs-lookup"><span data-stu-id="694f3-109">For more info about HLSL property pages, see [HLSL Property Pages](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).</span></span>

<span data-ttu-id="694f3-110">La méthode de compilation que vous utilisez en général dépend de la taille de votre \* fichier. HLSL.</span><span class="sxs-lookup"><span data-stu-id="694f3-110">The compile method that you use typically depends on the size of your \*.hlsl file.</span></span> <span data-ttu-id="694f3-111">Si vous incluez une grande quantité de code d’octet dans un en-tête, vous augmentez la taille et le temps de chargement initial de votre application.</span><span class="sxs-lookup"><span data-stu-id="694f3-111">If you include a large amount of byte code in a header, you increase the size and the initial load time of your app.</span></span> <span data-ttu-id="694f3-112">Vous forcez également tous les codes d’octet à résider en mémoire même après la création du nuanceur, ce qui gaspille les ressources.</span><span class="sxs-lookup"><span data-stu-id="694f3-112">You also force all byte code to reside in memory even after the shader is created, which wastes resources.</span></span> <span data-ttu-id="694f3-113">Toutefois, lorsque vous incluez le code d’octet dans un en-tête, vous pouvez réduire la complexité du code et simplifier la création de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="694f3-113">But when you include byte code in a header, you can reduce code complexity and simplify shader creation.</span></span>

<span data-ttu-id="694f3-114">Examinons à présent les différentes façons de compiler le code et les conventions de votre nuanceur pour les extensions de fichier pour le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="694f3-114">Let's now look at various ways to compile your shader code and conventions for file extensions for shader code.</span></span>

-   [<span data-ttu-id="694f3-115">Utilisation des extensions de fichier de code du nuanceur</span><span class="sxs-lookup"><span data-stu-id="694f3-115">Using shader code file extensions</span></span>](#using-shader-code-file-extensions)
-   [<span data-ttu-id="694f3-116">Compiler au moment de la génération dans des fichiers objets</span><span class="sxs-lookup"><span data-stu-id="694f3-116">Compiling at build time to object files</span></span>](#compiling-at-build-time-to-object-files)
-   [<span data-ttu-id="694f3-117">Compiler au moment de la génération dans des fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="694f3-117">Compiling at build time to header files</span></span>](#compiling-at-build-time-to-header-files)
-   [<span data-ttu-id="694f3-118">Compilation avec D3DCompileFromFile</span><span class="sxs-lookup"><span data-stu-id="694f3-118">Compiling with D3DCompileFromFile</span></span>](#compiling-with-d3dcompilefromfile)
-   [<span data-ttu-id="694f3-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="694f3-119">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="694f3-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="694f3-120">Related topics</span></span>](#related-topics)

## <a name="using-shader-code-file-extensions"></a><span data-ttu-id="694f3-121">Utilisation des extensions de fichier de code du nuanceur</span><span class="sxs-lookup"><span data-stu-id="694f3-121">Using shader code file extensions</span></span>

<span data-ttu-id="694f3-122">Pour se conformer à la Convention Microsoft, utilisez les extensions de fichier suivantes pour votre code de nuanceur :</span><span class="sxs-lookup"><span data-stu-id="694f3-122">To conform to Microsoft convention, use these file extensions for your shader code:</span></span>

-   <span data-ttu-id="694f3-123">Un fichier avec l’extension. HLSL contient le code source[HLSL](dx-graphics-hlsl-reference.md)(High Level Shading Language).</span><span class="sxs-lookup"><span data-stu-id="694f3-123">A file with the .hlsl extension holds High Level Shading Language ([HLSL](dx-graphics-hlsl-reference.md)) source code.</span></span>
-   <span data-ttu-id="694f3-124">Un fichier avec l’extension. CSO contient un objet de nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="694f3-124">A file with the .cso extension holds a compiled shader object.</span></span>
-   <span data-ttu-id="694f3-125">Un fichier avec l’extension. h est un fichier d’en-tête, mais dans un contexte de code de nuanceur, ce fichier d’en-tête définit un tableau d’octets qui contient les données de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="694f3-125">A file with the .h extension is a header file, but in a shader code context, this header file defines a byte array that holds shader data.</span></span>

## <a name="compiling-at-build-time-to-object-files"></a><span data-ttu-id="694f3-126">Compiler au moment de la génération dans des fichiers objets</span><span class="sxs-lookup"><span data-stu-id="694f3-126">Compiling at build time to object files</span></span>

<span data-ttu-id="694f3-127">Si vous compilez vos fichiers. HLSL dans des fichiers objets nuanceur binaires, votre application doit lire les données de ces fichiers objets (. CSO est l’extension par défaut pour ces fichiers objets), assigner les données aux tableaux d’octets et créer des objets nuanceur à partir de ces tableaux d’octets.</span><span class="sxs-lookup"><span data-stu-id="694f3-127">If you compile your .hlsl files into binary shader object files, your app needs to read the data from those object files (.cso is the default extension for these object files), assign the data to byte arrays, and create shader objects from those byte arrays.</span></span> <span data-ttu-id="694f3-128">Par exemple, pour créer un nuanceur de sommets ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader) \* \* ), appelez la méthode [**ID3D11Device :: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) avec un tableau d’octets qui contient le code d’octet du nuanceur de sommets compilé.</span><span class="sxs-lookup"><span data-stu-id="694f3-128">For example, to create a vertex shader ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader)\*\*), call the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method with a byte array that contains compiled vertex shader byte code.</span></span> <span data-ttu-id="694f3-129">L' [exemple de didacticiel Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) montre comment créer des objets nuanceur à partir de tableaux d’octets qu’il a obtenus à partir de fichiers objets de nuanceur binaire. CSO.</span><span class="sxs-lookup"><span data-stu-id="694f3-129">The [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) shows how to create shader objects from byte arrays that it obtained from .cso binary shader object files.</span></span> <span data-ttu-id="694f3-130">Dans cet exemple de code de l' [exemple de didacticiel Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), la propriété **fichiers de sortie** pour le fichier SimpleVertexShader. HLSL spécifie de compiler dans le fichier objet SimpleVertexShader. CSO.</span><span class="sxs-lookup"><span data-stu-id="694f3-130">In this example code from the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), the **Ouput Files** property for the SimpleVertexShader.hlsl file specifies to compile into the SimpleVertexShader.cso object file.</span></span>

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

## <a name="compiling-at-build-time-to-header-files"></a><span data-ttu-id="694f3-131">Compiler au moment de la génération dans des fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="694f3-131">Compiling at build time to header files</span></span>

<span data-ttu-id="694f3-132">Si vous compilez vos fichiers. HLSL dans des tableaux d’octets qui sont définis dans des fichiers d’en-tête, vous devez inclure ces fichiers d’en-tête dans votre code.</span><span class="sxs-lookup"><span data-stu-id="694f3-132">If you compile your .hlsl files into byte arrays that are defined in header files, you need to include those header files in your code.</span></span> <span data-ttu-id="694f3-133">L' [exemple Media extensions](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) indique comment créer des objets nuanceur à partir de tableaux d’octets qui sont définis dans des fichiers d’en-tête et que vous incluez dans votre projet au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="694f3-133">The [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) shows how to create shader objects from byte arrays that are defined in header files and that you include in your project at compile time.</span></span> <span data-ttu-id="694f3-134">Dans cet exemple de code de l' [exemple Media extensions](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample), la propriété **fichiers de sortie** pour le fichier PixelShader. HLSL spécifie de compiler dans le tableau d’octets *g \_ psshader* défini dans le fichier d’en-tête PixelShader. h.</span><span class="sxs-lookup"><span data-stu-id="694f3-134">In this example code from the [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample), the **Ouput Files** property for the PixelShader.hlsl file specifies to compile into the *g\_psshader* byte array that is defined in the PixelShader.h header file.</span></span>


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a><span data-ttu-id="694f3-135">Compilation avec D3DCompileFromFile</span><span class="sxs-lookup"><span data-stu-id="694f3-135">Compiling with D3DCompileFromFile</span></span>

<span data-ttu-id="694f3-136">Vous pouvez également utiliser la fonction [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) au moment de l’exécution pour compiler le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="694f3-136">You can also use the [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function at run time to compile shader code.</span></span> <span data-ttu-id="694f3-137">Pour plus d’informations sur la façon de procéder, consultez [Comment : compiler un nuanceur](/windows/desktop/direct3d11/how-to--compile-a-shader).</span><span class="sxs-lookup"><span data-stu-id="694f3-137">For more info about how to do this, see [How To: Compile a Shader](/windows/desktop/direct3d11/how-to--compile-a-shader).</span></span>

> [!Note]  
> <span data-ttu-id="694f3-138">Les applications du Windows Store prennent en charge l’utilisation de [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) pour le développement, mais pas pour le déploiement.</span><span class="sxs-lookup"><span data-stu-id="694f3-138">Windows Store apps support using [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) for development but not for deployment.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="694f3-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="694f3-139">Related Topics</span></span>

[<span data-ttu-id="694f3-140">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="694f3-140">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="694f3-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="694f3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="694f3-142">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="694f3-142">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 