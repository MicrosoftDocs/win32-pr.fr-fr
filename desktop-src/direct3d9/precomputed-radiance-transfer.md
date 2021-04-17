---
description: Transfert de luminance précalculé (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Transfert de luminance précalculé (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94829a2559888c61ae795309bac5d1ab699d7f27
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104553346"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a><span data-ttu-id="e04e0-103">Transfert de luminance précalculé (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e04e0-103">Precomputed Radiance Transfer (Direct3D 9)</span></span>

## <a name="using-precomputed-radiance-transfer"></a><span data-ttu-id="e04e0-104">Utilisation du transfert de luminance précalculé</span><span class="sxs-lookup"><span data-stu-id="e04e0-104">Using Precomputed Radiance Transfer</span></span>

<span data-ttu-id="e04e0-105">Il existe plusieurs formes de complexité dans des scènes intéressantes, notamment la façon dont l’environnement d’éclairage est modélisé (autrement dit, les modèles d’éclairage de zone par rapport aux points/directionnels) et le type d’effets globaux modélisés (par exemple, les ombres, les interreflets, la diffusion sous-surface). Les techniques de rendu interactives traditionnelles modélisent une quantité limitée de cette complexité.</span><span class="sxs-lookup"><span data-stu-id="e04e0-105">There are several forms of complexity present in interesting scenes, including how the lighting environment is modeled (that is, area lighting models versus point/directional ones) and what kind of global effects are modeled (for example, shadows, interreflections, subsurface scattering.) Traditional interactive rendering techniques model a limited amount of this complexity.</span></span> <span data-ttu-id="e04e0-106">PRT active ces effets avec des restrictions significatives :</span><span class="sxs-lookup"><span data-stu-id="e04e0-106">PRT enables these effects with some significant restrictions:</span></span>

-   <span data-ttu-id="e04e0-107">Les objets sont supposés être rigides (c’est-à-dire, aucune déformations).</span><span class="sxs-lookup"><span data-stu-id="e04e0-107">Objects are assumed to be rigid (that is, no deformations).</span></span>
-   <span data-ttu-id="e04e0-108">Il s’agit d’une approche centrée sur les objets (à moins que les objets ne soient déplacés ensemble, ces effets globaux ne sont pas maintenus entre eux).</span><span class="sxs-lookup"><span data-stu-id="e04e0-108">It is an object-centric approach (unless objects are moved together, these global effects are not maintained between them).</span></span>
-   <span data-ttu-id="e04e0-109">Seule l’éclairage à basse fréquence est modélisé (ce qui entraîne des ombres douces). Pour les lumières haute fréquence (ombres nettes), les techniques traditionnelles devraient être utilisées.</span><span class="sxs-lookup"><span data-stu-id="e04e0-109">Only low-frequency lighting is modeled (resulting in soft shadows.) For high-frequency lights (sharp shadows), traditional techniques would have to be employed.</span></span>

<span data-ttu-id="e04e0-110">PRT requiert l’un des éléments suivants, mais pas les deux :</span><span class="sxs-lookup"><span data-stu-id="e04e0-110">PRT requires either of the following, but not both:</span></span>

-   <span data-ttu-id="e04e0-111">modèles hautement fractionnés et vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e04e0-111">highly-tessellated models and vs\_1\_1</span></span>
-   <span data-ttu-id="e04e0-112">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e04e0-112">ps\_2\_0</span></span>

### <a name="standard-diffuse-lighting-versus-prt"></a><span data-ttu-id="e04e0-113">Éclairage diffus standard par rapport à PRT</span><span class="sxs-lookup"><span data-stu-id="e04e0-113">Standard Diffuse Lighting versus PRT</span></span>

<span data-ttu-id="e04e0-114">L’illustration suivante est rendue à l’aide du modèle d’éclairage traditionnel (n · l).</span><span class="sxs-lookup"><span data-stu-id="e04e0-114">The following illustration is rendered using the traditional (n · l) lighting model.</span></span> <span data-ttu-id="e04e0-115">Les ombres nettes peuvent être activées à l’aide d’une autre méthode de mise en Shadow et d’une certaine forme de technique d’occultation (cartes de profondeur des tons foncés ou volumes</span><span class="sxs-lookup"><span data-stu-id="e04e0-115">Sharp shadows could be enabled using another pass and some form of shadowing technique (shadow depth maps or shadow volumes).</span></span> <span data-ttu-id="e04e0-116">L’ajout de plusieurs lumières nécessiterait soit plusieurs passes (si des ombres doivent être utilisées), soit des nuanceurs plus complexes avec des techniques traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="e04e0-116">Adding multiple lights would require either multiple passes (if shadows are to be used) or more complex shaders with traditional techniques.</span></span>

![capture d’écran d’une illustration rendue à l’aide du modèle d’éclairage traditionnel](images/prt-diffuse-cropped.png)

<span data-ttu-id="e04e0-118">L’illustration suivante est rendue avec PRT à l’aide de la meilleure approximation d’une lumière directionnelle unique qu’il peut résoudre.</span><span class="sxs-lookup"><span data-stu-id="e04e0-118">The next illustration is rendered with PRT using the best approximation of a single directional light that it can resolve.</span></span> <span data-ttu-id="e04e0-119">Il en résulte des ombres douces qui seraient difficiles à produire avec les techniques traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="e04e0-119">This results in soft shadows that would be difficult to produce with traditional techniques.</span></span> <span data-ttu-id="e04e0-120">Étant donné que PRT modélise toujours des environnements d’éclairage complets en ajoutant plusieurs lumières ou en utilisant une carte d’environnement, vous modifiez uniquement les valeurs (mais pas le nombre) des constantes utilisées par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e04e0-120">Because PRT always models complete lighting environments adding multiple lights or using an environment map, you would only change the values (but not the number) of constants used by the shader.</span></span>

![capture d’écran d’une illustration rendue à l’aide de PRT](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a><span data-ttu-id="e04e0-122">PRT avec interreflets</span><span class="sxs-lookup"><span data-stu-id="e04e0-122">PRT with Interreflections</span></span>

<span data-ttu-id="e04e0-123">L’éclairage direct atteint la surface directement à partir de la lumière.</span><span class="sxs-lookup"><span data-stu-id="e04e0-123">Direct lighting reaches the surface directly from the light.</span></span> <span data-ttu-id="e04e0-124">Les interreflets ont une lumière qui atteint la surface après avoir rebondissant une autre surface un certain nombre de fois.</span><span class="sxs-lookup"><span data-stu-id="e04e0-124">Interreflections are light reaching the surface after bouncing off some other surface some number of times.</span></span> <span data-ttu-id="e04e0-125">PRT peut modéliser ce comportement sans modifier les performances au moment de l’exécution en exécutant simplement le simulateur avec des paramètres différents.</span><span class="sxs-lookup"><span data-stu-id="e04e0-125">PRT can model this behavior without changing the performance at run time by simply running the simulator with different parameters.</span></span>

<span data-ttu-id="e04e0-126">L’illustration suivante est créée à l’aide de l’PRT direct uniquement (0 rebonds sans interréflexions).</span><span class="sxs-lookup"><span data-stu-id="e04e0-126">The following illustration is created using direct PRT only (0 bounces with no interreflections).</span></span>

![capture d’écran d’une illustration rendue à l’aide d’un PRT direct uniquement](images/prt-nointerreflections.png)

<span data-ttu-id="e04e0-128">L’illustration suivante est créée à l’aide de PRT avec des interreflets (2 rebonds avec des interreflets).</span><span class="sxs-lookup"><span data-stu-id="e04e0-128">The following illustration is created using PRT with interreflections (2 bounces with interreflections).</span></span>

![capture d’écran d’une illustration rendue à l’aide de PRT avec interreflets](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a><span data-ttu-id="e04e0-130">PRT avec diffusion sous-surface</span><span class="sxs-lookup"><span data-stu-id="e04e0-130">PRT with Subsurface Scattering</span></span>

<span data-ttu-id="e04e0-131">La diffusion sous-surface est une technique qui modélise la façon dont la lumière passe par certains matériaux.</span><span class="sxs-lookup"><span data-stu-id="e04e0-131">Subsurface scattering is a technique that models how light passes through certain materials.</span></span> <span data-ttu-id="e04e0-132">En guise d’exemple, appuyez sur un appareil Torch allumé sur la paume de votre main.</span><span class="sxs-lookup"><span data-stu-id="e04e0-132">As an example, press a lit flashlight against the palm of your hand.</span></span> <span data-ttu-id="e04e0-133">La lumière de la torche passe à la main, rebondne (en changeant la couleur du processus) et quitte l’autre côté de votre main.</span><span class="sxs-lookup"><span data-stu-id="e04e0-133">The light from the flashlight passes through your hand, bounces around (changing color in the process), and exits from the other side of your hand.</span></span> <span data-ttu-id="e04e0-134">Cela peut également être modélisé avec des modifications simples dans le simulateur et aucune modification du Runtime.</span><span class="sxs-lookup"><span data-stu-id="e04e0-134">This can also be modeled with simple changes to the simulator and no changes to the runtime.</span></span>

<span data-ttu-id="e04e0-135">L’illustration suivante montre PRT avec la diffusion sous-surface.</span><span class="sxs-lookup"><span data-stu-id="e04e0-135">The following illustration demonstrates PRT with subsurface scattering.</span></span>

![capture d’écran d’une illustration rendue à l’aide de PRT avec diffusion sous-surface](images/prt-subsurface.png)

## <a name="how-prt-works"></a><span data-ttu-id="e04e0-137">Fonctionnement de PRT</span><span class="sxs-lookup"><span data-stu-id="e04e0-137">How PRT Works</span></span>

<span data-ttu-id="e04e0-138">Les termes suivants sont utiles pour comprendre le fonctionnement de PRT, comme illustré dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="e04e0-138">The following terms are useful for understanding how PRT works, as illustrated in the following diagram.</span></span>

<span data-ttu-id="e04e0-139">Luminance source : le luminance source représente l’environnement d’éclairage dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="e04e0-139">Source Radiance: The source radiance represents the lighting environment as a whole.</span></span> <span data-ttu-id="e04e0-140">Dans PRT, un environnement arbitraire est approximatif à l’aide de la base d’harmonique sphérique : cet éclairage est supposé être distant par rapport à l’objet (la même hypothèse que celle qui est faite avec les mappages d’environnement).</span><span class="sxs-lookup"><span data-stu-id="e04e0-140">In PRT an arbitrary environment is approximated using the spherical harmonic basis - this lighting is assumed to be distant relative to the object (the same assumption that is made with environment maps.)</span></span>

<span data-ttu-id="e04e0-141">Quitter luminance : Exit luminance est la lumière qui quitte un point sur la surface de toute source possible (réfléchi luminance, diffusion subsurface, émission).</span><span class="sxs-lookup"><span data-stu-id="e04e0-141">Exit Radiance: Exit radiance is the light leaving from a point on the surface from any possible source (reflected radiance, subsurface scattering, emission).</span></span>

<span data-ttu-id="e04e0-142">Transférer les vecteurs : les vecteurs de transfert mappent les luminance sources dans les luminance de sortie et sont précalculés hors connexion à l’aide d’une simulation de transport léger complexe.</span><span class="sxs-lookup"><span data-stu-id="e04e0-142">Transfer Vectors: Transfer vectors map Source Radiance into exit radiance and are precomputed offline using a complex light transport simulation.</span></span>

![Diagramme illustrant le fonctionnement de PRT](images/prt-lightingpicture.png)

<span data-ttu-id="e04e0-144">PRT détermine le processus de rendu en deux étapes, comme indiqué dans le diagramme suivant :</span><span class="sxs-lookup"><span data-stu-id="e04e0-144">PRT factors the rendering process into two stages, as shown in the following diagram:</span></span>

1.  <span data-ttu-id="e04e0-145">Une simulation de transport de lumière coûteuse Précalcule le coefficient de transfert qui peut être utilisé au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e04e0-145">An expensive light transport simulation precomputes transfer coefficients that can be used at run time.</span></span>
2.  <span data-ttu-id="e04e0-146">Une phase d’exécution relativement légère est tout d’abord proche de l’environnement d’éclairage à l’aide de la base d’harmonique sphérique, puis utilise ces coefficients d’éclairage et les coefficients de transfert précalculés (de l’étape 1) avec un nuanceur simple, ce qui entraîne la sortie de luminance (la lumière quittant l’objet).</span><span class="sxs-lookup"><span data-stu-id="e04e0-146">A relatively lightweight run-time stage first approximates the lighting environment using the spherical harmonic basis, then uses these lighting coefficients and the precomputed transfer coefficients (from stage 1) with a simple shader, resulting in exit radiance (the light leaving the object).</span></span>

![diagramme du workflow de données PRT](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a><span data-ttu-id="e04e0-148">Utilisation de l’API PRT</span><span class="sxs-lookup"><span data-stu-id="e04e0-148">How to Use the PRT API</span></span>

1.  <span data-ttu-id="e04e0-149">Calculez les vecteurs de transfert avec l’une des valeurs de calcul... méthodes de [**ID3DXPRTEngine**](id3dxprtengine.md).</span><span class="sxs-lookup"><span data-stu-id="e04e0-149">Compute the transfer vectors with one of the Compute... methods of [**ID3DXPRTEngine**](id3dxprtengine.md).</span></span>

    <span data-ttu-id="e04e0-150">Le traitement direct de ces vecteurs de transfert requiert une quantité significative de calcul de mémoire et de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e04e0-150">Directly dealing with these transfer vectors requires a significant amount of memory and shader computation.</span></span> <span data-ttu-id="e04e0-151">La compression réduit considérablement la quantité de mémoire et le calcul de nuanceur requis.</span><span class="sxs-lookup"><span data-stu-id="e04e0-151">Compression significantly reduces the amount of memory and shader computation required.</span></span>

    <span data-ttu-id="e04e0-152">Les valeurs d’éclairage finales sont calculées dans un nuanceur de sommets qui implémente l’équation de rendu compressé suivante.</span><span class="sxs-lookup"><span data-stu-id="e04e0-152">The final lighting values are calculated in a vertex shader that implements the following compressed rendering equation.</span></span>

    ![équation du rendu PRT](images/prt-shaderequation.png)

    <span data-ttu-id="e04e0-154">Où :</span><span class="sxs-lookup"><span data-stu-id="e04e0-154">Where:</span></span>

    

    | <span data-ttu-id="e04e0-155">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e04e0-155">Parameter</span></span>      | <span data-ttu-id="e04e0-156">Description</span><span class="sxs-lookup"><span data-stu-id="e04e0-156">Description</span></span>                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="e04e0-157">PR</span><span class="sxs-lookup"><span data-stu-id="e04e0-157">Rₚ</span></span>             | <span data-ttu-id="e04e0-158">Un seul canal de sortie luminance au sommet p et est évalué à chaque vertex de la maille.</span><span class="sxs-lookup"><span data-stu-id="e04e0-158">A single channel of exit radiance at vertex p and is evaluated at every vertex on the mesh.</span></span>                     |
    | <span data-ttu-id="e04e0-159">MK</span><span class="sxs-lookup"><span data-stu-id="e04e0-159">Mₖ</span></span>             | <span data-ttu-id="e04e0-160">Moyenne du cluster k.</span><span class="sxs-lookup"><span data-stu-id="e04e0-160">The mean for cluster k.</span></span> <span data-ttu-id="e04e0-161">Il s’agit d’un vecteur de coefficient de commande ².</span><span class="sxs-lookup"><span data-stu-id="e04e0-161">This is an Order² vector of coefficients.</span></span>                                               |
    | <span data-ttu-id="e04e0-162">k</span><span class="sxs-lookup"><span data-stu-id="e04e0-162">k</span></span>              | <span data-ttu-id="e04e0-163">ID de cluster pour le vertex p.</span><span class="sxs-lookup"><span data-stu-id="e04e0-163">The cluster ID for vertex p.</span></span>                                                                                    |
    | <span data-ttu-id="e04e0-164">L<sup>'</sup></span><span class="sxs-lookup"><span data-stu-id="e04e0-164">L<sup>'</sup></span></span>  | <span data-ttu-id="e04e0-165">Approximation de la source luminance dans les fonctions de base SH.</span><span class="sxs-lookup"><span data-stu-id="e04e0-165">The approximation of the source radiance into the SH basis functions.</span></span> <span data-ttu-id="e04e0-166">Il s’agit d’un vecteur de coefficient de commande ².</span><span class="sxs-lookup"><span data-stu-id="e04e0-166">This is an Order² vector of coefficients.</span></span> |
    | <span data-ttu-id="e04e0-167">j</span><span class="sxs-lookup"><span data-stu-id="e04e0-167">j</span></span>              | <span data-ttu-id="e04e0-168">Entier qui additionne le nombre de vecteurs PCA.</span><span class="sxs-lookup"><span data-stu-id="e04e0-168">An integer that sums over the number of PCA vectors.</span></span>                                                            |
    | <span data-ttu-id="e04e0-169">w<sub>PJ</sub></span><span class="sxs-lookup"><span data-stu-id="e04e0-169">w<sub>pj</sub></span></span> | <span data-ttu-id="e04e0-170">Poids de JTH PCA pour le point p.</span><span class="sxs-lookup"><span data-stu-id="e04e0-170">The jth PCA weight for point p.</span></span> <span data-ttu-id="e04e0-171">Il s’agit d’un coefficient unique.</span><span class="sxs-lookup"><span data-stu-id="e04e0-171">This is a single coefficient.</span></span>                                                   |
    | <span data-ttu-id="e04e0-172">B<sub>kJ</sub></span><span class="sxs-lookup"><span data-stu-id="e04e0-172">B<sub>kj</sub></span></span> | <span data-ttu-id="e04e0-173">Le vecteur de base JTH PCA pour le cluster k.</span><span class="sxs-lookup"><span data-stu-id="e04e0-173">The jth PCA basis vector for cluster k.</span></span> <span data-ttu-id="e04e0-174">Il s’agit d’un vecteur de coefficient de commande ².</span><span class="sxs-lookup"><span data-stu-id="e04e0-174">This is an Order² vector of coefficients.</span></span>                               |

    

     

    <span data-ttu-id="e04e0-175">L’extraction... les méthodes de [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) permettent d’accéder aux données compressées à partir de la simulation.</span><span class="sxs-lookup"><span data-stu-id="e04e0-175">The Extract... methods of [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) provide access to compressed data from the simulation.</span></span>

2.  <span data-ttu-id="e04e0-176">Calculez la source luminance.</span><span class="sxs-lookup"><span data-stu-id="e04e0-176">Compute the source radiance.</span></span>

    <span data-ttu-id="e04e0-177">Il existe plusieurs fonctions d’assistance dans l’API pour gérer un large éventail de scénarios d’éclairage courants.</span><span class="sxs-lookup"><span data-stu-id="e04e0-177">There are several helper functions in the API to handle a variety of common lighting scenarios.</span></span>

    

    | <span data-ttu-id="e04e0-178">Fonction</span><span class="sxs-lookup"><span data-stu-id="e04e0-178">Function</span></span>                                                         | <span data-ttu-id="e04e0-179">Objectif</span><span class="sxs-lookup"><span data-stu-id="e04e0-179">Purpose</span></span>                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="e04e0-180">**D3DXSHEvalDirectionalLight**</span><span class="sxs-lookup"><span data-stu-id="e04e0-180">**D3DXSHEvalDirectionalLight**</span></span>](d3dxshevaldirectionallight.md) | <span data-ttu-id="e04e0-181">Arrondit une lumière directionnelle conventionnelle.</span><span class="sxs-lookup"><span data-stu-id="e04e0-181">Approximates a conventional directional light.</span></span>                                                              |
    | [<span data-ttu-id="e04e0-182">**D3DXSHEvalSphericalLight**</span><span class="sxs-lookup"><span data-stu-id="e04e0-182">**D3DXSHEvalSphericalLight**</span></span>](d3dxshevalsphericallight.md)     | <span data-ttu-id="e04e0-183">Approximation des sources de lumière sphérique locales.</span><span class="sxs-lookup"><span data-stu-id="e04e0-183">Approximates local spherical light sources.</span></span> <span data-ttu-id="e04e0-184">(Notez que PRT fonctionne uniquement avec les environnements d’éclairage à distance.)</span><span class="sxs-lookup"><span data-stu-id="e04e0-184">(Note that PRT only works with distance lighting environments.)</span></span> |
    | [<span data-ttu-id="e04e0-185">**D3DXSHEvalConeLight**</span><span class="sxs-lookup"><span data-stu-id="e04e0-185">**D3DXSHEvalConeLight**</span></span>](d3dxshevalconelight.md)               | <span data-ttu-id="e04e0-186">Se rapproche d’une source de lumière de zone éloignée.</span><span class="sxs-lookup"><span data-stu-id="e04e0-186">Approximates a distant area light source.</span></span> <span data-ttu-id="e04e0-187">Un exemple est le soleil (très petit angle de cône).</span><span class="sxs-lookup"><span data-stu-id="e04e0-187">An example would be the sun (very small cone angle).</span></span>              |
    | [<span data-ttu-id="e04e0-188">**D3DXSHEvalHemisphereLight**</span><span class="sxs-lookup"><span data-stu-id="e04e0-188">**D3DXSHEvalHemisphereLight**</span></span>](d3dxshevalhemispherelight.md)   | <span data-ttu-id="e04e0-189">Évalue une lumière qui est une interpolation linéaire entre deux couleurs (une sur chaque pôle d’une sphère).</span><span class="sxs-lookup"><span data-stu-id="e04e0-189">Evaluates a light that is a linear interpolation between two colors (one on each pole of a sphere).</span></span>         |

    

     

3.  <span data-ttu-id="e04e0-190">Calculez le luminance de sortie.</span><span class="sxs-lookup"><span data-stu-id="e04e0-190">Compute the exit radiance.</span></span>

    <span data-ttu-id="e04e0-191">L’équation 1 doit maintenant être évaluée à chaque point à l’aide d’un nuanceur de sommets ou de pixels.</span><span class="sxs-lookup"><span data-stu-id="e04e0-191">Equation 1 now has to be evaluated at every point using either a vertex or pixel shader.</span></span> <span data-ttu-id="e04e0-192">Avant de pouvoir évaluer le nuanceur, les constantes doivent être précalculées et chargées dans la table constante (pour plus d’informations, consultez l' [exemple de démonstration PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) ).</span><span class="sxs-lookup"><span data-stu-id="e04e0-192">Before the shader can be evaluated, constants have to be precomputed and loaded into the constant table (see the [PRT Demo Sample](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) for details).</span></span> <span data-ttu-id="e04e0-193">Le nuanceur lui-même est une implémentation simple de cette équation.</span><span class="sxs-lookup"><span data-stu-id="e04e0-193">The shader itself is a straightforward implementation of this equation.</span></span>

    ```
    struct VS_OUTPUT
    {
        float4 Position   : POSITION;   // vertex position 
        float2 TextureUV  : TEXCOORD0;  // vertex texture coordinates 
        float4 Diffuse    : COLOR0;     // vertex diffuse color
    };

    VS_OUTPUT Output;   
    Output.Position = mul(vPos, mWorldViewProjection);

    float4 vExitR = float4(0,0,0,0);
    float4 vExitG = float4(0,0,0,0);
    float4 vExitB = float4(0,0,0,0);
        
    for (int i=0; i < (NUM_PCA_VECTORS/4); i++) 
    {
       vExitR += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*0];
       vExitG += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*1];
       vExitB += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*2];
    }
       
    float4 vExitRadiance = vClusteredPCA[iClusterOffset];
    vExitRadiance.r += dot(vExitR,1);
    vExitRadiance.g += dot(vExitG,1);
    vExitRadiance.b += dot(vExitB,1);

    Output.Diffuse = vExitRadiance;
    ```

    

## <a name="references"></a><span data-ttu-id="e04e0-194">Références</span><span class="sxs-lookup"><span data-stu-id="e04e0-194">References</span></span>

<span data-ttu-id="e04e0-195">Pour plus d’informations sur les harmoniques PRT et sphériques, consultez les documents suivants :</span><span class="sxs-lookup"><span data-stu-id="e04e0-195">For more information about PRT and spherical harmonics, see the following papers:</span></span>


```
Precomputed Radiance Transfer for Real-Time Rendering in Dynamic, 
Low-Frequency Lighting Environments 
P.-P. Sloan, J. Kautz, J. Snyder
SIGGRAPH 2002 

Clustered Principal Components for Precomputed Radiance Transfer 
P.-P. Sloan, J. Hall, J. Hart, J. Snyder 
SIGGRAPH 2003 

Efficient Evaluation of Irradiance Environment Maps 
P.-P. Sloan 
ShaderX 2,  W. Engel 

Spherical Harmonic Lighting: The Gritty Details 
R. Green 
GDC 2003 

An Efficient Representation for Irradiance Environment Maps 
R. Ramamoorthi, P. Hanrahan 

A Practical Model for Subsurface Light Transport 
H. W. Jensen, S. R. Marschner, M. Levoy, and P. Hanrahan 
SIGGRAPH 2001 

Bi-Scale Radiance Transfer 
P.-P. Sloan, X. Liu, H.-Y. Shum, J. Snyder
SIGGRAPH 2003 

Fast, Arbitrary BRDF Shading for Low-Frequency Lighting Using Spherical 
Harmonics 
J. Kautz, P.-P. Sloan, J. Snyder
12th Eurographics Workshop on Rendering 

Precomputing Interactive Dynamic Deformable Scenes 
D. James, K. Fatahalian 
SIGGRAPH 2003 

All-Frequency Shadows Using Non-linear Wavelet Lighting Approximation 
R. Ng, R. Ramamoorth, P. Hanrahan 
SIGGRAPH 2003 

Matrix Radiance Transfer 
J. Lehtinen, J. Kautz
SIGGRAPH 2003 

Math World 
E. W. Weisstein, Wolfram Research, Inc. 

Quantum Theory of Angular Momentum 
D. A. Varshalovich, A.N. Moskalev, V.K. Khersonskii 
```



## <a name="related-topics"></a><span data-ttu-id="e04e0-196">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e04e0-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e04e0-197">Rubriques avancées</span><span class="sxs-lookup"><span data-stu-id="e04e0-197">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="e04e0-198">Équations PRT (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e04e0-198">PRT Equations (Direct3D 9)</span></span>](prt-equations.md)
</dt> <dt>

[<span data-ttu-id="e04e0-199">Représentation de PRT avec des textures (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e04e0-199">Representing PRT With Textures (Direct3D 9)</span></span>](representing-prt-with-textures.md)
</dt> <dt>

[<span data-ttu-id="e04e0-200">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="e04e0-200">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="e04e0-201">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="e04e0-201">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="e04e0-202">**ID3DXPRTEngine**</span><span class="sxs-lookup"><span data-stu-id="e04e0-202">**ID3DXPRTEngine**</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="e04e0-203">**ID3DXTextureGutterHelper**</span><span class="sxs-lookup"><span data-stu-id="e04e0-203">**ID3DXTextureGutterHelper**</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="e04e0-204">Fonctions de transfert luminance précalculées</span><span class="sxs-lookup"><span data-stu-id="e04e0-204">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="e04e0-205">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="e04e0-205">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



