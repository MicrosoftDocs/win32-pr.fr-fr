---
description: 'Vous créez un objet de mémoire tampon de vertex en appelant la méthode IDirect3DDevice9 :: CreateVertexBuffer, qui accepte cinq paramètres.'
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: Création d’une mémoire tampon de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffc831ab508f14d61b8e42861f75422ff6a04bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515170"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="56dfd-103">Création d’une mémoire tampon de vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="56dfd-103">Creating a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="56dfd-104">Vous créez un objet de mémoire tampon de vertex en appelant la méthode [**IDirect3DDevice9 :: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) , qui accepte cinq paramètres.</span><span class="sxs-lookup"><span data-stu-id="56dfd-104">You create a vertex buffer object by calling the [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method, which accepts five parameters.</span></span> <span data-ttu-id="56dfd-105">Le premier paramètre spécifie la longueur de la mémoire tampon du vertex, en octets.</span><span class="sxs-lookup"><span data-stu-id="56dfd-105">The first parameter specifies the vertex buffer length, in bytes.</span></span> <span data-ttu-id="56dfd-106">Utilisez l’opérateur sizeof pour déterminer la taille d’un format de vertex, en octets.</span><span class="sxs-lookup"><span data-stu-id="56dfd-106">Use the sizeof operator to determine the size of a vertex format, in bytes.</span></span> <span data-ttu-id="56dfd-107">Considérez le format de vertex personnalisé suivant.</span><span class="sxs-lookup"><span data-stu-id="56dfd-107">Consider the following custom vertex format.</span></span>


```
struct CUSTOMVERTEX {
        FLOAT x, y, z;
        FLOAT rhw;
        DWORD color;
        FLOAT tu, tv;   // Texture coordinates
};

// Custom flexible vertex format (FVF) describing the custom vertex structure
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)
```



<span data-ttu-id="56dfd-108">Pour créer une mémoire tampon de vertex pour contenir quatre structures CUSTOMVERTEX, spécifiez \[ 4 \* sizeof (CUSTOMVERTEX) \] pour le paramètre de *longueur* .</span><span class="sxs-lookup"><span data-stu-id="56dfd-108">To create a vertex buffer to hold four CUSTOMVERTEX structures, specify \[4\*sizeof(CUSTOMVERTEX)\] for the *Length* parameter.</span></span>

