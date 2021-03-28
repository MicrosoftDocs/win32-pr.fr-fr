---
title: DXGI_FORMAT de décompression et d’empaquetage pour la modification d’image In-Place
description: Le \_ fichier D3DX DXGIFormatConvert. inl contient des fonctions de conversion de format Inline que vous pouvez utiliser dans le nuanceur de calcul ou le nuanceur de pixels sur du matériel Direct3D 11.
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c613a3f0068537733961b58a8a4c2b4528d21f25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309577"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a><span data-ttu-id="8e0f8-103">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="8e0f8-103">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>

<span data-ttu-id="8e0f8-104">Le \_ fichier D3DX DXGIFormatConvert. inl contient des fonctions de conversion de format Inline que vous pouvez utiliser dans le nuanceur de calcul ou le nuanceur de pixels sur du matériel Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-104">The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="8e0f8-105">Vous pouvez utiliser ces fonctions dans votre application pour lire et écrire simultanément dans une texture.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-105">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="8e0f8-106">Autrement dit, vous pouvez effectuer une modification d’image sur place.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-106">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="8e0f8-107">Pour utiliser ces fonctions de conversion de format Inline, incluez le \_ fichier D3DX DXGIFormatConvert. inl dans votre application.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-107">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>

<span data-ttu-id="8e0f8-108">La vue d’accès non ordonnée (UAV) de Direct3D 11 d’une ressource Texture1D, Texture2D ou Texture3D prend en charge les lectures et écritures d’accès aléatoires dans la mémoire à partir d’un nuanceur de calcul ou d’un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-108">Direct3D 11's Unordered Access View (UAV) of a Texture1D, Texture2D, or Texture3D resource supports random access reads and writes to memory from a compute shader or pixel shader.</span></span> <span data-ttu-id="8e0f8-109">Toutefois, Direct3D 11 prend en charge simultanément la lecture et l’écriture dans uniquement le \_ format de texture dxgi format \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-109">However, Direct3D 11 supports simultaneously both reading from and writing to only the DXGI\_FORMAT\_R32\_UINT texture format.</span></span> <span data-ttu-id="8e0f8-110">Par exemple, Direct3D 11 ne prend pas en charge simultanément la lecture et l’écriture dans d’autres formats plus utiles, tels que le \_ format dxgi \_ R8G8B8A8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-110">For example, Direct3D 11 does not support simultaneously both reading from and writing to other, more useful formats, such as DXGI\_FORMAT\_R8G8B8A8\_UNORM.</span></span> <span data-ttu-id="8e0f8-111">Vous pouvez utiliser uniquement un UAV pour l’accès aléatoire en écriture dans de tels formats, ou vous pouvez utiliser uniquement un nuanceur Affichage des ressources (SRV) pour accéder de manière aléatoire à la lecture à partir d’autres formats.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-111">You can use only a UAV to random access write to such other formats, or you can use only a Shader Resource View (SRV) to random access read from such other formats.</span></span> <span data-ttu-id="8e0f8-112">Le matériel de conversion de format n’est pas disponible pour la lecture et l’écriture simultanées dans d’autres formats.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-112">Format conversion hardware is not available to simultaneously both read from and write to such other formats.</span></span>

<span data-ttu-id="8e0f8-113">Toutefois, vous pouvez toujours simultanément lire et écrire dans ces autres formats en convertissant la texture au format de texture DXGI \_ format \_ R32 \_ uint lorsque vous créez un UAV, à condition que le format d’origine de la ressource prenne en charge le cast au \_ format dxgi \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-113">However, you can still simultaneously both read from and write to such other formats by casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, as long as the original format of the resource supports casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="8e0f8-114">La plupart des formats d’élément de 32 bits prennent en charge la conversion au \_ format dxgi \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-114">Most 32 bit per element formats support casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="8e0f8-115">En effectuant un cast de la texture au \_ format de texture dxgi format \_ R32 \_ uint lorsque vous créez un UAV, vous pouvez effectuer des lectures et des écritures simultanées dans la texture tant que le nuanceur effectue une décompression de format manuel lors de la lecture et de l’empaquetage en écriture.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-115">By casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, you can then simultaneous perform reads and writes to the texture as long as the shader performs manual format unpacking on read and packing on write.</span></span>

