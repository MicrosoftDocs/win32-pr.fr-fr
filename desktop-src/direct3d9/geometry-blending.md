---
description: Direct3D permet à une application d’augmenter le réalisme de ses scènes en affichant des objets polygones segmentés, en particulier des caractères, qui ont des jointures lissées.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Fusion géométrique (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19daa40f7d7d8193ae486640bc613dd7a666ec7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745381"
---
# <a name="geometry-blending-direct3d-9"></a><span data-ttu-id="589b2-103">Fusion géométrique (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="589b2-103">Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="589b2-104">Direct3D permet à une application d’augmenter le réalisme de ses scènes en affichant des objets polygones segmentés, en particulier des caractères, qui ont des jointures lissées.</span><span class="sxs-lookup"><span data-stu-id="589b2-104">Direct3D enables an application to increase the realism of its scenes by rendering segmented polygonal objects - especially characters - that have smoothly blended joints.</span></span> <span data-ttu-id="589b2-105">Ces effets sont souvent appelés « pelures ».</span><span class="sxs-lookup"><span data-stu-id="589b2-105">These effects are often referred to as skinning.</span></span> <span data-ttu-id="589b2-106">Le système réalise cet effet en appliquant des matrices de transformation universelles supplémentaires à un seul ensemble de vertex pour créer plusieurs résultats, puis en effectuant une fusion linéaire entre les vertex résultants pour créer un ensemble unique de géométrie pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="589b2-106">The system achieves this effect by applying additional world transformation matrices to a single set of vertices to create multiple results, and then performing a linear blend between the resultant vertices to create a single set of geometry for rendering.</span></span> <span data-ttu-id="589b2-107">L’illustration suivante d’une banane illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="589b2-107">The following illustration of a banana shows this process.</span></span>

![illustration du processus de fusion de deux objets avec la texture Banana](images/geometry-blend.png)

<span data-ttu-id="589b2-109">L’illustration précédente montre comment vous pouvez imaginer le processus de fusion géométrique.</span><span class="sxs-lookup"><span data-stu-id="589b2-109">The preceding illustration shows how you might imagine the geometry-blending process.</span></span> <span data-ttu-id="589b2-110">Dans un appel de rendu unique, le système prend les sommets de la banane, les transforme deux fois sans modification, et une fois avec une rotation simple, et fusionne les résultats pour créer une banane tordue.</span><span class="sxs-lookup"><span data-stu-id="589b2-110">In a single rendering call, the system takes the vertices for the banana, transforms them twice - once without modification, and once with a simple rotation - and blends the results to create a bent banana.</span></span> <span data-ttu-id="589b2-111">Le système fusionne la position du vertex, ainsi que la normale du vertex lorsque l’éclairage est activé.</span><span class="sxs-lookup"><span data-stu-id="589b2-111">The system blends the vertex position, as well as the vertex normal when lighting is enabled.</span></span> <span data-ttu-id="589b2-112">Les applications ne sont pas limitées à deux chemins de fusion ; Direct3D peut mélanger la géométrie entre jusqu’à quatre matrices universelles, y compris la matrice universelle standard, [**D3DTS \_ World**](d3dts-world.md).</span><span class="sxs-lookup"><span data-stu-id="589b2-112">Applications are not limited to two blending paths; Direct3D can blend geometry between as many as four world matrices, including the standard world matrix, [**D3DTS\_WORLD**](d3dts-world.md).</span></span>

> [!Note]
>
> <span data-ttu-id="589b2-113">Lorsque l’éclairage est activé, les normales de vertex sont transformées par une matrice de vue mondiale inverse correspondante, pondérée de la même façon que les calculs de position de vertex.</span><span class="sxs-lookup"><span data-stu-id="589b2-113">When lighting is enabled, vertex normals are transformed by a corresponding inverse world-view matrix, weighted in the same way as the vertex position computations.</span></span> <span data-ttu-id="589b2-114">Le système normalise le vecteur normal résultant si l' \_ État de rendu D3DRS NORMALIZENORMALS est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="589b2-114">The system normalizes the resulting normal vector if the D3DRS\_NORMALIZENORMALS render state is set to **TRUE**.</span></span>

 

<span data-ttu-id="589b2-115">Sans la fusion géométrique, les modèles articulés dynamiques sont souvent rendus dans des segments.</span><span class="sxs-lookup"><span data-stu-id="589b2-115">Without geometry blending, dynamic articulated models are often rendered in segments.</span></span> <span data-ttu-id="589b2-116">Par exemple, considérez un modèle 3D du bras humain.</span><span class="sxs-lookup"><span data-stu-id="589b2-116">For instance, consider a 3D model of the human arm.</span></span> <span data-ttu-id="589b2-117">Dans la vue la plus simple, un ARM a deux parties : le bras supérieur qui se connecte au corps et le bras inférieur qui se connecte à la main.</span><span class="sxs-lookup"><span data-stu-id="589b2-117">In the simplest view, an arm has two parts: the upper arm which connects to the body, and the lower arm, which connects to the hand.</span></span> <span data-ttu-id="589b2-118">Les deux sont connectés au coude et le bras inférieur tourne à ce point.</span><span class="sxs-lookup"><span data-stu-id="589b2-118">The two are connected at the elbow, and the lower arm rotates at that point.</span></span> <span data-ttu-id="589b2-119">Une application qui restitue un ARM peut conserver des données de vertex pour le bras supérieur et inférieur, chacun avec une matrice de transformation universelle distincte.</span><span class="sxs-lookup"><span data-stu-id="589b2-119">An application that renders an arm might retain vertex data for the upper and lower arm, each with a separate world transformation matrix.</span></span> <span data-ttu-id="589b2-120">L'exemple de code suivant illustre ceci.</span><span class="sxs-lookup"><span data-stu-id="589b2-120">The following code example illustrates this.</span></span>


```
typedef struct _Arm
{
    VERTEX upper_arm_verts[200];
    D3DMATRIX matWorld_Upper;

    VERTEX lower_arm_verts[200];
    D3DMATRIX matWorld_Lower;
} ARM, *LPARM;

ARM MyArm; // This needs to be initialized.
```



<span data-ttu-id="589b2-121">Pour restituer le ARM, deux appels de rendu sont effectués, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="589b2-121">To render the arm, two rendering calls are made, as shown in the following code.</span></span>


```
// Render the upper arm.
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Upper );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );

// Render the lower arm, updating its world matrix to articulate
// the arm by pi/4 radians (45 degrees) at the elbow.
MyArm.matWorld_Lower = RotateMyArm(MyArm.matWorld, pi/4);
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Lower );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );
```



<span data-ttu-id="589b2-122">L’illustration suivante est une banane, modifiée pour utiliser cette technique.</span><span class="sxs-lookup"><span data-stu-id="589b2-122">The following illustration is a banana, modified to use this technique.</span></span>

![illustration d’une banane fusionnée sans fusion géométrique](images/noblend.png)

<span data-ttu-id="589b2-124">Les différences entre la géométrie fusionnée et la géométrie qui n’est pas fusionnée sont évidentes.</span><span class="sxs-lookup"><span data-stu-id="589b2-124">The differences between the blended geometry and the nonblended geometry are obvious.</span></span> <span data-ttu-id="589b2-125">Cet exemple est quelque peu extrême.</span><span class="sxs-lookup"><span data-stu-id="589b2-125">This example is somewhat extreme.</span></span> <span data-ttu-id="589b2-126">Dans une application réelle, les jointures de modèles segmentés sont conçues de façon à ce que les coutures ne soient pas aussi évidentes.</span><span class="sxs-lookup"><span data-stu-id="589b2-126">In a real-world application, the joints of segmented models are designed so that seams are not as obvious.</span></span> <span data-ttu-id="589b2-127">Toutefois, les jointures sont visibles à des moments, ce qui présente des défis constants pour les concepteurs de modèles.</span><span class="sxs-lookup"><span data-stu-id="589b2-127">However, seams are visible at times, which presents constant challenges for model designers.</span></span>

<span data-ttu-id="589b2-128">La fusion géométrique dans Direct3D présente une alternative au scénario de modélisation segmentée classique.</span><span class="sxs-lookup"><span data-stu-id="589b2-128">Geometry blending in Direct3D presents an alternative to the classic segmented-modeling scenario.</span></span> <span data-ttu-id="589b2-129">Toutefois, l’amélioration de la qualité visuelle des objets segmentés survient au détriment des calculs de fusion pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="589b2-129">However, the improved visual quality of segmented objects comes at the cost of the blending computations during rendering.</span></span> <span data-ttu-id="589b2-130">Pour réduire l’impact de ces opérations supplémentaires, le pipeline de géométrie Direct3D est optimisé pour mélanger la géométrie avec la surcharge la moins possible.</span><span class="sxs-lookup"><span data-stu-id="589b2-130">To minimize the impact of these additional operations, the Direct3D geometry pipeline is optimized to blend geometry with the least possible overhead.</span></span> <span data-ttu-id="589b2-131">Les applications qui utilisent intelligemment les services de fusion de géométrie proposés par Direct3D peuvent améliorer le réalisme de leurs caractères tout en évitant de sérieux répercussions sur les performances.</span><span class="sxs-lookup"><span data-stu-id="589b2-131">Applications that intelligently use the geometry blending services offered by Direct3D can improve the realism of their characters while avoiding serious performance repercussions.</span></span>

## <a name="blending-transform-and-render-states"></a><span data-ttu-id="589b2-132">Fusion des États de transformation et de rendu</span><span class="sxs-lookup"><span data-stu-id="589b2-132">Blending Transform and Render States</span></span>

<span data-ttu-id="589b2-133">La méthode [**IDirect3DDevice9 :: setTransform**](/windows/desktop/api) reconnaît les macros internationales [**D3DTS \_**](d3dts-world.md) et [**D3DTS \_ worldn**](d3dts-worldn.md) , qui correspondent à des valeurs qui peuvent être définies par la macro D3DTS [**\_ WORLDMATRIX**](d3dts-worldmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="589b2-133">The [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method recognizes the [**D3DTS\_WORLD**](d3dts-world.md) and [**D3DTS\_WORLDn**](d3dts-worldn.md) macros, which correspond to values that can be defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro.</span></span> <span data-ttu-id="589b2-134">Ces macros sont utilisées pour identifier les matrices entre lesquelles la géométrie sera fusionnée.</span><span class="sxs-lookup"><span data-stu-id="589b2-134">These macros are used to identify the matrices between which geometry will be blended.</span></span>

<span data-ttu-id="589b2-135">Le type énuméré [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) comprend l' \_ État de rendu D3DRS VERTEXBLEND pour activer et contrôler la fusion géométrique.</span><span class="sxs-lookup"><span data-stu-id="589b2-135">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes the D3DRS\_VERTEXBLEND render state to enable and control geometry blending.</span></span> <span data-ttu-id="589b2-136">Les valeurs valides pour cet état de rendu sont définies par le type énuméré [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="589b2-136">Valid values for this render state are defined by the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="589b2-137">Si la fusion géométrique est activée, le format du vertex doit inclure le nombre approprié de poids de fusion.</span><span class="sxs-lookup"><span data-stu-id="589b2-137">If geometry blending is enabled, the vertex format must include the appropriate number of blending weights.</span></span>

## <a name="blending-weights"></a><span data-ttu-id="589b2-138">Fusion des poids</span><span class="sxs-lookup"><span data-stu-id="589b2-138">Blending Weights</span></span>

<span data-ttu-id="589b2-139">Une pondération de fusion, parfois appelée pondération bêta, contrôle la portée à laquelle une matrice universelle donnée affecte un vertex.</span><span class="sxs-lookup"><span data-stu-id="589b2-139">A blending weight, sometimes called a beta weight, controls the extent to which a given world matrix affects a vertex.</span></span> <span data-ttu-id="589b2-140">Les pondérations de fusion sont des valeurs à virgule flottante comprises entre 0,0 et 1,0, encodées au format vertex, où la valeur 0,0 signifie que le vertex n’est pas fusionné avec cette matrice et 1,0 signifie que le vertex est affecté en totalité par la matrice.</span><span class="sxs-lookup"><span data-stu-id="589b2-140">Blending weights are floating-point values that range from 0.0 to 1.0, encoded in the vertex format, where a value of 0.0 means the vertex is not blended with that matrix, and 1.0 means that the vertex is affected in full by the matrix.</span></span>

<span data-ttu-id="589b2-141">Les pondérations de fusion Geometry sont encodées au format de vertex, qui apparaissent juste après la position de chaque vertex, comme décrit dans la [fonction Fixed des codes d’erreur (Direct3D 9)](fixed-function-fvf-codes.md).</span><span class="sxs-lookup"><span data-stu-id="589b2-141">Geometry blending weights are encoded in the vertex format, appearing immediately after the position for each vertex, as described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span> <span data-ttu-id="589b2-142">Vous communiquez le nombre de poids de fusion dans le format de vertex en incluant l’une des [constantes](d3dfvf.md) de la Commission de la Commission dans la description de vertex que vous fournissez aux méthodes de rendu.</span><span class="sxs-lookup"><span data-stu-id="589b2-142">You communicate the number of blending weights in the vertex format by including one of the [FVF constants](d3dfvf.md) in the vertex description that you provide to the rendering methods.</span></span>

<span data-ttu-id="589b2-143">Le système effectue une fusion linéaire entre les résultats pondérés des matrices de fusion.</span><span class="sxs-lookup"><span data-stu-id="589b2-143">The system performs a linear blend between the weighted results of the blend matrices.</span></span> <span data-ttu-id="589b2-144">L’équation suivante est la formule de fusion complète.</span><span class="sxs-lookup"><span data-stu-id="589b2-144">The following equation is the complete blending formula.</span></span>

![équation de la fusion linéaire, à l’aide de matrices de transformation universelle](images/vert-blend-formula.png)

<span data-ttu-id="589b2-146">Dans l’équation précédente, vBlend est le vertex de sortie, les éléments v sont les vertex produits par la matrice universelle appliquée ([**D3DTS \_ worldn**](d3dts-worldn.md)).</span><span class="sxs-lookup"><span data-stu-id="589b2-146">In the preceding equation, vBlend is the output vertex, the v-elements are the vertices produced by the applied world matrix ([**D3DTS\_WORLDn**](d3dts-worldn.md)).</span></span> <span data-ttu-id="589b2-147">Les éléments W sont les valeurs de poids correspondantes dans le format de vertex.</span><span class="sxs-lookup"><span data-stu-id="589b2-147">The W elements are the corresponding weight values within the vertex format.</span></span> <span data-ttu-id="589b2-148">Un sommet fusionné entre n matrices peut avoir-1 valeurs de poids de fusion, une pour chaque matrice de fusion, à l’exception de la dernière.</span><span class="sxs-lookup"><span data-stu-id="589b2-148">A vertex blended between n matrices can have - 1 blending weight values, one for each blending matrix, except the last.</span></span> <span data-ttu-id="589b2-149">Le système génère automatiquement le poids de la dernière matrice mondiale de sorte que la somme de tous les poids soit 1,0, exprimée en notation Sigma ici.</span><span class="sxs-lookup"><span data-stu-id="589b2-149">The system automatically generates the weight for the last world matrix so that the sum of all weights is 1.0, expressed in sigma notation here.</span></span> <span data-ttu-id="589b2-150">Cette formule peut être simplifiée pour chacun des cas pris en charge par Direct3D, qui est présenté dans les équations suivantes.</span><span class="sxs-lookup"><span data-stu-id="589b2-150">This formula can be simplified for each of the cases supported by Direct3D, which is shown in the following equations.</span></span>

![équations de la fusion linéaire pour trois cas de fusion](images/vert-blend-formulas-simple.png)

<span data-ttu-id="589b2-152">Il s’agit des formes simplifiées de la formule de fusion complète pour les deux, trois et quatre cas de matrice de fusion.</span><span class="sxs-lookup"><span data-stu-id="589b2-152">These are the simplified forms of the complete blending formula for the two, three, and four blend matrix cases.</span></span>

> [!Note]  
> <span data-ttu-id="589b2-153">Bien que Direct3D comprenne des descripteurs de la Commission de la Commission pour définir des vertex qui contiennent jusqu’à cinq poids de fusion, seuls trois peuvent être utilisés dans cette version de DirectX.</span><span class="sxs-lookup"><span data-stu-id="589b2-153">Although Direct3D includes FVF descriptors to define vertices that contain up to five blending weights, only three can be used in this release of DirectX.</span></span>

 

<span data-ttu-id="589b2-154">Des informations supplémentaires sont contenues dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="589b2-154">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="589b2-155">Utilisation de la fusion géométrique (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="589b2-155">Using Geometry Blending (Direct3D 9)</span></span>](using-geometry-blending.md)
-   [<span data-ttu-id="589b2-156">Fusion de vertex indexée (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="589b2-156">Indexed Vertex Blending (Direct3D 9)</span></span>](indexed-vertex-blending.md)
-   [<span data-ttu-id="589b2-157">Interpolation de vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="589b2-157">Vertex Tweening (Direct3D 9)</span></span>](vertex-tweening.md)

## <a name="related-topics"></a><span data-ttu-id="589b2-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="589b2-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="589b2-159">Pipeline de vertex</span><span class="sxs-lookup"><span data-stu-id="589b2-159">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