<span data-ttu-id="56dfd-109">Le deuxième paramètre est un ensemble de contrôles d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="56dfd-109">The second parameter is a set of usage controls.</span></span> <span data-ttu-id="56dfd-110">Entre autres choses, sa valeur détermine si la mémoire tampon de vertex peut contenir des informations de découpage, sous la forme d’indicateurs de séquence, pour les vertex qui existent en dehors de la zone d’affichage.</span><span class="sxs-lookup"><span data-stu-id="56dfd-110">Among other things, its value determines whether the vertex buffer is capable of containing clipping information - in the form of clip flags - for vertices that exist outside the viewing area.</span></span> <span data-ttu-id="56dfd-111">Pour créer une mémoire tampon de vertex qui ne peut pas contenir d’indicateurs de clip, incluez l' \_ indicateur D3DUSAGE DONOTCLIP pour le paramètre *usage* .</span><span class="sxs-lookup"><span data-stu-id="56dfd-111">To create a vertex buffer that cannot contain clip flags, include the D3DUSAGE\_DONOTCLIP flag for the *Usage* parameter.</span></span> <span data-ttu-id="56dfd-112">L' \_ indicateur D3DUSAGE DONOTCLIP est appliqué uniquement si vous indiquez également que la mémoire tampon de vertex contiendra des vertex transformés-l' \_ indicateur de XYZRHW D3DFVF est inclus dans le paramètre de la Commission de la *Commission* .</span><span class="sxs-lookup"><span data-stu-id="56dfd-112">The D3DUSAGE\_DONOTCLIP flag is applied only if you also indicate that the vertex buffer will contain transformed vertices - the D3DFVF\_XYZRHW flag is included in the *FVF* parameter.</span></span> <span data-ttu-id="56dfd-113">La méthode [**IDirect3DDevice9 :: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) ignore l' \_ indicateur D3DUSAGE DONOTCLIP si vous indiquez que la mémoire tampon contient des vertex non transformés (l’indicateur D3DFVF \_ XYZ).</span><span class="sxs-lookup"><span data-stu-id="56dfd-113">The [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method ignores the D3DUSAGE\_DONOTCLIP flag if you indicate that the buffer will contain untransformed vertices (the D3DFVF\_XYZ flag).</span></span> <span data-ttu-id="56dfd-114">Les indicateurs de découpage occupent de la mémoire supplémentaire, ce qui rend légèrement plus volumineux une mémoire tampon de vertex prenant en charge le découpage que la mémoire tampon de vertex</span><span class="sxs-lookup"><span data-stu-id="56dfd-114">Clipping flags occupy additional memory, making a clipping-capable vertex buffer slightly larger than a vertex buffer incapable of containing clipping flags.</span></span> <span data-ttu-id="56dfd-115">Étant donné que ces ressources sont allouées lors de la création de la mémoire tampon de vertex, vous devez demander à l’avance une mémoire tampon de vertex qui prend en charge le découpage.</span><span class="sxs-lookup"><span data-stu-id="56dfd-115">Because these resources are allocated when the vertex buffer is created, you must request a clipping-capable vertex buffer ahead of time.</span></span>

<span data-ttu-id="56dfd-116">Le troisième paramètre, le prix de la *Commission*, est une combinaison de [D3DFVF](d3dfvf.md) qui décrivent le format de vertex de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="56dfd-116">The third parameter, *FVF*, is a combination of [D3DFVF](d3dfvf.md) that describe the vertex format of the vertex buffer.</span></span> <span data-ttu-id="56dfd-117">Si vous spécifiez 0 pour ce paramètre, la mémoire tampon de vertex est une mémoire tampon de vertex non-Commission.</span><span class="sxs-lookup"><span data-stu-id="56dfd-117">If you specify 0 for this parameter, then the vertex buffer is a non-FVF vertex buffer.</span></span> <span data-ttu-id="56dfd-118">Pour plus d’informations, consultez la rubrique sur les [mémoires tampons de vertex (Direct3D 9)](fvf-vertex-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="56dfd-118">For more information, see [FVF Vertex Buffers (Direct3D 9)](fvf-vertex-buffers.md).</span></span> <span data-ttu-id="56dfd-119">Le quatrième paramètre décrit la classe de mémoire dans laquelle placer la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="56dfd-119">The fourth parameter describes the memory class into which to place the vertex buffer.</span></span>

<span data-ttu-id="56dfd-120">Le dernier paramètre que [**IDirect3DDevice9 :: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) accepte est l’adresse d’une variable qui sera remplie avec un pointeur vers la nouvelle interface [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) de l’objet de mémoire tampon de vertex, si l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="56dfd-120">The final parameter that [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) accepts is the address of a variable that will be filled with a pointer to the new [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface of the vertex buffer object, if the call succeeds.</span></span>

<span data-ttu-id="56dfd-121">Vous ne pouvez pas produire d’indicateurs de clip pour une mémoire tampon de vertex qui a été créée sans prise en charge pour eux.</span><span class="sxs-lookup"><span data-stu-id="56dfd-121">You cannot produce clip flags for a vertex buffer that was created without support for them.</span></span>

<span data-ttu-id="56dfd-122">L’exemple de code C++ suivant montre à quoi peut ressembler la création d’une mémoire tampon de vertex dans le code.</span><span class="sxs-lookup"><span data-stu-id="56dfd-122">The following C++ code example shows what creating a vertex buffer might look like in code.</span></span>


```
   
// d3dDevice contains the address of an IDirect3DDevice9 interface
// g_pVB is a variable of type LPDIRECT3DVERTEXBUFFER9 

// The custom vertex type
struct CUSTOMVERTEX {
    FLOAT x, y, z;
    FLOAT rhw;
    DWORD color;
    FLOAT tu, tv;   // The texture coordinates
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)

// Create a clipping-capable vertex buffer. Allocate enough memory 
// in the default memory pool to hold three CUSTOMVERTEX 
// structures

    if( FAILED( d3dDevice->CreateVertexBuffer( 3*sizeof(CUSTOMVERTEX),
            0 /*Usage*/, D3DFVF_CUSTOMVERTEX, D3DPOOL_DEFAULT, &g_pVB, NULL ) ) )
        return E_FAIL;
```



## <a name="related-topics"></a><span data-ttu-id="56dfd-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56dfd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56dfd-124">Mémoires tampons de vertex</span><span class="sxs-lookup"><span data-stu-id="56dfd-124">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