<span data-ttu-id="8e0f8-116">L’avantage de la conversion de la texture au \_ format de texture dxgi au format \_ R32 \_ uint est que, par la suite, vous pouvez utiliser le format approprié (par exemple, DXGI \_ format \_ R16G16 \_ float) avec d’autres vues sur la même texture, telles que les vues de cible de rendu (RTVs) ou SRVs.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-116">The benefit of casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format is that later on you can use the appropriate format (for example, DXGI\_FORMAT\_R16G16\_FLOAT) with other views on the same texture, such as Render Target Views (RTVs) or SRVs.</span></span> <span data-ttu-id="8e0f8-117">Par conséquent, le matériel peut effectuer le DÉCOMPRESSION et l’empaquetage standard du format automatique, peut effectuer un filtrage de texture, et ainsi de suite lorsqu’il n’existe aucune limitation matérielle.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-117">Therefore, the hardware can perform the typical automatic format unpack and pack, can perform texture filtering, and so on where there are no hardware limitations.</span></span>

<span data-ttu-id="8e0f8-118">Dans le scénario suivant, une application doit effectuer la séquence d’actions suivante pour effectuer une modification d’image sur place.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-118">The following scenario requires that an application take the following sequence of actions to perform in-place image editing.</span></span>

<span data-ttu-id="8e0f8-119">Supposons que vous souhaitiez créer une texture sur laquelle vous pouvez utiliser un nuanceur de pixels ou un nuanceur de calcul pour effectuer une modification sur place, et que vous souhaitez que les données de texture soient stockées dans un format qui est un descendant de l’un des formats non TYPÉs suivants :</span><span class="sxs-lookup"><span data-stu-id="8e0f8-119">Suppose you want to make a texture on which you can use a pixel shader or compute shader to perform in-place editing, and you want the texture data to be stored in a format that is a descendant of one of the following TYPELESS formats:</span></span>

-   <span data-ttu-id="8e0f8-120">DXGI \_ format \_ R10G10B10A2 non \_ typé</span><span class="sxs-lookup"><span data-stu-id="8e0f8-120">DXGI\_FORMAT\_R10G10B10A2\_TYPELESS</span></span>
-   <span data-ttu-id="8e0f8-121">DXGI \_ format \_ R8G8B8A8 non \_ typé</span><span class="sxs-lookup"><span data-stu-id="8e0f8-121">DXGI\_FORMAT\_R8G8B8A8\_TYPELESS</span></span>
-   <span data-ttu-id="8e0f8-122">DXGI \_ format \_ B8G8R8A8 non \_ typé</span><span class="sxs-lookup"><span data-stu-id="8e0f8-122">DXGI\_FORMAT\_B8G8R8A8\_TYPELESS</span></span>
-   <span data-ttu-id="8e0f8-123">DXGI \_ format \_ B8G8R8X8 non \_ typé</span><span class="sxs-lookup"><span data-stu-id="8e0f8-123">DXGI\_FORMAT\_B8G8R8X8\_TYPELESS</span></span>
-   <span data-ttu-id="8e0f8-124">DXGI \_ format \_ R16G16 non \_ typé</span><span class="sxs-lookup"><span data-stu-id="8e0f8-124">DXGI\_FORMAT\_R16G16\_TYPELESS</span></span>

<span data-ttu-id="8e0f8-125">Par exemple, le format \_ dxgi \_ R10G10B10A2 \_ UNORM est un descendant du format dxgi \_ \_ R10G10B10A2 \_ type.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-125">For example, the DXGI\_FORMAT\_R10G10B10A2\_UNORM format is a descendant of the DXGI\_FORMAT\_R10G10B10A2\_TYPELESS format.</span></span> <span data-ttu-id="8e0f8-126">Par conséquent, \_ le format dxgi \_ R10G10B10A2 \_ UNORM prend en charge le modèle d’utilisation décrit dans l’ordre suivant.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-126">Therefore, DXGI\_FORMAT\_R10G10B10A2\_UNORM supports the usage pattern that is described in the following sequence.</span></span> <span data-ttu-id="8e0f8-127">Les formats qui descendent du \_ format dxgi \_ R32 \_ sans type, comme dxgi \_ format \_ R32 \_ float, sont pris en charge de manière triviale, sans nécessiter l’aide de conversion de format décrite dans l’ordre suivant.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-127">Formats that descend from DXGI\_FORMAT\_R32\_TYPELESS, such as DXGI\_FORMAT\_R32\_FLOAT, are trivially supported without requiring any of the format conversion help that is described in the following sequence.</span></span>

<span data-ttu-id="8e0f8-128">**Pour effectuer une modification d’image sur place**</span><span class="sxs-lookup"><span data-stu-id="8e0f8-128">**To perform in-place image editing**</span></span>

