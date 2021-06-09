---
description: De nombreuses techniques de rendu et de génération de contenu requièrent une carte unique et sans chevauchement d’un signal 2D (par exemple, une texture) sur une maille.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Utilisation de UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8faeaa0a416f6f062c81c4101ff47d5222ca75d
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826327"
---
# <a name="using-uvatlas-direct3d-9"></a><span data-ttu-id="fa07f-103">Utilisation de UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fa07f-103">Using UVAtlas (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="fa07f-104">UVAtlas a été livré à l’origine dans la bibliothèque utilty D3DX9 maintenant dépréciée.</span><span class="sxs-lookup"><span data-stu-id="fa07f-104">UVAtlas was originally shipped in the now-deprecated D3DX9 utilty library.</span></span> <span data-ttu-id="fa07f-105">La dernière version est disponible à l’adresse [UV Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas).</span><span class="sxs-lookup"><span data-stu-id="fa07f-105">The latest version is available at [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas).</span></span>

<span data-ttu-id="fa07f-106">De nombreuses techniques de rendu et de génération de contenu requièrent une carte unique et sans chevauchement d’un signal 2D (par exemple, une texture) sur une maille.</span><span class="sxs-lookup"><span data-stu-id="fa07f-106">Many rendering and content generation techniques require a unique, non-overlapping map of a 2D signal (such as a texture) onto a mesh.</span></span> <span data-ttu-id="fa07f-107">Ces techniques sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa07f-107">Such techniques include:</span></span>

-   <span data-ttu-id="fa07f-108">Mappage normal/de déplacement</span><span class="sxs-lookup"><span data-stu-id="fa07f-108">Normal/displacement mapping</span></span>
-   <span data-ttu-id="fa07f-109">Simulations d’espace de textures PRT et cartes de lumière</span><span class="sxs-lookup"><span data-stu-id="fa07f-109">Texture-space PRT simulations and light maps</span></span>
-   <span data-ttu-id="fa07f-110">Peinture de surface</span><span class="sxs-lookup"><span data-stu-id="fa07f-110">Surface painting</span></span>
-   <span data-ttu-id="fa07f-111">Éclairage de l’espace de texture</span><span class="sxs-lookup"><span data-stu-id="fa07f-111">Texture-space lighting</span></span>

<span data-ttu-id="fa07f-112">La génération manuelle d’un mappage UV unique est souvent longue et fastidieuse. Cela est particulièrement vrai lorsque la géométrie d’entrée est complexe et efficace/à faible distorsion-l’utilisation de l’espace est souhaitée.</span><span class="sxs-lookup"><span data-stu-id="fa07f-112">Generating a unique UV mapping manually is often time-consuming and tedious; this is especially true when the input geometry is complex and efficient/low-distortion texture-space utilization is desired.</span></span> <span data-ttu-id="fa07f-113">L’illustration suivante montre un exemple de maillage et son Atlas de texture correspondant.</span><span class="sxs-lookup"><span data-stu-id="fa07f-113">The following illustration shows an example mesh and its corresponding texture atlas.</span></span>

![Affiche un exemple de maillage et son Atlas de texture correspondant.](images/uvatlas1.jpg)

<span data-ttu-id="fa07f-115">Cet exemple montre un maillage (à gauche) et la carte normale d’espace UV correspondante (à droite).</span><span class="sxs-lookup"><span data-stu-id="fa07f-115">This example shows a mesh (on the left) and the corresponding UV-space normal map (on the right).</span></span> <span data-ttu-id="fa07f-116">Notez que l’Atlas de textures contient plusieurs groupes ou clusters de données ; chaque cluster est appelé un graphique et, dans l’exemple ci-dessus, l’affichage contient les données normales d’une partie de la maille.</span><span class="sxs-lookup"><span data-stu-id="fa07f-116">Notice that the texture atlas contains several groups or clusters of data; each cluster is called a chart and in the example above, displays contains the normal data for a portion of the mesh.</span></span>

