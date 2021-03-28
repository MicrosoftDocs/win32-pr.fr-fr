---
title: Prise en main avec l’étape de Input-Assembler
description: Quelques étapes sont nécessaires pour initialiser l’étape de l’assembleur d’entrée (IA).
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901b3facfef781e3f44acf75bee737f280dece55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382198"
---
# <a name="getting-started-with-the-input-assembler-stage"></a><span data-ttu-id="b71d7-103">Prise en main avec l’étape de Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="b71d7-103">Getting Started with the Input-Assembler Stage</span></span>

<span data-ttu-id="b71d7-104">Quelques étapes sont nécessaires pour initialiser l’étape de l’assembleur d’entrée (IA).</span><span class="sxs-lookup"><span data-stu-id="b71d7-104">There are a few steps necessary to initialize the input-assembler (IA) stage.</span></span> <span data-ttu-id="b71d7-105">Par exemple, vous devez créer des ressources de mémoire tampon avec les données de vertex dont le pipeline a besoin, indiquer à l’étape IA où se trouvent les mémoires tampons et le type de données qu’elles contiennent, et spécifier le type de primitives à assembler à partir des données.</span><span class="sxs-lookup"><span data-stu-id="b71d7-105">For example, you need to create buffer resources with the vertex data that the pipeline needs, tell the IA stage where the buffers are and what type of data they contain, and specify the type of primitives to assemble from the data.</span></span>

<span data-ttu-id="b71d7-106">Les étapes de base nécessaires à la configuration de l’étape IA, présentées dans le tableau suivant, sont traitées dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b71d7-106">The basic steps involved in setting up the IA stage, shown in the following table, are covered in this topic.</span></span>



