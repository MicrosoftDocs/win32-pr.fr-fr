---
description: Utilisation de textures compressées (Direct3D 9)
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: Utilisation de textures compressées (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 643b0618043f12ff3e1a84b806c86edb780ad929
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747604"
---
# <a name="using-compressed-textures-direct3d-9"></a><span data-ttu-id="a9945-103">Utilisation de textures compressées (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a9945-103">Using Compressed Textures (Direct3D 9)</span></span>

## <a name="determining-support-for-compressed-textures"></a><span data-ttu-id="a9945-104">Détermination de la prise en charge des textures compressées</span><span class="sxs-lookup"><span data-stu-id="a9945-104">Determining Support for Compressed Textures</span></span>

<span data-ttu-id="a9945-105">Pour tester l’adaptateur, spécifiez un format de pixel qui utilise DXT1, DXT2, DXT3, DXT4 ou DXT5.</span><span class="sxs-lookup"><span data-stu-id="a9945-105">To test the adapter, specify any pixel format that uses the DXT1, DXT2, DXT3, DXT4, or DXT5.</span></span> <span data-ttu-id="a9945-106">Si [**IDirect3D9 :: CheckDeviceFormat**](/windows/desktop/api) retourne D3D \_ OK, l’appareil peut créer une texture directement à partir d’une surface de texture compressée qui utilise ce format.</span><span class="sxs-lookup"><span data-stu-id="a9945-106">If [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) returns D3D\_OK, the device can create texture directly from a compressed texture surface that uses that format.</span></span> <span data-ttu-id="a9945-107">Si c’est le cas, vous pouvez utiliser des surfaces de texture compressées directement avec Direct3D en appelant la méthode [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="a9945-107">If so, you can use compressed texture surfaces directly with Direct3D by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="a9945-108">L’exemple de code suivant montre comment déterminer si l’adaptateur prend en charge un format de texture compressé.</span><span class="sxs-lookup"><span data-stu-id="a9945-108">The following code example shows how to determine if the adapter supports a compressed texture format.</span></span>


```
BOOL IsCompressedTextureFormatOk( D3DFORMAT TextureFormat, 
                                  D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);

    return SUCCEEDED( hr );
}
```



<span data-ttu-id="a9945-109">Si l’appareil ne prend pas en charge la texturation à partir des surfaces de texture compressées, vous pouvez toujours stocker des données de texture dans une surface formatée compressée, mais vous devez convertir toutes les textures compressées dans un format pris en charge avant de pouvoir les utiliser pour la texturation.</span><span class="sxs-lookup"><span data-stu-id="a9945-109">If the device does not support texturing from compressed texture surfaces, you can still store texture data in a compressed format surface, but you must convert any compressed textures to a supported format before they can be used for texturing.</span></span>

## <a name="creating-compressed-textures"></a><span data-ttu-id="a9945-110">Création de textures compressées</span><span class="sxs-lookup"><span data-stu-id="a9945-110">Creating Compressed Textures</span></span>

<span data-ttu-id="a9945-111">Après avoir créé un appareil qui prend en charge un format de texture compressé sur l’adaptateur, vous pouvez créer une ressource de texture compressée.</span><span class="sxs-lookup"><span data-stu-id="a9945-111">After creating a device that supports a compressed texture format on the adapter, you can create a compressed texture resource.</span></span> <span data-ttu-id="a9945-112">Appelez [**IDirect3DDevice9 :: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) et spécifiez un format de texture compressé pour le paramètre de format.</span><span class="sxs-lookup"><span data-stu-id="a9945-112">Call [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) and specify a compressed texture format for the Format parameter.</span></span>

<span data-ttu-id="a9945-113">Avant de charger une image dans un objet texture, récupérez un pointeur vers la surface de texture en appelant la méthode [**IDirect3DTexture9 :: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) .</span><span class="sxs-lookup"><span data-stu-id="a9945-113">Before loading an image into a texture object, retrieve a pointer to the texture surface by calling the [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) method.</span></span>

<span data-ttu-id="a9945-114">À présent, vous pouvez utiliser n’importe quelle fonction D3DXLoadSurfacexxx pour charger une image sur la surface Récupérée à l’aide de [**IDirect3DTexture9 :: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel).</span><span class="sxs-lookup"><span data-stu-id="a9945-114">Now you can use any D3DXLoadSurfacexxx function to load an image to the surface that was retrieved by using [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel).</span></span> <span data-ttu-id="a9945-115">Ces fonctions gèrent la conversion vers et à partir des formats de texture compressés.</span><span class="sxs-lookup"><span data-stu-id="a9945-115">These functions handle conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="a9945-116">Vous pouvez créer et convertir des fichiers de texture compressée (DDS) à l’aide de l’éditeur de texture DirectX (Dxtex.exe) fourni avec le kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="a9945-116">You can create and convert compressed texture (DDS) files using the DirectX Texture Editor (Dxtex.exe) supplied with the DirectX SDK.</span></span> <span data-ttu-id="a9945-117">Vous pouvez obtenir Dxtex.exe et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="a9945-117">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="a9945-118">Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="a9945-118">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="a9945-119">L’avantage de ce comportement est qu’une application peut copier le contenu d’une surface compressée dans un fichier sans calculer la quantité de stockage requise pour une surface d’une largeur et d’une hauteur particulières dans un format spécifique.</span><span class="sxs-lookup"><span data-stu-id="a9945-119">The advantage of this behavior is that an application can copy the contents of a compressed surface to a file without calculating how much storage is required for a surface of a particular width and height in the specific format.</span></span>

<span data-ttu-id="a9945-120">Le tableau suivant présente les cinq types de textures compressées.</span><span class="sxs-lookup"><span data-stu-id="a9945-120">The following table shows the five types of compressed textures.</span></span> <span data-ttu-id="a9945-121">Pour plus d’informations sur la façon dont les données sont stockées, consultez [formats de texture compressés (Direct3D 9)](compressed-texture-formats.md).</span><span class="sxs-lookup"><span data-stu-id="a9945-121">For more information about how the data is stored, see [Compressed Texture Formats (Direct3D 9)](compressed-texture-formats.md).</span></span> <span data-ttu-id="a9945-122">Vous avez uniquement besoin de ces informations si vous écrivez vos propres routines de compression.</span><span class="sxs-lookup"><span data-stu-id="a9945-122">You only need this information if you are writing your own compression routines.</span></span>



| <span data-ttu-id="a9945-123">FOURCC</span><span class="sxs-lookup"><span data-stu-id="a9945-123">FOURCC</span></span> | <span data-ttu-id="a9945-124">Description</span><span class="sxs-lookup"><span data-stu-id="a9945-124">Description</span></span>        | <span data-ttu-id="a9945-125">Alpha prémultiplié ?</span><span class="sxs-lookup"><span data-stu-id="a9945-125">Alpha premultiplied?</span></span> |
|--------|--------------------|----------------------|
| <span data-ttu-id="a9945-126">DXT1</span><span class="sxs-lookup"><span data-stu-id="a9945-126">DXT1</span></span>   | <span data-ttu-id="a9945-127">Alpha opaque/1 bits</span><span class="sxs-lookup"><span data-stu-id="a9945-127">Opaque/1-bit alpha</span></span> | <span data-ttu-id="a9945-128">N/A</span><span class="sxs-lookup"><span data-stu-id="a9945-128">N/A</span></span>                  |
| <span data-ttu-id="a9945-129">DXT2</span><span class="sxs-lookup"><span data-stu-id="a9945-129">DXT2</span></span>   | <span data-ttu-id="a9945-130">Alpha explicite</span><span class="sxs-lookup"><span data-stu-id="a9945-130">Explicit alpha</span></span>     | <span data-ttu-id="a9945-131">Oui</span><span class="sxs-lookup"><span data-stu-id="a9945-131">Yes</span></span>                  |
| <span data-ttu-id="a9945-132">DXT3</span><span class="sxs-lookup"><span data-stu-id="a9945-132">DXT3</span></span>   | <span data-ttu-id="a9945-133">Alpha explicite</span><span class="sxs-lookup"><span data-stu-id="a9945-133">Explicit alpha</span></span>     | <span data-ttu-id="a9945-134">Non</span><span class="sxs-lookup"><span data-stu-id="a9945-134">No</span></span>                   |
| <span data-ttu-id="a9945-135">DXT4</span><span class="sxs-lookup"><span data-stu-id="a9945-135">DXT4</span></span>   | <span data-ttu-id="a9945-136">Alphabétique interpolé</span><span class="sxs-lookup"><span data-stu-id="a9945-136">Interpolated alpha</span></span> | <span data-ttu-id="a9945-137">Oui</span><span class="sxs-lookup"><span data-stu-id="a9945-137">Yes</span></span>                  |
| <span data-ttu-id="a9945-138">DXT5</span><span class="sxs-lookup"><span data-stu-id="a9945-138">DXT5</span></span>   | <span data-ttu-id="a9945-139">Alphabétique interpolé</span><span class="sxs-lookup"><span data-stu-id="a9945-139">Interpolated alpha</span></span> | <span data-ttu-id="a9945-140">Non</span><span class="sxs-lookup"><span data-stu-id="a9945-140">No</span></span>                   |



 

<span data-ttu-id="a9945-141">Lorsque vous transférez des données d’un format nonpremultiplied vers un format prémultiplié, Direct3D met à l’échelle les couleurs en fonction des valeurs alpha.</span><span class="sxs-lookup"><span data-stu-id="a9945-141">When you transfer data from a nonpremultiplied format to a premultiplied format, Direct3D scales the colors based on the alpha values.</span></span> <span data-ttu-id="a9945-142">Le transfert de données à partir d’un format prémultiplié vers un format nonpremultiplied n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a9945-142">Transferring data from a premultiplied format to a nonpremultiplied format is not supported.</span></span> <span data-ttu-id="a9945-143">Si vous essayez de transférer des données à partir d’une source alpha prémultipliée vers une destination alpha nonpremultiplied, la méthode retourne D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a9945-143">If you try to transfer data from a premultiplied alpha source to a nonpremultiplied alpha destination, the method returns D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="a9945-144">Si vous transférez des données à partir d’une source alpha prémultipliée vers une destination qui n’a pas de valeur alpha, les composants de couleur source, qui ont été mis à l’échelle par alpha, sont copiés comme c’est le cas.</span><span class="sxs-lookup"><span data-stu-id="a9945-144">If you transfer data from a premultiplied alpha source to a destination that has no alpha, the source color components, which have been scaled by alpha, are copied as is.</span></span>

## <a name="decompressing-compressed-texture-surfaces"></a><span data-ttu-id="a9945-145">Décompression des surfaces de texture compressées</span><span class="sxs-lookup"><span data-stu-id="a9945-145">Decompressing Compressed Texture Surfaces</span></span>

<span data-ttu-id="a9945-146">Comme pour la compression d’une surface de texture, la décompression d’une texture compressée est effectuée via les services de copie Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a9945-146">As with compressing a texture surface, decompressing a compressed texture is performed through Direct3D copying services.</span></span>

<span data-ttu-id="a9945-147">Pour copier une surface de texture compressée dans une surface de texture non compressée, utilisez la fonction [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md).</span><span class="sxs-lookup"><span data-stu-id="a9945-147">To copy a compressed texture surface to a uncompressed texture surface, use the function [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md).</span></span> <span data-ttu-id="a9945-148">Cette fonction gère la compression vers et à partir des surfaces compressées et non compressées.</span><span class="sxs-lookup"><span data-stu-id="a9945-148">This functions handles compression to and from compressed and uncompressed surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9945-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a9945-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9945-150">Ressources de texture compressées</span><span class="sxs-lookup"><span data-stu-id="a9945-150">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 