1.  <span data-ttu-id="8e0f8-129">Créez une texture avec le format approprié sans TYPE, qui est spécifié dans le scénario précédent avec les indicateurs de liaison requis, par exemple D3D11 \_ lier les \_ ressources d’accès non trié \_ \| d3d11 \_ lier le \_ nuanceur \_ .</span><span class="sxs-lookup"><span data-stu-id="8e0f8-129">Create a texture with the appropriate TYPELESS-dependent format that is specified in the previous scenario together with the required bind flags, such as D3D11\_BIND\_UNORDERED\_ACCESS \| D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
2.  <span data-ttu-id="8e0f8-130">Pour la modification d’image sur place, créez un UAV avec le \_ \_ format dxgi R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-130">For in-place image editing, create a UAV with the DXGI\_FORMAT\_R32\_UINT format.</span></span> <span data-ttu-id="8e0f8-131">En général, l’API Direct3D 11 n’autorise pas la conversion entre des familles de format différentes.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-131">The Direct3D 11 API typically does not allow casting between different format "families."</span></span> <span data-ttu-id="8e0f8-132">Toutefois, l’API Direct3D 11 fait une exception avec le format \_ dxgi \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-132">However, the Direct3D 11 API makes an exception with the DXGI\_FORMAT\_R32\_UINT format.</span></span>
3.  <span data-ttu-id="8e0f8-133">Dans le nuanceur de calcul ou le nuanceur de pixels, utilisez les fonctions de Pack de format inline et de décompression appropriées fournies dans le \_ fichier D3DX DXGIFormatConvert. inl.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-133">In the compute shader or pixel shader, use the appropriate inline format pack and unpack functions that are provided in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="8e0f8-134">Par exemple, supposons que le \_ format dxgi \_ R32 \_ uint UAV de la texture contienne vraiment les \_ données au format dxgi R10G10B10A2 UNORM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8e0f8-134">For example, suppose the DXGI\_FORMAT\_R32\_UINT UAV of the texture really holds DXGI\_FORMAT\_R10G10B10A2\_UNORM-formatted data.</span></span> <span data-ttu-id="8e0f8-135">Une fois que l’application a lu un uint à partir du UAV dans le nuanceur, elle doit appeler la fonction suivante pour décompresser le format de la texture :</span><span class="sxs-lookup"><span data-stu-id="8e0f8-135">After the application reads a uint from the UAV into the shader, it must call the following function to unpack the texture format:</span></span>

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    <span data-ttu-id="8e0f8-136">Ensuite, pour écrire dans le UAV dans le même nuanceur, l’application appelle la fonction suivante pour empaqueter les données de nuanceur dans un uint que l’application peut écrire dans le UAV :</span><span class="sxs-lookup"><span data-stu-id="8e0f8-136">Then, to write to the UAV in the same shader, the application calls the following function to pack shader data into a uint that the application can write to the UAV:</span></span>

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  <span data-ttu-id="8e0f8-137">L’application peut ensuite créer d’autres vues, telles que SRVs, avec le format requis.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-137">The application can then create other views, such as SRVs, with the required format.</span></span> <span data-ttu-id="8e0f8-138">Par exemple, l’application peut créer un SRV avec le format \_ dxgi \_ R10G10B10A2 \_ UNORM si la ressource a été créée en tant que \_ format dxgi R10G10B10A2 sans \_ \_ type.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-138">For example, the application can create a SRV with the DXGI\_FORMAT\_R10G10B10A2\_UNORM format if the resource was created as DXGI\_FORMAT\_R10G10B10A2\_TYPELESS.</span></span> <span data-ttu-id="8e0f8-139">Lorsqu’un nuanceur accède à ce SRV, le matériel peut effectuer une conversion automatique de type comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-139">When a shader accesses that SRV, the hardware can perform automatic type conversion as usual.</span></span>

> [!Note]  
> <span data-ttu-id="8e0f8-140">Si le nuanceur doit écrire uniquement dans un UAV ou être lu en tant que SRV, aucune de ces tâches de conversion n’est nécessaire, car vous pouvez utiliser UAVs ou SRVs entièrement typé.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-140">If the shader must write only to a UAV, or read as an SRV, none of this conversion work is needed because you can use fully typed UAVs or SRVs.</span></span> <span data-ttu-id="8e0f8-141">Les fonctions de conversion de format fournies dans D3DX \_ DXGIFormatConvert. inl sont potentiellement utiles uniquement si vous souhaitez effectuer des opérations de lecture et d’écriture simultanées dans le UAV d’une texture.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-141">The format conversion functions provided in D3DX\_DXGIFormatConvert.inl are potentially useful only if you want to perform simultaneous reading from and writing to a UAV of a texture.</span></span>

 

