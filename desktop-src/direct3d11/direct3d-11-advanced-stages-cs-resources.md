---
title: Nouveaux types de ressources
description: Plusieurs nouveaux types de ressources ont été ajoutés dans Direct3D 11.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Mémoire tampon d’adresse en octets (vue d’ensemble)
- Mémoire tampon de lecture/écriture (vue d’ensemble)
- Mémoire tampon structurée (vue d’ensemble)
- Mémoire tampon d’accès non triée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b7a75ec95917a5ee819126e42dce3117994574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382291"
---
# <a name="new-resource-types"></a><span data-ttu-id="61304-107">Nouveaux types de ressources</span><span class="sxs-lookup"><span data-stu-id="61304-107">New Resource Types</span></span>

<span data-ttu-id="61304-108">Plusieurs nouveaux types de ressources ont été ajoutés dans Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="61304-108">Several new resource types have been added in Direct3D 11.</span></span>

-   [<span data-ttu-id="61304-109">Mémoires tampons et textures en lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="61304-109">Read/Write Buffers and Textures</span></span>](#readwrite-buffers-and-textures)
-   [<span data-ttu-id="61304-110">Mémoire tampon structurée</span><span class="sxs-lookup"><span data-stu-id="61304-110">Structured Buffer</span></span>](#structured-buffer)
-   [<span data-ttu-id="61304-111">Mémoire tampon d’adresse en octets</span><span class="sxs-lookup"><span data-stu-id="61304-111">Byte Address Buffer</span></span>](#byte-address-buffer)
-   [<span data-ttu-id="61304-112">Tampon ou texture d’accès non ordonné</span><span class="sxs-lookup"><span data-stu-id="61304-112">Unordered Access Buffer or Texture</span></span>](#unordered-access-buffer-or-texture)
    -   [<span data-ttu-id="61304-113">Ajouter et consommer une mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="61304-113">Append and Consume Buffer</span></span>](#append-and-consume-buffer)
-   [<span data-ttu-id="61304-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="61304-114">Related topics</span></span>](#related-topics)

## <a name="readwrite-buffers-and-textures"></a><span data-ttu-id="61304-115">Mémoires tampons et textures en lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="61304-115">Read/Write Buffers and Textures</span></span>

<span data-ttu-id="61304-116">Les ressources du Shader Model 4 sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="61304-116">Shader model 4 resources are read only.</span></span> <span data-ttu-id="61304-117">Le Shader Model 5 implémente un nouveau jeu correspondant de ressources de lecture/écriture :</span><span class="sxs-lookup"><span data-stu-id="61304-117">Shader model 5 implements a new corresponding set of read/write resources:</span></span>

-   [<span data-ttu-id="61304-118">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="61304-118">RWBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   <span data-ttu-id="61304-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span><span class="sxs-lookup"><span data-stu-id="61304-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span></span>
-   <span data-ttu-id="61304-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span><span class="sxs-lookup"><span data-stu-id="61304-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span></span>
-   [<span data-ttu-id="61304-121">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="61304-121">RWTexture3D</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

<span data-ttu-id="61304-122">Ces ressources requièrent une variable de ressource pour accéder à la mémoire (par le biais de l’indexation), car il n’existe aucune méthode permettant d’accéder directement à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="61304-122">These resources require a resource variable to access memory (through indexing) as there are no methods for accessing memory directly.</span></span> <span data-ttu-id="61304-123">Une variable de ressource peut être utilisée sur les côtés gauche et droit d’une équation ; s’il est utilisé sur le côté droit, le type de modèle doit être un composant unique (float, int ou uint).</span><span class="sxs-lookup"><span data-stu-id="61304-123">A resource variable can be used on the left and right sides of an equation; if used on the right side, the template type must be single component (float, int, or uint).</span></span>

## <a name="structured-buffer"></a><span data-ttu-id="61304-124">Mémoire tampon structurée</span><span class="sxs-lookup"><span data-stu-id="61304-124">Structured Buffer</span></span>

<span data-ttu-id="61304-125">Une mémoire tampon structurée est une mémoire tampon qui contient des éléments de tailles égales.</span><span class="sxs-lookup"><span data-stu-id="61304-125">A structured buffer is a buffer that contains elements of equal sizes.</span></span> <span data-ttu-id="61304-126">Utilisez une structure avec un ou plusieurs types de membres pour définir un élément.</span><span class="sxs-lookup"><span data-stu-id="61304-126">Use a structure with one or more member types to define an element.</span></span> <span data-ttu-id="61304-127">Voici une structure avec trois membres.</span><span class="sxs-lookup"><span data-stu-id="61304-127">Here is a structure with three members.</span></span>


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



<span data-ttu-id="61304-128">Utilisez cette structure pour déclarer une mémoire tampon structurée comme suit :</span><span class="sxs-lookup"><span data-stu-id="61304-128">Use this structure to declare a structured buffer like this:</span></span>


```
StructuredBuffer<MyStruct> mySB;
```



<span data-ttu-id="61304-129">Outre l’indexation, une mémoire tampon structurée prend en charge l’accès à un membre unique comme suit :</span><span class="sxs-lookup"><span data-stu-id="61304-129">In addition to indexing, a structured buffer supports accessing a single member like this:</span></span>


```
float4 myColor = mySb[27].Color;
```



<span data-ttu-id="61304-130">Utilisez les types d’objets suivants pour accéder à une mémoire tampon structurée :</span><span class="sxs-lookup"><span data-stu-id="61304-130">Use the following object types to access a structured buffer:</span></span>

-   <span data-ttu-id="61304-131">[StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) est une mémoire tampon structurée en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="61304-131">[StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) is a read only structured buffer.</span></span>
-   <span data-ttu-id="61304-132">[RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) est une mémoire tampon structurée en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="61304-132">[RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) is a read/write structured buffer.</span></span>

<span data-ttu-id="61304-133">Les [fonctions atomiques](direct3d-11-advanced-stages-cs-atomic-functions.md) qui implémentent des opérations verrouillées sont autorisées sur les éléments int et uint dans un **RWStructuredBuffer**.</span><span class="sxs-lookup"><span data-stu-id="61304-133">[Atomic functions](direct3d-11-advanced-stages-cs-atomic-functions.md) which implement interlocked operations are allowed on int and uint elements in an **RWStructuredBuffer**.</span></span>

## <a name="byte-address-buffer"></a><span data-ttu-id="61304-134">Mémoire tampon d’adresse en octets</span><span class="sxs-lookup"><span data-stu-id="61304-134">Byte Address Buffer</span></span>

<span data-ttu-id="61304-135">Une mémoire tampon d’adresse en octets est une mémoire tampon dont le contenu est adressable par un décalage d’octet.</span><span class="sxs-lookup"><span data-stu-id="61304-135">A byte address buffer is a buffer whose contents are addressable by a byte offset.</span></span> <span data-ttu-id="61304-136">Normalement, le contenu d’une [mémoire tampon](overviews-direct3d-11-resources-buffers-intro.md) est indexé par élément à l’aide d’un Stride pour chaque élément et le numéro d’élément (N) comme indiqué par S \* N.</span><span class="sxs-lookup"><span data-stu-id="61304-136">Normally, the contents of a [buffer](overviews-direct3d-11-resources-buffers-intro.md) are indexed per element using a stride for each element (S) and the element number (N) as given by S\*N.</span></span> <span data-ttu-id="61304-137">Une mémoire tampon d’adresse d’octet, qui peut également être appelée mémoire tampon brute, utilise un décalage de valeur d’octet par rapport au début de la mémoire tampon pour accéder aux données.</span><span class="sxs-lookup"><span data-stu-id="61304-137">A byte address buffer, which can also be called a raw buffer, uses a byte value offset from the beginning of the buffer to access data.</span></span> <span data-ttu-id="61304-138">La valeur de l’octet doit être un multiple de quatre afin qu’il soit aligné sur la valeur DWORD.</span><span class="sxs-lookup"><span data-stu-id="61304-138">The byte value must be a multiple of four so that it is DWORD aligned.</span></span> <span data-ttu-id="61304-139">Si une autre valeur est fournie, le comportement n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="61304-139">If any other value is provided, behavior is undefined.</span></span>

<span data-ttu-id="61304-140">Le Shader Model 5 introduit des objets pour accéder à une [mémoire tampon d’adresse en lecture](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) seule, ainsi qu’à une [mémoire tampon d’adresse d’octets en lecture-écriture](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer).</span><span class="sxs-lookup"><span data-stu-id="61304-140">Shader model 5 introduces objects for accessing a [read-only byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) as well as a [read-write byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer).</span></span> <span data-ttu-id="61304-141">Le contenu d’une mémoire tampon d’adresse en octets est conçu pour être un entier non signé 32 bits. Si la valeur de la mémoire tampon n’est pas vraiment un entier non signé, utilisez une fonction telle que [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) pour la lire.</span><span class="sxs-lookup"><span data-stu-id="61304-141">The contents of a byte address buffer is designed to be a 32-bit unsigned integer; if the value in the buffer is not really an unsigned integer, use a function such as [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) to read it.</span></span>

## <a name="unordered-access-buffer-or-texture"></a><span data-ttu-id="61304-142">Tampon ou texture d’accès non ordonné</span><span class="sxs-lookup"><span data-stu-id="61304-142">Unordered Access Buffer or Texture</span></span>

<span data-ttu-id="61304-143">Une ressource d’accès non ordonnée (qui comprend des mémoires tampons, des textures et des tableaux de textures sans échantillonnage multiple) autorise un accès en lecture/écriture non ordonné de manière temporelle à partir de plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="61304-143">An unordered access resource (which includes buffers, textures, and texture arrays - without multisampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="61304-144">Cela signifie que ce type de ressource peut être lu/écrit simultanément par plusieurs threads sans générer de conflits de mémoire à l’aide de [fonctions atomiques](direct3d-11-advanced-stages-cs-atomic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="61304-144">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts through the use of [Atomic Functions](direct3d-11-advanced-stages-cs-atomic-functions.md).</span></span>

<span data-ttu-id="61304-145">Créez une texture ou une mémoire tampon d’accès non triée en appelant une fonction telle que [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) ou [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) et en passant l’indicateur d’accès non ordonné à la **\_ liaison \_ \_ d3d11** à partir de l’énumération de l' [**\_ \_ indicateur de liaison d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="61304-145">Create an unordered access buffer or texture by calling a function such as [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) or [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and passing in the **D3D11\_BIND\_UNORDERED\_ACCESS** flag from the [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) enumeration.</span></span>

<span data-ttu-id="61304-146">Les ressources d’accès non ordonnées ne peuvent être liées qu’à des nuanceurs de pixels et des nuanceurs de calcul.</span><span class="sxs-lookup"><span data-stu-id="61304-146">Unordered access resources can only be bound to pixel shaders and compute shaders.</span></span> <span data-ttu-id="61304-147">Pendant l’exécution, les nuanceurs de pixels ou les nuanceurs de calcul exécutés en parallèle ont les mêmes ressources d’accès non ordonnées liées.</span><span class="sxs-lookup"><span data-stu-id="61304-147">During execution, pixel shaders or compute shaders running in parallel have the same unordered access resources bound.</span></span>

### <a name="append-and-consume-buffer"></a><span data-ttu-id="61304-148">Ajouter et consommer une mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="61304-148">Append and Consume Buffer</span></span>

<span data-ttu-id="61304-149">Une mémoire tampon d’ajout et de consommation est un type spécial de ressource non triée qui prend en charge l’ajout et la suppression de valeurs à partir de la fin d’une mémoire tampon de la même manière qu’une pile fonctionne.</span><span class="sxs-lookup"><span data-stu-id="61304-149">An append and consume buffer is a special type of an unordered resource that supports adding and removing values from the end of a buffer similar to the way a stack works.</span></span>

<span data-ttu-id="61304-150">Une mémoire tampon d’ajout et de consommation doit être une mémoire tampon structurée :</span><span class="sxs-lookup"><span data-stu-id="61304-150">An append and consume buffer must be a structured buffer:</span></span>

-   [<span data-ttu-id="61304-151">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="61304-151">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="61304-152">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="61304-152">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

<span data-ttu-id="61304-153">Utilisez ces ressources par le biais de leurs méthodes, ces ressources n’utilisent pas de variables de ressource.</span><span class="sxs-lookup"><span data-stu-id="61304-153">Use these resources through their methods, these resources do not use resource variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61304-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="61304-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61304-155">Vue d’ensemble du nuanceur de calcul</span><span class="sxs-lookup"><span data-stu-id="61304-155">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 