---
description: Les coordonnées de texture dans Direct3D peuvent inclure un, deux, trois ou quatre éléments à virgule flottante pour adresser des textures avec différents niveaux de dimension.
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: Formats de coordonnée de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c95eada1cf21f0a4db38589794b08b88023e72d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747613"
---
# <a name="texture-coordinate-formats-direct3d-9"></a><span data-ttu-id="c30dc-103">Formats de coordonnée de texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c30dc-103">Texture Coordinate Formats (Direct3D 9)</span></span>

<span data-ttu-id="c30dc-104">Les coordonnées de texture dans Direct3D peuvent inclure un, deux, trois ou quatre éléments à virgule flottante pour adresser des textures avec différents niveaux de dimension.</span><span class="sxs-lookup"><span data-stu-id="c30dc-104">Texture coordinates in Direct3D can include one, two, three, or four floating point elements to address textures with varying levels of dimension.</span></span> <span data-ttu-id="c30dc-105">Une texture 1D-une surface de texture avec des dimensions de texels 1-par-n, est traitée par une coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="c30dc-105">A 1D texture - a texture surface with dimensions of 1-by-n texels - is addressed by one texture coordinate.</span></span> <span data-ttu-id="c30dc-106">Le cas le plus courant, les textures 2D, sont traités avec deux coordonnées de texture couramment appelées « vous » et « v ».</span><span class="sxs-lookup"><span data-stu-id="c30dc-106">The most common case, 2D textures, are addressed with two texture coordinates commonly called u and v.</span></span> <span data-ttu-id="c30dc-107">Direct3D prend en charge deux types de textures 3D, de cartes d’environnement cubique et de textures de volume.</span><span class="sxs-lookup"><span data-stu-id="c30dc-107">Direct3D supports two types of 3D textures, cubic-environment maps and volume textures.</span></span> <span data-ttu-id="c30dc-108">Les cartes d’environnement cubiques ne sont pas véritablement en 3D, mais elles sont traitées par un vecteur à 3 éléments.</span><span class="sxs-lookup"><span data-stu-id="c30dc-108">Cubic environment maps aren't truly 3D, but they are addressed with a 3-element vector.</span></span> <span data-ttu-id="c30dc-109">Pour plus d’informations, consultez [mappage d’environnement cubique (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="c30dc-109">For details, see [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>

<span data-ttu-id="c30dc-110">Comme décrit dans les [codes de fonction fixe (Direct3D 9)](fixed-function-fvf-codes.md), les applications encodent des coordonnées de texture au format vertex.</span><span class="sxs-lookup"><span data-stu-id="c30dc-110">As described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md), applications encode texture coordinates in the vertex format.</span></span> <span data-ttu-id="c30dc-111">Le format vertex peut inclure plusieurs jeux de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="c30dc-111">The vertex format can include multiple sets of texture coordinates.</span></span> <span data-ttu-id="c30dc-112">Utilisez la D3DFVF \_ TEX0 à D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) pour décrire un format de vertex qui n’a pas de coordonnées de texture, ou jusqu’à huit jeux.</span><span class="sxs-lookup"><span data-stu-id="c30dc-112">Use the D3DFVF\_TEX0 through D3DFVF\_TEX8 [D3DFVF](d3dfvf.md) to describe a vertex format that includes no texture coordinates, or as many as eight sets.</span></span>

<span data-ttu-id="c30dc-113">Chaque jeu de coordonnées de texture peut avoir entre un et quatre éléments.</span><span class="sxs-lookup"><span data-stu-id="c30dc-113">Each texture coordinate set can have between one and four elements.</span></span> <span data-ttu-id="c30dc-114">Les \_ indicateurs D3DFVF TEXTUREFORMAT1 à D3DFVF \_ TEXTUREFORMAT4 décrivent le nombre d’éléments dans une coordonnée de texture dans un jeu, mais ces indicateurs ne sont pas utilisés eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="c30dc-114">The D3DFVF\_TEXTUREFORMAT1 through D3DFVF\_TEXTUREFORMAT4 flags describe the number of elements in a texture coordinate in a set, but these flags aren't used by themselves.</span></span> <span data-ttu-id="c30dc-115">Au lieu de cela, le jeu de macros [**\_ TEXCOORDSIZEN D3DFVF**](d3dfvf-texcoordsizen.md) utilise ces indicateurs pour créer des modèles binaires qui décrivent le nombre d’éléments utilisés par un jeu de coordonnées de texture particulier au format de vertex.</span><span class="sxs-lookup"><span data-stu-id="c30dc-115">Rather, the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros use these flags to create bit patterns that describe the number of elements used by a particular set of texture coordinates in the vertex format.</span></span> <span data-ttu-id="c30dc-116">Ces macros acceptent un paramètre unique qui identifie l’index du jeu de coordonnées dont le nombre d’éléments est défini.</span><span class="sxs-lookup"><span data-stu-id="c30dc-116">These macros accept a single parameter that identifies the index of the coordinate set whose number of elements is being defined.</span></span> <span data-ttu-id="c30dc-117">L’exemple suivant illustre l’utilisation de ces macros.</span><span class="sxs-lookup"><span data-stu-id="c30dc-117">The following example illustrates how these macros are used.</span></span>


```
// This vertex format contains two sets of texture coordinates.
// The first set (index 0) has 2 elements, and the second set 
// has 1 element. The description for this vertex format would be: 
//     dwFVF = D3DFVF_XYZ  | D3DFVF_NORMAL | D3DFVF_DIFFUSE | D3DFVF_TEX2 |
//             D3DFVF_TEXCOORDSIZE2(0) | D3DFVF_TEXCOORDSIZE1(1); 
//
typedef struct CVF
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DCOLOR  diffuse;
    float     u, v;   // 1st set, 2D
    float     t;      // 2nd set, 1D
} CustomVertexFormat;
```



> [!Note]  
> <span data-ttu-id="c30dc-118">À l’exception des cartes de l’environnement cubique et des textures de volume, les rastériseurs ne peuvent pas traiter les textures à l’aide de plus de deux éléments.</span><span class="sxs-lookup"><span data-stu-id="c30dc-118">With the exception of cubic-environment maps and volume textures, rasterizers cannot address textures by using any more than two elements.</span></span> <span data-ttu-id="c30dc-119">Les applications peuvent fournir jusqu’à trois éléments pour une coordonnée de texture, mais uniquement si la texture est un mappage de cube, une texture de volume ou l' \_ indicateur de transformation de texture projeté D3DTTFF est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c30dc-119">Applications can supply up to three elements for a texture coordinate, but only if the texture is a cube map, a volume texture, or the D3DTTFF\_PROJECTED texture transform flag is used.</span></span> <span data-ttu-id="c30dc-120">L' \_ indicateur D3DTTFF projeté amène le rastériseur à diviser les deux premiers éléments par le troisième (ou n) élément.</span><span class="sxs-lookup"><span data-stu-id="c30dc-120">The D3DTTFF\_PROJECTED flag causes the rasterizer to divide the first two elements by the third (or n) element.</span></span> <span data-ttu-id="c30dc-121">Pour plus d’informations, consultez [transformations de coordonnées de texture (Direct3D 9)](texture-coordinate-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="c30dc-121">For more information, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c30dc-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c30dc-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c30dc-123">Coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="c30dc-123">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