<span data-ttu-id="8e0f8-142">La liste suivante répertorie les fonctions de conversion de format incluses dans le \_ fichier D3DX DXGIFormatConvert. inl.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-142">The following is the list of format conversion functions that are included in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="8e0f8-143">Ces fonctions sont classées par le \_ format dxgi qu’elles décompressent et compressent.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-143">These functions are categorized by the DXGI\_FORMAT that they unpack and pack.</span></span> <span data-ttu-id="8e0f8-144">Chacun des formats pris en charge descend de l’un des formats non TYPÉs listés dans le scénario précédent et prend en charge le casting au \_ format dxgi \_ R32 \_ uint en tant que UAV.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-144">Each of the supported formats descends from one of the TYPELESS formats listed in the preceding scenario and supports casting to DXGI\_FORMAT\_R32\_UINT as a UAV.</span></span>

<dl> <dt>

<span data-ttu-id="8e0f8-145"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI \_ format \_ R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="8e0f8-145"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="8e0f8-146"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI \_ format \_ R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="8e0f8-146"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="8e0f8-147"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI \_ format \_ R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="8e0f8-147"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="8e0f8-148"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>DXGI \_ format \_ R8G8B8A8 \_ UNORM \_ sRVB</span><span class="sxs-lookup"><span data-stu-id="8e0f8-148"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="8e0f8-149">La \_ fonction inexact-type utilise des instructions de nuanceur qui n’ont pas une précision suffisamment élevée pour fournir la réponse exacte.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-149">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="8e0f8-150">La fonction alternative utilise une table de recherche stockée dans le nuanceur pour fournir une conversion de virgule flottante en SRGB >exacte.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-150">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="8e0f8-151"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI \_ format \_ R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="8e0f8-151"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI\_FORMAT\_R8G8B8A8\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="8e0f8-152"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>\_Format dxgi \_ R8G8B8A8 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="8e0f8-152"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI\_FORMAT\_R8G8B8A8\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="8e0f8-153"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>\_Format dxgi \_ R8G8B8A8 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="8e0f8-153"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>DXGI\_FORMAT\_R8G8B8A8\_SINT</span></span>
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="8e0f8-154"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI \_ format \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="8e0f8-154"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="8e0f8-155"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>DXGI \_ format \_ B8G8R8A8 \_ UNORM \_ sRVB</span><span class="sxs-lookup"><span data-stu-id="8e0f8-155"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="8e0f8-156">La \_ fonction inexact-type utilise des instructions de nuanceur qui n’ont pas une précision suffisamment élevée pour fournir la réponse exacte.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-156">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="8e0f8-157">La fonction alternative utilise une table de recherche stockée dans le nuanceur pour fournir une conversion de virgule flottante en SRGB >exacte.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-157">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="8e0f8-158"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI \_ format \_ B8G8R8X8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="8e0f8-158"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="8e0f8-159"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>DXGI \_ format \_ B8G8R8X8 \_ UNORM \_ sRVB</span><span class="sxs-lookup"><span data-stu-id="8e0f8-159"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="8e0f8-160">La \_ fonction inexact-type utilise des instructions de nuanceur qui n’ont pas une précision suffisamment élevée pour fournir la réponse exacte.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-160">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="8e0f8-161">La fonction alternative utilise une table de recherche stockée dans le nuanceur pour fournir une conversion de virgule flottante en SRGB >exacte.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-161">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="8e0f8-162"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI \_ format \_ R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="8e0f8-162"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI\_FORMAT\_R16G16\_FLOAT</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="8e0f8-163"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI \_ format \_ R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="8e0f8-163"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI\_FORMAT\_R16G16\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="8e0f8-164"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI \_ format \_ R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="8e0f8-164"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI\_FORMAT\_R16G16\_UINT</span></span>
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="8e0f8-165"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>\_Format dxgi \_ R16G16 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="8e0f8-165"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI\_FORMAT\_R16G16\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="8e0f8-166"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>\_Format dxgi \_ R16G16 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="8e0f8-166"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>DXGI\_FORMAT\_R16G16\_SINT</span></span>
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="8e0f8-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e0f8-167">Related Topics</span></span>

[<span data-ttu-id="8e0f8-168">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="8e0f8-168">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="8e0f8-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e0f8-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e0f8-170">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="8e0f8-170">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




