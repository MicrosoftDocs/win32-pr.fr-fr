---
title: Comment créer une texture
description: Cette rubrique montre comment créer une texture.
ms.assetid: dfe88635-b2c2-48f8-a21e-cce845b518fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d3c4715bb4c790ea772dcbba4834051946747e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674238"
---
# <a name="how-to-create-a-texture"></a><span data-ttu-id="ea7f9-103">Comment : créer une texture</span><span class="sxs-lookup"><span data-stu-id="ea7f9-103">How to: Create a Texture</span></span>

<span data-ttu-id="ea7f9-104">La façon la plus simple de créer une texture est de décrire ses propriétés et d’appeler l’API de création de texture.</span><span class="sxs-lookup"><span data-stu-id="ea7f9-104">The simplest way to create a texture is to describe its properties and call the texture creation API.</span></span> <span data-ttu-id="ea7f9-105">Cette rubrique montre comment créer une texture.</span><span class="sxs-lookup"><span data-stu-id="ea7f9-105">This topic shows how to create a texture.</span></span>

<span data-ttu-id="ea7f9-106">**Pour créer une texture**</span><span class="sxs-lookup"><span data-stu-id="ea7f9-106">**To create a texture**</span></span>

1.  <span data-ttu-id="ea7f9-107">Remplissez une structure [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) avec une description des paramètres de texture.</span><span class="sxs-lookup"><span data-stu-id="ea7f9-107">Fill in a [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) structure with a description of the texture parameters.</span></span>
2.  <span data-ttu-id="ea7f9-108">Créez la texture en appelant [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) avec la description de la texture.</span><span class="sxs-lookup"><span data-stu-id="ea7f9-108">Create the texture by calling [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) with the texture description.</span></span>

<span data-ttu-id="ea7f9-109">Cet exemple crée une texture 256 x 256, avec [**utilisation dynamique**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), pour une utilisation en tant que [**ressource de nuanceur**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) avec [**accès en écriture**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)de l’UC.</span><span class="sxs-lookup"><span data-stu-id="ea7f9-109">This example creates a 256 x 256 texture, with [**dynamic usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), for use as a [**shader resource**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) with [**cpu write access**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span></span>


```
D3D11_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D11_USAGE_DYNAMIC;
desc.BindFlags = D3D11_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
desc.MiscFlags = 0;

ID3D11Device *pd3dDevice; // Don't forget to initialize this
ID3D11Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



## <a name="related-topics"></a><span data-ttu-id="ea7f9-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea7f9-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea7f9-111">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ea7f9-111">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="ea7f9-112">Textures</span><span class="sxs-lookup"><span data-stu-id="ea7f9-112">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




