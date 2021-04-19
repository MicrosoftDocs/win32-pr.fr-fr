---
description: Les objets de mémoire tampon de vertex permettent aux applications d’accéder directement à la mémoire allouée pour les données de vertex.
ms.assetid: 63d255b7-fa7d-411b-9cdb-52113f30c933
title: Accès au contenu d’une mémoire tampon de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b5e4a4986e064d3736f83567f5dd6d479d0dbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513143"
---
# <a name="accessing-the-contents-of-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="b7c0f-103">Accès au contenu d’une mémoire tampon de vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b7c0f-103">Accessing the Contents of a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="b7c0f-104">Les objets de mémoire tampon de vertex permettent aux applications d’accéder directement à la mémoire allouée pour les données de vertex.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-104">Vertex buffer objects enable applications to directly access the memory allocated for vertex data.</span></span> <span data-ttu-id="b7c0f-105">Vous pouvez récupérer un pointeur vers la mémoire tampon de vertex en appelant la méthode [**IDirect3DVertexBuffer9 :: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) , puis en accédant à la mémoire si nécessaire pour remplir la mémoire tampon avec les nouvelles données de vertex ou pour lire les données qu’elle contient déjà.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-105">You can retrieve a pointer to vertex buffer memory by calling the [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) method, and then accessing the memory as needed to fill the buffer with new vertex data or to read any data it already contains.</span></span> <span data-ttu-id="b7c0f-106">La méthode **IDirect3DVertexBuffer9 :: Lock** accepte quatre paramètres.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-106">The **IDirect3DVertexBuffer9::Lock** method accepts four parameters.</span></span> <span data-ttu-id="b7c0f-107">Le premier, *OffsetToLock*, est le décalage dans les données de vertex.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-107">The first, *OffsetToLock*, is the offset into the vertex data.</span></span> <span data-ttu-id="b7c0f-108">Le deuxième paramètre est la taille, exprimée en octets, des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-108">The second parameter is the size, measured in bytes, of the vertex data.</span></span> <span data-ttu-id="b7c0f-109">Le troisième paramètre accepté est l’adresse d’un pointeur qui pointe vers les données de vertex, si l’appel est concluant.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-109">The third parameter accepted is the address of a pointer that points to the vertex data, if the call succeeds.</span></span>

