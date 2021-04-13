---
description: Votre application manipule les ressources afin d’afficher une scène.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Manipulation des ressources (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886dfee3af024d103dab8666687f1b053a5fb46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385492"
---
# <a name="manipulating-resources-direct3d-9"></a><span data-ttu-id="228df-103">Manipulation des ressources (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="228df-103">Manipulating Resources (Direct3D 9)</span></span>

<span data-ttu-id="228df-104">Votre application manipule les ressources afin d’afficher une scène.</span><span class="sxs-lookup"><span data-stu-id="228df-104">Your application manipulates resources in order to render a scene.</span></span> <span data-ttu-id="228df-105">Tout d’abord, une application doit créer une ressource de texture avec l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="228df-105">First, an application needs to create a texture resource with one of the following methods:</span></span>

-   [<span data-ttu-id="228df-106">**IDirect3DDevice9::CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="228df-106">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="228df-107">**IDirect3DDevice9::CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="228df-107">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="228df-108">**IDirect3DDevice9::CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="228df-108">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

<span data-ttu-id="228df-109">Une ressource de texture peut être créée à la place avec l’une des fonctions de texturation D3DXCreatexxx.</span><span class="sxs-lookup"><span data-stu-id="228df-109">A texture resource can instead be created with one of the D3DXCreatexxx texturing functions.</span></span>

<span data-ttu-id="228df-110">Les objets de texture retournés par les méthodes de création de texture sont des conteneurs pour les surfaces ou les volumes ; ces conteneurs sont génériquement appelés mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="228df-110">The texture objects returned by the texture creation methods are containers for surfaces or volumes; these containers are generically known as buffers.</span></span> <span data-ttu-id="228df-111">Les mémoires tampons détenues par la ressource héritent des utilisations, du format et du pool de la ressource, mais ont leur propre type.</span><span class="sxs-lookup"><span data-stu-id="228df-111">The buffers owned by the resource inherit the usages, format, and pool of the resource but have their own type.</span></span> <span data-ttu-id="228df-112">Pour plus d’informations, consultez [Propriétés des ressources (Direct3D 9)](resource-properties.md).</span><span class="sxs-lookup"><span data-stu-id="228df-112">For more information, see [Resource Properties (Direct3D 9)](resource-properties.md).</span></span>

<span data-ttu-id="228df-113">L’application obtient l’accès aux surfaces contenues, à des fins de chargement d’illustrations, en appelant les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="228df-113">The application gains access to the contained surfaces, for the purpose of loading artwork, by calling the following methods.</span></span> <span data-ttu-id="228df-114">Pour plus d’informations, consultez [verrouillage des ressources (Direct3D 9)](locking-resources.md).</span><span class="sxs-lookup"><span data-stu-id="228df-114">For details, see [Locking Resources (Direct3D 9)](locking-resources.md).</span></span>

-   [<span data-ttu-id="228df-115">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="228df-115">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [<span data-ttu-id="228df-116">**IDirect3DTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="228df-116">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [<span data-ttu-id="228df-117">**IDirect3DVolumeTexture9 :: LockBox**</span><span class="sxs-lookup"><span data-stu-id="228df-117">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

<span data-ttu-id="228df-118">Les méthodes Lock acceptent les arguments qui dénotent la surface contenue (par exemple, la face du sous-niveau ou du cube mipmap des pointeurs de texture et de retour aux pixels).</span><span class="sxs-lookup"><span data-stu-id="228df-118">The lock methods take arguments denoting the contained surface - for example, the mipmap sub-level or cube face of the texture - and return pointers to the pixels.</span></span> <span data-ttu-id="228df-119">L’application typique n’utilise jamais directement un objet surface.</span><span class="sxs-lookup"><span data-stu-id="228df-119">The typical application never uses a surface object directly.</span></span>

<span data-ttu-id="228df-120">Créez des ressources orientées géométrie en appelant [**IDirect3DDevice9 :: CreateIndexBuffer**](/windows/desktop/api) ou [**IDirect3DDevice9 :: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).</span><span class="sxs-lookup"><span data-stu-id="228df-120">Create geometry-oriented resources by calling [**IDirect3DDevice9::CreateIndexBuffer**](/windows/desktop/api) or [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).</span></span>

<span data-ttu-id="228df-121">Verrouillez et remplissez les ressources de mémoire tampon en appelant [**IDirect3DIndexBuffer9 :: Lock**](/windows/desktop/api) ou [**IDirect3DVertexBuffer9 :: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), en fonction de la ressource.</span><span class="sxs-lookup"><span data-stu-id="228df-121">Lock and fill the buffer resources by calling either [**IDirect3DIndexBuffer9::Lock**](/windows/desktop/api) or [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), depending upon the resource.</span></span>

<span data-ttu-id="228df-122">Pour les ressources de texture managée, le processus de création de ressource se termine ici.</span><span class="sxs-lookup"><span data-stu-id="228df-122">For managed texture resources, the resource creation process ends here.</span></span> <span data-ttu-id="228df-123">Pour les ressources de texture non managées, une application promeut des ressources mémoire système vers des ressources accessibles par l’appareil (pour l’accélération matérielle) en appelant [**IDirect3DDevice9 :: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span><span class="sxs-lookup"><span data-stu-id="228df-123">For non-managed texture resources, an application promotes system memory resources to device-accessible resources (for hardware acceleration) by calling [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

<span data-ttu-id="228df-124">Pour présenter des images rendues à partir de ressources, l’application a également besoin de mémoires tampons de stencil de couleur et de profondeur.</span><span class="sxs-lookup"><span data-stu-id="228df-124">To present images rendered from resources, the application also needs color and depth-stencil buffers.</span></span> <span data-ttu-id="228df-125">Pour les applications classiques, la mémoire tampon de couleur appartient à la chaîne de permutation de l’appareil, qui est une collection de surfaces de mémoire tampon d’arrière-plan, et est implicitement créée avec l’appareil.</span><span class="sxs-lookup"><span data-stu-id="228df-125">For typical applications, the color buffer is owned by the device's swap chain, which is a collection of back-buffer surfaces, and is implicitly created with the device.</span></span> <span data-ttu-id="228df-126">Les surfaces de stencil de profondeur peuvent être créées implicitement ou explicitement créées à l’aide de la méthode [**IDirect3DDevice9 :: CreateDepthStencilSurface**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="228df-126">Depth-stencil surfaces can be implicitly created, or explicitly created by using the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="228df-127">L’application associe un appareil et sa mémoire tampon de profondeur et de couleur à un appel à [**IDirect3DDevice9 :: SetRenderTarget**](/windows/desktop/api) ou [**IDirect3DDevice9 :: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).</span><span class="sxs-lookup"><span data-stu-id="228df-127">The application associates a device and its depth and color buffer with a call to [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) or [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).</span></span>

<span data-ttu-id="228df-128">Pour plus d’informations sur la présentation de l’image finale, consultez [présentation d’une scène (Direct3D 9)](presenting-a-scene.md).</span><span class="sxs-lookup"><span data-stu-id="228df-128">For details on presenting the final image, see [Presenting a Scene (Direct3D 9)](presenting-a-scene.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="228df-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="228df-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="228df-130">Ressources Direct3D</span><span class="sxs-lookup"><span data-stu-id="228df-130">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 
