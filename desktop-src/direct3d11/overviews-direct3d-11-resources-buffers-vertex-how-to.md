---
title: Comment créer une mémoire tampon de vertex
description: Cette rubrique montre comment initialiser une mémoire tampon de vertex statique, autrement dit, une mémoire tampon de vertex qui ne change pas.
ms.assetid: 584a39d1-7629-429a-b451-64b1432cb48f
keywords:
- mémoire tampon de vertex, création
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e0b3d9d8f731b01e7c919105c21c8d150f864a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310437"
---
# <a name="how-to-create-a-vertex-buffer"></a><span data-ttu-id="cdbe7-104">Comment : créer une mémoire tampon de vertex</span><span class="sxs-lookup"><span data-stu-id="cdbe7-104">How to: Create a Vertex Buffer</span></span>

<span data-ttu-id="cdbe7-105">Les [mémoires tampons de vertex](overviews-direct3d-11-resources-buffers-intro.md) contiennent des données par vertex.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-105">[Vertex buffers](overviews-direct3d-11-resources-buffers-intro.md) contain per vertex data.</span></span> <span data-ttu-id="cdbe7-106">Cette rubrique montre comment initialiser une [mémoire tampon de vertex](overviews-direct3d-11-resources-buffers-intro.md)statique, autrement dit, une mémoire tampon de vertex qui ne change pas.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-106">This topic shows how to initialize a static [vertex buffer](overviews-direct3d-11-resources-buffers-intro.md), that is, a vertex buffer that does not change.</span></span> <span data-ttu-id="cdbe7-107">Pour obtenir de l’aide sur l’initialisation d’une mémoire tampon non statique, consultez la section [Notes](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="cdbe7-107">For help initializing a non-static buffer, see the [remarks](#remarks) section.</span></span>

<span data-ttu-id="cdbe7-108">**Pour initialiser une mémoire tampon de vertex statique**</span><span class="sxs-lookup"><span data-stu-id="cdbe7-108">**To initialize a static vertex buffer**</span></span>

1.  <span data-ttu-id="cdbe7-109">Définissez une structure qui décrit un vertex.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-109">Define a structure that describes a vertex.</span></span> <span data-ttu-id="cdbe7-110">Par exemple, si vos données de vertex contiennent des données de position et des données de couleur, votre structure aurait un vecteur qui décrit la position et un autre qui décrit la couleur.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-110">For example, if your vertex data contains position data and color data, your structure would have one vector that describes the position and another that describes the color.</span></span>
2.  <span data-ttu-id="cdbe7-111">Allouez de la mémoire (à l’aide de malloc ou New) pour la structure que vous avez définie à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-111">Allocate memory (using malloc or new) for the structure that you defined in step one.</span></span> <span data-ttu-id="cdbe7-112">Remplissez cette mémoire tampon avec les données de vertex réelles qui décrivent votre géométrie.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-112">Fill this buffer with the actual vertex data that describes your geometry.</span></span>
3.  <span data-ttu-id="cdbe7-113">Créez une description de la mémoire tampon en remplissant une structure [**\_ \_ desc de tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="cdbe7-113">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="cdbe7-114">Transmettez l' \_ indicateur de tampon de vertex de liaison d3d11 \_ \_ au membre **BindFlags** et transmettez la taille de la structure de l’étape 1 au membre **ByteWidth** .</span><span class="sxs-lookup"><span data-stu-id="cdbe7-114">Pass the D3D11\_BIND\_VERTEX\_BUFFER flag to the **BindFlags** member and pass the size of the structure from step one to the **ByteWidth** member.</span></span>
4.  <span data-ttu-id="cdbe7-115">Créez une description des données de sous-ressource en remplissant une structure de [**\_ \_ données**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) de sous-ressource d3d11.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="cdbe7-116">Le membre **pSysMem** de la structure de données de sous- [**\_ ressources \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) doit pointer directement vers les données de ressources créées à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-116">The **pSysMem** member of the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure should point directly to the resource data created in step two.</span></span>
5.  <span data-ttu-id="cdbe7-117">Appelez [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) lors du passage de la structure DESC de la [**\_ \_ mémoire tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , de la structure de données de la sous- [**\_ ressource \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) et de l’adresse d’un pointeur vers l’interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) à initialiser.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="cdbe7-118">L’exemple de code suivant montre comment créer une mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-118">The following code example demonstrates how to create a vertex buffer.</span></span> <span data-ttu-id="cdbe7-119">Cet exemple suppose que **g \_ pd3dDevice** est un objet [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) valide.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object.</span></span>


```
ID3D11Buffer*      g_pVertexBuffer;

// Define the data-type that
// describes a vertex.
struct SimpleVertexCombined
{
    XMFLOAT3 Pos;  
    XMFLOAT3 Col;  
};

// Supply the actual vertex data.
SimpleVertexCombined verticesCombo[] =
{
    XMFLOAT3( 0.0f, 0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.0f, 0.5f ),
    XMFLOAT3( 0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.5f, 0.0f, 0.0f ),
    XMFLOAT3( -0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.5f, 0.0f ),
};

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage            = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
bufferDesc.BindFlags        = D3D11_BIND_VERTEX_BUFFER;
bufferDesc.CPUAccessFlags   = 0;
bufferDesc.MiscFlags        = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = verticesCombo;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the vertex buffer.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer );
    
```



## <a name="remarks"></a><span data-ttu-id="cdbe7-120">Notes</span><span class="sxs-lookup"><span data-stu-id="cdbe7-120">Remarks</span></span>

<span data-ttu-id="cdbe7-121">Voici quelques méthodes permettant d’initialiser une mémoire tampon de vertex qui change au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-121">Here are some ways to initialize a vertex buffer that changes over time.</span></span>

1.  <span data-ttu-id="cdbe7-122">Créez une deuxième mémoire tampon avec l' [**\_ utilisation \_ intermédiaire de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); remplissez la deuxième mémoire tampon à l’aide de [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext :: DEMAPPAGE**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); utilisez [**ID3D11DeviceContext :: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) pour copier à partir de la mémoire tampon de mise en lots vers la mémoire tampon par défaut.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-122">Create a 2nd buffer with [**D3D11\_USAGE\_STAGING**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); fill the second buffer using [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); use [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) to copy from the staging buffer to the default buffer.</span></span>
2.  <span data-ttu-id="cdbe7-123">Utilisez [**ID3D11DeviceContext :: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) pour copier des données à partir de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-123">Use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to copy data from memory.</span></span>
3.  <span data-ttu-id="cdbe7-124">Créez un tampon avec [**\_ l’utilisation \_ dynamique de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)et remplissez-le avec [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext :: DEMAPPAGE**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (en utilisant les indicateurs Discard et NoOverwrite de manière appropriée).</span><span class="sxs-lookup"><span data-stu-id="cdbe7-124">Create a buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), and fill it with [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (using the Discard and NoOverwrite flags appropriately).</span></span>

<span data-ttu-id="cdbe7-125">\#1 et \# 2 sont utiles pour le contenu qui change moins d’une fois par frame.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-125">\#1 and \#2 are useful for content that changes less than once per frame.</span></span> <span data-ttu-id="cdbe7-126">En général, les lectures GPU sont rapides et les mises à jour de l’UC sont plus lentes.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-126">In general, GPU reads will be fast and CPU updates will be slower.</span></span>

<span data-ttu-id="cdbe7-127">\#3 est utile pour le contenu qui change plus d’une fois par frame.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-127">\#3 is useful for content that changes more than once per frame.</span></span> <span data-ttu-id="cdbe7-128">En général, les lectures GPU sont plus lentes, mais les mises à jour de l’UC sont plus rapides.</span><span class="sxs-lookup"><span data-stu-id="cdbe7-128">In general, GPU reads will be slower, but CPU updates will be faster.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdbe7-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cdbe7-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdbe7-130">Mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="cdbe7-130">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="cdbe7-131">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="cdbe7-131">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




