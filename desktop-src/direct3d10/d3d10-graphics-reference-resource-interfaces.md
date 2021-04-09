---
description: 'Direct3D 10 définit un certain nombre d’interfaces pour les deux types de ressources de base : les mémoires tampons et les textures.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Interfaces de ressource (graphiques Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677130d99ede09cec86cf0d45bc0ec0bc5f9093
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110538"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a><span data-ttu-id="9cfb1-103">Interfaces de ressource (graphiques Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="9cfb1-103">Resource Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="9cfb1-104">Direct3D 10 définit un certain nombre d’interfaces pour les deux types de ressources de base : les [mémoires tampons](d3d10-graphics-programming-guide-resources-types.md) et les textures.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-104">Direct3D 10 defines a number of interfaces for the two basic types of resources: [buffers](d3d10-graphics-programming-guide-resources-types.md) and textures.</span></span>



| <span data-ttu-id="9cfb1-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="9cfb1-105">Interfaces</span></span>                                           | <span data-ttu-id="9cfb1-106">Description</span><span class="sxs-lookup"><span data-stu-id="9cfb1-106">Description</span></span>                                          |
|------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="9cfb1-107">**Interface ID3D10Buffer**</span><span class="sxs-lookup"><span data-stu-id="9cfb1-107">**ID3D10Buffer Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | <span data-ttu-id="9cfb1-108">Accède aux données de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-108">Accesses buffer data.</span></span>                                |
| [<span data-ttu-id="9cfb1-109">**Interface ID3D10Resource**</span><span class="sxs-lookup"><span data-stu-id="9cfb1-109">**ID3D10Resource Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | <span data-ttu-id="9cfb1-110">Classe de base pour une ressource.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-110">Base class for a resource.</span></span>                           |
| [<span data-ttu-id="9cfb1-111">**Interface ID3D10Texture1D**</span><span class="sxs-lookup"><span data-stu-id="9cfb1-111">**ID3D10Texture1D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | <span data-ttu-id="9cfb1-112">Accède aux données dans une texture 1D ou un tableau de texture 1D.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-112">Accesses data in a 1D texture or a 1D texture array.</span></span> |
| [<span data-ttu-id="9cfb1-113">**Interface ID3D10Texture2D**</span><span class="sxs-lookup"><span data-stu-id="9cfb1-113">**ID3D10Texture2D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | <span data-ttu-id="9cfb1-114">Accède aux données dans une texture 2D ou un tableau de texture 2D</span><span class="sxs-lookup"><span data-stu-id="9cfb1-114">Accesses data in a 2D texture or a 2D texture array</span></span>  |
| [<span data-ttu-id="9cfb1-115">**Interface ID3D10Texture3D**</span><span class="sxs-lookup"><span data-stu-id="9cfb1-115">**ID3D10Texture3D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | <span data-ttu-id="9cfb1-116">Accède aux données dans une texture 3D ou un tableau de texture 3D.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-116">Accesses data in a 3D texture or a 3D texture array.</span></span> |



 

<span data-ttu-id="9cfb1-117">Une application utilise une vue pour lier une ressource à une [étape de pipeline](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="9cfb1-117">An application uses a view to bind a resource to a [pipeline stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> <span data-ttu-id="9cfb1-118">La [vue](d3d10-graphics-programming-guide-resources-access-views.md) définit comment la ressource est accessible pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-118">The [view](d3d10-graphics-programming-guide-resources-access-views.md) defines how the resource can be accessed during rendering.</span></span> <span data-ttu-id="9cfb1-119">L’API contient ces interfaces d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-119">The API contains these view interfaces.</span></span>



| <span data-ttu-id="9cfb1-120">Interfaces</span><span class="sxs-lookup"><span data-stu-id="9cfb1-120">Interfaces</span></span>                                                               | <span data-ttu-id="9cfb1-121">Description</span><span class="sxs-lookup"><span data-stu-id="9cfb1-121">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9cfb1-122">**Interface ID3D10DepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="9cfb1-122">**ID3D10DepthStencilView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | <span data-ttu-id="9cfb1-123">Accède aux données dans une texture de [stencil de profondeur](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) .</span><span class="sxs-lookup"><span data-stu-id="9cfb1-123">Accesses data in a [depth-stencil](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) texture.</span></span> |
| [<span data-ttu-id="9cfb1-124">**Interface ID3D10RenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="9cfb1-124">**ID3D10RenderTargetView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | <span data-ttu-id="9cfb1-125">Accède aux données d’une [cible de rendu](d3d10-graphics-programming-guide-resources-creating-textures.md).</span><span class="sxs-lookup"><span data-stu-id="9cfb1-125">Accesses data in a [render target](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>        |
| [<span data-ttu-id="9cfb1-126">**Interface ID3D10ShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="9cfb1-126">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | <span data-ttu-id="9cfb1-127">Accède aux données d’une ressource Shader dans Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-127">Accesses data in a shader-resource in Direct3D 10.0.</span></span>                                                         |
| [<span data-ttu-id="9cfb1-128">**Interface ID3D10ShaderResourceView1**</span><span class="sxs-lookup"><span data-stu-id="9cfb1-128">**ID3D10ShaderResourceView1 Interface**</span></span>](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | <span data-ttu-id="9cfb1-129">Accède aux données d’une ressource Shader dans Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-129">Accesses data in a shader-resource in Direct3D 10.1.</span></span>                                                         |
| [<span data-ttu-id="9cfb1-130">**Interface ID3D10View**</span><span class="sxs-lookup"><span data-stu-id="9cfb1-130">**ID3D10View Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | <span data-ttu-id="9cfb1-131">Classe de base pour une vue.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-131">Base class for a view.</span></span>                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="9cfb1-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9cfb1-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cfb1-133">Référence de ressource</span><span class="sxs-lookup"><span data-stu-id="9cfb1-133">Resource Reference</span></span>](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
