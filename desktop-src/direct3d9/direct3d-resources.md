---
description: Les ressources sont les textures et les mémoires tampons utilisées pour le rendu d’une scène.
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: Ressources Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7745318db3d880711ee962edb086996764455ec8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109166"
---
# <a name="direct3d-resources-direct3d-9"></a><span data-ttu-id="898dd-103">Ressources Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="898dd-103">Direct3D Resources (Direct3D 9)</span></span>

<span data-ttu-id="898dd-104">Les ressources sont les textures et les mémoires tampons utilisées pour le rendu d’une scène.</span><span class="sxs-lookup"><span data-stu-id="898dd-104">Resources are the textures and buffers that are used to render a scene.</span></span> <span data-ttu-id="898dd-105">Les applications doivent créer, charger, copier et utiliser des ressources.</span><span class="sxs-lookup"><span data-stu-id="898dd-105">Applications need to create, load, copy, and use resources.</span></span> <span data-ttu-id="898dd-106">Cette section fournit une brève introduction aux ressources et aux étapes et méthodes utilisées par les applications lors de l’utilisation de ressources.</span><span class="sxs-lookup"><span data-stu-id="898dd-106">This section gives a brief introduction to resources and the steps and methods used by applications when working with resources.</span></span>

<span data-ttu-id="898dd-107">Toutes les ressources, y compris les ressources Geometry [**IDirect3DIndexBuffer9**](/windows/desktop/api) et [**IDirect3DVertexBuffer9**](/windows/desktop/api), héritent de l’interface [**IDirect3DResource9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="898dd-107">All resources, including the geometry resources [**IDirect3DIndexBuffer9**](/windows/desktop/api) and [**IDirect3DVertexBuffer9**](/windows/desktop/api), inherit from the [**IDirect3DResource9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="898dd-108">Les ressources de texture, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api)et [**IDirect3DVolumeTexture9**](/windows/desktop/api), héritent également de l’interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) .</span><span class="sxs-lookup"><span data-stu-id="898dd-108">The texture resources, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api), and [**IDirect3DVolumeTexture9**](/windows/desktop/api), also inherit from the [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface.</span></span>

-   [<span data-ttu-id="898dd-109">Propriétés de ressource (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="898dd-109">Resource Properties (Direct3D 9)</span></span>](resource-properties.md)
-   [<span data-ttu-id="898dd-110">Manipulation des ressources (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="898dd-110">Manipulating Resources (Direct3D 9)</span></span>](manipulating-resources.md)
-   [<span data-ttu-id="898dd-111">Verrouillage des ressources (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="898dd-111">Locking Resources (Direct3D 9)</span></span>](locking-resources.md)
-   [<span data-ttu-id="898dd-112">Relations entre les ressources (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="898dd-112">Resource Relationships (Direct3D 9)</span></span>](resource-relationships.md)
-   [<span data-ttu-id="898dd-113">Gestion des ressources (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="898dd-113">Managing Resources (Direct3D 9)</span></span>](managing-resources.md)
-   [<span data-ttu-id="898dd-114">Ressources gérées par l’application et stratégies d’allocation (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="898dd-114">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [<span data-ttu-id="898dd-115">Mémoires tampons d’index (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="898dd-115">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
-   [<span data-ttu-id="898dd-116">Mémoires tampons de vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="898dd-116">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)

## <a name="related-topics"></a><span data-ttu-id="898dd-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="898dd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="898dd-118">Prise en main</span><span class="sxs-lookup"><span data-stu-id="898dd-118">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