| <span data-ttu-id="b71d7-107">Étape</span><span class="sxs-lookup"><span data-stu-id="b71d7-107">Step</span></span>                                                                                    | <span data-ttu-id="b71d7-108">Description</span><span class="sxs-lookup"><span data-stu-id="b71d7-108">Description</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b71d7-109">Créer des mémoires tampons d’entrée</span><span class="sxs-lookup"><span data-stu-id="b71d7-109">Create Input Buffers</span></span>](#create-input-buffers)                                           | <span data-ttu-id="b71d7-110">Créer et initialiser des mémoires tampons d’entrée avec des données de vertex d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b71d7-110">Create and initialize input buffers with input vertex data.</span></span>                                           |
| [<span data-ttu-id="b71d7-111">Créer l’objet Input-Layout</span><span class="sxs-lookup"><span data-stu-id="b71d7-111">Create the Input-Layout Object</span></span>](#create-the-input-layout-object)                       | <span data-ttu-id="b71d7-112">Définissez la façon dont les données de la mémoire tampon du vertex sont diffusées dans l’étape IA à l’aide d’un objet de disposition d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b71d7-112">Define how the vertex buffer data will be streamed into the IA stage by using an input-layout object.</span></span> |
| [<span data-ttu-id="b71d7-113">Lier des objets à l’étape Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="b71d7-113">Bind Objects to the Input-Assembler Stage</span></span>](#bind-objects-to-the-input-assembler-stage) | <span data-ttu-id="b71d7-114">Liez les objets créés (mémoires tampons d’entrée et objet de disposition d’entrée) à l’étape IA.</span><span class="sxs-lookup"><span data-stu-id="b71d7-114">Bind the created objects (input buffers and the input-layout object) to the IA stage.</span></span>                 |
| [<span data-ttu-id="b71d7-115">Spécifiez le type primitif</span><span class="sxs-lookup"><span data-stu-id="b71d7-115">Specify the Primitive Type</span></span>](#specify-the-primitive-type)                               | <span data-ttu-id="b71d7-116">Identifiez la manière dont les vertex seront assemblés en Primitives.</span><span class="sxs-lookup"><span data-stu-id="b71d7-116">Identify how the vertices will be assembled into primitives.</span></span>                                          |
| [<span data-ttu-id="b71d7-117">Méthodes Call Draw</span><span class="sxs-lookup"><span data-stu-id="b71d7-117">Call Draw Methods</span></span>](#call-draw-methods)                                                 | <span data-ttu-id="b71d7-118">Envoyez les données liées à l’étape IA via le pipeline.</span><span class="sxs-lookup"><span data-stu-id="b71d7-118">Send the data bound to the IA stage through the pipeline.</span></span>                                             |



 

<span data-ttu-id="b71d7-119">Une fois que vous avez compris ces étapes, passez à [l’utilisation des valeurs System-Generated](d3d10-graphics-programming-guide-input-assembler-stage-using.md).</span><span class="sxs-lookup"><span data-stu-id="b71d7-119">After you understand these steps, move on to [Using System-Generated Values](d3d10-graphics-programming-guide-input-assembler-stage-using.md).</span></span>

## <a name="create-input-buffers"></a><span data-ttu-id="b71d7-120">Créer des mémoires tampons d’entrée</span><span class="sxs-lookup"><span data-stu-id="b71d7-120">Create Input Buffers</span></span>

<span data-ttu-id="b71d7-121">Il existe deux types de mémoires tampons d’entrée : les tampons de [vertex](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) et les mémoires tampons d’index.</span><span class="sxs-lookup"><span data-stu-id="b71d7-121">There are two types of input buffers: [vertex buffers](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and index buffers.</span></span> <span data-ttu-id="b71d7-122">Les mémoires tampons de vertex fournissent des données de vertex à l’étape IA.</span><span class="sxs-lookup"><span data-stu-id="b71d7-122">Vertex buffers supply vertex data to the IA stage.</span></span> <span data-ttu-id="b71d7-123">Les mémoires tampons d’index sont facultatives. ils fournissent des index aux vertex à partir de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="b71d7-123">Index buffers are optional; they provide indices to vertices from the vertex buffer.</span></span> <span data-ttu-id="b71d7-124">Vous pouvez créer une ou plusieurs mémoires tampons de vertex et, éventuellement, un tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="b71d7-124">You may create one or more vertex buffers and, optionally, an index buffer.</span></span>

<span data-ttu-id="b71d7-125">Après avoir créé les ressources de mémoire tampon, vous devez créer un objet de disposition d’entrée pour décrire la disposition des données à l’étape IA, puis lier les ressources de la mémoire tampon à l’étape IA.</span><span class="sxs-lookup"><span data-stu-id="b71d7-125">After you create the buffer resources, you need to create an input-layout object to describe the data layout to the IA stage, and then you need to bind the buffer resources to the IA stage.</span></span> <span data-ttu-id="b71d7-126">La création et la liaison de mémoires tampons ne sont pas nécessaires si vos nuanceurs n’utilisent pas de tampons.</span><span class="sxs-lookup"><span data-stu-id="b71d7-126">Creating and binding buffers is not necessary if your shaders don't use buffers.</span></span> <span data-ttu-id="b71d7-127">Pour obtenir un exemple de nuanceur de vertex et de pixels simple qui dessine un triangle unique, consultez [utilisation de l’étape Input-Assembler sans tampons](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="b71d7-127">For an example of a simple vertex and pixel shader that draws a single triangle, see [Using the Input-Assembler Stage without Buffers](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).</span></span>

<span data-ttu-id="b71d7-128">Pour obtenir de l’aide sur la création d’une mémoire tampon de vertex, consultez [créer une mémoire tampon de vertex](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span><span class="sxs-lookup"><span data-stu-id="b71d7-128">For help with creating a vertex buffer, see [Create a Vertex Buffer](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span> <span data-ttu-id="b71d7-129">Pour obtenir de l’aide sur la création d’un tampon d’index, consultez créer un tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="b71d7-129">For help with creating an index buffer, see Create an Index Buffer.</span></span>

## <a name="create-the-input-layout-object"></a><span data-ttu-id="b71d7-130">Créer l’objet Input-Layout</span><span class="sxs-lookup"><span data-stu-id="b71d7-130">Create the Input-Layout Object</span></span>

<span data-ttu-id="b71d7-131">L’objet de disposition d’entrée encapsule l’état d’entrée de l’étape IA.</span><span class="sxs-lookup"><span data-stu-id="b71d7-131">The input-layout object encapsulates the input state of the IA stage.</span></span> <span data-ttu-id="b71d7-132">Cela comprend une description des données d’entrée liées à l’étape IA.</span><span class="sxs-lookup"><span data-stu-id="b71d7-132">This includes a description of the input data that is bound to the IA stage.</span></span> <span data-ttu-id="b71d7-133">Les données sont diffusées dans l’étape IA à partir de la mémoire, à partir d’une ou de plusieurs mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="b71d7-133">The data is streamed into the IA stage from memory, from one or more vertex buffers.</span></span> <span data-ttu-id="b71d7-134">La description identifie les données d’entrée qui sont liées à partir d’une ou de plusieurs mémoires tampons de vertex et donne au runtime la possibilité de vérifier les types de données d’entrée par rapport aux types de paramètres d’entrée du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="b71d7-134">The description identifies the input data that is bound from one or more vertex buffers and gives the runtime the ability to check the input data types against the shader input parameter types.</span></span> <span data-ttu-id="b71d7-135">Ce type de vérification vérifie non seulement que les types sont compatibles, mais également que chacun des éléments requis par le nuanceur est disponible dans les ressources de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b71d7-135">This type checking not only verifies that the types are compatible, but also that each of the elements that the shader requires is available in the buffer resources.</span></span>

<span data-ttu-id="b71d7-136">Un objet de disposition d’entrée est créé à partir d’un tableau de descriptions d’éléments d’entrée et d’un pointeur vers le nuanceur compilé (consultez [**ID3D11Device :: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)).</span><span class="sxs-lookup"><span data-stu-id="b71d7-136">An input-layout object is created from an array of input-element descriptions and a pointer to the compiled shader (see [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)).</span></span> <span data-ttu-id="b71d7-137">Le tableau contient un ou plusieurs éléments d’entrée ; chaque élément d’entrée décrit un élément de données de vertex unique à partir d’une seule mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="b71d7-137">The array contains one or more input elements; each input element describes a single vertex-data element from a single vertex buffer.</span></span> <span data-ttu-id="b71d7-138">L’ensemble des descriptions d’élément d’entrée décrit tous les éléments de données de vertex de toutes les mémoires tampon de vertex qui seront liées à l’étape IA.</span><span class="sxs-lookup"><span data-stu-id="b71d7-138">The entire set of input-element descriptions describes all of the vertex-data elements from all of the vertex buffers that will be bound to the IA stage.</span></span>

<span data-ttu-id="b71d7-139">La description de disposition suivante décrit une mémoire tampon de vertex unique qui contient trois éléments de données de vertex :</span><span class="sxs-lookup"><span data-stu-id="b71d7-139">The following layout description describes a single vertex buffer that contains three vertex-data elements:</span></span>


```
D3D11_INPUT_ELEMENT_DESC layout[] =
{
    { L"POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT, 0, 12, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
};
```



<span data-ttu-id="b71d7-140">Une description d’élément d’entrée décrit chaque élément contenu par un seul vertex dans une mémoire tampon de vertex, y compris la taille, le type, l’emplacement et l’objectif.</span><span class="sxs-lookup"><span data-stu-id="b71d7-140">An input-element description describes each element contained by a single vertex in a vertex buffer, including size, type, location, and purpose.</span></span> <span data-ttu-id="b71d7-141">Chaque ligne identifie le type de données à l’aide de la sémantique, de l’index sémantique et du format de données.</span><span class="sxs-lookup"><span data-stu-id="b71d7-141">Each row identifies the type of data by using the semantic, the semantic index, and the data format.</span></span> <span data-ttu-id="b71d7-142">Une [sémantique](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) est une chaîne de texte qui identifie la façon dont les données sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="b71d7-142">A [semantic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) is a text string that identifies how the data will be used.</span></span> <span data-ttu-id="b71d7-143">Dans cet exemple, la première ligne identifie les données de position à 3 composants (*xyz*, par exemple); la deuxième ligne identifie les données de texture à 2 composants (*UV*, par exemple); la troisième ligne identifie les données normales.</span><span class="sxs-lookup"><span data-stu-id="b71d7-143">In this example, the first row identifies 3-component position data (*xyz*, for example); the second row identifies 2-component texture data (*UV*, for example); and the third row identifies normal data.</span></span>

<span data-ttu-id="b71d7-144">Dans cet exemple de description d’un élément d’entrée, l’index sémantique (qui est le deuxième paramètre) est défini sur zéro pour les trois lignes.</span><span class="sxs-lookup"><span data-stu-id="b71d7-144">In this example of an input-element description, the semantic index (which is the second parameter) is set to zero for all three rows.</span></span> <span data-ttu-id="b71d7-145">L’index sémantique permet de faire la distinction entre deux lignes qui utilisent la même sémantique.</span><span class="sxs-lookup"><span data-stu-id="b71d7-145">The semantic index helps distinguish between two rows that use the same semantics.</span></span> <span data-ttu-id="b71d7-146">Étant donné qu’il n’existe pas de sémantique similaire dans cet exemple, l’index sémantique peut être défini sur sa valeur par défaut, zéro.</span><span class="sxs-lookup"><span data-stu-id="b71d7-146">Since there are no similar semantics in this example, the semantic index can be set to its default value, zero.</span></span>

<span data-ttu-id="b71d7-147">Le troisième paramètre est le *format*.</span><span class="sxs-lookup"><span data-stu-id="b71d7-147">The third parameter is the *format*.</span></span> <span data-ttu-id="b71d7-148">Le format (voir [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) spécifie le nombre de composants par élément et le type de données, qui définit la taille des données pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="b71d7-148">The format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) specifies the number of components per element, and the data type, which defines the size of the data for each element.</span></span> <span data-ttu-id="b71d7-149">Le format peut être entièrement typé au moment de la création de la ressource, ou vous pouvez créer une ressource à l’aide d’un **\_ format dxgi**, qui identifie le nombre de composants dans un élément, mais laisse le type de données non défini.</span><span class="sxs-lookup"><span data-stu-id="b71d7-149">The format can be fully typed at the time of resource creation, or you may create a resource by using a **DXGI\_FORMAT**, which identifies the number of components in an element, but leaves the data type undefined.</span></span>

### <a name="input-slots"></a><span data-ttu-id="b71d7-150">Emplacements d’entrée</span><span class="sxs-lookup"><span data-stu-id="b71d7-150">Input Slots</span></span>

<span data-ttu-id="b71d7-151">Les données entrent dans la phase IA via des entrées appelées *emplacements d’entrée*, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="b71d7-151">Data enters the IA stage through inputs called *input slots*, as shown in the following illustration.</span></span> <span data-ttu-id="b71d7-152">L’étape IA a *n* emplacements d’entrée, qui sont conçus pour contenir jusqu’à *n* mémoires tampons de vertex qui fournissent des données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b71d7-152">The IA stage has *n* input slots, which are designed to accommodate up to *n* vertex buffers that provide input data.</span></span> <span data-ttu-id="b71d7-153">Chaque mémoire tampon de vertex doit être assignée à un autre emplacement. ces informations sont stockées dans la déclaration de disposition d’entrée lors de la création de l’objet de disposition d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b71d7-153">Each vertex buffer must be assigned to a different slot; this information is stored in the input-layout declaration when the input-layout object is created.</span></span> <span data-ttu-id="b71d7-154">Vous pouvez également spécifier un décalage à partir du début de chaque mémoire tampon jusqu’au premier élément de la mémoire tampon à lire.</span><span class="sxs-lookup"><span data-stu-id="b71d7-154">You may also specify an offset from the start of each buffer to the first element in the buffer to be read.</span></span>

![illustration des emplacements d’entrée pour l’étape IA](images/d3d10-ia-slots.png)

<span data-ttu-id="b71d7-156">Les deux paramètres suivants sont l' *emplacement d’entrée* et le *décalage d’entrée*.</span><span class="sxs-lookup"><span data-stu-id="b71d7-156">The next two parameters are the *input slot* and the *input offset*.</span></span> <span data-ttu-id="b71d7-157">Lorsque vous utilisez plusieurs mémoires tampons, vous pouvez les lier à un ou plusieurs emplacements d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b71d7-157">When you use multiple buffers, you can bind them to one or more input slots.</span></span> <span data-ttu-id="b71d7-158">Le décalage d’entrée est le nombre d’octets entre le début de la mémoire tampon et le début des données.</span><span class="sxs-lookup"><span data-stu-id="b71d7-158">The input offset is the number of bytes between the start of the buffer and the beginning of the data.</span></span>

### <a name="reusing-input-layout-objects"></a><span data-ttu-id="b71d7-159">Réutilisation des objets Input-Layout</span><span class="sxs-lookup"><span data-stu-id="b71d7-159">Reusing Input-Layout Objects</span></span>

<span data-ttu-id="b71d7-160">Chaque objet de disposition d’entrée est créé sur la base d’une signature de nuanceur ; Cela permet à l’API de valider les éléments d’objet de disposition d’entrée par rapport à la signature de nuanceur-entrée pour s’assurer qu’il existe une correspondance exacte entre les types et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="b71d7-160">Each input-layout object is created based on a shader signature; this allows the API to validate the input-layout-object elements against the shader-input signature to make sure that there is an exact match of types and semantics.</span></span> <span data-ttu-id="b71d7-161">Vous pouvez créer un objet de disposition d’entrée unique pour de nombreux nuanceurs, à condition que toutes les signatures de nuanceur-entrée correspondent exactement.</span><span class="sxs-lookup"><span data-stu-id="b71d7-161">You can create a single input-layout object for many shaders, as long as all of the shader-input signatures exactly match.</span></span>

## <a name="bind-objects-to-the-input-assembler-stage"></a><span data-ttu-id="b71d7-162">Lier des objets à l’étape Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="b71d7-162">Bind Objects to the Input-Assembler Stage</span></span>

<span data-ttu-id="b71d7-163">Après avoir créé les ressources de mémoire tampon de vertex et un objet de disposition d’entrée, vous pouvez les lier à l’étape IA en appelant [**ID3D11DeviceContext :: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) et [**ID3D11DeviceContext :: IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).</span><span class="sxs-lookup"><span data-stu-id="b71d7-163">After you create vertex buffer resources and an input layout object, you can bind them to the IA stage by calling [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) and [**ID3D11DeviceContext::IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).</span></span> <span data-ttu-id="b71d7-164">L’exemple suivant illustre la liaison d’une mémoire tampon de vertex unique et d’un objet de disposition d’entrée à l’étape IA :</span><span class="sxs-lookup"><span data-stu-id="b71d7-164">The following example shows the binding of a single vertex buffer and an input-layout object to the IA stage:</span></span>


```
UINT stride = sizeof( SimpleVertex );
UINT offset = 0;
g_pd3dDevice->IASetVertexBuffers( 
    0,                // the first input slot for binding
    1,                // the number of buffers in the array
    &g_pVertexBuffer, // the array of vertex buffers
    &stride,          // array of stride values, one for each buffer
    &offset );        // array of offset values, one for each buffer

// Set the input layout
g_pd3dDevice->IASetInputLayout( g_pVertexLayout );
```



<span data-ttu-id="b71d7-165">La liaison de l’objet de disposition d’entrée requiert uniquement un pointeur vers l’objet.</span><span class="sxs-lookup"><span data-stu-id="b71d7-165">Binding the input-layout object only requires a pointer to the object.</span></span>

<span data-ttu-id="b71d7-166">Dans l’exemple précédent, une seule mémoire tampon de vertex est liée ; Toutefois, plusieurs mémoires tampons de vertex peuvent être liées par un appel unique à [**ID3D11DeviceContext :: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers), et le code suivant montre un appel de ce type pour lier trois mémoires tampons de vertex :</span><span class="sxs-lookup"><span data-stu-id="b71d7-166">In the preceding example, a single vertex buffer is bound; however, multiple vertex buffers can be bound by a single call to [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers), and the following code shows such a call to bind three vertex buffers:</span></span>


```
UINT strides[3];
strides[0] = sizeof(SimpleVertex1);
strides[1] = sizeof(SimpleVertex2);
strides[2] = sizeof(SimpleVertex3);
UINT offsets[3] = { 0, 0, 0 };
g_pd3dDevice->IASetVertexBuffers( 
    0,                 //first input slot for binding
    3,                 //number of buffers in the array
    &g_pVertexBuffers, //array of three vertex buffers
    &strides,          //array of stride values, one for each buffer
    &offsets );        //array of offset values, one for each buffer
```



<span data-ttu-id="b71d7-167">Un tampon d’index est lié à l’étape IA en appelant [**ID3D11DeviceContext :: IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).</span><span class="sxs-lookup"><span data-stu-id="b71d7-167">An index buffer is bound to the IA stage by calling [**ID3D11DeviceContext::IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).</span></span>

## <a name="specify-the-primitive-type"></a><span data-ttu-id="b71d7-168">Spécifiez le type primitif</span><span class="sxs-lookup"><span data-stu-id="b71d7-168">Specify the Primitive Type</span></span>

<span data-ttu-id="b71d7-169">Une fois les mémoires tampons d’entrée liées, l’étape IA doit être informée de la manière d’assembler les vertex dans des primitives.</span><span class="sxs-lookup"><span data-stu-id="b71d7-169">After the input buffers have been bound, the IA stage must be told how to assemble the vertices into primitives.</span></span> <span data-ttu-id="b71d7-170">Pour ce faire, vous spécifiez le [type primitif](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) en appelant [**ID3D11DeviceContext :: IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); le code suivant appelle cette fonction pour définir les données sous la forme d’une liste de triangles sans contiguïté :</span><span class="sxs-lookup"><span data-stu-id="b71d7-170">This is done by specifying the [primitive type](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) by calling [**ID3D11DeviceContext::IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); the following code calls this function to define the data as a triangle list without adjacency:</span></span>


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



<span data-ttu-id="b71d7-171">Les autres types primitifs sont répertoriés dans [**la \_ \_ topologie de la primitive D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).</span><span class="sxs-lookup"><span data-stu-id="b71d7-171">The rest of the primitive types are listed in [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).</span></span>

## <a name="call-draw-methods"></a><span data-ttu-id="b71d7-172">Méthodes Call Draw</span><span class="sxs-lookup"><span data-stu-id="b71d7-172">Call Draw Methods</span></span>

<span data-ttu-id="b71d7-173">Une fois que les ressources d’entrée ont été liées au pipeline, une application appelle une méthode de dessin pour afficher les primitives.</span><span class="sxs-lookup"><span data-stu-id="b71d7-173">After input resources have been bound to the pipeline, an application calls a draw method to render primitives.</span></span> <span data-ttu-id="b71d7-174">Il existe plusieurs méthodes de dessin, qui sont présentées dans le tableau suivant : certains utilisent des mémoires tampons d’index, d’autres utilisent des données d’instance et d’autres données de réutilisation de la phase de sortie en continu comme entrée de l’étape assembleur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b71d7-174">There are several draw methods, which are shown in the following table; some use index buffers, some use instance data, and some reuse data from the streaming-output stage as input to the input-assembler stage.</span></span>



| <span data-ttu-id="b71d7-175">Dessiner des méthodes</span><span class="sxs-lookup"><span data-stu-id="b71d7-175">Draw Methods</span></span>                                                                                  | <span data-ttu-id="b71d7-176">Description</span><span class="sxs-lookup"><span data-stu-id="b71d7-176">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b71d7-177">**ID3D11DeviceContext ::D RAW**</span><span class="sxs-lookup"><span data-stu-id="b71d7-177">**ID3D11DeviceContext::Draw**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | <span data-ttu-id="b71d7-178">Dessinez des primitives non indexées et non-instanciées.</span><span class="sxs-lookup"><span data-stu-id="b71d7-178">Draw non-indexed, non-instanced primitives.</span></span>                                                            |
| [<span data-ttu-id="b71d7-179">**ID3D11DeviceContext ::D rawInstanced**</span><span class="sxs-lookup"><span data-stu-id="b71d7-179">**ID3D11DeviceContext::DrawInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | <span data-ttu-id="b71d7-180">Dessinez des primitives non indexées et instanciées.</span><span class="sxs-lookup"><span data-stu-id="b71d7-180">Draw non-indexed, instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="b71d7-181">**ID3D11DeviceContext ::D rawIndexed**</span><span class="sxs-lookup"><span data-stu-id="b71d7-181">**ID3D11DeviceContext::DrawIndexed**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | <span data-ttu-id="b71d7-182">Dessinez des primitives indexées et non instanciées.</span><span class="sxs-lookup"><span data-stu-id="b71d7-182">Draw indexed, non-instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="b71d7-183">**ID3D11DeviceContext ::D rawIndexedInstanced**</span><span class="sxs-lookup"><span data-stu-id="b71d7-183">**ID3D11DeviceContext::DrawIndexedInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | <span data-ttu-id="b71d7-184">Dessinez des primitives indexées et indexées.</span><span class="sxs-lookup"><span data-stu-id="b71d7-184">Draw indexed, instanced primitives.</span></span>                                                                    |
| [<span data-ttu-id="b71d7-185">**ID3D11DeviceContext ::D rawAuto**</span><span class="sxs-lookup"><span data-stu-id="b71d7-185">**ID3D11DeviceContext::DrawAuto**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | <span data-ttu-id="b71d7-186">Dessinez des primitives non indexées et non instanciées à partir des données d’entrée provenant de l’étape de sortie en continu.</span><span class="sxs-lookup"><span data-stu-id="b71d7-186">Draw non-indexed, non-instanced primitives from input data that comes from the streaming-output stage.</span></span> |



 

<span data-ttu-id="b71d7-187">Chaque méthode Draw restitue un type de topologie unique.</span><span class="sxs-lookup"><span data-stu-id="b71d7-187">Each draw method renders a single topology type.</span></span> <span data-ttu-id="b71d7-188">Pendant le rendu, les primitives incomplètes (celles sans nombre de vertex suffisant, les primitives partielles, etc.) sont ignorées silencieusement.</span><span class="sxs-lookup"><span data-stu-id="b71d7-188">During rendering, incomplete primitives (those without enough vertices, lacking indices, partial primitives, and so on) are silently discarded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b71d7-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b71d7-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b71d7-190">Étape assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="b71d7-190">Input-Assembler Stage</span></span>](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 