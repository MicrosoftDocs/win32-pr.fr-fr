---
title: Comment initialiser une texture par programmation
description: Cette rubrique contient plusieurs exemples montrant comment initialiser des textures créées avec différents types d’utilisation.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5584885b885f6026ee32a3e4c52a24aad78c3c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840309"
---
# <a name="how-to-initialize-a-texture-programmatically"></a><span data-ttu-id="4172d-103">Comment : initialiser une texture par programmation</span><span class="sxs-lookup"><span data-stu-id="4172d-103">How to: Initialize a Texture Programmatically</span></span>

<span data-ttu-id="4172d-104">Vous pouvez initialiser une texture pendant la création de l’objet, ou vous pouvez remplir l’objet par programme après sa création.</span><span class="sxs-lookup"><span data-stu-id="4172d-104">You can initialize a texture during object creation, or you can fill the object programmatically after it is created.</span></span> <span data-ttu-id="4172d-105">Cette rubrique contient plusieurs exemples montrant comment initialiser des textures créées avec différents types d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="4172d-105">This topic has several examples showing how to initialize textures that are created with different types of usages.</span></span> <span data-ttu-id="4172d-106">Cet exemple suppose que vous savez déjà comment [créer une texture](overviews-direct3d-11-resources-textures-create.md).</span><span class="sxs-lookup"><span data-stu-id="4172d-106">This example assumes you already know how to [Create a Texture](overviews-direct3d-11-resources-textures-create.md).</span></span>

-   [<span data-ttu-id="4172d-107">Utilisation par défaut</span><span class="sxs-lookup"><span data-stu-id="4172d-107">Default Usage</span></span>](#default-usage)
-   [<span data-ttu-id="4172d-108">Utilisation dynamique</span><span class="sxs-lookup"><span data-stu-id="4172d-108">Dynamic Usage</span></span>](#dynamic-usage)
-   [<span data-ttu-id="4172d-109">Utilisation intermédiaire</span><span class="sxs-lookup"><span data-stu-id="4172d-109">Staging Usage</span></span>](#staging-usage)
-   [<span data-ttu-id="4172d-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4172d-110">Related topics</span></span>](#related-topics)

## <a name="default-usage"></a><span data-ttu-id="4172d-111">Utilisation par défaut</span><span class="sxs-lookup"><span data-stu-id="4172d-111">Default Usage</span></span>

<span data-ttu-id="4172d-112">Le type d’utilisation le plus courant est l’utilisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="4172d-112">The most common type of usage is default usage.</span></span> <span data-ttu-id="4172d-113">Pour remplir une texture par défaut (une par défaut créée avec **\_ l' \_ utilisation de d3d11**), vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="4172d-113">To fill a default texture (one created with **D3D11\_USAGE\_DEFAULT**) you can either:</span></span>

-   <span data-ttu-id="4172d-114">Appelez [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) et initialisez *pInitialData* pour pointer vers les données fournies par une application.</span><span class="sxs-lookup"><span data-stu-id="4172d-114">Call [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and initialize *pInitialData* to point to data provided from an application.</span></span>

    <span data-ttu-id="4172d-115">or</span><span class="sxs-lookup"><span data-stu-id="4172d-115">or</span></span>

-   <span data-ttu-id="4172d-116">Après l’appel de [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), utilisez [**ID3D11DeviceContext :: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) pour remplir la texture par défaut avec les données d’un pointeur fourni par l’application.</span><span class="sxs-lookup"><span data-stu-id="4172d-116">After calling [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to fill the default texture with data from a pointer provided by the application.</span></span>

## <a name="dynamic-usage"></a><span data-ttu-id="4172d-117">Utilisation dynamique</span><span class="sxs-lookup"><span data-stu-id="4172d-117">Dynamic Usage</span></span>

<span data-ttu-id="4172d-118">Pour remplir une texture dynamique (créée avec **\_ l’utilisation \_ dynamique de d3d11**) :</span><span class="sxs-lookup"><span data-stu-id="4172d-118">To fill a dynamic texture (one created with **D3D11\_USAGE\_DYNAMIC**):</span></span>

1.  <span data-ttu-id="4172d-119">Obtient un pointeur vers la mémoire de texture en passant la valeur d’écriture de la carte de d3d11 lors de l’appel de [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map). **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4172d-119">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE\_DISCARD** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="4172d-120">Écrire des données dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="4172d-120">Write data to the memory.</span></span>
3.  <span data-ttu-id="4172d-121">Appelez [**ID3D11DeviceContext :: DEMAPPAGE**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) lorsque vous avez fini d’écrire des données.</span><span class="sxs-lookup"><span data-stu-id="4172d-121">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

## <a name="staging-usage"></a><span data-ttu-id="4172d-122">Utilisation intermédiaire</span><span class="sxs-lookup"><span data-stu-id="4172d-122">Staging Usage</span></span>

<span data-ttu-id="4172d-123">Pour remplir une texture intermédiaire (un créé avec **d3d11 \_ usage \_ Staging**) :</span><span class="sxs-lookup"><span data-stu-id="4172d-123">To fill a staging texture (one created with **D3D11\_USAGE\_STAGING**):</span></span>

1.  <span data-ttu-id="4172d-124">Obtient un pointeur vers la mémoire de texture en passant **l' \_ \_ écriture** de la carte de d3d11 lors de l’appel de [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span><span class="sxs-lookup"><span data-stu-id="4172d-124">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="4172d-125">Écrire des données dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="4172d-125">Write data to the memory.</span></span>
3.  <span data-ttu-id="4172d-126">Appelez [**ID3D11DeviceContext :: DEMAPPAGE**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) lorsque vous avez fini d’écrire des données.</span><span class="sxs-lookup"><span data-stu-id="4172d-126">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

<span data-ttu-id="4172d-127">Une texture intermédiaire peut ensuite être utilisée comme paramètre source de [**ID3D11DeviceContext :: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) ou [**ID3D11DeviceContext :: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) pour remplir une ressource par défaut ou dynamique.</span><span class="sxs-lookup"><span data-stu-id="4172d-127">A staging texture can then be used as the source parameter to [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) or [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) to fill a default or dynamic resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4172d-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4172d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4172d-129">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="4172d-129">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="4172d-130">Textures</span><span class="sxs-lookup"><span data-stu-id="4172d-130">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