<span data-ttu-id="b7c0f-110">Le dernier paramètre, *Flags*, indique au système la manière dont la mémoire doit être verrouillée.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-110">The last parameter, *Flags*, tells the system how the memory should be locked.</span></span> <span data-ttu-id="b7c0f-111">Spécifiez les constantes pour le paramètre *Flags* en fonction de la façon dont les données du vertex sont accessibles.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-111">Specify constants for the *Flags* parameter according to the way the vertex data will be accessed.</span></span> <span data-ttu-id="b7c0f-112">Assurez-vous que la valeur choisie pour [**D3DUSAGE**](d3dusage.md) correspond à la valeur choisie pour [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="b7c0f-112">Make sure the value chosen for [**D3DUSAGE**](d3dusage.md) matches the value chosen for [D3DLOCK](d3dlock.md).</span></span> <span data-ttu-id="b7c0f-113">Par exemple, si vous créez une mémoire tampon de vertex avec accès en écriture uniquement, il n’est pas judicieux d’essayer de lire les données en spécifiant D3DLOCK \_ ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-113">For example, if you are creating a vertex buffer with write access only, it doesn't make sense to try to read the data by specifying D3DLOCK\_READONLY.</span></span> <span data-ttu-id="b7c0f-114">En utilisant judicieusement ces indicateurs, le pilote peut verrouiller la mémoire et fournir les meilleures performances, en fonction du type d’accès demandé.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-114">Wisely using these flags allows the driver to lock the memory and provide the best performance, given the requested access type.</span></span>

<span data-ttu-id="b7c0f-115">Une fois que vous avez fini de remplir ou de lire les données de vertex, appelez la méthode [**IDirect3DVertexBuffer9 :: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) , comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-115">After you finish filling or reading the vertex data, call the [**IDirect3DVertexBuffer9::Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) method, as shown in the following code example.</span></span>


```
// This code example assumes the g_pVB is a variable of type 
//   LPDIRECT3DVERTEXBUFFER9 and that g_Vertices has been  
//   properly initialized with vertices

// Lock the buffer to gain access to the vertices 
VOID* pVertices;

if(FAILED(g_pVB->Lock(0, sizeof(g_Vertices), 
        (BYTE**)&pVertices, 0 ) ) ) 
    return E_FAIL;

memcpy(pVertices, g_Vertices, sizeof(g_Vertices));
g_pVB->Unlock();
```



<span data-ttu-id="b7c0f-116">Si vous créez une mémoire tampon de vertex avec l' \_ indicateur WRITEONLY D3DUSAGE, n’utilisez pas l' \_ indicateur de verrouillage ReadOnly D3DLOCK.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-116">If you create a vertex buffer with the D3DUSAGE\_WRITEONLY flag, do not use the D3DLOCK\_READONLY locking flag.</span></span> <span data-ttu-id="b7c0f-117">Utilisez l' \_ indicateur D3DLOCK ReadOnly si votre application lit uniquement à partir de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-117">Use the D3DLOCK\_READONLY flag if your application will read only from the vertex buffer memory.</span></span> <span data-ttu-id="b7c0f-118">L’inclusion de cet indicateur permet à Direct3D d’optimiser ses procédures internes pour améliorer l’efficacité, étant donné que l’accès à la mémoire est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-118">Including this flag enables Direct3D to optimize its internal procedures to improve efficiency, given that access to the memory will be read-only.</span></span>

<span data-ttu-id="b7c0f-119">Pour [](performance-optimizations.md) plus d’informations sur l’utilisation de D3DLOCK \_ ignore ou D3DLOCK \_ NOOVERWRITE pour le paramètre flags de [**IDirect3DVertexBuffer9 :: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), consultez Utilisation de mémoires tampons de vertex et d’index dynamiques.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-119">See [Using Dynamic Vertex and Index Buffers](performance-optimizations.md) for information about using D3DLOCK\_DISCARD or D3DLOCK\_NOOVERWRITE for the Flags parameter of [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock).</span></span>

<span data-ttu-id="b7c0f-120">En C++, étant donné que vous accédez directement à la mémoire allouée pour la mémoire tampon de vertex, assurez-vous que votre application accède correctement à la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-120">In C++, because you directly access the memory allocated for the vertex buffer, make sure your application properly accesses the allocated memory.</span></span> <span data-ttu-id="b7c0f-121">Dans le cas contraire, vous risquez de rendre cette mémoire non valide.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-121">Otherwise, you risk rendering that memory invalid.</span></span> <span data-ttu-id="b7c0f-122">Utilisez la Stride du format de vertex que votre application utilise pour passer d’un vertex dans la mémoire tampon allouée à une autre.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-122">Use the stride of the vertex format that your application uses to move from one vertex in the allocated buffer to another.</span></span> <span data-ttu-id="b7c0f-123">La mémoire tampon de vertex est un tableau simple de vertex spécifié dans le groupe de prix final.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-123">The vertex buffer memory is a simple array of vertices specified in FVF.</span></span> <span data-ttu-id="b7c0f-124">Utilisez le Stride de la structure de format de vertex que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-124">Use the stride of whatever vertex format structure you define.</span></span> <span data-ttu-id="b7c0f-125">Vous pouvez calculer le Stride de chaque vertex au moment de l’exécution en examinant le [D3DFVF](d3dfvf.md) contenu dans la description de la mémoire tampon du vertex.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-125">You can calculate the stride of each vertex at run time by examining the [D3DFVF](d3dfvf.md) contained in the vertex buffer description.</span></span> <span data-ttu-id="b7c0f-126">Le tableau suivant indique la taille de chaque composant de vertex.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-126">The following table shows the size for each vertex component.</span></span>



| <span data-ttu-id="b7c0f-127">Indicateur de format de vertex</span><span class="sxs-lookup"><span data-stu-id="b7c0f-127">Vertex Format Flag</span></span> | <span data-ttu-id="b7c0f-128">Taille</span><span class="sxs-lookup"><span data-stu-id="b7c0f-128">Size</span></span>              |
|--------------------|-------------------|
| <span data-ttu-id="b7c0f-129">\_Diffusion D3DFVF</span><span class="sxs-lookup"><span data-stu-id="b7c0f-129">D3DFVF\_DIFFUSE</span></span>    | <span data-ttu-id="b7c0f-130">sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="b7c0f-130">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="b7c0f-131">D3DFVF \_ normal</span><span class="sxs-lookup"><span data-stu-id="b7c0f-131">D3DFVF\_NORMAL</span></span>     | <span data-ttu-id="b7c0f-132">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="b7c0f-132">sizeof(float) x 3</span></span> |
| <span data-ttu-id="b7c0f-133">D3DFVF \_ spéculaire</span><span class="sxs-lookup"><span data-stu-id="b7c0f-133">D3DFVF\_SPECULAR</span></span>   | <span data-ttu-id="b7c0f-134">sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="b7c0f-134">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="b7c0f-135">D3DFVF \_ TEXn</span><span class="sxs-lookup"><span data-stu-id="b7c0f-135">D3DFVF\_TEXn</span></span>       | <span data-ttu-id="b7c0f-136">sizeof (float) x n</span><span class="sxs-lookup"><span data-stu-id="b7c0f-136">sizeof(float) x n</span></span> |
| <span data-ttu-id="b7c0f-137">D3DFVF \_ xyz</span><span class="sxs-lookup"><span data-stu-id="b7c0f-137">D3DFVF\_XYZ</span></span>        | <span data-ttu-id="b7c0f-138">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="b7c0f-138">sizeof(float) x 3</span></span> |
| <span data-ttu-id="b7c0f-139">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="b7c0f-139">D3DFVF\_XYZRHW</span></span>     | <span data-ttu-id="b7c0f-140">sizeof (float) x 4</span><span class="sxs-lookup"><span data-stu-id="b7c0f-140">sizeof(float) x 4</span></span> |



 

<span data-ttu-id="b7c0f-141">Le nombre de coordonnées de texture présentes dans le format vertex est décrit par les \_ indicateurs D3DFVF Tex n (où n est une valeur comprise entre 0 et 8).</span><span class="sxs-lookup"><span data-stu-id="b7c0f-141">The number of texture coordinates present in the vertex format is described by the D3DFVF\_TEX n flags (where n is a value from 0 to 8).</span></span> <span data-ttu-id="b7c0f-142">Multipliez le nombre de jeux de coordonnées de texture par la taille d’un jeu de coordonnées de texture, qui peut être comprise entre un et quatre virgules flottantes, pour calculer la mémoire requise pour ce nombre de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-142">Multiply the number of texture coordinate sets by the size of one set of texture coordinates, which can range from one to four floats, to calculate the memory required for that number of texture coordinates.</span></span>

<span data-ttu-id="b7c0f-143">Utilisez le Stride de vertex total pour incrémenter et décrémenter le pointeur de mémoire si nécessaire pour accéder à des vertex particuliers.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-143">Use the total vertex stride to increment and decrement the memory pointer as needed to access particular vertices.</span></span>

## <a name="retrieving-vertex-buffer-descriptions"></a><span data-ttu-id="b7c0f-144">Récupération des descriptions des mémoires tampons de vertex</span><span class="sxs-lookup"><span data-stu-id="b7c0f-144">Retrieving Vertex Buffer Descriptions</span></span>

<span data-ttu-id="b7c0f-145">Vous pouvez récupérer des informations sur une mémoire tampon de vertex en appelant la méthode [**IDirect3DVertexBuffer9 :: GetDesc**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="b7c0f-145">You can retrieve information about a vertex buffer by calling the [**IDirect3DVertexBuffer9::GetDesc**](/windows/desktop/api) method.</span></span> <span data-ttu-id="b7c0f-146">Cette méthode remplit les membres de la structure [**D3DVERTEXBUFFER \_ desc**](d3dvertexbuffer-desc.md) avec des informations sur la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="b7c0f-146">This method fills the members of the [**D3DVERTEXBUFFER\_DESC**](d3dvertexbuffer-desc.md) structure with information about the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7c0f-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7c0f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7c0f-148">Mémoires tampons de vertex</span><span class="sxs-lookup"><span data-stu-id="b7c0f-148">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