<span data-ttu-id="fa07f-117">Les API D3DX UVAtlas génèrent automatiquement un Atlas de texture optimal et sans chevauchement.</span><span class="sxs-lookup"><span data-stu-id="fa07f-117">The D3DX UVAtlas APIs automatically generate an optimal, non-overlapping texture atlas.</span></span> <span data-ttu-id="fa07f-118">Les API fournissent des paramètres d’entrée qui vous permettent d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa07f-118">The APIs provide input parameters that allow you to:</span></span>

-   <span data-ttu-id="fa07f-119">Réduire l’étirement, la distorsion et le sous-échantillonnage de texture.</span><span class="sxs-lookup"><span data-stu-id="fa07f-119">Minimize texture stretch, distortion, and undersampling.</span></span>
-   <span data-ttu-id="fa07f-120">Agrandissez la densité de compression de l’espace de texture pour une utilisation efficace de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="fa07f-120">Maximize texture-space packing density for efficient use of memory.</span></span>
-   <span data-ttu-id="fa07f-121">Fournissez un échantillonnage pair sur la maille, en minimisant les discontinuités de la fréquence d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="fa07f-121">Provide an even sampling across the mesh, minimizing discontinuities in sampling frequency.</span></span>

## <a name="how-uvatlas-works"></a><span data-ttu-id="fa07f-122">Fonctionnement de UVAtlas</span><span class="sxs-lookup"><span data-stu-id="fa07f-122">How UVAtlas Works</span></span>

<span data-ttu-id="fa07f-123">Les API UVAtlas (voir [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md)) génèrent un Atlas de texture en partitionnant une surface en graphiques et en compaquetant les graphiques dans un Atlas de texture.</span><span class="sxs-lookup"><span data-stu-id="fa07f-123">The UVAtlas APIs (see [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generate a texture atlas by partitioning a surface into charts and packing the charts into a texture atlas.</span></span> <span data-ttu-id="fa07f-124">Utilisez [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) et [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) pour effectuer ces étapes séparément. ou utilisez [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) pour partitionner, paramétrer et compresser en un seul appel.</span><span class="sxs-lookup"><span data-stu-id="fa07f-124">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) and [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) to perform these steps separately; or use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) to partition, parameterize and pack in a single call.</span></span>

