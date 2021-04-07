---
description: La création de mémoires tampons requiert la définition des données que la mémoire tampon stockera, la fourniture des données d’initialisation et la configuration des indicateurs d’utilisation et de liaison appropriés. Pour créer des textures, consultez Création de ressources de texture (Direct3D 10).
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: Création de ressources de mémoire tampon (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748516"
---
# <a name="creating-buffer-resources-direct3d-10"></a><span data-ttu-id="0e3f6-104">Création de ressources de mémoire tampon (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0e3f6-104">Creating Buffer Resources (Direct3D 10)</span></span>

<span data-ttu-id="0e3f6-105">La création de mémoires tampons requiert la définition des données que la mémoire tampon stockera, la fourniture des données d’initialisation et la configuration des indicateurs d’utilisation et de liaison appropriés.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-105">Creating buffers requires defining the data that the buffer will store, providing initialization data, and setting up appropriate usage and binding flags.</span></span> <span data-ttu-id="0e3f6-106">Pour créer des textures, consultez [création de ressources de texture (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).</span><span class="sxs-lookup"><span data-stu-id="0e3f6-106">To create textures, see [Creating Texture Resources (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>

-   [<span data-ttu-id="0e3f6-107">Créer une mémoire tampon de vertex</span><span class="sxs-lookup"><span data-stu-id="0e3f6-107">Create a Vertex Buffer</span></span>](#create-a-vertex-buffer)
    -   [<span data-ttu-id="0e3f6-108">Créer une description de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="0e3f6-108">Create a Buffer Description</span></span>](#create-a-buffer-description)
    -   [<span data-ttu-id="0e3f6-109">Créer les données d’initialisation pour la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="0e3f6-109">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
    -   [<span data-ttu-id="0e3f6-110">Créer la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="0e3f6-110">Create the Buffer</span></span>](#create-the-buffer)
-   [<span data-ttu-id="0e3f6-111">Créer un tampon d’index</span><span class="sxs-lookup"><span data-stu-id="0e3f6-111">Create an Index Buffer</span></span>](#create-an-index-buffer)
-   [<span data-ttu-id="0e3f6-112">Créer une mémoire tampon constante</span><span class="sxs-lookup"><span data-stu-id="0e3f6-112">Create a Constant Buffer</span></span>](#create-a-constant-buffer)
-   [<span data-ttu-id="0e3f6-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e3f6-113">Related topics</span></span>](#related-topics)

## <a name="create-a-vertex-buffer"></a><span data-ttu-id="0e3f6-114">Créer une mémoire tampon de vertex</span><span class="sxs-lookup"><span data-stu-id="0e3f6-114">Create a Vertex Buffer</span></span>

<span data-ttu-id="0e3f6-115">Les étapes de création d’une [mémoire tampon de vertex](d3d10-graphics-programming-guide-resources-types.md) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-115">The steps to creating a [vertex buffer](d3d10-graphics-programming-guide-resources-types.md) are as follows.</span></span>

-   [<span data-ttu-id="0e3f6-116">Créer une description de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="0e3f6-116">Create a Buffer Description</span></span>](#create-a-buffer-description)
-   [<span data-ttu-id="0e3f6-117">Créer les données d’initialisation pour la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="0e3f6-117">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
-   [<span data-ttu-id="0e3f6-118">Créer la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="0e3f6-118">Create the Buffer</span></span>](#create-the-buffer)

### <a name="create-a-buffer-description"></a><span data-ttu-id="0e3f6-119">Créer une description de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="0e3f6-119">Create a Buffer Description</span></span>

<span data-ttu-id="0e3f6-120">Lors de la création d’une mémoire tampon de vertex, une description de mémoire tampon (voir [**D3D10 \_ buffer \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) est utilisée pour définir la manière dont les données sont organisées dans la mémoire tampon, comment le pipeline peut accéder à la mémoire tampon et comment la mémoire tampon sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-120">When creating a vertex buffer, a buffer description (see [**D3D10\_BUFFER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) is used to define how data is organized within the buffer, how the pipeline can access the buffer, and how the buffer will be used.</span></span>

<span data-ttu-id="0e3f6-121">L’exemple suivant montre comment créer une description de mémoire tampon pour un triangle unique avec des sommets qui contiennent des valeurs de position et de couleur.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-121">The following example demonstrates how to create a buffer description for a single triangle with vertices that contain position and color values.</span></span>


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



<span data-ttu-id="0e3f6-122">Dans cet exemple, la description de la mémoire tampon est initialisée avec presque tous les paramètres par défaut pour [**l’utilisation**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), l’accès de l' [**UC**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) et les [**indicateurs divers**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag).</span><span class="sxs-lookup"><span data-stu-id="0e3f6-122">In this example, the buffer description is initialized with almost all default settings for [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**CPU access**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) and [**miscellaneous flags**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag).</span></span> <span data-ttu-id="0e3f6-123">Les autres paramètres concernent l' [**indicateur de liaison**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) qui identifie la ressource comme une mémoire tampon de vertex uniquement et la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-123">The other settings are for the [**bind flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) which identifies the resource as a vertex buffer only, and the size of the buffer.</span></span>

<span data-ttu-id="0e3f6-124">Les indicateurs d’accès à l’utilisation et à l’UC sont importants pour les performances.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-124">The usage and CPU access flags are important for performance.</span></span> <span data-ttu-id="0e3f6-125">Ces deux indicateurs déterminent la fréquence à laquelle une ressource est accédée, le type de mémoire dans lequel la ressource peut être chargée et le processeur dont elle a besoin pour accéder à la ressource.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-125">These two flags together determine how often a resource gets accessed, what type of memory the resource could be loaded into, and what processor needs to access the resource.</span></span> <span data-ttu-id="0e3f6-126">Utilisation par défaut cette ressource ne sera pas très souvent mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-126">Default usage this resource will not be updated very often.</span></span> <span data-ttu-id="0e3f6-127">Le fait de définir un accès processeur à 0 signifie que le processeur n’a pas besoin de lire ou d’écrire la ressource.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-127">Setting CPU access to 0 means that the CPU will not need to either read or write the resource.</span></span> <span data-ttu-id="0e3f6-128">Pris en charge, cela signifie que le runtime peut charger la ressource dans la mémoire la plus performante pour le GPU puisque la ressource ne requiert pas d’accès au processeur.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-128">Taken in combination, this means that the runtime can load the resource into the highest performing memory for the GPU since the resource does not require CPU access.</span></span>

<span data-ttu-id="0e3f6-129">Comme prévu, il existe un compromis entre les meilleures performances et l’accessibilité à tout moment par les deux processeurs.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-129">As expected, there is a tradeoff between best performance and any-time accessibility by either processor.</span></span> <span data-ttu-id="0e3f6-130">Par exemple, l’utilisation par défaut sans accès UC signifie que la ressource peut être mise à la disposition exclusive du GPU.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-130">For example, the default usage with no CPU access means that the resource can be made available to the GPU exclusively.</span></span> <span data-ttu-id="0e3f6-131">Cela peut inclure le chargement de la ressource dans la mémoire qui n’est pas directement accessible par le processeur.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-131">This could include loading the resource into memory not directly accessible by the CPU.</span></span> <span data-ttu-id="0e3f6-132">La ressource ne peut être modifiée qu’avec [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).</span><span class="sxs-lookup"><span data-stu-id="0e3f6-132">The resource could only be modified with [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).</span></span>

### <a name="create-the-initialization-data-for-the-buffer"></a><span data-ttu-id="0e3f6-133">Créer les données d’initialisation pour la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="0e3f6-133">Create the Initialization Data for the Buffer</span></span>

<span data-ttu-id="0e3f6-134">Une mémoire tampon n’est qu’une collection d’éléments et est présentée comme un tableau 1D.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-134">A buffer is just a collection of elements and is laid out as a 1D array.</span></span> <span data-ttu-id="0e3f6-135">Par conséquent, le pas de la mémoire système et le pas de la tranche de mémoire système sont les mêmes ; taille de la déclaration de données de vertex.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-135">As a result, the system memory pitch and system memory slice pitch are both the same; the size of the vertex data declaration.</span></span> <span data-ttu-id="0e3f6-136">Une application peut fournir des données d’initialisation quand une mémoire tampon est créée à l’aide d’une description de sous- [**ressource**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), qui contient un pointeur vers les données de ressource réelles et contient des informations sur la taille et la disposition de ces données.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-136">An application can provide initialization data when a buffer is created using a [**subresource description**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), which contains a pointer to the actual resource data and contains information about the size and layout of that data.</span></span>

<span data-ttu-id="0e3f6-137">Toute mémoire tampon créée avec une utilisation immuable ( [**voir \_ utilisation \_ de D3D10 immuable**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) doit être initialisée au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-137">Any buffer created with immutable usage (see [**D3D10\_USAGE\_IMMUTABLE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) must be initialized at creation time.</span></span> <span data-ttu-id="0e3f6-138">Les mémoires tampons qui utilisent l’un des autres indicateurs d’utilisation peuvent être mises à jour après l’initialisation à l’aide de [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)et [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource), ou en accédant à la mémoire sous-jacente à l’aide de la méthode [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) .</span><span class="sxs-lookup"><span data-stu-id="0e3f6-138">Buffers that use any of the other usage flags can be updated after initialization using [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion), and [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource), or by accessing its underlying memory using the [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) method.</span></span>

### <a name="create-the-buffer"></a><span data-ttu-id="0e3f6-139">Créer la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="0e3f6-139">Create the Buffer</span></span>

<span data-ttu-id="0e3f6-140">L’utilisation de la description de la mémoire tampon et des données d’initialisation (facultatives) appellent [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) pour créer une mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-140">Using the buffer description and the initialization data (which is optional) call [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) to create a vertex buffer.</span></span> <span data-ttu-id="0e3f6-141">L’extrait de code suivant montre comment créer une mémoire tampon de vertex à partir d’un tableau de données de vertex déclarées par l’application.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-141">The following code snippet demonstrates how to create a vertex buffer from an array of vertex data declared by the application.</span></span>


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a><span data-ttu-id="0e3f6-142">Créer un tampon d’index</span><span class="sxs-lookup"><span data-stu-id="0e3f6-142">Create an Index Buffer</span></span>

<span data-ttu-id="0e3f6-143">La création d’un tampon d’index est très similaire à la création d’une mémoire tampon de vertex. avec deux différences.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-143">Creating an index buffer is very similar to creating a vertex buffer; with two differences.</span></span> <span data-ttu-id="0e3f6-144">Une mémoire tampon d’index contient uniquement des données 16 bits ou 32 bits (à la place de la large gamme de formats disponibles pour une mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-144">An index buffer contains only 16-bit or 32-bit data (instead of the wide range of formats available to a vertex buffer.</span></span> <span data-ttu-id="0e3f6-145">Un tampon d’index requiert également un indicateur de liaison d’index-buffer.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-145">An index buffer also requires an index-buffer bind flag.</span></span>

<span data-ttu-id="0e3f6-146">L’exemple suivant montre comment créer un tampon d’index à partir d’un tableau de données d’index.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-146">The following example demonstrates how to create an index buffer from an array of index data.</span></span>


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a><span data-ttu-id="0e3f6-147">Créer une mémoire tampon constante</span><span class="sxs-lookup"><span data-stu-id="0e3f6-147">Create a Constant Buffer</span></span>

<span data-ttu-id="0e3f6-148">Direct3D 10 introduit une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-148">Direct3D 10 introduces a constant buffer.</span></span> <span data-ttu-id="0e3f6-149">Une mémoire tampon constante, ou une mémoire tampon constante de nuanceur, est une mémoire tampon qui contient des constantes de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0e3f6-149">A constant buffer, or shader constant buffer, is a buffer that contains shader constants.</span></span> <span data-ttu-id="0e3f6-150">Voici un exemple de création d’une mémoire tampon constante, extrait de l' [exemple HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="0e3f6-150">Here is an example of creating a constant buffer, taken from the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



<span data-ttu-id="0e3f6-151">Notez que, lors de l’utilisation de l’interface d' [**interface ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) , le processus de création, de liaison et de remise d’une mémoire tampon constante est géré par l’instance d' **interface ID3D10Effect** .</span><span class="sxs-lookup"><span data-stu-id="0e3f6-151">Note that when using the [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) interface the process of creating, binding and comitting a constant buffer is handled by the **ID3D10Effect Interface** instance.</span></span> <span data-ttu-id="0e3f6-152">Dans ce cas, il suffit de nescesary pour récupérer la variable de l’effet avec l’une des méthodes GetVariable comme [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) et mettre à jour la variable avec l’une des méthodes SetVariable comme [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix).</span><span class="sxs-lookup"><span data-stu-id="0e3f6-152">In that case it is only nescesary to get the variable from the effect with one of the GetVariable methods such as [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) and update the variable with one of the SetVariable methods such as [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix).</span></span> <span data-ttu-id="0e3f6-153">Pour obtenir un exemple d’utilisation de l' **interface ID3D10Effect** pour gérer une mémoire tampon constante, consultez le [didacticiel 7 : mappage de texture et mémoires tampons constantes](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="0e3f6-153">For an example of using **ID3D10Effect Interface** to manage a constant buffer see [Tutorial 7: Texture Mapping and Constant Buffers](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e3f6-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e3f6-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e3f6-155">Ressources (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0e3f6-155">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



