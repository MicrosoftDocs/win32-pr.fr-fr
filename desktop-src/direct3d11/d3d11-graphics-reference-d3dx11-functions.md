---
title: Fonctions D3DX (graphiques Direct3D 11)
description: Cette section contient des informations sur les fonctions D3DX 11.
ms.assetid: 7548c02e-c8c2-4629-95ac-d21ca7a39f0a
keywords:
- fonctions, DirectX 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b4c98dda5f85f03af1add120d22b95fa620d4a45e8e4db80d3b607f2c3e70e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126053"
---
# <a name="d3dx-functions-direct3d-11-graphics"></a>Fonctions D3DX (graphiques Direct3D 11)

Cette section contient des informations sur les fonctions D3DX 11.

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 


## <a name="in-this-section"></a>Contenu de cette section



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> .
</blockquote>
<br/> Compilez un nuanceur ou un effet à partir d’un fichier.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .
</blockquote>
<br/> Compilez un nuanceur ou un effet qui est chargé en mémoire.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser des <a href="/windows/desktop/menurc/resources-functions">fonctions de ressource</a>, puis de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .
</blockquote>
<br/> Compilez un nuanceur ou un effet à partir d’une ressource.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>ComputeNormalMap</strong>.
</blockquote>
<br/> Convertit une carte de hauteur en une carte normale. Les composants (x, y, z) de chaque normal sont mappés aux canaux (r, g, b) de la texture de sortie.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Consultez la section Notes.
</blockquote>
<br/> Créer un processeur de données asynchrones pour un nuanceur.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Consultez la section Notes.
</blockquote>
<br/> Créez un chargeur de fichiers asynchrones.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Consultez la section Notes.
</blockquote>
<br/> Créez un chargeur de mémoire asynchrone.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Consultez la section Notes.
</blockquote>
<br/> Créez un chargeur de ressources asynchrones.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Consultez la section Notes.
</blockquote>
<br/> Créer un processeur de données pour un nuanceur de manière asynchrone.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Consultez la section Notes.
</blockquote>
<br/> Créez un processeur de données à utiliser avec une <a href="id3dx11threadpump.md"><strong>pompe de thread</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Consultez la section Notes.
</blockquote>
<br/> Créez un processeur de données à utiliser avec une <a href="id3dx11threadpump.md"><strong>pompe de thread</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Consultez la section Notes.
</blockquote>
<br/> Créez un processeur de données qui chargera une ressource, puis créez une vue de ressource de nuanceur pour celle-ci. Les processeurs de données sont un composant de la fonctionnalité de chargement de données asynchrone dans D3DX11 qui utilise des <a href="id3dx11threadpump.md"><strong>pompes de thread</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les éléments suivants :</p>
<ul>
<li>Bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMFILE</strong> (où xxx est DDS ou WIC)</li>
<li>Bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXFILE</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Créer un affichage des ressources de nuanceur à partir d’un fichier.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les éléments suivants :</p>
<ul>
<li>Bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (où xxx est DDS ou WIC)</li>
<li>Bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Créer un affichage des ressources de nuanceur à partir d’un fichier en mémoire.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les <a href="/windows/desktop/menurc/resources-functions">fonctions de ressource</a>, puis les suivantes :</p>
<ul>
<li>Bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (où xxx est DDS ou WIC)</li>
<li>Bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Créer un affichage des ressources de nuanceur à partir d’une ressource.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les éléments suivants :</p>
<ul>
<li>Bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMFILE</strong> (où xxx est DDS ou WIC)</li>
<li>Bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXFILE</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> Créer une ressource de texture à partir d’un fichier.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les éléments suivants :</p>
<ul>
<li>Bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (où xxx est DDS ou WIC)</li>
<li>Bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> Créer une ressource de texture à partir d’un fichier résidant dans la mémoire système.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les <a href="/windows/desktop/menurc/resources-functions">fonctions de ressource</a>, puis les suivantes :</p>
<ul>
<li>Bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (où xxx est DDS ou WIC)</li>
<li>Bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> Créer une texture à partir d’une autre ressource.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Consultez la section Notes.
</blockquote>
<br/> Créer une pompe de thread.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GenerateMipMaps</strong> et <strong>GenerateMipMaps3D</strong>.
</blockquote>
<br/> Génère une chaîne mipmap à l’aide d’un filtre de texture particulier.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GETMETADATAFROMXXXFILE</strong> (où xxx est WIC, DDS ou TGA. WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.
</blockquote>
<br/> Récupère des informations sur un fichier image donné.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GETMETADATAFROMXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA. WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.
</blockquote>
<br/> Obtenir des informations sur une image déjà chargée en mémoire.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les <a href="/windows/desktop/menurc/resources-functions">fonctions de ressource</a>, puis d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (outils), <strong>LOADFROMXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA). WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.
</blockquote>
<br/> Récupère des informations sur une image donnée dans une ressource.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>Redimensionner</strong>, <strong>convertir</strong>, <strong>compresser</strong>, <strong>décompresser</strong>et/ou <strong>CopyRectangle</strong>.
</blockquote>
<br/> Charge une texture à partir d’une texture.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser l’API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .
</blockquote>
<br/> Créer un nuanceur à partir d’un fichier sans le compiler.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser l’API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .
</blockquote>
<br/> Créer un nuanceur à partir de la mémoire sans le compiler.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser l’API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .
</blockquote>
<br/> Créez un nuanceur à partir d’une ressource sans le compiler.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> Then <strong>SAVETOXXXFILE</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux. Pour le scénario simplifié de création d’une capture d’écran à partir d’une texture de cible de rendu, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> , <strong>SaveDDSTextureToFile</strong> ou <strong>SaveWICTextureToFile</strong>.
</blockquote>
<br/> Enregistrer une texture dans un fichier.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> Then <strong>SAVETOXXXMEMORY</strong> (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.
</blockquote>
<br/> Enregistrer une texture dans la mémoire.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">mathématique des harmoniques sphériques</a> , <strong>SHProjectCubeMap</strong>.
</blockquote>
<br/> Projette une fonction représentée dans un mappage de cube dans des harmoniques sphériques.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la méthode <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>ID3D11DeviceContext :: ClearState</strong></a> .
</blockquote>
<br/> Supprime toutes les ressources de l’appareil en affectant à leurs pointeurs la <strong>valeur null</strong>. Cela doit être appelé lors de l’arrêt de votre application. Cela permet de s’assurer que, lorsque l’un d’eux libère toutes ses ressources, aucune d’entre elles n’est liée à l’appareil.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