-   [<span data-ttu-id="fa07f-125">Partitionnement et paramétrage d’une maille</span><span class="sxs-lookup"><span data-stu-id="fa07f-125">Partitioning and Parameterizing a Mesh</span></span>](#partitioning-and-parameterizing-a-mesh)
-   [<span data-ttu-id="fa07f-126">Utilisation de dizaines de mesures intégrés pour contrôler le paramétrage</span><span class="sxs-lookup"><span data-stu-id="fa07f-126">Using Integrated Metric Tensors to Control Parameterization</span></span>](#using-integrated-metric-tensors-to-control-parameterization)
-   [<span data-ttu-id="fa07f-127">Utilisation des données d’adjacence pour les froissures spécifiés par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="fa07f-127">Using Adjacency Data for User Specified Creases</span></span>](#using-adjacency-data-for-user-specified-creases)
-   [<span data-ttu-id="fa07f-128">Empaqueter des graphiques dans un Atlas</span><span class="sxs-lookup"><span data-stu-id="fa07f-128">Packing Charts Into an Atlas</span></span>](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a><span data-ttu-id="fa07f-129">Partitionnement et paramétrage d’une maille</span><span class="sxs-lookup"><span data-stu-id="fa07f-129">Partitioning and Parameterizing a Mesh</span></span>

<span data-ttu-id="fa07f-130">Tout d’abord, le maillage est partitionné en graphiques, puis chaque graphique est paramétré dans son propre \[ \] espace UV.</span><span class="sxs-lookup"><span data-stu-id="fa07f-130">First, the mesh is partitioned into charts, then each chart is parameterized into its own \[0,1\] UV-space.</span></span> <span data-ttu-id="fa07f-131">Un cylindre peut être paramétré par un graphique ; en revanche, une sphère nécessitera deux graphiques, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="fa07f-131">A cylinder can be parameterized by one chart; a sphere on the other hand will require two charts, as shown in the following illustration.</span></span>

![illustration d’une sphère partitionnée en deux graphiques](images/uvatlas3.jpg)

<span data-ttu-id="fa07f-133">Une maille qui peut être paramétrée avec un seul graphique est classée en tant que « homeomorphic sur un disque », ce qui signifie que vous pouvez répartir un disque flexible et extensible à l’infini sur le graphique et couvrir parfaitement la géométrie.</span><span class="sxs-lookup"><span data-stu-id="fa07f-133">A mesh which can be parameterized with a single chart is classified as "homeomorphic to a disk", meaning you could spread out an infinitely flexible, infinitely stretchable disk over the chart and cover the geometry perfectly.</span></span> <span data-ttu-id="fa07f-134">Cet étirement, appelé homeomorphism, est une fonction bidirectionnelle. Cela signifie que vous pouvez passer d’un paramétrage à l’autre sans perdre d’informations.</span><span class="sxs-lookup"><span data-stu-id="fa07f-134">This stretching, called a homeomorphism, is a bidirectional function; which means you can go from one parameterization to the other without losing information.</span></span>

<span data-ttu-id="fa07f-135">Très peu de maillages réels peuvent être paramétrés en deux dimensions sans les séparer en clusters ou en graphiques.</span><span class="sxs-lookup"><span data-stu-id="fa07f-135">Very few real-world meshes can be parameterized into two dimensions without separating the mesh into clusters, or charts.</span></span> <span data-ttu-id="fa07f-136">L’illustration suivante montre un autre exemple de maillage et son Atlas de textures correspondant.</span><span class="sxs-lookup"><span data-stu-id="fa07f-136">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Montre un exemple de maillage avec différentes formes et l’Atlas de texture correspondant.](images/uvatlas2.jpg)

<span data-ttu-id="fa07f-138">Il existe deux paramètres qui déterminent le nombre de graphiques créés :</span><span class="sxs-lookup"><span data-stu-id="fa07f-138">There are two parameters that determine the number of charts created:</span></span>

-   <span data-ttu-id="fa07f-139">Nombre maximal de graphiques autorisés pour l’Atlas</span><span class="sxs-lookup"><span data-stu-id="fa07f-139">The maximum number of charts allowed for the atlas</span></span>
-   <span data-ttu-id="fa07f-140">Quantité maximale d’étirement autorisée pour chaque graphique</span><span class="sxs-lookup"><span data-stu-id="fa07f-140">The maximum amount of stretch allowed for each chart</span></span>

<span data-ttu-id="fa07f-141">La quantité d’étirement détermine le nombre de graphiques qui sont générés et la qualité globale de l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="fa07f-141">The amount of stretch will determine the number of charts that are generated, and the overall quality of the sampling.</span></span> <span data-ttu-id="fa07f-142">Les étendues Stretch sont comprises entre 0,0 (sans Stretch) et 1,0 (n’importe quelle quantité d’étirement).</span><span class="sxs-lookup"><span data-stu-id="fa07f-142">Stretch ranges from 0.0 (no stretch) to 1.0 (any amount of stretch).</span></span> <span data-ttu-id="fa07f-143">D3DXUVAtlasCreate et D3DXUVAtlasPartition retournent l’Stretch maximal généré par l’algorithme.</span><span class="sxs-lookup"><span data-stu-id="fa07f-143">D3DXUVAtlasCreate and D3DXUVAtlasPartition return the maximum stretch generated by the algorithm.</span></span> <span data-ttu-id="fa07f-144">L’illustration suivante montre un autre exemple de maillage et son Atlas de textures correspondant.</span><span class="sxs-lookup"><span data-stu-id="fa07f-144">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![illustration d’un exemple de maillage et de l’Atlas de texture correspondant](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a><span data-ttu-id="fa07f-146">Utilisation de dizaines de mesures intégrés pour contrôler le paramétrage</span><span class="sxs-lookup"><span data-stu-id="fa07f-146">Using Integrated Metric Tensors to Control Parameterization</span></span>

<span data-ttu-id="fa07f-147">La hiérarchisation de l’espace de texture peut être spécifiée pour chaque triangle.</span><span class="sxs-lookup"><span data-stu-id="fa07f-147">Texture-space prioritization can be specified on a per-triangle basis.</span></span> <span data-ttu-id="fa07f-148">Des dizaines de métriques intégrés peuvent être fournis pour contrôler la façon dont les triangles sont étirés dans l’Atlas d’espace de texture qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="fa07f-148">Integrated Metric Tensors can be provided to control how triangles are stretched in the resulting texture-space atlas.</span></span> <span data-ttu-id="fa07f-149">Les IMT peuvent être spécifiés directement ou calculés en fonction d’un signal d’entrée à l’aide des fonctions de calcul D3DX IMT.</span><span class="sxs-lookup"><span data-stu-id="fa07f-149">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions.</span></span> <span data-ttu-id="fa07f-150">Une métrique intégrée tenseur (ou IMT) est une matrice 2x2 2x2 qui décrit comment un triangle est étiré dans l’Atlas.</span><span class="sxs-lookup"><span data-stu-id="fa07f-150">An integrated metric tensor (or IMT) is a symmetrical 2x2 matrix that describes how a triangle is stretched in the atlas.</span></span> <span data-ttu-id="fa07f-151">Chaque IMT est défini par 3 valeurs float, appelées (a, b, c).</span><span class="sxs-lookup"><span data-stu-id="fa07f-151">Each IMT is defined by 3 floats, call them (a,b,c).</span></span> <span data-ttu-id="fa07f-152">Elles peuvent être réorganisées dans une matrice 2x2 symétrique comme suit :</span><span class="sxs-lookup"><span data-stu-id="fa07f-152">They can be arranged in a symmetric 2x2 matrix like this:</span></span>


```
a b
b c
```



<span data-ttu-id="fa07f-153">Le IMT peut ensuite être utilisé pour déterminer la distance entre deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="fa07f-153">Then the IMT can be used to find the distance between two vectors.</span></span> <span data-ttu-id="fa07f-154">À partir de deux vecteurs v1 et v2, où :</span><span class="sxs-lookup"><span data-stu-id="fa07f-154">Given two vectors v1 and v2, where :</span></span>


```
vector v1
vector v2 = v1 + (s,t)
```



<span data-ttu-id="fa07f-155">La distance entre v1 et V2 peut être calculée comme suit :</span><span class="sxs-lookup"><span data-stu-id="fa07f-155">The distance between v1 and v2 can be calculated as:</span></span>


```
sqrt((s, t) * M * (s, t)^T)
```



<span data-ttu-id="fa07f-156">En d’autres termes, le vecteur (s, t) peut être la grandeur de l’étirement dans une direction arbitraire dans l’espace u-v.</span><span class="sxs-lookup"><span data-stu-id="fa07f-156">In other words, the vector (s,t) could be the magnitude of the stretch in an arbitrary direction in u-v space.</span></span> <span data-ttu-id="fa07f-157">Dans ce cas, le vecteur s est une direction entre le premier et le deuxième vertex, et t est le produit croisé de la normale et du s.</span><span class="sxs-lookup"><span data-stu-id="fa07f-157">In this case, the s vector is a direction from the first to the second vertex, and t is the cross product of the normal and s.</span></span> <span data-ttu-id="fa07f-158">Exemple :</span><span class="sxs-lookup"><span data-stu-id="fa07f-158">For instance:</span></span>


```
(1,1) * (1,1) = (2,2)
        (1,1)
IMT(1,1,1) scales by 2
```




```
(1,-1) * (1,1) = (0,0)
         (1,1)
IMT(2,0,2) scales by 2 with no shearing
```



<span data-ttu-id="fa07f-159">Les IMT peuvent être spécifiés directement ou calculés en fonction d’un signal d’entrée à l’aide des fonctions de calcul D3DX IMT : D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal et D3DXComputeIMTFromTexture \_ Graphics.</span><span class="sxs-lookup"><span data-stu-id="fa07f-159">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal, and D3DXComputeIMTFromTexture\_graphics.</span></span>

<span data-ttu-id="fa07f-160">Spécifiez les données IMT directement si vous souhaitez contrôler la façon dont l’espace de texture est alloué à des triangles individuels.</span><span class="sxs-lookup"><span data-stu-id="fa07f-160">Specify IMT data directly if you want to control how texture-space is allocated to individual triangles.</span></span> <span data-ttu-id="fa07f-161">En procédant ainsi, allouez plus d’espace dans l’Atlas à des zones importantes d’une maille (comme le visage d’un personnage ou le logo du coffre, ou les régions d’une scène près du parcours de marche d’un joueur).</span><span class="sxs-lookup"><span data-stu-id="fa07f-161">By doing so, allocate more area in the atlas to important areas of a mesh (such as a character's face or chest logo, or regions of a scene near a player's walking-path).</span></span> <span data-ttu-id="fa07f-162">En spécifiant des IMT qui sont des multiples de la matrice d’identité, les triangles résultants sont mis à l’échelle uniformément dans l’espace de texture.</span><span class="sxs-lookup"><span data-stu-id="fa07f-162">By specifying IMT's that are multiples of the identity matrix, the resulting triangles will be scaled uniformly in texture space.</span></span>

<span data-ttu-id="fa07f-163">Par exemple, à partir d’une carte normale haute résolution, vous pouvez calculer IMT pour fournir plus d’espace de texture aux zones de signal de fréquence supérieure dans la carte normale.</span><span class="sxs-lookup"><span data-stu-id="fa07f-163">For example, given a high-resolution normal map, you can compute IMT to provide more texture-space to areas of higher frequency signal in the normal map.</span></span> <span data-ttu-id="fa07f-164">Les triangles qui sont « plats » (qui sont mappés à des régions constantes de la carte normale d’origine) recevront moins d’espace de texture.</span><span class="sxs-lookup"><span data-stu-id="fa07f-164">Triangles that are "flat" (that mapped to constant regions of the original normal map) will receive less texture space.</span></span> <span data-ttu-id="fa07f-165">Les triangles qui contiennent un grand nombre de détails de la carte normale reçoivent plus de zone de texture dans le résultat final.</span><span class="sxs-lookup"><span data-stu-id="fa07f-165">Triangles that contain a great deal of normal-map detail will receive more texture area in the final result.</span></span> <span data-ttu-id="fa07f-166">Vous pouvez ensuite rééchantillonner la carte normale en une texture plus petite tout en conservant les détails, ou vous pouvez recalculer la carte normale avec le mappage UV optimal.</span><span class="sxs-lookup"><span data-stu-id="fa07f-166">You can then resample the normal map into a smaller texture but maintain detail, or you can recompute the normal map with the more optimal UV mapping.</span></span>

### <a name="using-adjacency-data-for-user-specified-creases"></a><span data-ttu-id="fa07f-167">Utilisation des données d’adjacence pour les froissures spécifiés par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="fa07f-167">Using Adjacency Data for User Specified Creases</span></span>

<span data-ttu-id="fa07f-168">Les informations d’adjacence définies par l’utilisateur peuvent être fournies à la fonction de partitionnement pour décrire des froissures prédéfinis dans la maille, et ainsi définir une limite de graphique entre des visages adjacents.</span><span class="sxs-lookup"><span data-stu-id="fa07f-168">User-defined adjacency information can be provided to the partitioning function to describe pre-defined creases in the mesh, and thus define a chart boundary between adjacent faces.</span></span> <span data-ttu-id="fa07f-169">C’est un moyen simple pour l’appelant de spécifier son propre partitionnement de graphique comme entrée dans l’algorithme, ce qui permet d’affiner davantage les graphiques pour que l’étirement soit inférieur au maximum autorisé.</span><span class="sxs-lookup"><span data-stu-id="fa07f-169">This is a simple way for the caller to specify their own chart partitioning as input into the algorithm, which will further refine charts to bring the stretch under the maximum allowed.</span></span>

### <a name="example"></a><span data-ttu-id="fa07f-170">Exemple</span><span class="sxs-lookup"><span data-stu-id="fa07f-170">Example</span></span>

<span data-ttu-id="fa07f-171">Cet exemple montre comment vous pouvez utiliser les API UVAtlas et la visionneuse DirectX (Dxviewer.exe) pour rechercher et corriger les discontinuités dans votre modèle qui peuvent affecter considérablement la taille de votre Atlas de texture.</span><span class="sxs-lookup"><span data-stu-id="fa07f-171">This example illustrates how you might use the UVAtlas APIs and the DirectX Viewer (Dxviewer.exe) to find and fix discontinuities in your model that can dramatically affect the size of your texture atlas.</span></span> <span data-ttu-id="fa07f-172">Vous pouvez obtenir Dxviewer.exe et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="fa07f-172">You can get Dxviewer.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="fa07f-173">Dxviewer.exe a été supprimé du kit de développement logiciel (SDK) DirectX après la version du 2009 août afin de l’afficher, vous aurez besoin d’au moins le kit de développement logiciel (SDK) DirectX du 2009 août.</span><span class="sxs-lookup"><span data-stu-id="fa07f-173">Dxviewer.exe was removed from the DirectX SDK after the August 2009 version so to get it you'll need at least the August 2009 DirectX SDK.</span></span> <span data-ttu-id="fa07f-174">Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="fa07f-174">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="fa07f-175">Supposons que vous avez commencé avec un modèle dans votre logiciel de génération de contenu préféré (cet exemple utilise un modèle de tête de nain créé dans Maya).</span><span class="sxs-lookup"><span data-stu-id="fa07f-175">Assume you started with some model in your favorite content generation software (this example uses a dwarf head model that was created in Maya).</span></span> <span data-ttu-id="fa07f-176">Exportez le modèle texturé dans un fichier. x et créez un Atlas de texture avec D3DXUVAtlasCreate.</span><span class="sxs-lookup"><span data-stu-id="fa07f-176">Export the textured model to an .x file and create a texture atlas with D3DXUVAtlasCreate.</span></span> <span data-ttu-id="fa07f-177">L’Atlas de texture qui en résulte ressemble à l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="fa07f-177">The resulting texture atlas would look something like the following illustration.</span></span>

![illustration d’un modèle d’Atlas pour un nain](images/uvatlas5.jpg)

<span data-ttu-id="fa07f-179">L’Atlas a 22 graphiques et une extension maximale de 0,994.</span><span class="sxs-lookup"><span data-stu-id="fa07f-179">The atlas has 22 charts and a maximum stretch of 0.994.</span></span>

<span data-ttu-id="fa07f-180">Examinez maintenant le modèle texturé pour voir comment l’Atlas de texture est mappé à la géométrie.</span><span class="sxs-lookup"><span data-stu-id="fa07f-180">Now look at the textured model to see how well the texture atlas maps to the geometry.</span></span> <span data-ttu-id="fa07f-181">Pour ce faire, chargez le modèle dans l’outil visionneuse :</span><span class="sxs-lookup"><span data-stu-id="fa07f-181">To do this, load the model into the viewer tool:</span></span>

-   <span data-ttu-id="fa07f-182">Ouvrez l’outil visionneuse à partir des utilitaires DirectX.</span><span class="sxs-lookup"><span data-stu-id="fa07f-182">Open the viewer tool from the DirectX Utilities.</span></span>
-   <span data-ttu-id="fa07f-183">Chargez le fichier. x en cliquant sur le bouton Ouvrir.</span><span class="sxs-lookup"><span data-stu-id="fa07f-183">Load the .x file by clicking the Open button.</span></span>
-   <span data-ttu-id="fa07f-184">Activation de l’option d’affichage froissures en cliquant sur le bouton afficher et en sélectionnant froissures dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fa07f-184">Enabling the crease viewing option by clicking the view button and selecting Creases from popup.</span></span>

<span data-ttu-id="fa07f-185">L’illustration suivante montre ce que vous devez voir dans l’outil visionneuse.</span><span class="sxs-lookup"><span data-stu-id="fa07f-185">The following illustration shows what you should see in the viewer tool.</span></span>

![illustration d’une maille texturée dans l’outil visionneuse](images/uvatlas6c.jpg)

<span data-ttu-id="fa07f-187">Chaque ligne est un pli qui est un bord adjacent entre deux graphiques dans l’Atlas de textures.</span><span class="sxs-lookup"><span data-stu-id="fa07f-187">Each line is a crease which is an adjacent edge between two charts in the texture atlas.</span></span> <span data-ttu-id="fa07f-188">Le nombre de graphiques générés par l’algorithme est dû à de légères différences, peut-être en raison de discontinuités dans les normales.</span><span class="sxs-lookup"><span data-stu-id="fa07f-188">The number of charts generated by the algorithm is caused by slight differences perhaps due to discontinuities in the normals.</span></span> <span data-ttu-id="fa07f-189">Ces petites différences peuvent être réduites en soudant des données, c’est-à-dire en forçant les données qui sont pratiquement égales à.</span><span class="sxs-lookup"><span data-stu-id="fa07f-189">These small differences can be reduced by welding data, that is, forcing data that is nearly equal to be equal.</span></span> <span data-ttu-id="fa07f-190">Pour souder les normales et les skinweights :</span><span class="sxs-lookup"><span data-stu-id="fa07f-190">To weld the normals and the skinweights:</span></span>

-   <span data-ttu-id="fa07f-191">Exécutez l’outil DirectX OPS (dxops.exe) avec la ligne de commande suivante sur la maille (en remplaçant « modelName. x » par le nom de votre modèle) :</span><span class="sxs-lookup"><span data-stu-id="fa07f-191">Run the DirectX Ops (dxops.exe) tool with the following command line on the mesh (replacing 'modelName.x' with the name of your model):</span></span>
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

<span data-ttu-id="fa07f-192">Cela permet de comparer les normales et les skinweights, et où ils diffèrent de la valeur par moins de 2,01, les données sont égales.</span><span class="sxs-lookup"><span data-stu-id="fa07f-192">This compares the normals and skinweights, and where they differ in value by less than 2.01, the data is made equal.</span></span> <span data-ttu-id="fa07f-193">Les illustrations suivantes montrent un maximum d’œil pour voir les froissures avant le soudage (à gauche) et les froissures après soudure (à droite) :</span><span class="sxs-lookup"><span data-stu-id="fa07f-193">The following illustrations shows a close up of the eye to see the creases before welding (on the left) and the creases after welding (on the right):</span></span>

![illustration des froissures avant le soudage](images/uvatlas6a.jpg)![illustration des froissures après soudure](images/uvatlas6b.jpg)

<span data-ttu-id="fa07f-196">Figure 7 : suppression des froissures par soudure</span><span class="sxs-lookup"><span data-stu-id="fa07f-196">Figure 7: Removing creases by welding</span></span>

<span data-ttu-id="fa07f-197">Dans cet exemple, la soudure a retiré 86 sommets du maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="fa07f-197">In this example, welding removed 86 vertices from the input mesh.</span></span> <span data-ttu-id="fa07f-198">Avec moins de froissures dans la maille, vous pouvez régénérer l’Atlas, comme le montre l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="fa07f-198">With fewer creases in the mesh, you can regenerate the atlas, as the following illustration shows.</span></span>

![illustration du nouvel Atlas avec les froissures supprimés](images/uvatlas8.jpg)

<span data-ttu-id="fa07f-200">L’Atlas n’a que 7 graphiques et une valeur maximale de 0,0776 environ.</span><span class="sxs-lookup"><span data-stu-id="fa07f-200">The atlas only has 7 charts and a maximum stretch of approximately 0.0776.</span></span> <span data-ttu-id="fa07f-201">Le nouvel Atlas s’intègre désormais à une texture plus petite (environ 30% de plus petite taille dans cet exemple).</span><span class="sxs-lookup"><span data-stu-id="fa07f-201">The new atlas now fits into a smaller texture (approximately 30% smaller in this example).</span></span>

### <a name="packing-charts-into-an-atlas"></a><span data-ttu-id="fa07f-202">Empaqueter des graphiques dans un Atlas</span><span class="sxs-lookup"><span data-stu-id="fa07f-202">Packing Charts Into an Atlas</span></span>

<span data-ttu-id="fa07f-203">Une fois qu’un maillage a été partitionné en graphiques paramétrés individuellement, les graphiques doivent être compactés efficacement dans une seule carte de texture.</span><span class="sxs-lookup"><span data-stu-id="fa07f-203">Once a mesh has been partitioned into individually-parameterized charts, the charts need to be packed efficiently into a single texture map.</span></span> <span data-ttu-id="fa07f-204">Il s’agit de la deuxième étape de D3DXUVAtlasCreate ou peut être appelée explicitement en appelant D3DXUVAtlasPack.</span><span class="sxs-lookup"><span data-stu-id="fa07f-204">This is performed as the second step of D3DXUVAtlasCreate or can be invoked explicitly by calling D3DXUVAtlasPack.</span></span>

<span data-ttu-id="fa07f-205">Les graphiques compactés sont séparés par une largeur de reliure spécifiée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fa07f-205">Packed charts are separated by a user-specified gutter width.</span></span> <span data-ttu-id="fa07f-206">La largeur de la reliure correspond à la quantité de séparation entre les graphiques et permet l’interpolation bilinéaire et le mappage MIP pour éviter le rendu des artefacts aux limites du graphique.</span><span class="sxs-lookup"><span data-stu-id="fa07f-206">The gutter width is the amount of separation between charts, and allows for bilinear interpolation and mip-mapping to avoid rendering artifacts at chart boundaries.</span></span> <span data-ttu-id="fa07f-207">D3DX fournit une interface pour remplir automatiquement ces gouttières. pour plus d’informations, consultez [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="fa07f-207">D3DX provides an interface for automatically filling in these gutters - see [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) for more information.</span></span>

## <a name="integrating-uvatlas-into-your-pipeline"></a><span data-ttu-id="fa07f-208">Intégration de UVAtlas dans votre pipeline</span><span class="sxs-lookup"><span data-stu-id="fa07f-208">Integrating UVAtlas Into Your Pipeline</span></span>

<span data-ttu-id="fa07f-209">En plus d’être appelé par l’artiste avant la peinture de texture, ces fonctions peuvent être intégrées dans un pipeline d’art automatisé.</span><span class="sxs-lookup"><span data-stu-id="fa07f-209">In addition to being artist-invoked prior to texture painting, these functions can be integrated into an automated art pipeline.</span></span> <span data-ttu-id="fa07f-210">Par exemple, un appel UVAtlas peut être émis automatiquement après la mise à jour d’un élément multimédia, avant d’effectuer une simulation PRT ou un test de mappage normal.</span><span class="sxs-lookup"><span data-stu-id="fa07f-210">For example, a UVAtlas call can be issued automatically after an asset is updated, prior to performing a PRT simulation or normal mapping pass.</span></span> <span data-ttu-id="fa07f-211">Cela évite de devoir réparer manuellement manuellement le mappage UV d’un objet si la topologie du maillage a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="fa07f-211">This avoids any need to manually manual repair of an object's UV mapping if the mesh's topology has been modified.</span></span>

<span data-ttu-id="fa07f-212">Pour obtenir des exemples d’utilisation des fonctions UVAtlas, consultez l' [outil Command-Line de l’Atlas UV (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) .</span><span class="sxs-lookup"><span data-stu-id="fa07f-212">See the [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) for example usage of the UVAtlas functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa07f-213">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa07f-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa07f-214">Rubriques avancées</span><span class="sxs-lookup"><span data-stu-id="fa07f-214">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
