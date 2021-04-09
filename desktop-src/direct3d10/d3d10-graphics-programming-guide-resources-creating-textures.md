---
description: Une ressource de texture est une collection structurée de données.
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: Création de ressources de texture (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950666"
---
# <a name="creating-texture-resources-direct3d-10"></a><span data-ttu-id="281bd-103">Création de ressources de texture (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="281bd-103">Creating Texture Resources (Direct3D 10)</span></span>

<span data-ttu-id="281bd-104">Une ressource de [texture](d3d10-graphics-programming-guide-resources-types.md) est une collection structurée de données.</span><span class="sxs-lookup"><span data-stu-id="281bd-104">A [texture](d3d10-graphics-programming-guide-resources-types.md) resource is a structured collection of data.</span></span> <span data-ttu-id="281bd-105">En règle générale, les valeurs de couleur sont stockées dans des textures et sont accessibles pendant le rendu par le [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) à différentes étapes à la fois pour l’entrée et la sortie.</span><span class="sxs-lookup"><span data-stu-id="281bd-105">Typically, color values are stored in textures and accessed during rendering by the [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) at various stages for both input and output.</span></span> <span data-ttu-id="281bd-106">La création de textures et la définition de la façon dont elles seront utilisées sont une partie importante du rendu des scènes attrayantes dans Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="281bd-106">Creating textures and defining how they will be used is an important part of rendering interesting-looking scenes in Direct3D 10.</span></span>

<span data-ttu-id="281bd-107">Bien que les textures contiennent généralement des informations de couleur, la création de textures à l’aide de différents [**\_ formats de dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) leur permet de stocker différents types de données.</span><span class="sxs-lookup"><span data-stu-id="281bd-107">Even though textures typically contain color information, creating textures using different [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enables them to store different kinds of data.</span></span> <span data-ttu-id="281bd-108">Ces données peuvent ensuite être exploitées par le pipeline Direct3D 10 de manière non traditionnelle.</span><span class="sxs-lookup"><span data-stu-id="281bd-108">This data can then be leveraged by the Direct3D 10 pipeline in non-traditional ways.</span></span>

<span data-ttu-id="281bd-109">Toutes les textures ont des limites sur la quantité de mémoire qu’elles consomment et le nombre de texels qu’elles contiennent.</span><span class="sxs-lookup"><span data-stu-id="281bd-109">All textures have limits on how much memory they consume, and how many texels they contain.</span></span> <span data-ttu-id="281bd-110">Ces limites sont spécifiées par des [constantes de ressources](d3d10-graphics-reference-resource-constants.md).</span><span class="sxs-lookup"><span data-stu-id="281bd-110">These limits are specified by [resource constants](d3d10-graphics-reference-resource-constants.md).</span></span>

-   [<span data-ttu-id="281bd-111">Créer une texture à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="281bd-111">Create a Texture from a File</span></span>](#create-a-texture-from-a-file)
    -   [<span data-ttu-id="281bd-112">Créer une texture et une vue séparément</span><span class="sxs-lookup"><span data-stu-id="281bd-112">Create Texture and View Separately</span></span>](#create-texture-and-view-separately)
    -   [<span data-ttu-id="281bd-113">Créer une texture et une vue simultanément</span><span class="sxs-lookup"><span data-stu-id="281bd-113">Create Texture and View Simultaneously</span></span>](#create-texture-and-view-simultaneously)
-   [<span data-ttu-id="281bd-114">Création de textures vides</span><span class="sxs-lookup"><span data-stu-id="281bd-114">Creating Empty Textures</span></span>](#creating-empty-textures)
    -   [<span data-ttu-id="281bd-115">Rendu dans une texture</span><span class="sxs-lookup"><span data-stu-id="281bd-115">Rendering to a texture</span></span>](#rendering-to-a-texture)
    -   [<span data-ttu-id="281bd-116">Remplissage manuel des textures</span><span class="sxs-lookup"><span data-stu-id="281bd-116">Filling Textures Manually</span></span>](#filling-textures-manually)
-   [<span data-ttu-id="281bd-117">Plusieurs Rendertargets</span><span class="sxs-lookup"><span data-stu-id="281bd-117">Multiple Rendertargets</span></span>](#multiple-rendertargets)
-   [<span data-ttu-id="281bd-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="281bd-118">Related topics</span></span>](#related-topics)

## <a name="create-a-texture-from-a-file"></a><span data-ttu-id="281bd-119">Créer une texture à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="281bd-119">Create a Texture from a File</span></span>

> [!Note]  
> <span data-ttu-id="281bd-120">La [bibliothèque de l’utilitaire D3DX](d3d10-graphics-reference-d3dx10.md) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="281bd-120">The [D3DX utility library](d3d10-graphics-reference-d3dx10.md) is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="281bd-121">Lorsque vous créez une texture dans Direct3D 10, vous devez également créer une [vue](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="281bd-121">When you create a texture in Direct3D 10, you also need to create a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span> <span data-ttu-id="281bd-122">Une vue est un objet qui indique à l’appareil Comment accéder à une texture pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="281bd-122">A view is an object that tells the device how a texture should be accessed during rendering.</span></span> <span data-ttu-id="281bd-123">La méthode la plus courante pour accéder à une texture est de la lire à l’aide d’un [nuanceur](../direct3dhlsl/dx-graphics-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="281bd-123">The most common way to access a texture is to read from it using a [shader](../direct3dhlsl/dx-graphics-hlsl.md).</span></span> <span data-ttu-id="281bd-124">Un affichage des ressources de nuanceur indique à un nuanceur comment lire à partir d’une texture pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="281bd-124">A shader-resource view will tell a shader how to read from a texture during rendering.</span></span> <span data-ttu-id="281bd-125">Le type de vue qu’une texture utilisera doit être spécifié au moment de sa création.</span><span class="sxs-lookup"><span data-stu-id="281bd-125">The kind of view a texture will use must be specified when you create it.</span></span>

<span data-ttu-id="281bd-126">La création d’une texture et le chargement de ses données initiales peuvent être effectuées de deux manières différentes : créer une texture et une vue séparément, ou créer la texture et la vue en même temps.</span><span class="sxs-lookup"><span data-stu-id="281bd-126">Creating a texture and loading its initial data can be done in two different ways: create a texture and view separately, or create both the texture and the view at the same time.</span></span> <span data-ttu-id="281bd-127">L’API fournit les deux techniques pour vous permettre de choisir celle qui répond le mieux à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="281bd-127">The API provides both techniques so you can choose which better suits your needs.</span></span>

### <a name="create-texture-and-view-separately"></a><span data-ttu-id="281bd-128">Créer une texture et une vue séparément</span><span class="sxs-lookup"><span data-stu-id="281bd-128">Create Texture and View Separately</span></span>

<span data-ttu-id="281bd-129">Le moyen le plus simple de créer une texture est de le charger à partir d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="281bd-129">The easiest way to create a texture is to load it from an image file.</span></span> <span data-ttu-id="281bd-130">Pour créer la texture, il suffit de remplir une structure et de fournir le nom de la texture à [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="281bd-130">To create the texture, just fill in one structure and provide the texture's name to [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).</span></span>


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



<span data-ttu-id="281bd-131">La fonction D3DX [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) effectue trois opérations : tout d’abord, elle crée un objet de texture Direct3D 10. Deuxièmement, il lit le fichier image d’entrée ; Troisièmement, il stocke les données de l’image dans l’objet texture.</span><span class="sxs-lookup"><span data-stu-id="281bd-131">The D3DX function [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) does three things: first, it creates a Direct3D 10 texture object; second, it reads the input image file; third, it stores the image data in the texture object.</span></span> <span data-ttu-id="281bd-132">Dans l’exemple ci-dessus, un fichier BMP est chargé, mais la fonction peut charger divers types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="281bd-132">In the sample above, a BMP file is loaded, but the function can load a variety of file types.</span></span>

<span data-ttu-id="281bd-133">L’indicateur de liaison indique que la texture sera créée en tant que ressource de nuanceur, ce qui permet à une étape du nuanceur de lire à partir de la texture pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="281bd-133">The bind flag indicates the texture will be created as a shader resource which allows a shader stage to read from the texture during rendering.</span></span>

<span data-ttu-id="281bd-134">L’exemple ci-dessus ne spécifie pas tous les paramètres de chargement.</span><span class="sxs-lookup"><span data-stu-id="281bd-134">The above example does not specify all of the loading parameters.</span></span> <span data-ttu-id="281bd-135">En fait, il est souvent préférable de simplement réinitialiser les paramètres de chargement, car cela permet à D3DX de choisir des valeurs appropriées en fonction de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="281bd-135">In fact, it's often beneficial to simply zero out the loading parameters as this enables D3DX to choose appropriate values based on the input image.</span></span> <span data-ttu-id="281bd-136">Si vous souhaitez que l’image d’entrée détermine tous les paramètres avec lesquels la texture est créée, spécifiez simplement la **valeur null** pour le paramètre **loadInfo** comme suit :</span><span class="sxs-lookup"><span data-stu-id="281bd-136">If you want the input image to determine all of the parameters the texture is created with, simply specify **NULL** for the **loadInfo** parameter like this:</span></span>


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



<span data-ttu-id="281bd-137">La spécification de **null** pour les informations de chargement est un raccourci simple mais puissant.</span><span class="sxs-lookup"><span data-stu-id="281bd-137">Specifying **NULL** for the loading information is a simple yet powerful shortcut.</span></span>

<span data-ttu-id="281bd-138">Maintenant qu’une texture a été créée, vous devez créer un affichage des ressources de nuanceur afin que la texture puisse être liée en tant qu’entrée à un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="281bd-138">Now that a texture has been created, you need to create a shader-resource view so that the texture can be bound as an input to a shader.</span></span> <span data-ttu-id="281bd-139">Étant donné que [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) retourne un pointeur vers une ressource et non un pointeur vers une texture, vous devez déterminer le type exact de ressource qui a été chargé, puis vous pouvez créer une vue de ressource de nuanceur à l’aide de [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="281bd-139">Since [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) returns a pointer to a resource and not a pointer to a texture, you have to determine the exact type of resource that was loaded, and then you can create a shader-resource view using [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



<span data-ttu-id="281bd-140">Bien que l’exemple ci-dessus crée une vue de ressource de nuanceur 2D, le code permettant de créer d’autres types d’affichage des ressources de nuanceur est très similaire.</span><span class="sxs-lookup"><span data-stu-id="281bd-140">Although the above sample creates a 2D shader-resource view, the code to create other shader-resource view types is very similar.</span></span> <span data-ttu-id="281bd-141">Une étape de nuanceur peut maintenant utiliser cette texture comme entrée.</span><span class="sxs-lookup"><span data-stu-id="281bd-141">Any shader stage can now use this texture as an input.</span></span>

<span data-ttu-id="281bd-142">L’utilisation de [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) et de [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) pour créer une texture et de sa vue associée est une façon de préparer une texture à être liée à une étape de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="281bd-142">Using [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) to create a texture and its associated view is one way to prepare a texture to be bound to a shader stage.</span></span> <span data-ttu-id="281bd-143">Une autre façon de procéder consiste à créer la texture et sa vue en même temps, ce qui est abordé dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="281bd-143">Another way to do so is to create both the texture and its view at the same time, which is discussed in the next section.</span></span>

### <a name="create-texture-and-view-simultaneously"></a><span data-ttu-id="281bd-144">Créer une texture et une vue simultanément</span><span class="sxs-lookup"><span data-stu-id="281bd-144">Create Texture and View Simultaneously</span></span>

<span data-ttu-id="281bd-145">Direct3D 10 nécessite à la fois une texture et une vue de ressource de nuanceur pour lire à partir d’une texture pendant l’exécution.</span><span class="sxs-lookup"><span data-stu-id="281bd-145">Direct3D 10 requires both a texture and a shader-resource view to read from a texture during runtime.</span></span> <span data-ttu-id="281bd-146">Étant donné que la création d’une texture et d’une vue de la ressource Shader est une tâche courante, D3DX fournit le [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) pour le faire pour vous.</span><span class="sxs-lookup"><span data-stu-id="281bd-146">Since the creation of a texture and a shader-resource view is such a common task, D3DX provides the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) to do it for you.</span></span>


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



<span data-ttu-id="281bd-147">Avec un seul appel D3DX, les affichages texture et shader-Resource sont créés.</span><span class="sxs-lookup"><span data-stu-id="281bd-147">With a single D3DX call, both the texture and shader-resource view are created.</span></span> <span data-ttu-id="281bd-148">La fonctionnalité du paramètre **loadInfo** est inchangée. vous pouvez l’utiliser pour personnaliser la manière dont la texture est créée, ou dériver les paramètres nécessaires du fichier d’entrée en spécifiant la **valeur null** pour le paramètre **loadInfo** .</span><span class="sxs-lookup"><span data-stu-id="281bd-148">The functionality of the **loadInfo** parameter is unchanged; you can use it to customize how the texture is created, or derive the necessary parameters from the input file by specifying **NULL** for the **loadInfo** parameter.</span></span>

<span data-ttu-id="281bd-149">L’objet [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) retourné par la fonction [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) peut être utilisé ultérieurement pour récupérer l’interface [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) d’origine, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="281bd-149">The [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) object returned by the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) function can later be used to retrieve the original [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) interface if it is needed.</span></span> <span data-ttu-id="281bd-150">Pour ce faire, vous pouvez appeler la méthode [**GetResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) .</span><span class="sxs-lookup"><span data-stu-id="281bd-150">This can be done by calling the [**GetResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) method.</span></span>

<span data-ttu-id="281bd-151">D3DX fournit une fonction unique pour créer une texture et une vue de ressource de nuanceur en tant que convienience. C’est à vous de choisir la méthode de création d’une texture et d’afficher le mieux adapté aux besoins de votre application.</span><span class="sxs-lookup"><span data-stu-id="281bd-151">D3DX provides a single function to create a texture and shader-resource view as a convienience; it is up to you to decide which method of creating a texture and view best suits the needs of your application.</span></span>

<span data-ttu-id="281bd-152">Maintenant que vous savez comment créer une texture et son affichage des ressources de nuanceur, la section suivante vous montre comment vous pouvez échantillonner (Lire) à partir de cette texture à l’aide d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="281bd-152">Now that you know how to create a texture and its shader-resource view, the next section will show you how you can sample (read) from that texture using a shader.</span></span>

## <a name="creating-empty-textures"></a><span data-ttu-id="281bd-153">Création de textures vides</span><span class="sxs-lookup"><span data-stu-id="281bd-153">Creating Empty Textures</span></span>

<span data-ttu-id="281bd-154">Parfois, les applications veulent créer une texture et calculer les données à stocker dans la texture, ou utiliser le [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) graphique pour effectuer le rendu sur cette texture et utiliser ultérieurement les résultats dans un autre traitement.</span><span class="sxs-lookup"><span data-stu-id="281bd-154">Sometimes applications will want to create a texture and compute the data to be stored in the texture, or use the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) to render to this texture and later use the results in other processing.</span></span> <span data-ttu-id="281bd-155">Ces textures peuvent être mises à jour par le pipeline graphique ou par l’application elle-même, selon le type d' [**utilisation**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) spécifié pour la texture lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="281bd-155">These textures could be updated by the graphics pipeline or by the application itself, depending on what kind of [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) was specified for the texture when it was created.</span></span>

### <a name="rendering-to-a-texture"></a><span data-ttu-id="281bd-156">Rendu dans une texture</span><span class="sxs-lookup"><span data-stu-id="281bd-156">Rendering to a texture</span></span>

<span data-ttu-id="281bd-157">Le cas le plus courant de la création d’une texture vide à remplir avec des données pendant l’exécution est le cas où une application souhaite effectuer un rendu sur une texture, puis utiliser les résultats de l’opération de rendu dans une passe suivante.</span><span class="sxs-lookup"><span data-stu-id="281bd-157">The most common case of creating an empty texture to be filled with data during runtime is the case where an application wants to render to a texture and then use the results of the rendering operation in a subsequent pass.</span></span> <span data-ttu-id="281bd-158">Les textures créées à cet effet doivent spécifier [**l’utilisation**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)par défaut.</span><span class="sxs-lookup"><span data-stu-id="281bd-158">Textures created with this purpose should specify default [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

<span data-ttu-id="281bd-159">L’exemple de code suivant crée une texture vide à partir de laquelle le pipeline peut être rendu et utilisé par la suite comme entrée d’un [nuanceur](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span><span class="sxs-lookup"><span data-stu-id="281bd-159">The following code sample creates an empty texture that the pipeline can render to and subsequently use as an input to a [shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span></span>


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



<span data-ttu-id="281bd-160">La création de la texture requiert que l’application spécifie des informations sur les propriétés que la texture aura.</span><span class="sxs-lookup"><span data-stu-id="281bd-160">Creating the texture requires the application to specify some information about the properties the texture will have.</span></span> <span data-ttu-id="281bd-161">La largeur et la hauteur de la texture dans texels sont définies sur 256.</span><span class="sxs-lookup"><span data-stu-id="281bd-161">The width and height of the texture in texels is set to 256.</span></span> <span data-ttu-id="281bd-162">Pour cette cible de rendu, un seul niveau de mipmap est tout ce dont nous avons besoin.</span><span class="sxs-lookup"><span data-stu-id="281bd-162">For this render target, a single mipmap level is all we need.</span></span> <span data-ttu-id="281bd-163">Une seule cible de rendu est nécessaire pour que la taille du tableau soit définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="281bd-163">Only one render target is required so the array size is set to 1.</span></span> <span data-ttu-id="281bd-164">Chaque Texel contient des valeurs à virgule flottante 4 32 bits qui peuvent être utilisées pour stocker des informations très précises (consultez le [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="281bd-164">Each texel contains four 32-bit floating point values, which can be used to store very precise information (see [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="281bd-165">Un échantillon par pixel est tout ce qui sera nécessaire.</span><span class="sxs-lookup"><span data-stu-id="281bd-165">One sample per pixel is all that will be needed.</span></span> <span data-ttu-id="281bd-166">L’utilisation est définie sur la valeur par défaut, car elle permet l’emplacement le plus efficace de la cible de rendu en mémoire.</span><span class="sxs-lookup"><span data-stu-id="281bd-166">The usage is set to default because this allows for the most efficient placement of the render target in memory.</span></span> <span data-ttu-id="281bd-167">Enfin, le fait que la texture soit liée en tant que cible de rendu et qu’une ressource de nuanceur à différents moments dans le temps est spécifié.</span><span class="sxs-lookup"><span data-stu-id="281bd-167">Finally, the fact that the texture will be bound as a render target and a shader resource at different points in time is specified.</span></span>

<span data-ttu-id="281bd-168">Les textures ne peuvent pas être liées directement au pipeline ; Utilisez une vue de cible de rendu comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="281bd-168">Textures cannot be bound for rendering to the pipeline directly; use a render-target view as shown in the following code sample.</span></span>


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



<span data-ttu-id="281bd-169">Le format de l’affichage de la cible de rendu est simplement défini sur le format de la texture d’origine.</span><span class="sxs-lookup"><span data-stu-id="281bd-169">The format of the render-target view is simply set to the format of the original texture.</span></span> <span data-ttu-id="281bd-170">Les informations de la ressource doivent être interprétées comme une texture 2D et nous voulons uniquement utiliser le premier niveau de mipmap de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="281bd-170">The information in the resource should be interpreted as a 2D texture, and we only want to use the first mipmap level of the render target.</span></span>

<span data-ttu-id="281bd-171">De la même façon qu’une vue de cible de rendu doit être créée afin que la cible de rendu puisse être liée pour la sortie au pipeline, une vue de ressource de nuanceur doit être créée afin que la cible de rendu puisse être liée au pipeline en tant qu’entrée.</span><span class="sxs-lookup"><span data-stu-id="281bd-171">Similarly to how a render-target view must be created so that the render target can be bound for output to the pipeline, a shader-resource view must be created so that the render target can be bound to the pipeline as an input.</span></span> <span data-ttu-id="281bd-172">L’exemple de code suivant illustre cela.</span><span class="sxs-lookup"><span data-stu-id="281bd-172">The following code sample demonstrates this.</span></span>


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



<span data-ttu-id="281bd-173">Les paramètres des descriptions des affichages des ressources de nuanceur sont très similaires à ceux des descriptions de la vue de la cible de rendu et ont été choisis pour les mêmes raisons.</span><span class="sxs-lookup"><span data-stu-id="281bd-173">The parameters of shader-resource view descriptions are very similar to those of render-target view descriptions and were chosen for the same reasons.</span></span>

### <a name="filling-textures-manually"></a><span data-ttu-id="281bd-174">Remplissage manuel des textures</span><span class="sxs-lookup"><span data-stu-id="281bd-174">Filling Textures Manually</span></span>

<span data-ttu-id="281bd-175">Parfois, les applications souhaitent calculer des valeurs au moment de l’exécution, les placer dans une texture manuellement, puis faire en sorte que le [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) graphique utilise cette texture dans les opérations de rendu ultérieures.</span><span class="sxs-lookup"><span data-stu-id="281bd-175">Sometimes applications would like to compute values at runtime, put them into a texture manually and then have the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) use this texture in later rendering operations.</span></span> <span data-ttu-id="281bd-176">Pour ce faire, l’application doit créer une texture vide de manière à permettre au processeur d’accéder à la mémoire sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="281bd-176">To do this, the application must create an empty texture in such a way to allow the CPU to access the underlying memory.</span></span> <span data-ttu-id="281bd-177">Cela s’effectue en créant une texture dynamique et en obtenant l’accès à la mémoire sous-jacente en appelant une méthode particulière.</span><span class="sxs-lookup"><span data-stu-id="281bd-177">This is done by creating a dynamic texture and gaining access to the underlying memory by calling a particular method.</span></span> <span data-ttu-id="281bd-178">L'exemple de code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="281bd-178">The following code sample demonstrates how to do this.</span></span>


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



<span data-ttu-id="281bd-179">Notez que le format est défini sur 32 bits par pixel, où chaque composant est défini par 8 bits.</span><span class="sxs-lookup"><span data-stu-id="281bd-179">Note that the format is set to a 32 bits per pixel where each component is defined by 8 bits.</span></span> <span data-ttu-id="281bd-180">Le paramètre d’utilisation est défini sur dynamique, tandis que les indicateurs de liaison sont définis pour spécifier que la texture sera accessible par un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="281bd-180">The usage parameter is set to dynamic while the bind flags are set to specify the texture will be accessed by a shader.</span></span> <span data-ttu-id="281bd-181">Le reste de la description de la texture est semblable à la création d’une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="281bd-181">The rest of the texture description is similar to creating a render target.</span></span>

<span data-ttu-id="281bd-182">Le [**mappage**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) d’appel permet à l’application d’accéder à la mémoire sous-jacente de la texture.</span><span class="sxs-lookup"><span data-stu-id="281bd-182">Calling [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) enables the application to access the underlying memory of the texture.</span></span> <span data-ttu-id="281bd-183">Le pointeur récupéré est ensuite utilisé pour remplir la texture avec les données.</span><span class="sxs-lookup"><span data-stu-id="281bd-183">The pointer retrieved is then used to fill the texture with data.</span></span> <span data-ttu-id="281bd-184">Cela peut être observé dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="281bd-184">This can be seen in the following code sample.</span></span>


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a><span data-ttu-id="281bd-185">Plusieurs Rendertargets</span><span class="sxs-lookup"><span data-stu-id="281bd-185">Multiple Rendertargets</span></span>

<span data-ttu-id="281bd-186">Jusqu’à huit vues de cible de rendu peuvent être liées au pipeline à la fois (avec [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)).</span><span class="sxs-lookup"><span data-stu-id="281bd-186">Up to eight render-target views can be bound to the pipeline at a time (with [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)).</span></span> <span data-ttu-id="281bd-187">Pour chaque pixel (ou pour chaque échantillon si l’échantillonnage multiple est activé), la fusion est effectuée indépendamment pour chaque affichage de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="281bd-187">For each pixel (or each sample if multisampling is enabled), blending is done independently for each render-target view.</span></span> <span data-ttu-id="281bd-188">Deux des variables d’état de fusion-BlendEnable et RenderTargetWriteMask-sont des tableaux de huit, chaque membre de tableau correspond à une vue de cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="281bd-188">Two of the blend state variables - BlendEnable and RenderTargetWriteMask - are arrays of eight, each array member corresponds to a render-target view.</span></span> <span data-ttu-id="281bd-189">Quand vous utilisez plusieurs cibles de rendu, chaque cible de rendu doit être du même [type de ressource](d3d10-graphics-programming-guide-resources-types.md) (tampon, texture 1D, tableau de texture 2D, etc.) et doit avoir la même dimension (largeur, hauteur, profondeur pour les textures 3D et taille de tableau pour les tableaux de texture).</span><span class="sxs-lookup"><span data-stu-id="281bd-189">When using multiple render targets, each render target must be the same [resource type](d3d10-graphics-programming-guide-resources-types.md) (buffer, 1D texture, 2D texture array, etc.) and must have the same dimension (width, height, depth for 3D textures, and array size for texture arrays).</span></span> <span data-ttu-id="281bd-190">Si les cibles de rendu sont échantillonnées, elles doivent toutes avoir le même nombre d’échantillons par pixel.</span><span class="sxs-lookup"><span data-stu-id="281bd-190">If the render targets are multisampled, then they must all have the same number of samples per pixel.</span></span>

<span data-ttu-id="281bd-191">Il ne peut y avoir qu’une seule mémoire tampon de stencil de profondeur active, quel que soit le nombre de cibles de rendu actives.</span><span class="sxs-lookup"><span data-stu-id="281bd-191">There can only be one depth-stencil buffer active, regardless of how many render targets are active.</span></span> <span data-ttu-id="281bd-192">Lorsque vous utilisez des tableaux de texture comme cibles de rendu, toutes les dimensions de vue doivent correspondre.</span><span class="sxs-lookup"><span data-stu-id="281bd-192">When using texture arrays as render targets, all view dimensions must match.</span></span> <span data-ttu-id="281bd-193">Les cibles de rendu n’ont pas besoin d’avoir le même format de texture.</span><span class="sxs-lookup"><span data-stu-id="281bd-193">The render targets do not need to have the same texture format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="281bd-194">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="281bd-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="281bd-195">Ressources (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="281bd-195">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
