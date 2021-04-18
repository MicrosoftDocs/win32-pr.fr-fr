---
description: Cette section décrit les nuanceurs qui peuvent être utilisés pour le modèle de flux programmable.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Programmation d’un ou plusieurs flux (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43210823911648ed11227faef44d980b60d0a335
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515905"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a><span data-ttu-id="83092-103">Programmation d’un ou plusieurs flux (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="83092-103">Programming One or More Streams (Direct3D 9)</span></span>

<span data-ttu-id="83092-104">Cette section décrit les nuanceurs qui peuvent être utilisés pour le modèle de flux programmable.</span><span class="sxs-lookup"><span data-stu-id="83092-104">This section describes shaders that can be used for the programmable stream model.</span></span>

## <a name="using-streams"></a><span data-ttu-id="83092-105">Utilisation des flux</span><span class="sxs-lookup"><span data-stu-id="83092-105">Using Streams</span></span>

<span data-ttu-id="83092-106">DirectX 8 a introduit la notion de flux pour lier les données aux registres d’entrée pour une utilisation par les nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="83092-106">DirectX 8 introduced the notion of a stream to bind data to input registers for use by shaders.</span></span> <span data-ttu-id="83092-107">Un flux est un tableau uniforme de données de composants, où chaque composant se compose d’un ou de plusieurs éléments qui représentent une entité unique telle que la position, la normale, la couleur, etc.</span><span class="sxs-lookup"><span data-stu-id="83092-107">A stream is a uniform array of component data, where each component consists of one or more elements that represent a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="83092-108">Les flux permettent aux graphiques d’effectuer un accès direct à la mémoire à partir de plusieurs mémoires tampons de vertex en parallèle et fournissent également un mappage plus naturel à partir des données d’application.</span><span class="sxs-lookup"><span data-stu-id="83092-108">Streams enable graphic chips to perform a direct memory access from multiple vertex buffers in parallel and also provide a more natural mapping from application data.</span></span> <span data-ttu-id="83092-109">Ils activent également la multitexture triviale plutôt que la multipasse.</span><span class="sxs-lookup"><span data-stu-id="83092-109">They also enable trivial multitexture versus multipass.</span></span> <span data-ttu-id="83092-110">Considérez-le comme suit :</span><span class="sxs-lookup"><span data-stu-id="83092-110">Think of it like this:</span></span>

-   <span data-ttu-id="83092-111">Un vertex est composé de n flux.</span><span class="sxs-lookup"><span data-stu-id="83092-111">A vertex is composed of n streams.</span></span>
-   <span data-ttu-id="83092-112">Un flux est composé de m éléments.</span><span class="sxs-lookup"><span data-stu-id="83092-112">A stream is composed of m elements.</span></span>
-   <span data-ttu-id="83092-113">Un élément est \[ position, couleur, normal et coordonnée de texture \] .</span><span class="sxs-lookup"><span data-stu-id="83092-113">An element is \[position, color, normal, texture coordinate\].</span></span>

<span data-ttu-id="83092-114">La méthode [**IDirect3DDevice9 :: SetStreamSource**](/windows/desktop/api) lie une mémoire tampon de vertex à un flux de données de périphérique, en créant une association entre les données de vertex et l’un des nombreux ports de flux de données qui alimentent les fonctions de traitement Primitives.</span><span class="sxs-lookup"><span data-stu-id="83092-114">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="83092-115">Les références réelles aux données de flux ne se produisent pas tant qu’une méthode de dessin, telle que [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="83092-115">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="83092-116">Le mappage des éléments de vertex d’entrée aux registres d’entrée de vertex pour les nuanceurs de vertex programmables est défini dans la déclaration de nuanceur, mais les éléments de vertex d’entrée n’ont pas de sémantique spécifique concernant leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="83092-116">The mapping of the input vertex elements to the vertex input registers for programmable vertex shaders is defined in the shader declaration, but the input vertex elements do not have specific semantics about their use.</span></span> <span data-ttu-id="83092-117">L’interprétation des éléments de vertex d’entrée est programmée à l’aide des instructions du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="83092-117">The interpretation of the input vertex elements is programmed using the shader instructions.</span></span> <span data-ttu-id="83092-118">La fonction de nuanceur de sommets est définie par un tableau d’instructions qui sont appliquées à chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="83092-118">The vertex shader function is defined by an array of instructions that are applied to each vertex.</span></span> <span data-ttu-id="83092-119">Les registres de sortie de vertex sont écrits explicitement dans, à l’aide des instructions de la fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="83092-119">The vertex output registers are explicitly written to, using instructions in the shader function.</span></span>

<span data-ttu-id="83092-120">Toutefois, dans le cas présent, il est moins nécessaire d’utiliser le mappage sémantique des éléments aux registres, ainsi que des informations supplémentaires sur la raison de l’utilisation des flux et le problème à résoudre à l’aide de flux.</span><span class="sxs-lookup"><span data-stu-id="83092-120">For this discussion, though, be less concerned with the semantic mapping of elements to registers and more concerned with the reason for using streams and what problem is solved by using streams.</span></span> <span data-ttu-id="83092-121">Le principal avantage des flux est qu’ils suppriment les coûts de données de vertex précédemment associés à la multitexturation.</span><span class="sxs-lookup"><span data-stu-id="83092-121">The main benefit of streams is that they remove the vertex data costs previously associated with multitexturing.</span></span> <span data-ttu-id="83092-122">Avant les flux, un utilisateur devait dupliquer des jeux de données de vertex pour gérer le cas d’une seule et de plusieurs textures sans éléments de données inutilisés, ou transporter des éléments de données qui seraient inutilisés, sauf dans le cas de la multitexture.</span><span class="sxs-lookup"><span data-stu-id="83092-122">Before streams, a user had to either duplicate vertex data sets to handle the single and multitexture case with no unused data elements, or carry data elements that would be unused except in the multitexture case.</span></span>

<span data-ttu-id="83092-123">Voici un exemple d’utilisation de deux jeux de données de vertex : un pour une texture unique et un pour la multitexturation.</span><span class="sxs-lookup"><span data-stu-id="83092-123">Here is an example of using two sets of vertex data, one for single texture and one for multitexturing.</span></span>


```
struct CUSTOMVERTEX_TEX1
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
};
 
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="83092-124">L’alternative consistait à avoir un seul élément vertex qui contenait les deux jeux de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="83092-124">The alternative was to have a single vertex element that contained both sets of texture coordinates.</span></span>


```
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="83092-125">Avec ces données de vertex, une seule copie des données de position et de couleur est transportée en mémoire, au détriment de l’acheminement des deux jeux de coordonnées de texture pour le rendu, même dans le cas de la texture unique.</span><span class="sxs-lookup"><span data-stu-id="83092-125">With this vertex data, only one copy of the position and color data are carried in memory, at the expense of carrying both sets of texture coordinates around for rendering even in the single texture case.</span></span>

<span data-ttu-id="83092-126">Maintenant que le compromis est clair, les flux fournissent un correctif élégant à ce dilemme.</span><span class="sxs-lookup"><span data-stu-id="83092-126">Now that the tradeoff is clear, streams provide an elegant fix to this dilemma.</span></span> <span data-ttu-id="83092-127">Voici un ensemble de définitions de vertex pour la prise en charge de trois flux : l’un avec la position et la couleur, l’autre avec le premier jeu de coordonnées de texture et l’autre avec le deuxième jeu de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="83092-127">Here is a set of vertex definitions to support three streams: one with position and color, one with the first set of texture coordinates, and one with the second set of texture coordinates.</span></span>


```
// Multistream vertex
// Stream 0, pos, diffuse, specular
struct POSCOLORVERTEX
{
    FLOAT x, y, z;
    DWORD diffColor, specColor;
};
#define D3DFVF_POSCOLORVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_SPECULAR)
// Stream 1, tex coord 0
struct TEXC0VERTEX
{
    FLOAT tu1, tv1;
};
#define D3DFVF_TEXC0VERTEX (D3DFVF_TEX1)

// Stream 2, tex coord 1
struct TEXC1VERTEX
{
    FLOAT tu2, tv2;
};
#define D3DFVF_TEXC1VERTEX (D3DFVF_TEX0)
```



<span data-ttu-id="83092-128">La déclaration de vertex se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="83092-128">The vertex declaration would be as follows:</span></span>


```
// Multitexture - multistream

D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},
    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    D3DDECL_END()
};
```



<span data-ttu-id="83092-129">Créez maintenant l’objet de déclaration de vertex et définissez-le comme indiqué :</span><span class="sxs-lookup"><span data-stu-id="83092-129">Now create the vertex declaration object and set it as shown:</span></span>


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a><span data-ttu-id="83092-130">Exemples de combinaisons</span><span class="sxs-lookup"><span data-stu-id="83092-130">Examples of Combinations</span></span>

### <a name="one-stream-diffuse-color"></a><span data-ttu-id="83092-131">Couleur diffuse d’une diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="83092-131">One Stream Diffuse Color</span></span>

<span data-ttu-id="83092-132">La déclaration de vertex et les paramètres de flux pour le rendu des couleurs diffuses se présentent comme suit :</span><span class="sxs-lookup"><span data-stu-id="83092-132">The vertex declaration and stream settings for diffuse color rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0,  0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0 ,
    {0, 16,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBVertexShader0, 0,
                                      sizeof(CUSTOMVERTEX));
   m_pd3dDevice->SetStreamSource(1, NULL, 0, 0);
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-texture"></a><span data-ttu-id="83092-133">Deux flux avec la couleur et la texture</span><span class="sxs-lookup"><span data-stu-id="83092-133">Two Streams with Color and Texture</span></span>

<span data-ttu-id="83092-134">La déclaration de vertex et les paramètres de flux pour le rendu de la texture unique se présentent comme suit :</span><span class="sxs-lookup"><span data-stu-id="83092-134">The vertex declaration and stream settings for single texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0,
                                           sizeof(POSCOLORVERTEX));
   m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0,
                                           sizeof(TEXC0VERTEX));
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-two-textures"></a><span data-ttu-id="83092-135">Deux flux avec des couleurs et deux textures</span><span class="sxs-lookup"><span data-stu-id="83092-135">Two Streams with Color and two Textures</span></span>

