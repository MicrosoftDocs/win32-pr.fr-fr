---
description: 'Les ressources de texture sont implémentées dans l’interface IDirect3DTexture9. Pour obtenir un pointeur vers une interface de texture, appelez la méthode IDirect3DDevice9 :: CreateTexture ou l’une des fonctions D3DX suivantes.'
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Ressources de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14134ca53b7735426e3f01340308282858da5516
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200813"
---
# <a name="texture-resources-direct3d-9"></a><span data-ttu-id="7b703-104">Ressources de texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7b703-104">Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="7b703-105">Les ressources de texture sont implémentées dans l’interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="7b703-105">Texture resources are implemented in the [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface.</span></span> <span data-ttu-id="7b703-106">Pour obtenir un pointeur vers une interface de texture, appelez la méthode [**IDirect3DDevice9 :: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) ou l’une des fonctions D3DX suivantes.</span><span class="sxs-lookup"><span data-stu-id="7b703-106">To obtain a pointer to a texture interface, call the [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) method or any of the following D3DX functions.</span></span>

-   [<span data-ttu-id="7b703-107">**D3DXCreateTexture**</span><span class="sxs-lookup"><span data-stu-id="7b703-107">**D3DXCreateTexture**</span></span>](d3dxcreatetexture.md)
-   [<span data-ttu-id="7b703-108">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="7b703-108">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
-   [<span data-ttu-id="7b703-109">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="7b703-109">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
-   [<span data-ttu-id="7b703-110">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="7b703-110">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
-   [<span data-ttu-id="7b703-111">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="7b703-111">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
-   [<span data-ttu-id="7b703-112">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="7b703-112">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
-   [<span data-ttu-id="7b703-113">**D3DXCreateTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="7b703-113">**D3DXCreateTextureFromResourceEx**</span></span>](d3dxcreatetexturefromresourceex.md)

<span data-ttu-id="7b703-114">L’exemple de code suivant utilise [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) pour charger une texture à partir de Tiger.bmp.</span><span class="sxs-lookup"><span data-stu-id="7b703-114">The following code example uses [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) to load a texture from Tiger.bmp.</span></span>


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



<span data-ttu-id="7b703-115">Le premier paramètre que [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) accepte est un pointeur vers une interface [**IDirect3DDevice9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="7b703-115">The first parameter that [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) accepts is a pointer to an [**IDirect3DDevice9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="7b703-116">Le deuxième paramètre indique à Direct3D le nom du fichier à partir duquel la texture doit être chargée.</span><span class="sxs-lookup"><span data-stu-id="7b703-116">The second parameter tells Direct3D the name of the file from which to load the texture.</span></span> <span data-ttu-id="7b703-117">Le troisième paramètre prend l’adresse d’un pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , représentant l’objet de texture créé.</span><span class="sxs-lookup"><span data-stu-id="7b703-117">The third parameter takes the address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

## <a name="rendering-with-texture-resources"></a><span data-ttu-id="7b703-118">Rendu avec des ressources de texture</span><span class="sxs-lookup"><span data-stu-id="7b703-118">Rendering with Texture Resources</span></span>

<span data-ttu-id="7b703-119">Direct3D prend en charge la fusion de plusieurs textures par le biais du concept de étapes de texture.</span><span class="sxs-lookup"><span data-stu-id="7b703-119">Direct3D supports multiple texture blending through the concept of texture stages.</span></span> <span data-ttu-id="7b703-120">Chaque étape de texture contient une texture et des opérations qui peuvent être effectuées sur la texture.</span><span class="sxs-lookup"><span data-stu-id="7b703-120">Each texture stage contains a texture and operations that can be performed on the texture.</span></span> <span data-ttu-id="7b703-121">Les textures dans les étapes de texture forment le jeu de textures actuelles.</span><span class="sxs-lookup"><span data-stu-id="7b703-121">The textures in the texture stages form the set of current textures.</span></span> <span data-ttu-id="7b703-122">Pour plus d’informations, consultez [Blending texture (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="7b703-122">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="7b703-123">L’état de chaque texture est encapsulé dans son étape de texture.</span><span class="sxs-lookup"><span data-stu-id="7b703-123">The state of each texture is encapsulated in its texture stage.</span></span>

<span data-ttu-id="7b703-124">Dans une application C++, l’état de chaque texture doit être défini à l’aide de la méthode [**IDirect3DDevice9 :: SetTextureStageState**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="7b703-124">In a C++ application, the state of each texture must be set with the [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="7b703-125">Transmettez le numéro intermédiaire (0-7) en tant que valeur du premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="7b703-125">Pass the stage number (0-7) as the value of the first parameter.</span></span> <span data-ttu-id="7b703-126">Définissez la valeur du deuxième paramètre sur un membre du type énuméré [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="7b703-126">Set the value of the second parameter to a member of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="7b703-127">Le dernier paramètre est la valeur d’État pour l’état de texture particulier.</span><span class="sxs-lookup"><span data-stu-id="7b703-127">The final parameter is the state value for the particular texture state.</span></span>

<span data-ttu-id="7b703-128">À l’aide de pointeurs d’interface de texture, votre application peut restituer une fusion allant jusqu’à huit textures.</span><span class="sxs-lookup"><span data-stu-id="7b703-128">Using texture interface pointers, your application can render a blend of up to eight textures.</span></span> <span data-ttu-id="7b703-129">Définissez les textures actuelles en appelant la méthode [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="7b703-129">Set the current textures by invoking the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="7b703-130">Direct3D fusionne toutes les textures actuelles sur les primitives qu’elle restitue.</span><span class="sxs-lookup"><span data-stu-id="7b703-130">Direct3D blends all current textures onto the primitives that it renders.</span></span>

> [!Note]  
> <span data-ttu-id="7b703-131">La méthode [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) incrémente le décompte de références de la surface de texture qui est assignée.</span><span class="sxs-lookup"><span data-stu-id="7b703-131">The [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method increments the reference count of the texture surface being assigned.</span></span> <span data-ttu-id="7b703-132">Lorsque la texture n’est plus nécessaire, vous devez définir la texture à l’étape appropriée sur **null**.</span><span class="sxs-lookup"><span data-stu-id="7b703-132">When the texture is no longer needed, you should set the texture at the appropriate stage to **NULL**.</span></span> <span data-ttu-id="7b703-133">Si vous ne le faites pas, la surface n’est pas libérée, ce qui entraîne une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="7b703-133">If you fail to do this, the surface will not be released, resulting in a memory leak.</span></span>

 

<span data-ttu-id="7b703-134">Votre application peut définir l’état d’habillage de texture pour les textures actuelles en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) .</span><span class="sxs-lookup"><span data-stu-id="7b703-134">Your application can set the texture wrapping state for the current textures by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method.</span></span> <span data-ttu-id="7b703-135">Transmettez une valeur de D3DRS \_ WRAP0 à D3DRS \_ WRAP7 comme valeur du premier paramètre et utilisez une combinaison des \_ indicateurs D3DWRAPCOORD 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD \_ 2 et D3DWRAPCOORD \_ 3 pour activer l’habillage dans les directions u, v ou w.</span><span class="sxs-lookup"><span data-stu-id="7b703-135">Pass a value from D3DRS\_WRAP0 through D3DRS\_WRAP7 as the value of the first parameter, and use a combination of the D3DWRAPCOORD\_0, D3DWRAPCOORD\_1, D3DWRAPCOORD\_2, and D3DWRAPCOORD\_3 flags to enable wrapping in the u, v, or w directions.</span></span>

<span data-ttu-id="7b703-136">Votre application peut également définir la perspective de texture et les États de filtrage de texture.</span><span class="sxs-lookup"><span data-stu-id="7b703-136">Your application can also set the texture perspective and texture filtering states.</span></span> <span data-ttu-id="7b703-137">Consultez [filtrage de texture (Direct3D 9)](texture-filtering.md).</span><span class="sxs-lookup"><span data-stu-id="7b703-137">See [Texture Filtering (Direct3D 9)](texture-filtering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b703-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b703-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b703-139">Textures Direct3D</span><span class="sxs-lookup"><span data-stu-id="7b703-139">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
