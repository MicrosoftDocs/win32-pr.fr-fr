---
title: Utilisation des ressources dynamiques
description: Vous créez et utilisez des ressources dynamiques lorsque votre application doit modifier des données dans ces ressources. Vous pouvez créer des textures et des mémoires tampons pour une utilisation dynamique.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41e00cda7236040679c7863454e4cc18d81106b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190863"
---
# <a name="how-to-use-dynamic-resources"></a><span data-ttu-id="d11f1-104">Comment : utiliser des ressources dynamiques</span><span class="sxs-lookup"><span data-stu-id="d11f1-104">How to: Use dynamic resources</span></span>

<span data-ttu-id="d11f1-105">**API importantes**</span><span class="sxs-lookup"><span data-stu-id="d11f1-105">**Important APIs**</span></span>

-   [<span data-ttu-id="d11f1-106">**ID3D11DeviceContext :: Map**</span><span class="sxs-lookup"><span data-stu-id="d11f1-106">**ID3D11DeviceContext::Map**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [<span data-ttu-id="d11f1-107">**ID3D11DeviceContext :: DEMAPPAGE**</span><span class="sxs-lookup"><span data-stu-id="d11f1-107">**ID3D11DeviceContext::Unmap**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [<span data-ttu-id="d11f1-108">**Utilisation de D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="d11f1-108">**D3D11\_USAGE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

<span data-ttu-id="d11f1-109">Vous créez et utilisez des ressources dynamiques lorsque votre application doit modifier des données dans ces ressources.</span><span class="sxs-lookup"><span data-stu-id="d11f1-109">You create and use dynamic resources when your app needs to change data in those resources.</span></span> <span data-ttu-id="d11f1-110">Vous pouvez créer des textures et des mémoires tampons pour une utilisation dynamique.</span><span class="sxs-lookup"><span data-stu-id="d11f1-110">You can create textures and buffers for dynamic usage.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d11f1-111">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="d11f1-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d11f1-112">Technologies</span><span class="sxs-lookup"><span data-stu-id="d11f1-112">Technologies</span></span>

-   [<span data-ttu-id="d11f1-113">Comment : créer une texture</span><span class="sxs-lookup"><span data-stu-id="d11f1-113">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
-   [<span data-ttu-id="d11f1-114">Comment : initialiser une texture par programmation</span><span class="sxs-lookup"><span data-stu-id="d11f1-114">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [<span data-ttu-id="d11f1-115">Comment : créer une mémoire tampon constante</span><span class="sxs-lookup"><span data-stu-id="d11f1-115">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a><span data-ttu-id="d11f1-116">Prérequis</span><span class="sxs-lookup"><span data-stu-id="d11f1-116">Prerequisites</span></span>

<span data-ttu-id="d11f1-117">Nous partons du principe que vous êtes familiarisé avec C++.</span><span class="sxs-lookup"><span data-stu-id="d11f1-117">We assume that you are familiar with C++.</span></span> <span data-ttu-id="d11f1-118">Vous avez également besoin d’une expérience de base dans les concepts de programmation graphique.</span><span class="sxs-lookup"><span data-stu-id="d11f1-118">You also need basic experience with graphics programming concepts.</span></span>

## <a name="instructions"></a><span data-ttu-id="d11f1-119">Instructions</span><span class="sxs-lookup"><span data-stu-id="d11f1-119">Instructions</span></span>

### <a name="step-1-specify-dynamic-usage"></a><span data-ttu-id="d11f1-120">Étape 1 : spécifier l’utilisation dynamique</span><span class="sxs-lookup"><span data-stu-id="d11f1-120">Step 1: Specify dynamic usage</span></span>

<span data-ttu-id="d11f1-121">Si vous souhaitez que votre application puisse apporter des modifications aux ressources, vous devez spécifier ces ressources comme étant dynamiques et accessibles en écriture au moment de leur création.</span><span class="sxs-lookup"><span data-stu-id="d11f1-121">If you want your app to be able to make changes to resources, you must specify those resources as dynamic and writable when you create them.</span></span>

<span data-ttu-id="d11f1-122">**Pour spécifier l’utilisation dynamique**</span><span class="sxs-lookup"><span data-stu-id="d11f1-122">**To specify dynamic usage**</span></span>

1.  <span data-ttu-id="d11f1-123">Spécifiez l’utilisation des ressources comme dynamique.</span><span class="sxs-lookup"><span data-stu-id="d11f1-123">Specify the resource usage as dynamic.</span></span> <span data-ttu-id="d11f1-124">Par exemple, spécifiez la valeur [**\_ \_ dynamique d’utilisation d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) dans le membre **usage** de la description de la [**\_ \_ mémoire tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) pour un vertex ou une mémoire tampon constante et spécifiez la valeur **\_ \_ dynamique d’utilisation d3d11** dans le membre **usage** de [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) pour une texture 2D.</span><span class="sxs-lookup"><span data-stu-id="d11f1-124">For example, specify the [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) value in the **Usage** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) for a vertex or constant buffer and specify the **D3D11\_USAGE\_DYNAMIC** value in the **Usage** member of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) for a 2D texture.</span></span>
2.  <span data-ttu-id="d11f1-125">Spécifiez la ressource comme accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="d11f1-125">Specify the resource as writable.</span></span> <span data-ttu-id="d11f1-126">Par exemple, spécifiez la valeur d' [**écriture d’accès au \_ processeur \_ \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) dans le membre **cpuaccessflags a** de la description de la [**\_ mémoire tampon \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) ou [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).</span><span class="sxs-lookup"><span data-stu-id="d11f1-126">For example, specify the [**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) value in the **CPUAccessFlags** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) or [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).</span></span>
3.  <span data-ttu-id="d11f1-127">Transmettez la description de la ressource à la fonction de création.</span><span class="sxs-lookup"><span data-stu-id="d11f1-127">Pass the resource description to the creation function.</span></span> <span data-ttu-id="d11f1-128">Par exemple, transmettez l’adresse de la description de la [**\_ mémoire tampon \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) à [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) et transmettez l’adresse de [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) à [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).</span><span class="sxs-lookup"><span data-stu-id="d11f1-128">For example, pass the address of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) to [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) and pass the address of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) to [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).</span></span>

<span data-ttu-id="d11f1-129">Voici un exemple de création d’une mémoire tampon de vertex dynamique :</span><span class="sxs-lookup"><span data-stu-id="d11f1-129">Here is an example of creating a dynamic vertex buffer:</span></span>


```C++
    // Create a vertex buffer for a triangle.

    float2 triangleVertices[] =
    {
        float2(-0.5f, -0.5f),
        float2(0.0f, 0.5f),
        float2(0.5f, -0.5f),
    };

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(float2)* ARRAYSIZE(triangleVertices);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;
    vertexBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
    vertexBufferDesc.MiscFlags = 0;
    vertexBufferDesc.StructureByteStride = 0;

    D3D11_SUBRESOURCE_DATA vertexBufferData;
    vertexBufferData.pSysMem = triangleVertices;
    vertexBufferData.SysMemPitch = 0;
    vertexBufferData.SysMemSlicePitch = 0;

    DX::ThrowIfFailed(
        m_d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        &vertexBufferData,
        &vertexBuffer2
        )
        );

```



### <a name="step-2-change-a-dynamic-resource"></a><span data-ttu-id="d11f1-130">Étape 2 : modifier une ressource dynamique</span><span class="sxs-lookup"><span data-stu-id="d11f1-130">Step 2: Change a dynamic resource</span></span>

<span data-ttu-id="d11f1-131">Si vous avez spécifié une ressource comme dynamique et accessible en écriture au moment de sa création, vous pouvez apporter des modifications ultérieurement à cette ressource.</span><span class="sxs-lookup"><span data-stu-id="d11f1-131">If you specified a resource as dynamic and writable when you created it, you can later make changes to that resource.</span></span>

<span data-ttu-id="d11f1-132">**Pour modifier des données dans une ressource dynamique**</span><span class="sxs-lookup"><span data-stu-id="d11f1-132">**To change data in a dynamic resource**</span></span>

1.  <span data-ttu-id="d11f1-133">Configurez les nouvelles données pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="d11f1-133">Set up the new data for the resource.</span></span> <span data-ttu-id="d11f1-134">Déclarez une variable de type de sous- [**\_ \_ ressource mappée d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) et initialisez-la sur zéro.</span><span class="sxs-lookup"><span data-stu-id="d11f1-134">Declare a [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) type variable and initialize it to zero.</span></span> <span data-ttu-id="d11f1-135">Vous utiliserez cette variable pour modifier la ressource.</span><span class="sxs-lookup"><span data-stu-id="d11f1-135">You'll use this variable to change the resource.</span></span>
2.  <span data-ttu-id="d11f1-136">Désactivez l’accès à l’unité de traitement graphique (GPU) aux données que vous souhaitez modifier et récupérez un pointeur vers la mémoire qui contient les données.</span><span class="sxs-lookup"><span data-stu-id="d11f1-136">Disable graphics processing unit (GPU) access to the data that you want to change and get a pointer to the memory that contains the data.</span></span> <span data-ttu-id="d11f1-137">Pour atteindre ce pointeur, transmettez [**d3d11 \_ Map \_ Write \_ ignore**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) au paramètre *maptype* lorsque vous appelez [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span><span class="sxs-lookup"><span data-stu-id="d11f1-137">To get this pointer, pass [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) to the *MapType* parameter when you call [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span> <span data-ttu-id="d11f1-138">Définissez ce pointeur sur l’adresse de la variable de sous- [**\_ \_ ressource mappée d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) à partir de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="d11f1-138">Set this pointer to the address of the [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) variable from the previous step.</span></span>
3.  <span data-ttu-id="d11f1-139">Écrivez les nouvelles données dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d11f1-139">Write the new data to the memory.</span></span>
4.  <span data-ttu-id="d11f1-140">Appelez [**ID3D11DeviceContext :: DEMAPPAGE**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) pour réactiver l’accès GPU aux données lorsque vous avez terminé d’écrire les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="d11f1-140">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) to reenable GPU access to the data when you're finished writing the new data.</span></span>

<span data-ttu-id="d11f1-141">Voici un exemple de modification d’une mémoire tampon de vertex dynamique :</span><span class="sxs-lookup"><span data-stu-id="d11f1-141">Here is an example of changing a dynamic vertex buffer:</span></span>


```C++
// This might get called as the result of a click event to double the size of the triangle.
void TriangleRenderer::MapDoubleVertices()
{
    D3D11_MAPPED_SUBRESOURCE mappedResource;
    ZeroMemory(&mappedResource, sizeof(D3D11_MAPPED_SUBRESOURCE));
    float2 vertices[] =
    {
        float2(-1.0f, -1.0f),
        float2(0.0f, 1.0f),
        float2(1.0f, -1.0f),
    };
    //  Disable GPU access to the vertex buffer data.
    auto m_d3dContext = m_deviceResources->GetD3DDeviceContext();
    m_d3dContext->Map(vertexBuffer2.Get(), 0, D3D11_MAP_WRITE_DISCARD, 0, &mappedResource);
    //  Update the vertex buffer here.
    memcpy(mappedResource.pData, vertices, sizeof(vertices));
    //  Reenable GPU access to the vertex buffer data.
    m_d3dContext->Unmap(vertexBuffer2.Get(), 0);
}
```



## <a name="remarks"></a><span data-ttu-id="d11f1-142">Notes</span><span class="sxs-lookup"><span data-stu-id="d11f1-142">Remarks</span></span>

### <a name="using-dynamic-textures"></a><span data-ttu-id="d11f1-143">Utilisation de textures dynamiques</span><span class="sxs-lookup"><span data-stu-id="d11f1-143">Using dynamic textures</span></span>

<span data-ttu-id="d11f1-144">Nous vous recommandons de ne créer qu’une seule texture dynamique par format et éventuellement par taille.</span><span class="sxs-lookup"><span data-stu-id="d11f1-144">We recommend that you create only one dynamic texture per format and possibly per size.</span></span> <span data-ttu-id="d11f1-145">Nous vous déconseillons de créer des des mipmaps, des cubes et des volumes dynamiques en raison de la surcharge supplémentaire dans le mappage de chaque niveau.</span><span class="sxs-lookup"><span data-stu-id="d11f1-145">We don't recommend creating dynamic mipmaps, cubes, and volumes because of the additional overhead in mapping every level.</span></span> <span data-ttu-id="d11f1-146">Pour des mipmaps, vous pouvez spécifier [**d3d11 \_ mapper l' \_ écriture \_ ignore**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) uniquement au niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="d11f1-146">For mipmaps, you can specify [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) only on the top level.</span></span> <span data-ttu-id="d11f1-147">Tous les niveaux sont ignorés en mappant simplement le niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="d11f1-147">All levels are discarded by mapping just the top level.</span></span> <span data-ttu-id="d11f1-148">Ce comportement est le même pour les volumes et les cubes.</span><span class="sxs-lookup"><span data-stu-id="d11f1-148">This behavior is the same for volumes and cubes.</span></span> <span data-ttu-id="d11f1-149">Pour les cubes, le niveau supérieur et le visage 0 sont mappés.</span><span class="sxs-lookup"><span data-stu-id="d11f1-149">For cubes, the top level and face 0 are mapped.</span></span>

### <a name="using-dynamic-buffers"></a><span data-ttu-id="d11f1-150">Utilisation de mémoires tampons dynamiques</span><span class="sxs-lookup"><span data-stu-id="d11f1-150">Using dynamic buffers</span></span>

<span data-ttu-id="d11f1-151">Lorsque vous appelez [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) sur une mémoire tampon de vertex statique alors que le GPU utilise la mémoire tampon, vous bénéficiez d’une baisse significative des performances.</span><span class="sxs-lookup"><span data-stu-id="d11f1-151">When you call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) on a static vertex buffer while the GPU is using the buffer, you get a significant performance penalty.</span></span> <span data-ttu-id="d11f1-152">Dans ce cas, **Map** doit attendre la fin de la lecture des données de vertex ou d’index à partir de la mémoire tampon avant que **Map** puisse revenir à l’application appelante, ce qui entraîne un délai important.</span><span class="sxs-lookup"><span data-stu-id="d11f1-152">In this situation, **Map** must wait until the GPU is finished reading vertex or index data from the buffer before **Map** can return to the calling app, which causes a significant delay.</span></span> <span data-ttu-id="d11f1-153">L’appel de **Map** , puis le rendu à partir d’une mémoire tampon statique plusieurs fois par trame, empêche également le GPU de mettre en mémoire tampon les commandes de rendu, car il doit terminer les commandes avant de retourner le pointeur de carte.</span><span class="sxs-lookup"><span data-stu-id="d11f1-153">Calling **Map** and then rendering from a static buffer several times per frame also prevents the GPU from buffering rendering commands because it must finish commands before returning the map pointer.</span></span> <span data-ttu-id="d11f1-154">Sans commandes mises en mémoire tampon, le GPU reste inactif jusqu’à ce que l’application ait fini de remplir la mémoire tampon de vertex ou le tampon d’index et envoie une commande de rendu.</span><span class="sxs-lookup"><span data-stu-id="d11f1-154">Without buffered commands, the GPU remains idle until after the app is finished filling the vertex buffer or index buffer and issues a rendering command.</span></span>

<span data-ttu-id="d11f1-155">Idéalement, les données de vertex ou d’index ne changeraient jamais, mais ce n’est pas toujours possible.</span><span class="sxs-lookup"><span data-stu-id="d11f1-155">Ideally the vertex or index data would never change, but this is not always possible.</span></span> <span data-ttu-id="d11f1-156">Dans de nombreux cas, l’application doit modifier des données de vertex ou d’index à chaque trame, voire plusieurs fois par frame.</span><span class="sxs-lookup"><span data-stu-id="d11f1-156">There are many situations where the app needs to change vertex or index data every frame, perhaps even multiple times per frame.</span></span> <span data-ttu-id="d11f1-157">Dans ce cas, nous vous recommandons de créer le vertex ou le tampon d’index avec [**\_ l’utilisation \_ dynamique de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span><span class="sxs-lookup"><span data-stu-id="d11f1-157">For these situations, we recommend that you create the vertex or index buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span> <span data-ttu-id="d11f1-158">Cet indicateur d’utilisation entraîne l’optimisation du runtime pour les opérations de mappage fréquentes.</span><span class="sxs-lookup"><span data-stu-id="d11f1-158">This usage flag causes the runtime to optimize for frequent map operations.</span></span> <span data-ttu-id="d11f1-159">**D3d11 \_ L’utilisation \_ dynamique** est utile uniquement lorsque la mémoire tampon est mappée fréquemment ; Si les données doivent rester constantes, placez-les dans un tampon statique ou un sommet d’index.</span><span class="sxs-lookup"><span data-stu-id="d11f1-159">**D3D11\_USAGE\_DYNAMIC** is only useful when the buffer is mapped frequently; if data is to remain constant, place that data in a static vertex or index buffer.</span></span>

<span data-ttu-id="d11f1-160">Pour bénéficier d’une amélioration des performances lorsque vous utilisez des mémoires tampons de vertex dynamiques, votre application doit appeler [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) avec les valeurs de [**\_ mappage de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) appropriées.</span><span class="sxs-lookup"><span data-stu-id="d11f1-160">To receive a performance improvement when you use dynamic vertex buffers, your app must call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) with the appropriate [**D3D11\_MAP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) values.</span></span> <span data-ttu-id="d11f1-161">[**D3d11 \_ Le mappage d' \_ écriture \_ ignore**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indique que l’application n’a pas besoin de conserver les anciennes données de vertex ou d’index dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d11f1-161">[**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app doesn't need to keep the old vertex or index data in the buffer.</span></span> <span data-ttu-id="d11f1-162">Si le GPU utilise toujours la mémoire tampon quand vous appelez **Map** avec **d3d11 \_ Map \_ Write \_ ignore**, le runtime retourne un pointeur vers une nouvelle région de mémoire au lieu des anciennes données de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d11f1-162">If the GPU is still using the buffer when you call **Map** with **D3D11\_MAP\_WRITE\_DISCARD**, the runtime returns a pointer to a new region of memory instead of the old buffer data.</span></span> <span data-ttu-id="d11f1-163">Cela permet au GPU de continuer à utiliser les anciennes données pendant que l’application place les données dans la nouvelle mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d11f1-163">This allows the GPU to continue using the old data while the app places data in the new buffer.</span></span> <span data-ttu-id="d11f1-164">Aucune gestion supplémentaire de la mémoire n’est nécessaire dans l’application. l’ancienne mémoire tampon est réutilisée ou détruite automatiquement lorsque le GPU en a terminé avec celle-ci.</span><span class="sxs-lookup"><span data-stu-id="d11f1-164">No additional memory management is required in the app; the old buffer is reused or destroyed automatically when the GPU is finished with it.</span></span>

> [!Note]  
> <span data-ttu-id="d11f1-165">Lorsque vous mappez une mémoire tampon avec l' [**écriture de d3d11 \_ Map \_ \_ ignorée**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), le runtime ignore toujours l’intégralité de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d11f1-165">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), the runtime always discards the entire buffer.</span></span> <span data-ttu-id="d11f1-166">Vous ne pouvez pas conserver les informations dans les zones non mappées de la mémoire tampon en spécifiant un champ d’offset différent de zéro ou une taille limitée.</span><span class="sxs-lookup"><span data-stu-id="d11f1-166">You can't preserve info in unmapped areas of the buffer by specifying a nonzero offset or limited size field.</span></span>

 

<span data-ttu-id="d11f1-167">Dans certains cas, la quantité de données dont l’application a besoin pour stocker par carte est petite, par exemple l’ajout de quatre sommets pour le rendu d’un sprite.</span><span class="sxs-lookup"><span data-stu-id="d11f1-167">There are cases where the amount of data the app needs to store per map is small, such as adding four vertices to render a sprite.</span></span> <span data-ttu-id="d11f1-168">[**D3d11 \_ MAPPER l' \_ écriture \_ sans \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) remplacement indique que l’application ne remplacera pas les données déjà en cours d’utilisation dans la mémoire tampon dynamique.</span><span class="sxs-lookup"><span data-stu-id="d11f1-168">[**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app will not overwrite data already in use in the dynamic buffer.</span></span> <span data-ttu-id="d11f1-169">L’appel [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) retourne un pointeur vers les anciennes données, ce qui permet à l’application d’ajouter de nouvelles données dans les régions inutilisées du vertex ou de la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="d11f1-169">The [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) call will return a pointer to the old data, which will allow the app to add new data in unused regions of the vertex or index buffer.</span></span> <span data-ttu-id="d11f1-170">L’application ne doit pas modifier les vertex ou les index utilisés dans une opération de dessin, car ils peuvent toujours être utilisés par le GPU.</span><span class="sxs-lookup"><span data-stu-id="d11f1-170">The app must not modify vertices or indices that are used in a draw operation as they might still be in use by the GPU.</span></span> <span data-ttu-id="d11f1-171">Nous vous recommandons de faire en sorte que l’application utilise ensuite l' [**\_ écriture d3d11 map \_ \_ ignorée**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) une fois que la mémoire tampon dynamique est pleine pour recevoir une nouvelle région de mémoire, qui ignore les anciennes données de vertex ou d’index une fois l’exécution du GPU terminée.</span><span class="sxs-lookup"><span data-stu-id="d11f1-171">We recommend that the app then use [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) after the dynamic buffer is full to receive a new region of memory, which discards the old vertex or index data after the GPU is finished.</span></span>

<span data-ttu-id="d11f1-172">Le mécanisme de requête asynchrone est utile pour déterminer si les vertex sont toujours utilisés par le GPU.</span><span class="sxs-lookup"><span data-stu-id="d11f1-172">The asynchronous query mechanism is useful to determine if vertices are still in use by the GPU.</span></span> <span data-ttu-id="d11f1-173">Émettez une requête de [**type \_ \_ événement de requête d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) après le dernier appel de dessin qui utilise les vertex.</span><span class="sxs-lookup"><span data-stu-id="d11f1-173">Issue a query of type [**D3D11\_QUERY\_EVENT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) after the last draw call that uses the vertices.</span></span> <span data-ttu-id="d11f1-174">Les vertex ne sont plus utilisés quand [**ID3D11DeviceContext :: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d11f1-174">The vertices are no longer in use when [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) returns S\_OK.</span></span> <span data-ttu-id="d11f1-175">Lorsque vous mappez une mémoire tampon avec [**d3d11 \_ carte d' \_ écriture \_ ignorée**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) ou aucune valeur de mappage, vous avez toujours la garantie que les vertex sont correctement synchronisés avec le GPU.</span><span class="sxs-lookup"><span data-stu-id="d11f1-175">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) or no map values, you are always guaranteed that the vertices are synchronized properly with the GPU.</span></span> <span data-ttu-id="d11f1-176">Toutefois, lorsque vous mappez sans valeurs cartographiques, vous subissez la pénalité de performance décrite précédemment.</span><span class="sxs-lookup"><span data-stu-id="d11f1-176">But, when you map without map values, you will incur the performance penalty described earlier.</span></span>

> [!Note]  
> <span data-ttu-id="d11f1-177">Le runtime Direct3D 11,1, qui est disponible à partir de Windows 8, permet de mapper des mémoires tampons constantes dynamiques et des vues des ressources de nuanceur (SRVs) de mémoires tampons dynamiques avec la [**carte de d3d11 \_ \_ écriture \_ sans \_ remplacement**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map).</span><span class="sxs-lookup"><span data-stu-id="d11f1-177">The Direct3D 11.1 runtime, which is available starting with Windows 8, enables mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with [**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map).</span></span> <span data-ttu-id="d11f1-178">Les runtimes Direct3D 11 et versions antérieures limitent le mappage de mise à jour partielle non-remplacement aux mémoires tampons de vertex ou d’index.</span><span class="sxs-lookup"><span data-stu-id="d11f1-178">The Direct3D 11 and earlier runtimes limited no-overwrite partial-update mapping to vertex or index buffers.</span></span> <span data-ttu-id="d11f1-179">Pour déterminer si un périphérique Direct3D prend en charge ces fonctionnalités, appelez [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) avec les [**options de d3d11 de fonctionnalités de d3d11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).</span><span class="sxs-lookup"><span data-stu-id="d11f1-179">To determine if a Direct3D device supports these features, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).</span></span> <span data-ttu-id="d11f1-180">**CheckFeatureSupport** remplit les membres d’une structure d' [**\_ \_ \_ \_ options d3d11 des données de la fonctionnalité d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) avec les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d11f1-180">**CheckFeatureSupport** fills members of a [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) structure with the device's features.</span></span> <span data-ttu-id="d11f1-181">Les membres pertinents ici sont **MapNoOverwriteOnDynamicConstantBuffer** et **MapNoOverwriteOnDynamicBufferSRV**.</span><span class="sxs-lookup"><span data-stu-id="d11f1-181">The relevant members here are **MapNoOverwriteOnDynamicConstantBuffer** and **MapNoOverwriteOnDynamicBufferSRV**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d11f1-182">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d11f1-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d11f1-183">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d11f1-183">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




