---
title: Fonctions D3DX (graphiques Direct3D 11)
description: Cette section contient des informations sur les fonctions D3DX 11.
ms.assetid: 7548c02e-c8c2-4629-95ac-d21ca7a39f0a
keywords:
- fonctions, DirectX 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b76c1764f464461b4800a9161ac37dcff8c539a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383535"
---
# <a name="d3dx-functions-direct3d-11-graphics"></a><span data-ttu-id="9f05c-104">Fonctions D3DX (graphiques Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="9f05c-104">D3DX Functions (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="9f05c-105">Cette section contient des informations sur les fonctions D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="9f05c-105">This section contains information about the D3DX 11 functions.</span></span>

> [!Note]  
> <span data-ttu-id="9f05c-106">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 


## <a name="in-this-section"></a><span data-ttu-id="9f05c-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="9f05c-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f05c-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="9f05c-108">Topic</span></span></th>
<th><span data-ttu-id="9f05c-109">Description</span><span class="sxs-lookup"><span data-stu-id="9f05c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9f05c-110"><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-110"><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-111">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-111">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-112">Au lieu d’utiliser cette fonction, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9f05c-112">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-113">Compilez un nuanceur ou un effet à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="9f05c-113">Compile a shader or an effect from a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-114"><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-114"><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-115">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-115">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-116">Au lieu d’utiliser cette fonction, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9f05c-116">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-117">Compilez un nuanceur ou un effet qui est chargé en mémoire.</span><span class="sxs-lookup"><span data-stu-id="9f05c-117">Compile a shader or an effect that is loaded in memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-118"><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-118"><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-119">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-119">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-120">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser des <a href="/windows/desktop/menurc/resources-functions">fonctions de ressource</a>, puis de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9f05c-120">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-121">Compilez un nuanceur ou un effet à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="9f05c-121">Compile a shader or an effect from a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-122"><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-122"><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-123">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-123">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-124">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>ComputeNormalMap</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f05c-124">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>ComputeNormalMap</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-125">Convertit une carte de hauteur en une carte normale.</span><span class="sxs-lookup"><span data-stu-id="9f05c-125">Converts a height map into a normal map.</span></span> <span data-ttu-id="9f05c-126">Les composants (x, y, z) de chaque normal sont mappés aux canaux (r, g, b) de la texture de sortie.</span><span class="sxs-lookup"><span data-stu-id="9f05c-126">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-127"><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-127"><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-128">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-128">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="9f05c-129">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="9f05c-129">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-130">Créer un processeur de données asynchrones pour un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="9f05c-130">Create an asynchronous-data processor for a shader.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-131"><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-131"><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-132">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-132">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="9f05c-133">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="9f05c-133">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-134">Créez un chargeur de fichiers asynchrones.</span><span class="sxs-lookup"><span data-stu-id="9f05c-134">Create an asynchronous-file loader.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-135"><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-135"><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-136">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-136">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="9f05c-137">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="9f05c-137">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-138">Créez un chargeur de mémoire asynchrone.</span><span class="sxs-lookup"><span data-stu-id="9f05c-138">Create an asynchronous-memory loader.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-139"><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-139"><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-140">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-140">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="9f05c-141">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="9f05c-141">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-142">Créez un chargeur de ressources asynchrones.</span><span class="sxs-lookup"><span data-stu-id="9f05c-142">Create an asynchronous-resource loader.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-143"><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-143"><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-144">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-144">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="9f05c-145">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="9f05c-145">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-146">Créer un processeur de données pour un nuanceur de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="9f05c-146">Create a data processor for a shader asynchronously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-147"><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-147"><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-148">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-148">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="9f05c-149">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="9f05c-149">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-150">Créez un processeur de données à utiliser avec une <a href="id3dx11threadpump.md"><strong>pompe de thread</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9f05c-150">Create a data processor to be used with a <a href="id3dx11threadpump.md"><strong>thread pump</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-151"><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-151"><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-152">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-152">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="9f05c-153">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="9f05c-153">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-154">Créez un processeur de données à utiliser avec une <a href="id3dx11threadpump.md"><strong>pompe de thread</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9f05c-154">Create a data processor to be used with a <a href="id3dx11threadpump.md"><strong>thread pump</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-155"><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-155"><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-156">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-156">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="9f05c-157">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="9f05c-157">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-158">Créez un processeur de données qui chargera une ressource, puis créez une vue de ressource de nuanceur pour celle-ci.</span><span class="sxs-lookup"><span data-stu-id="9f05c-158">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="9f05c-159">Les processeurs de données sont un composant de la fonctionnalité de chargement de données asynchrone dans D3DX11 qui utilise des <a href="id3dx11threadpump.md"><strong>pompes de thread</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9f05c-159">Data processors are a component of the asynchronous data loading feature in D3DX11 that uses <a href="id3dx11threadpump.md"><strong>thread pumps</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-160"><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-160"><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-161">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-161">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="9f05c-162">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9f05c-162">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="9f05c-163">Bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMFILE</strong> (où xxx est DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="9f05c-163"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromFile</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="9f05c-164">Bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXFILE</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis <strong>CreateShaderResourceView</strong></span><span class="sxs-lookup"><span data-stu-id="9f05c-164"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="9f05c-165">Créer un affichage des ressources de nuanceur à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="9f05c-165">Create a shader-resource view from a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-166"><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-166"><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-167">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-167">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="9f05c-168">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9f05c-168">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="9f05c-169">Bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (où xxx est DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="9f05c-169"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="9f05c-170">Bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis <strong>CreateShaderResourceView</strong></span><span class="sxs-lookup"><span data-stu-id="9f05c-170"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="9f05c-171">Créer un affichage des ressources de nuanceur à partir d’un fichier en mémoire.</span><span class="sxs-lookup"><span data-stu-id="9f05c-171">Create a shader-resource view from a file in memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-172"><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-172"><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-173">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-173">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="9f05c-174">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les <a href="/windows/desktop/menurc/resources-functions">fonctions de ressource</a>, puis les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9f05c-174">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then these:</span></span></p>
<ul>
<li><span data-ttu-id="9f05c-175">Bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (où xxx est DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="9f05c-175"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="9f05c-176">Bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis <strong>CreateShaderResourceView</strong></span><span class="sxs-lookup"><span data-stu-id="9f05c-176"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="9f05c-177">Créer un affichage des ressources de nuanceur à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="9f05c-177">Create a shader-resource view from a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-178"><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-178"><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-179">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-179">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="9f05c-180">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9f05c-180">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="9f05c-181">Bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMFILE</strong> (où xxx est DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="9f05c-181"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromFile</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="9f05c-182">Bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXFILE</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis <strong>CreateTexture</strong></span><span class="sxs-lookup"><span data-stu-id="9f05c-182"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="9f05c-183">Créer une ressource de texture à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="9f05c-183">Create a texture resource from a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-184"><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-184"><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-185">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-185">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="9f05c-186">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9f05c-186">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="9f05c-187">Bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (où xxx est DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="9f05c-187"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="9f05c-188">Bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis <strong>CreateTexture</strong></span><span class="sxs-lookup"><span data-stu-id="9f05c-188"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="9f05c-189">Créer une ressource de texture à partir d’un fichier résidant dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="9f05c-189">Create a texture resource from a file residing in system memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-190"><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-190"><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-191">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-191">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="9f05c-192">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les <a href="/windows/desktop/menurc/resources-functions">fonctions de ressource</a>, puis les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9f05c-192">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then these:</span></span></p>
<ul>
<li><span data-ttu-id="9f05c-193">Bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (où xxx est DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="9f05c-193"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="9f05c-194">Bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis <strong>CreateTexture</strong></span><span class="sxs-lookup"><span data-stu-id="9f05c-194"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="9f05c-195">Créer une texture à partir d’une autre ressource.</span><span class="sxs-lookup"><span data-stu-id="9f05c-195">Create a texture from another resource.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-196"><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-196"><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-197">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-197">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="9f05c-198">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="9f05c-198">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-199">Créer une pompe de thread.</span><span class="sxs-lookup"><span data-stu-id="9f05c-199">Create a thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-200"><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-200"><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-201">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-201">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-202">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GenerateMipMaps</strong> et <strong>GenerateMipMaps3D</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f05c-202">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GenerateMipMaps</strong> and <strong>GenerateMipMaps3D</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-203">Génère une chaîne mipmap à l’aide d’un filtre de texture particulier.</span><span class="sxs-lookup"><span data-stu-id="9f05c-203">Generates mipmap chain using a particular texture filter.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-204"><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-204"><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-205">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-205">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-206">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GETMETADATAFROMXXXFILE</strong> (où xxx est WIC, DDS ou TGA. WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.</span><span class="sxs-lookup"><span data-stu-id="9f05c-206">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GetMetadataFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-207">Récupère des informations sur un fichier image donné.</span><span class="sxs-lookup"><span data-stu-id="9f05c-207">Retrieves information about a given image file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-208"><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-208"><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-209">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-209">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-210">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GETMETADATAFROMXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA. WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.</span><span class="sxs-lookup"><span data-stu-id="9f05c-210">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GetMetadataFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-211">Obtenir des informations sur une image déjà chargée en mémoire.</span><span class="sxs-lookup"><span data-stu-id="9f05c-211">Get information about an image already loaded into memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-212"><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-212"><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-213">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-213">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-214">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les <a href="/windows/desktop/menurc/resources-functions">fonctions de ressource</a>, puis d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA). WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.</span><span class="sxs-lookup"><span data-stu-id="9f05c-214">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then use <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-215">Récupère des informations sur une image donnée dans une ressource.</span><span class="sxs-lookup"><span data-stu-id="9f05c-215">Retrieves information about a given image in a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-216"><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-216"><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-217">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-217">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-218">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>Redimensionner</strong>, <strong>convertir</strong>, <strong>compresser</strong>, <strong>décompresser</strong>et/ou <strong>CopyRectangle</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f05c-218">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>Resize</strong>, <strong>Convert</strong>, <strong>Compress</strong>, <strong>Decompress</strong>, and/or <strong>CopyRectangle</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-219">Charge une texture à partir d’une texture.</span><span class="sxs-lookup"><span data-stu-id="9f05c-219">Load a texture from a texture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-220"><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-220"><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-221">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-221">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-222">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser l’API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9f05c-222">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-223">Créer un nuanceur à partir d’un fichier sans le compiler.</span><span class="sxs-lookup"><span data-stu-id="9f05c-223">Create a shader from a file without compiling it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-224"><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-224"><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-225">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-225">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-226">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser l’API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9f05c-226">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-227">Créer un nuanceur à partir de la mémoire sans le compiler.</span><span class="sxs-lookup"><span data-stu-id="9f05c-227">Create a shader from memory without compiling it.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-228"><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-228"><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-229">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-229">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-230">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser l’API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9f05c-230">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-231">Créez un nuanceur à partir d’une ressource sans le compiler.</span><span class="sxs-lookup"><span data-stu-id="9f05c-231">Create a shader from a resource without compiling it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-232"><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-232"><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-233">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-233">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-234">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> Then <strong>SAVETOXXXFILE</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.</span><span class="sxs-lookup"><span data-stu-id="9f05c-234">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>CaptureTexture</strong> then <strong>SaveToXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span> <span data-ttu-id="9f05c-235">Pour le scénario simplifié de création d’une capture d’écran à partir d’une texture de cible de rendu, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> , <strong>SaveDDSTextureToFile</strong> ou <strong>SaveWICTextureToFile</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f05c-235">For the simplified scenario of creating a screen shot from a render target texture, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library, <strong>SaveDDSTextureToFile</strong> or <strong>SaveWICTextureToFile</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-236">Enregistrer une texture dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="9f05c-236">Save a texture to a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-237"><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-237"><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-238">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-238">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-239">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> Then <strong>SAVETOXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.</span><span class="sxs-lookup"><span data-stu-id="9f05c-239">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>CaptureTexture</strong> then <strong>SaveToXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-240">Enregistrer une texture dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="9f05c-240">Save a texture to memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f05c-241"><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-241"><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-242">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-242">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-243">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">mathématique des harmoniques sphériques</a> , <strong>SHProjectCubeMap</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f05c-243">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">Spherical Harmonics Math</a> library, <strong>SHProjectCubeMap</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-244">Projette une fonction représentée dans un mappage de cube dans des harmoniques sphériques.</span><span class="sxs-lookup"><span data-stu-id="9f05c-244">Projects a function represented in a cube map into spherical harmonics.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f05c-245"><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f05c-245"><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-246">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f05c-246">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f05c-247">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la méthode <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>ID3D11DeviceContext :: ClearState</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9f05c-247">Instead of using this function, we recommend that you use the <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>ID3D11DeviceContext::ClearState</strong></a> method.</span></span>
</blockquote>
<br/> <span data-ttu-id="9f05c-248">Supprime toutes les ressources de l’appareil en affectant à leurs pointeurs la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f05c-248">Removes all resources from the device by setting their pointers to <strong>NULL</strong>.</span></span> <span data-ttu-id="9f05c-249">Cela doit être appelé lors de l’arrêt de votre application.</span><span class="sxs-lookup"><span data-stu-id="9f05c-249">This should be called during shutdown of your application.</span></span> <span data-ttu-id="9f05c-250">Cela permet de s’assurer que, lorsque l’un d’eux libère toutes ses ressources, aucune d’entre elles n’est liée à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9f05c-250">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="9f05c-251">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9f05c-251">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f05c-252">Référence D3DX 11</span><span class="sxs-lookup"><span data-stu-id="9f05c-252">D3DX 11 Reference</span></span>](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

