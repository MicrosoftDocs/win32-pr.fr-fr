---
description: Un code d’erreur de la Commission décrit le contenu des vertex stockés entrelacés dans un flux de données unique.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Correction des codes de fonction de la Commission (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd10b655c0692881e5d93b6c716ec9bcd8a76c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514298"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a><span data-ttu-id="52e0d-103">Correction des codes de fonction de la Commission (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="52e0d-103">Fixed Function FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="52e0d-104">Un code d’erreur de la Commission décrit le contenu des vertex stockés entrelacés dans un flux de données unique.</span><span class="sxs-lookup"><span data-stu-id="52e0d-104">A FVF code describes the contents of vertices stored interleaved in a single data stream.</span></span> <span data-ttu-id="52e0d-105">Elle spécifie généralement les données à traiter par le pipeline de traitement de vertex de fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="52e0d-105">It generally specifies data to be processed by the fixed function vertex processing pipeline.</span></span> <span data-ttu-id="52e0d-106">Il s’agit d’une déclaration de vertex de style plus ancienne ; pour afficher le style de déclaration de vertex actuel, consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="52e0d-106">This is an older-style vertex declaration; to see the current vertex declaration style, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="52e0d-107">Les applications Direct3D peuvent définir des vertex de modèle de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="52e0d-107">Direct3D applications can define model vertices in several different ways.</span></span> <span data-ttu-id="52e0d-108">La prise en charge des définitions de vertex flexibles, également appelées formats de vertex flexibles ou codes de format de vertex flexibles, permet à votre application d’utiliser uniquement les composants de vertex dont elle a besoin, en éliminant les composants qui ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="52e0d-108">Support for flexible vertex definitions, also known as flexible vertex formats or flexible vertex format codes, makes it possible for your application to use only the vertex components it needs, eliminating those components that aren't used.</span></span> <span data-ttu-id="52e0d-109">En utilisant uniquement les composants de vertex nécessaires, votre application peut économiser de la mémoire et réduire la bande passante de traitement nécessaire pour restituer les modèles.</span><span class="sxs-lookup"><span data-stu-id="52e0d-109">By using only the needed vertex components, your application can conserve memory and minimize the processing bandwidth required to render models.</span></span> <span data-ttu-id="52e0d-110">Vous décrivez comment vos vertex sont mis en forme à l’aide d’une combinaison de codes [D3DFVF](d3dfvf.md) .</span><span class="sxs-lookup"><span data-stu-id="52e0d-110">You describe how your vertices are formatted by using a combination of [D3DFVF](d3dfvf.md) codes.</span></span>

<span data-ttu-id="52e0d-111">La spécification de la Commission des prix finals comprend des formats de taille de point, spécifiés par D3DFVF \_ psize.</span><span class="sxs-lookup"><span data-stu-id="52e0d-111">The FVF specification includes formats for point size, specified by D3DFVF\_PSIZE.</span></span> <span data-ttu-id="52e0d-112">Cette taille est exprimée en unités d’espace de caméra pour les vertex non transformés et allumés (TL) et dans les unités d’espace de l’appareil pour les vertex TL.</span><span class="sxs-lookup"><span data-stu-id="52e0d-112">This size is expressed in camera space units for non-transformed and lit (TL) vertices, and in device-space units for TL vertices.</span></span>

<span data-ttu-id="52e0d-113">Les méthodes de rendu de l’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) fournissent aux applications C++ des méthodes qui acceptent une combinaison de ces indicateurs et les utilisent pour déterminer comment restituer les primitives.</span><span class="sxs-lookup"><span data-stu-id="52e0d-113">The rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface provide C++ applications with methods that accept a combination of these flags, and use them to determine how to render primitives.</span></span> <span data-ttu-id="52e0d-114">Fondamentalement, ces indicateurs indiquent au système quels sont les points de position, les poids de fusion de vertex, les couleurs normales, les couleurs et le nombre et le format des coordonnées de texture. votre application utilise et, indirectement, les parties du pipeline de rendu que vous souhaitez que Direct3D applique à celles-ci.</span><span class="sxs-lookup"><span data-stu-id="52e0d-114">Basically, these flags tell the system which vertex components - position, vertex blending weights, normal, colors, and the number and format of texture coordinates - your application uses and, indirectly, which parts of the rendering pipeline you want Direct3D to apply to them.</span></span> <span data-ttu-id="52e0d-115">En outre, la présence ou l’absence d’un indicateur de format de vertex particulier communique au système les champs de composant de vertex qui sont présents dans la mémoire et que vous avez omis.</span><span class="sxs-lookup"><span data-stu-id="52e0d-115">In addition, the presence or absence of a particular vertex format flag communicates to the system which vertex component fields are present in memory and which you've omitted.</span></span>

