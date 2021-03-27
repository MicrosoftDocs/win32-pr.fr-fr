---
title: Comment créer une mémoire tampon constante
description: Cette rubrique montre comment initialiser une mémoire tampon constante en préparation du rendu.
ms.assetid: 78694ac2-e850-402d-8c99-6afb0bd5d660
keywords:
- mémoire tampon constante, création
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1abb6718ad223ff389aa0b7ebf10ad1ec8bacd71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729564"
---
# <a name="how-to-create-a-constant-buffer"></a><span data-ttu-id="3faa7-104">Comment : créer une mémoire tampon constante</span><span class="sxs-lookup"><span data-stu-id="3faa7-104">How to: Create a Constant Buffer</span></span>

<span data-ttu-id="3faa7-105">Les [mémoires tampons constantes](overviews-direct3d-11-resources-buffers-intro.md) contiennent des données de constante de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3faa7-105">[Constant buffers](overviews-direct3d-11-resources-buffers-intro.md) contain shader constant data.</span></span> <span data-ttu-id="3faa7-106">Cette rubrique montre comment initialiser une [mémoire tampon constante](overviews-direct3d-11-resources-buffers-intro.md) en préparation du rendu.</span><span class="sxs-lookup"><span data-stu-id="3faa7-106">This topic shows how to initialize a [constant buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="3faa7-107">**Pour initialiser une mémoire tampon constante**</span><span class="sxs-lookup"><span data-stu-id="3faa7-107">**To initialize a constant buffer**</span></span>

1.  <span data-ttu-id="3faa7-108">Définissez une structure qui décrit les données constantes du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="3faa7-108">Define a structure that describes the vertex shader constant data.</span></span>
2.  <span data-ttu-id="3faa7-109">Allouez de la mémoire pour la structure que vous avez définie à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="3faa7-109">Allocate memory for the structure that you defined in step one.</span></span> <span data-ttu-id="3faa7-110">Remplissez cette mémoire tampon avec des données de constante de nuanceur vertex.</span><span class="sxs-lookup"><span data-stu-id="3faa7-110">Fill this buffer with vertex shader constant data.</span></span> <span data-ttu-id="3faa7-111">Vous pouvez utiliser **malloc** ou **New** pour allouer la mémoire, ou vous pouvez allouer de la mémoire pour la structure à partir de la pile.</span><span class="sxs-lookup"><span data-stu-id="3faa7-111">You can use **malloc** or **new** to allocate the memory, or you can allocate memory for the structure from the stack.</span></span>
3.  <span data-ttu-id="3faa7-112">Créez une description de la mémoire tampon en remplissant une structure [**\_ \_ desc de tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="3faa7-112">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="3faa7-113">Transmettez l' \_ indicateur de tampon de la constante de liaison d3d11 \_ \_ au membre **BindFlags** et transmettez la taille de la structure de la description de la mémoire tampon constante en octets au membre **ByteWidth** .</span><span class="sxs-lookup"><span data-stu-id="3faa7-113">Pass the D3D11\_BIND\_CONSTANT\_BUFFER flag to the **BindFlags** member and pass the size of the constant buffer description structure in bytes to the **ByteWidth** member.</span></span>

    > [!Note]  
    > <span data-ttu-id="3faa7-114">L’indicateur de tampon de la \_ constante de liaison d3d11 \_ \_ ne peut pas être combiné avec d’autres indicateurs.</span><span class="sxs-lookup"><span data-stu-id="3faa7-114">The D3D11\_BIND\_CONSTANT\_BUFFER flag cannot be combined with any other flags.</span></span>

     

4.  <span data-ttu-id="3faa7-115">Créez une description des données de sous-ressource en remplissant une structure de [**\_ \_ données**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) de sous-ressource d3d11.</span><span class="sxs-lookup"><span data-stu-id="3faa7-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="3faa7-116">Le membre **pSysMem** de la structure de données de sous- **\_ ressources \_ d3d11** doit pointer directement vers les données de constante de nuanceur de sommets que vous avez créées à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="3faa7-116">The **pSysMem** member of the **D3D11\_SUBRESOURCE\_DATA** structure must point directly to the vertex shader constant data that you created in step two.</span></span>
5.  <span data-ttu-id="3faa7-117">Appelez [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) lors du passage de la structure DESC de la [**\_ \_ mémoire tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , de la structure de données de la sous- [**\_ ressource \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) et de l’adresse d’un pointeur vers l’interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) à initialiser.</span><span class="sxs-lookup"><span data-stu-id="3faa7-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="3faa7-118">Ces exemples de code montrent comment créer une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="3faa7-118">These code examples demonstrate how to create a constant buffer.</span></span>

<span data-ttu-id="3faa7-119">Cet exemple suppose que **g \_ pd3dDevice** est un objet [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) valide et que **g \_ pd3dContext** est un objet [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) valide.</span><span class="sxs-lookup"><span data-stu-id="3faa7-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that **g\_pd3dContext** is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


```C++
ID3D11Buffer*   g_pConstantBuffer11 = NULL;

// Define the constant data used to communicate with shaders.
struct VS_CONSTANT_BUFFER
{
    XMFLOAT4X4 mWorldViewProj;                              
    XMFLOAT4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                                            
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
} VS_CONSTANT_BUFFER;

// Supply the vertex shader constant data.
VS_CONSTANT_BUFFER VsConstData;
VsConstData.mWorldViewProj = {...};
VsConstData.vSomeVectorThatMayBeNeededByASpecificShader = XMFLOAT4(1,2,3,4);
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader = 3.0f;
VsConstData.fTime = 1.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader2 = 2.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader3 = 4.0f;

// Fill in a buffer description.
D3D11_BUFFER_DESC cbDesc;
cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
cbDesc.Usage = D3D11_USAGE_DYNAMIC;
cbDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;
cbDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
cbDesc.MiscFlags = 0;
cbDesc.StructureByteStride = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = &VsConstData;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer.
hr = g_pd3dDevice->CreateBuffer( &cbDesc, &InitData, 
                                 &g_pConstantBuffer11 );

if( FAILED( hr ) )
   return hr;

// Set the buffer.
g_pd3dContext->VSSetConstantBuffers( 0, 1, &g_pConstantBuffer11 );
    
```



<span data-ttu-id="3faa7-120">Cet exemple montre la définition de CBuffer HLSL associée.</span><span class="sxs-lookup"><span data-stu-id="3faa7-120">This example shows the associated HLSL cbuffer definition.</span></span>

``` syntax
cbuffer VS_CONSTANT_BUFFER : register(b0)
{
    matrix mWorldViewProj;
    float4  vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};
```

> [!Note]  
> <span data-ttu-id="3faa7-121">Veillez à mettre en correspondance \_ la \_ disposition de la mémoire tampon constante Visual Studio en C++ avec la disposition HLSL.</span><span class="sxs-lookup"><span data-stu-id="3faa7-121">Make sure to match the VS\_CONSTANT\_BUFFER memory layout in C++ with the HLSL layout.</span></span> <span data-ttu-id="3faa7-122">Pour plus d’informations sur la façon dont le langage HLSL gère la disposition en mémoire, consultez [règles de compression pour les variables constantes](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span><span class="sxs-lookup"><span data-stu-id="3faa7-122">For info about how HLSL handles layout in memory, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3faa7-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3faa7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3faa7-124">Mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="3faa7-124">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="3faa7-125">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="3faa7-125">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 