<span data-ttu-id="83092-136">La déclaration de vertex et les paramètres de flux pour le rendu de plusieurs textures à deux textures se présentent comme suit :</span><span class="sxs-lookup"><span data-stu-id="83092-136">The vertex declaration and stream settings for two-texture multi-texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    
    D3DDECL_END()
};
 
m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0, 
                                          sizeof(POSCOLORVERTEX));
m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0, 
                                          sizeof(TEXC0VERTEX));
m_pd3dDevice->SetStreamSource(2, m_pVBTexC1, 0, 
                                          sizeof(TEXC1VERTEX));
```



<span data-ttu-id="83092-137">Dans tous les cas, l’appel de [**:D IDirect3DDevice9 rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) suivant suffit.</span><span class="sxs-lookup"><span data-stu-id="83092-137">In every case, the following [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) invocation suffices.</span></span>


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



<span data-ttu-id="83092-138">Cela montre la flexibilité des flux pour résoudre le problème de la duplication des données/la transmission redondante des données sur le bus (autrement dit, de gaspiller de la bande passante).</span><span class="sxs-lookup"><span data-stu-id="83092-138">This shows the flexibility of streams in solving the problem of data duplication/redundant data transmission across the bus (that is, of wasting bandwidth).</span></span>

## <a name="related-topics"></a><span data-ttu-id="83092-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83092-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83092-140">Déclaration de vertex</span><span class="sxs-lookup"><span data-stu-id="83092-140">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
