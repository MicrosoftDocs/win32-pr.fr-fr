---
title: Comment créer un tampon d’index
description: Cette rubrique montre comment initialiser un tampon d’index en vue de sa restitution.
ms.assetid: 4b33d32a-27fd-4652-87ac-3b7268881f89
keywords:
- mémoire tampon d’index, création
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c4c99639748876a5f5fd84e546aaf299885c76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197092"
---
# <a name="how-to-create-an-index-buffer"></a><span data-ttu-id="5a45c-104">Comment : créer un tampon d’index</span><span class="sxs-lookup"><span data-stu-id="5a45c-104">How to: Create an Index Buffer</span></span>

<span data-ttu-id="5a45c-105">Les [tampons d’index](overviews-direct3d-11-resources-buffers-intro.md) contiennent des données d’index.</span><span class="sxs-lookup"><span data-stu-id="5a45c-105">[Index buffers](overviews-direct3d-11-resources-buffers-intro.md) contain index data.</span></span> <span data-ttu-id="5a45c-106">Cette rubrique montre comment initialiser un [tampon d’index](overviews-direct3d-11-resources-buffers-intro.md) en vue de sa restitution.</span><span class="sxs-lookup"><span data-stu-id="5a45c-106">This topic shows how to initialize an [index buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="5a45c-107">**Pour initialiser un tampon d’index**</span><span class="sxs-lookup"><span data-stu-id="5a45c-107">**To initialize an index buffer**</span></span>

1.  <span data-ttu-id="5a45c-108">Créez une mémoire tampon qui contient vos informations d’index.</span><span class="sxs-lookup"><span data-stu-id="5a45c-108">Create a buffer that contains your index information.</span></span>
2.  <span data-ttu-id="5a45c-109">Créez une description de la mémoire tampon en remplissant une structure [**\_ \_ desc de tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="5a45c-109">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="5a45c-110">Transmettez l' \_ indicateur de tampon d’index de liaison d3d11 \_ \_ au membre **BindFlags** et transmettez la taille de la mémoire tampon en octets au membre **ByteWidth** .</span><span class="sxs-lookup"><span data-stu-id="5a45c-110">Pass the D3D11\_BIND\_INDEX\_BUFFER flag to the **BindFlags** member and pass the size of the buffer in bytes to the **ByteWidth** member.</span></span>
3.  <span data-ttu-id="5a45c-111">Créez une description des données de sous-ressource en remplissant une structure de [**\_ \_ données**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) de sous-ressource d3d11.</span><span class="sxs-lookup"><span data-stu-id="5a45c-111">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="5a45c-112">Le membre **pSysMem** doit pointer directement vers les données d’index créées à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="5a45c-112">The **pSysMem** member should point directly to the index data created in step one.</span></span>
4.  <span data-ttu-id="5a45c-113">Appelez [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) lors du passage de la structure DESC de la [**\_ \_ mémoire tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , de la structure de données de la sous- [**\_ ressource \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) et de l’adresse d’un pointeur vers l’interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) à initialiser.</span><span class="sxs-lookup"><span data-stu-id="5a45c-113">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="5a45c-114">L’exemple de code suivant montre comment créer une mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="5a45c-114">The following code example demonstrates how to create an index buffer.</span></span> <span data-ttu-id="5a45c-115">Cet exemple suppose que</span><span class="sxs-lookup"><span data-stu-id="5a45c-115">This example assumes that</span></span>


```
g_pd3dDevice
```



<span data-ttu-id="5a45c-116">est un objet [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) valide et</span><span class="sxs-lookup"><span data-stu-id="5a45c-116">is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that</span></span>


```
g_pd3dContext
```



<span data-ttu-id="5a45c-117">est un objet [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) valide.</span><span class="sxs-lookup"><span data-stu-id="5a45c-117">is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


```
ID3D11Buffer *g_pIndexBuffer = NULL;

// Create indices.
unsigned int indices[] = { 0, 1, 2 };

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage           = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
bufferDesc.BindFlags       = D3D11_BIND_INDEX_BUFFER;
bufferDesc.CPUAccessFlags  = 0;
bufferDesc.MiscFlags       = 0;

// Define the resource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = indices;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer with the device.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
if( FAILED( hr ) )
    return hr;

// Set the buffer.
g_pd3dContext->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
    
```



## <a name="related-topics"></a><span data-ttu-id="5a45c-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a45c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a45c-119">Mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="5a45c-119">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="5a45c-120">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="5a45c-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