<span data-ttu-id="52e0d-116">Pour déterminer les limitations de l’appareil, vous pouvez interroger un appareil pour connaître les valeurs de D3DFVFCAPS \_ DONOTSTRIPELEMENTS et D3DFVFCAPS \_ TEXCOORDCOUNTMASK dans le membre FVFCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="52e0d-116">To determine device limitations, you can query a device for the values of D3DFVFCAPS\_DONOTSTRIPELEMENTS and D3DFVFCAPS\_TEXCOORDCOUNTMASK in the FVFCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="52e0d-117">Les coordonnées de texture peuvent être déclarées dans différents formats, ce qui permet de résoudre les textures à l’aide d’une seule coordonnée ou jusqu’à quatre coordonnées de texture (pour les coordonnées de texture 2D projetées).</span><span class="sxs-lookup"><span data-stu-id="52e0d-117">Texture coordinates can be declared in different formats, allowing textures to be addressed using as few as one coordinate or as many as four texture coordinates (for 2D projected texture coordinates).</span></span> <span data-ttu-id="52e0d-118">Pour plus d’informations, consultez [formats de coordonnée de texture (Direct3D 9)](texture-coordinate-formats.md).</span><span class="sxs-lookup"><span data-stu-id="52e0d-118">For more information, see [Texture Coordinate Formats (Direct3D 9)](texture-coordinate-formats.md).</span></span> <span data-ttu-id="52e0d-119">Utilisez l’ensemble de macros [**\_ TEXCOORDSIZEN D3DFVF**](d3dfvf-texcoordsizen.md) pour créer des modèles de bits qui identifient les formats de coordonnée de texture utilisés par votre format de vertex.</span><span class="sxs-lookup"><span data-stu-id="52e0d-119">Use the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros to create bit patterns that identify the texture coordinate formats that your vertex format uses.</span></span>

<span data-ttu-id="52e0d-120">Aucune application n’utilise chaque composant.</span><span class="sxs-lookup"><span data-stu-id="52e0d-120">No application will use every component.</span></span> <span data-ttu-id="52e0d-121">Les champs mutuels homogènes W (RHW) et vertex normal s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="52e0d-121">The reciprocal homogeneous W (RHW) and vertex normal fields are mutually exclusive.</span></span> <span data-ttu-id="52e0d-122">De plus, la plupart des applications essaient d’utiliser les huit jeux de coordonnées de texture, mais Direct3D dispose de cette capacité.</span><span class="sxs-lookup"><span data-stu-id="52e0d-122">Nor will most applications try to use all eight sets of texture coordinates, but Direct3D has this capacity.</span></span> <span data-ttu-id="52e0d-123">Il existe plusieurs restrictions sur les indicateurs que vous pouvez utiliser avec d’autres indicateurs.</span><span class="sxs-lookup"><span data-stu-id="52e0d-123">There are several restrictions on which flags you can use with other flags.</span></span> <span data-ttu-id="52e0d-124">Par exemple, vous ne pouvez pas utiliser les \_ indicateurs D3DFVF XYZ et D3DFVF \_ XYZRHW ensemble, car cela indiquerait que votre application décrit la position d’un sommet avec les vertex non transformés et transformés.</span><span class="sxs-lookup"><span data-stu-id="52e0d-124">For example, you cannot use the D3DFVF\_XYZ and D3DFVF\_XYZRHW flags together, as this would indicate that your application is describing a vertex's position with both untransformed and transformed vertices.</span></span>

<span data-ttu-id="52e0d-125">Pour utiliser la fusion de vertex indexée, l' \_ indicateur D3DFVF LASTBETA \_ UBYTE4 doit apparaître à la fin de la déclaration de la Commission des prix finaux.</span><span class="sxs-lookup"><span data-stu-id="52e0d-125">To use indexed vertex blending, the D3DFVF\_LASTBETA\_UBYTE4 flag should appear at the end of the FVF declaration.</span></span> <span data-ttu-id="52e0d-126">La présence de cet indicateur indique que la cinquième pondération de fusion sera traitée comme une valeur DWORD au lieu de float.</span><span class="sxs-lookup"><span data-stu-id="52e0d-126">The presence of this flag indicates that the fifth blending weight will be treated as a DWORD instead of float.</span></span> <span data-ttu-id="52e0d-127">Pour plus d’informations, consultez la rubrique relative à la [fusion des vertex indexés (Direct3D 9)](indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="52e0d-127">For more information, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span>

<span data-ttu-id="52e0d-128">Les exemples de code suivants illustrent la différence entre un code d’erreur de la Commission qui utilise l' \_ indicateur D3DFVF LASTBETA \_ UBYTE4 et l’autre qui ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="52e0d-128">The following code samples shows the difference between an FVF code that uses the D3DFVF\_LASTBETA\_UBYTE4 flag and one that doesn't.</span></span> <span data-ttu-id="52e0d-129">L’indicateur D3DFVF \_ XYZB3 est présent lorsque quatre index de fusion sont utilisés, car vous pouvez toujours soustraire la somme des trois premiers du numéro 1 pour obtenir le quatrième (Blend ₄ = 1-(Blend ₁ + Blend ₂ + Blend ₃)).</span><span class="sxs-lookup"><span data-stu-id="52e0d-129">The flag D3DFVF\_XYZB3 is present when four blending indices are used because you always subtract the sum of the first three from the number one to obtain the fourth (blend₄ = 1 - (blend₁ + blend₂ + blend₃)).</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB3|D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



<span data-ttu-id="52e0d-130">La Commission de la Commission définie ci-dessous utilise l' \_ indicateur D3DFVF Last \_ UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="52e0d-130">The FVF defined below uses the D3DFVF\_LAST\_UBYTE4 flag.</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB4 | D3DFVF_LASTBETA_UBYTE4 |D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    DWORD       indices; // Referenced as v2.xyzw in the vertex shader 
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



## <a name="related-topics"></a><span data-ttu-id="52e0d-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52e0d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52e0d-132">Déclaration de vertex</span><span class="sxs-lookup"><span data-stu-id="52e0d-132">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
