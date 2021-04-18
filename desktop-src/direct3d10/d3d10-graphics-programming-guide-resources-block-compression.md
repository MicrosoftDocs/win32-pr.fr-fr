---
description: La compression de bloc est une technique de compression de texture qui réduit la taille de la texture.
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: Compression par bloc (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fcfb4bc91256415ab23686b7333df7d21df335d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564502"
---
# <a name="block-compression-direct3d-10"></a><span data-ttu-id="ed682-103">Compression par bloc (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ed682-103">Block Compression (Direct3D 10)</span></span>

<span data-ttu-id="ed682-104">La compression de bloc est une technique de compression de texture qui réduit la taille de la texture.</span><span class="sxs-lookup"><span data-stu-id="ed682-104">Block compression is a texture compression technique for reducing texture size.</span></span> <span data-ttu-id="ed682-105">En comparaison avec une texture de 32 bits par couleur, une texture compressée par bloc peut atteindre 75 pour cent de moins.</span><span class="sxs-lookup"><span data-stu-id="ed682-105">When compared to a texture with 32-bits per color, a block-compressed texture can be up to 75 percent smaller.</span></span> <span data-ttu-id="ed682-106">Les applications voient généralement une augmentation des performances lors de l’utilisation de la compression de bloc en raison de l’encombrement mémoire plus faible.</span><span class="sxs-lookup"><span data-stu-id="ed682-106">Applications usually see a performance increase when using block compression because of the smaller memory footprint.</span></span>

<span data-ttu-id="ed682-107">En cas de perte, la compression de bloc fonctionne bien et est recommandée pour toutes les textures qui sont transformées et filtrées par le pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed682-107">While lossy, block compression works well and is recommended for all textures that get transformed and filtered by the pipeline.</span></span> <span data-ttu-id="ed682-108">Les textures directement mappées à l’écran (éléments d’interface utilisateur tels que les icônes et le texte) ne sont pas de bons choix pour la compression, car les artefacts sont plus perceptibles.</span><span class="sxs-lookup"><span data-stu-id="ed682-108">Textures that are directly mapped to the screen (UI elements like icons and text) are not good choices for compression because artifacts are more noticeable.</span></span>

<span data-ttu-id="ed682-109">Une texture compressée par bloc doit être créée en tant que multiple de taille 4 dans toutes les dimensions et ne peut pas être utilisée comme sortie du pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed682-109">A block-compressed texture must be created as a multiple of size 4 in all dimensions and cannot be used as an output of the pipeline.</span></span>

-   [<span data-ttu-id="ed682-110">Fonctionnement de la compression de bloc</span><span class="sxs-lookup"><span data-stu-id="ed682-110">How Does Block Compression Work?</span></span>](#how-does-block-compression-work)
    -   [<span data-ttu-id="ed682-111">Stockage des données non compressées</span><span class="sxs-lookup"><span data-stu-id="ed682-111">Storing Uncompressed Data</span></span>](#storing-uncompressed-data)
    -   [<span data-ttu-id="ed682-112">Stockage des données compressées</span><span class="sxs-lookup"><span data-stu-id="ed682-112">Storing Compressed Data</span></span>](#storing-compressed-data)
-   [<span data-ttu-id="ed682-113">Utilisation de la compression de bloc</span><span class="sxs-lookup"><span data-stu-id="ed682-113">Using Block Compression</span></span>](#using-block-compression)
    -   [<span data-ttu-id="ed682-114">Taille virtuelle et taille physique</span><span class="sxs-lookup"><span data-stu-id="ed682-114">Virtual Size versus Physical Size</span></span>](#virtual-size-versus-physical-size)
-   [<span data-ttu-id="ed682-115">Algorithmes de compression</span><span class="sxs-lookup"><span data-stu-id="ed682-115">Compression Algorithms</span></span>](#compression-algorithms)
    -   [<span data-ttu-id="ed682-116">BC1</span><span class="sxs-lookup"><span data-stu-id="ed682-116">BC1</span></span>](#bc1)
    -   [<span data-ttu-id="ed682-117">BC2</span><span class="sxs-lookup"><span data-stu-id="ed682-117">BC2</span></span>](#bc2)
    -   [<span data-ttu-id="ed682-118">BC3</span><span class="sxs-lookup"><span data-stu-id="ed682-118">BC3</span></span>](#bc3)
    -   [<span data-ttu-id="ed682-119">TEXTURES BC4</span><span class="sxs-lookup"><span data-stu-id="ed682-119">BC4</span></span>](#bc4)
    -   [<span data-ttu-id="ed682-120">BC5</span><span class="sxs-lookup"><span data-stu-id="ed682-120">BC5</span></span>](#bc5)
-   [<span data-ttu-id="ed682-121">Conversion de format à l’aide de Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="ed682-121">Format Conversion Using Direct3D 10.1</span></span>](#format-conversion-using-direct3d-101)
-   [<span data-ttu-id="ed682-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ed682-122">Related topics</span></span>](#related-topics)

## <a name="how-does-block-compression-work"></a><span data-ttu-id="ed682-123">Fonctionnement de la compression de bloc</span><span class="sxs-lookup"><span data-stu-id="ed682-123">How Does Block Compression Work?</span></span>

<span data-ttu-id="ed682-124">La compression par bloc est une technique qui permet de réduire la quantité de mémoire requise pour stocker des données de couleur.</span><span class="sxs-lookup"><span data-stu-id="ed682-124">Block compression is a technique for reducing the amount of memory required to store color data.</span></span> <span data-ttu-id="ed682-125">En stockant des couleurs de leur taille d’origine et d’autres couleurs à l’aide d’un schéma d’encodage, vous pouvez réduire considérablement la quantité de mémoire requise pour stocker l’image.</span><span class="sxs-lookup"><span data-stu-id="ed682-125">By storing some colors in their original size, and other colors using an encoding scheme, you can dramatically reduce the amount of memory required to store the image.</span></span> <span data-ttu-id="ed682-126">Étant donné que le matériel décode automatiquement les données compressées, il n’y a aucune altération des performances pour l’utilisation des textures compressées.</span><span class="sxs-lookup"><span data-stu-id="ed682-126">Since the hardware automatically decodes compressed data, there is no performance penalty for using compressed textures.</span></span>

<span data-ttu-id="ed682-127">Pour voir le fonctionnement de la compression, observez les deux exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="ed682-127">To see how compression works, look at the following two examples.</span></span> <span data-ttu-id="ed682-128">Le premier exemple décrit la quantité de mémoire utilisée pour stocker des données non compressées ; le deuxième exemple décrit la quantité de mémoire utilisée pour stocker des données compressées.</span><span class="sxs-lookup"><span data-stu-id="ed682-128">The first example describes the amount of memory used when storing uncompressed data; the second example describes the amount of memory used when storing compressed data.</span></span>

### <a name="storing-uncompressed-data"></a><span data-ttu-id="ed682-129">Stockage des données non compressées</span><span class="sxs-lookup"><span data-stu-id="ed682-129">Storing Uncompressed Data</span></span>

<span data-ttu-id="ed682-130">L’illustration suivante représente une texture 4 × 4 non compressée.</span><span class="sxs-lookup"><span data-stu-id="ed682-130">The following illustration represents an uncompressed 4×4 texture.</span></span> <span data-ttu-id="ed682-131">Supposons que chaque couleur contient un composant de couleur unique (rouge par exemple) et qu’elle est stockée en un octet de mémoire.</span><span class="sxs-lookup"><span data-stu-id="ed682-131">Assume that each color contains a single color component (red for instance) and is stored in one byte of memory.</span></span>

![illustration d’une texture 4x4 non compressée](images/d3d10-block-compress-1.png)

<span data-ttu-id="ed682-133">Les données non compressées sont disposées en mémoire de façon séquentielle et nécessitent 16 octets, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="ed682-133">The uncompressed data is laid out in memory sequentially and requires 16 bytes, as shown in the following illustration.</span></span>

![illustration de données non compressées en mémoire séquentielle](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a><span data-ttu-id="ed682-135">Stockage des données compressées</span><span class="sxs-lookup"><span data-stu-id="ed682-135">Storing Compressed Data</span></span>

<span data-ttu-id="ed682-136">Maintenant que vous avez vu la quantité de mémoire utilisée par une image non compressée, consultez la quantité de mémoire enregistrée par une image compressée.</span><span class="sxs-lookup"><span data-stu-id="ed682-136">Now that you've seen how much memory an uncompressed image uses, take a look at how much memory a compressed image saves.</span></span> <span data-ttu-id="ed682-137">Le format de compression [BC1](#bc1) stocke 2 couleurs (1 octet chacune) et des index 16 3 bits (48 bits, ou 6 octets) qui sont utilisés pour interpoler les couleurs d’origine dans la texture, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="ed682-137">The [BC1](#bc1) compression format stores 2 colors (1 byte each) and 16 3-bit indices (48 bits, or 6 bytes) that are used to interpolate the original colors in the texture, as shown in the following illustration.</span></span>

![illustration du format de compression BC1](images/d3d10-block-compress-3.png)

<span data-ttu-id="ed682-139">L’espace total requis pour stocker les données compressées est de 8 octets, ce qui représente une économie de mémoire de 50% par rapport à l’exemple non compressé.</span><span class="sxs-lookup"><span data-stu-id="ed682-139">The total space required to store the compressed data is 8 bytes which is a 50-percent memory savings over the uncompressed example.</span></span> <span data-ttu-id="ed682-140">Les économies sont encore plus importantes lorsque plusieurs composants de couleur sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="ed682-140">The savings are even larger when more than one color component is used.</span></span>

<span data-ttu-id="ed682-141">Les économies importantes de mémoire fournies par la compression de bloc peuvent entraîner une augmentation des performances.</span><span class="sxs-lookup"><span data-stu-id="ed682-141">The substantial memory savings provided by block compression can lead to an increase in performance.</span></span> <span data-ttu-id="ed682-142">Cette performance est due au coût de la qualité de l’image (en raison de l’interpolation de couleur). Toutefois, la qualité inférieure n’est souvent pas perceptible.</span><span class="sxs-lookup"><span data-stu-id="ed682-142">This performance comes at the cost of image quality (due to color interpolation); however, the lower quality is often not noticeable.</span></span>

<span data-ttu-id="ed682-143">La section suivante vous montre comment Direct3D 10 vous permet d’utiliser facilement la compression de bloc dans votre application.</span><span class="sxs-lookup"><span data-stu-id="ed682-143">The next section shows you how Direct3D 10 makes it easy for you to use block compression in your application.</span></span>

## <a name="using-block-compression"></a><span data-ttu-id="ed682-144">Utilisation de la compression de bloc</span><span class="sxs-lookup"><span data-stu-id="ed682-144">Using Block Compression</span></span>

<span data-ttu-id="ed682-145">Créez une texture compressée par bloc comme une texture non compressée (consultez [créer une texture à partir d’un fichier](d3d10-graphics-programming-guide-resources-creating-textures.md)), sauf que vous spécifiez un format compressé par bloc.</span><span class="sxs-lookup"><span data-stu-id="ed682-145">Create a block-compressed texture just like an uncompressed texture (see [Create a Texture from a File](d3d10-graphics-programming-guide-resources-creating-textures.md)) except that you specify a block-compressed format.</span></span>


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



<span data-ttu-id="ed682-146">Ensuite, créez une vue pour lier la texture au pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed682-146">Next, create a view to bind the texture to the pipeline.</span></span> <span data-ttu-id="ed682-147">Dans la mesure où une texture compressée par bloc ne peut être utilisée qu’en tant qu’entrée d’une étape de nuanceur, vous souhaitez créer un affichage des ressources de nuanceur en appelant [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="ed682-147">Since a block-compressed texture can be used only as an input to a shader-stage, you want to create a shader-resource view by calling [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>

<span data-ttu-id="ed682-148">Utilisez une texture de bloc compressée de la même façon que vous utilisez une texture non compressée.</span><span class="sxs-lookup"><span data-stu-id="ed682-148">Use a block compressed texture the same way you would use an uncompressed texture.</span></span> <span data-ttu-id="ed682-149">Si votre application obtient un pointeur de mémoire vers des données compressées par bloc, vous devez prendre en compte le remplissage de la mémoire dans un mipmap qui entraîne une différence entre la taille déclarée et la taille réelle.</span><span class="sxs-lookup"><span data-stu-id="ed682-149">If your application will get a memory pointer to block-compressed data, you need to account for the memory padding in a mipmap that causes the declared size to differ from the actual size.</span></span>

### <a name="virtual-size-versus-physical-size"></a><span data-ttu-id="ed682-150">Taille virtuelle et taille physique</span><span class="sxs-lookup"><span data-stu-id="ed682-150">Virtual Size versus Physical Size</span></span>

<span data-ttu-id="ed682-151">Si vous avez un code d’application qui utilise un pointeur de mémoire pour parcourir la mémoire d’une texture de bloc compressée, il y a une considération importante qui peut nécessiter une modification dans le code de votre application.</span><span class="sxs-lookup"><span data-stu-id="ed682-151">If you have application code that uses a memory pointer to walk the memory of a block compressed texture, there is one important consideration that may require a modification in your application code.</span></span> <span data-ttu-id="ed682-152">Une texture compressée par bloc doit être un multiple de 4 dans toutes les dimensions, car les algorithmes de compression de bloc opèrent sur des blocs texels 4x4.</span><span class="sxs-lookup"><span data-stu-id="ed682-152">A block-compressed texture must be a multiple of 4 in all dimensions because the block-compression algorithms operate on 4x4 texel blocks.</span></span> <span data-ttu-id="ed682-153">Il s’agit d’un problème pour un mipmap dont les dimensions initiales sont divisible par 4, mais pas les niveaux subdivisés.</span><span class="sxs-lookup"><span data-stu-id="ed682-153">This will be a problem for a mipmap whose initial dimensions are divisible by 4, but subdivided levels are not.</span></span> <span data-ttu-id="ed682-154">Le diagramme suivant montre la différence de zone entre la taille virtuelle (déclarée) et la taille physique (réelle) de chaque niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="ed682-154">The following diagram shows the difference in area between the virtual (declared) size and the physical (actual) size of each mipmap level.</span></span>

![diagramme des niveaux de mipmap non compressés et compressés](images/d3d10-block-compress-pad.png)

<span data-ttu-id="ed682-156">Le côté gauche du diagramme montre les tailles de niveaux de mipmap générées pour une texture 60 × 40 non compressée.</span><span class="sxs-lookup"><span data-stu-id="ed682-156">The left side of the diagram shows the mipmap level sizes that are generated for an uncompressed 60×40 texture.</span></span> <span data-ttu-id="ed682-157">La taille de niveau supérieur est tirée de l’appel d’API qui génère la texture. chaque niveau suivant correspond à la moitié de la taille du niveau précédent.</span><span class="sxs-lookup"><span data-stu-id="ed682-157">The top level size is taken from the API call that generates the texture; each subsequent level is half the size of the previous level.</span></span> <span data-ttu-id="ed682-158">Pour une texture non compressée, il n’existe aucune différence entre la taille virtuelle (déclarée) et la taille physique (réelle).</span><span class="sxs-lookup"><span data-stu-id="ed682-158">For an uncompressed texture, there is no difference between the virtual (declared) size and the physical (actual) size.</span></span>

<span data-ttu-id="ed682-159">La partie droite du diagramme montre les tailles de niveaux mipmap générées pour la même texture 60 × 40 avec compression.</span><span class="sxs-lookup"><span data-stu-id="ed682-159">The right side of the diagram shows the mipmap level sizes that are generated for the same 60×40 texture with compression.</span></span> <span data-ttu-id="ed682-160">Notez que les deuxième et troisième niveaux ont une marge intérieure de la mémoire pour que les facteurs de taille de 4 soient à chaque niveau.</span><span class="sxs-lookup"><span data-stu-id="ed682-160">Notice that both the second and third levels have memory padding to make the sizes factors of 4 on every level.</span></span> <span data-ttu-id="ed682-161">Cela est nécessaire pour que les algorithmes puissent fonctionner sur des blocs Texel 4 × 4.</span><span class="sxs-lookup"><span data-stu-id="ed682-161">This is necessary so that the algorithms can operate on 4×4 texel blocks.</span></span> <span data-ttu-id="ed682-162">Cette expecially est évidente si vous considérez des niveaux de mipmap inférieurs à 4 × 4 ; la taille de ces très petits niveaux de mipmap est arrondie au facteur le plus proche de 4 lorsque la mémoire de texture est allouée.</span><span class="sxs-lookup"><span data-stu-id="ed682-162">This is expecially evident if you consider mipmap levels that are smaller than 4×4; the size of these very small mipmap levels will be rounded up to the nearest factor of 4 when texture memory is allocated.</span></span>

<span data-ttu-id="ed682-163">Le matériel d’échantillonnage utilise la taille virtuelle ; Lorsque la texture est échantillonnée, le remplissage de la mémoire est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ed682-163">Sampling hardware uses the virtual size; when the texture is sampled, the memory padding is ignored.</span></span> <span data-ttu-id="ed682-164">Pour les niveaux de mipmap inférieurs à 4 × 4, seules les quatre premières texels seront utilisées pour une carte 2 × 2, et seul le premier Texel sera utilisé par un bloc 1 × 1.</span><span class="sxs-lookup"><span data-stu-id="ed682-164">For mipmap levels that are smaller than 4×4, only the first four texels will be used for a 2×2 map, and only the first texel will be used by a 1×1 block.</span></span> <span data-ttu-id="ed682-165">Toutefois, il n’existe aucune structure d’API qui expose la taille physique (y compris le remplissage de la mémoire).</span><span class="sxs-lookup"><span data-stu-id="ed682-165">However, there is no API structure that exposes the physical size (including the memory padding).</span></span>

<span data-ttu-id="ed682-166">En résumé, veillez à utiliser des blocs de mémoire alignés lors de la copie des régions qui contiennent des données compressées par blocs.</span><span class="sxs-lookup"><span data-stu-id="ed682-166">In summary, be careful to use aligned memory blocks when copying regions that contain block-compressed data.</span></span> <span data-ttu-id="ed682-167">Pour effectuer cette opération dans une application qui obtient un pointeur de mémoire, assurez-vous que le pointeur utilise le pas de la surface pour prendre en compte la taille de la mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="ed682-167">To do this in an application that gets a memory pointer, make sure that the pointer uses the surface pitch to account for the physical memory size.</span></span>

## <a name="compression-algorithms"></a><span data-ttu-id="ed682-168">Algorithmes de compression</span><span class="sxs-lookup"><span data-stu-id="ed682-168">Compression Algorithms</span></span>

<span data-ttu-id="ed682-169">Les techniques de compression de bloc dans Direct3D fractionnent les données de texture non compressées en blocs de 4 × 4, compressent chaque bloc, puis stockent les données.</span><span class="sxs-lookup"><span data-stu-id="ed682-169">Block compression techniques in Direct3D break up uncompressed texture data into 4×4 blocks, compress each block, and then store the data.</span></span> <span data-ttu-id="ed682-170">Pour cette raison, les textures censées être compressées doivent avoir des dimensions de texture multiples de 4.</span><span class="sxs-lookup"><span data-stu-id="ed682-170">For this reason, textures are expected to be compressed must have texture dimensions that are multiples of 4.</span></span>

![diagramme de la compression de bloc](images/d3d10-compression-1.png)

<span data-ttu-id="ed682-172">Le diagramme précédent montre une texture partitionnée en blocs Texel.</span><span class="sxs-lookup"><span data-stu-id="ed682-172">The preceding diagram shows a texture partitioned into texel blocks.</span></span> <span data-ttu-id="ed682-173">Le premier bloc affiche la disposition des 16 texels étiquetés a-p, mais chaque bloc a la même organisation de données.</span><span class="sxs-lookup"><span data-stu-id="ed682-173">The first block shows the layout of the 16 texels labeled a-p, but every block has the same organization of data.</span></span>

<span data-ttu-id="ed682-174">Direct3D implémente plusieurs schémas de compression, chacun d’entre eux implémentant un compromis différent entre le nombre de composants stockés, le nombre de bits par composant et la quantité de mémoire consommée.</span><span class="sxs-lookup"><span data-stu-id="ed682-174">Direct3D implements several compression schemes, each implements a different tradeoff between number of components stored, the number of bits per component, and the amount of memory consumed.</span></span> <span data-ttu-id="ed682-175">Utilisez ce tableau pour vous aider à choisir le format le mieux adapté au type de données et à la résolution de données qui convient le mieux à votre application.</span><span class="sxs-lookup"><span data-stu-id="ed682-175">Use this table to help choose the format that works best with the type of data and the data resolution that best fits your application.</span></span>



| <span data-ttu-id="ed682-176">Données sources</span><span class="sxs-lookup"><span data-stu-id="ed682-176">Source Data</span></span>                     | <span data-ttu-id="ed682-177">Résolution de la compression des données (en bits)</span><span class="sxs-lookup"><span data-stu-id="ed682-177">Data Compression Resolution (in bits)</span></span> | <span data-ttu-id="ed682-178">Choisir ce format de compression</span><span class="sxs-lookup"><span data-stu-id="ed682-178">Choose this compression format</span></span> |
|---------------------------------|---------------------------------------|--------------------------------|
| <span data-ttu-id="ed682-179">Couleur à trois composants et alpha</span><span class="sxs-lookup"><span data-stu-id="ed682-179">Three-component color and alpha</span></span> | <span data-ttu-id="ed682-180">Couleur (5:6:5), alpha (1) ou non alpha</span><span class="sxs-lookup"><span data-stu-id="ed682-180">Color (5:6:5), Alpha (1) or no alpha</span></span>  | <span data-ttu-id="ed682-181">BC1</span><span class="sxs-lookup"><span data-stu-id="ed682-181">BC1</span></span>                            |
| <span data-ttu-id="ed682-182">Couleur à trois composants et alpha</span><span class="sxs-lookup"><span data-stu-id="ed682-182">Three-component color and alpha</span></span> | <span data-ttu-id="ed682-183">Couleur (5:6:5), alpha (4)</span><span class="sxs-lookup"><span data-stu-id="ed682-183">Color (5:6:5), Alpha (4)</span></span>              | [<span data-ttu-id="ed682-184">BC2</span><span class="sxs-lookup"><span data-stu-id="ed682-184">BC2</span></span>](#bc2)                    |
| <span data-ttu-id="ed682-185">Couleur à trois composants et alpha</span><span class="sxs-lookup"><span data-stu-id="ed682-185">Three-component color and alpha</span></span> | <span data-ttu-id="ed682-186">Couleur (5:6:5), alpha (8)</span><span class="sxs-lookup"><span data-stu-id="ed682-186">Color (5:6:5), Alpha (8)</span></span>              | [<span data-ttu-id="ed682-187">BC3</span><span class="sxs-lookup"><span data-stu-id="ed682-187">BC3</span></span>](#bc3)                    |
| <span data-ttu-id="ed682-188">Couleur d’un composant</span><span class="sxs-lookup"><span data-stu-id="ed682-188">One-component color</span></span>             | <span data-ttu-id="ed682-189">Un composant (8)</span><span class="sxs-lookup"><span data-stu-id="ed682-189">One component (8)</span></span>                     | [<span data-ttu-id="ed682-190">TEXTURES BC4</span><span class="sxs-lookup"><span data-stu-id="ed682-190">BC4</span></span>](#bc4)                    |
| <span data-ttu-id="ed682-191">Couleur à deux composants</span><span class="sxs-lookup"><span data-stu-id="ed682-191">Two-component color</span></span>             | <span data-ttu-id="ed682-192">Deux composants (8:8)</span><span class="sxs-lookup"><span data-stu-id="ed682-192">Two components (8:8)</span></span>                  | [<span data-ttu-id="ed682-193">BC5</span><span class="sxs-lookup"><span data-stu-id="ed682-193">BC5</span></span>](#bc5)                    |



 

### <a name="bc1"></a><span data-ttu-id="ed682-194">BC1</span><span class="sxs-lookup"><span data-stu-id="ed682-194">BC1</span></span>

<span data-ttu-id="ed682-195">Utilisez le premier format de compression de bloc (BC1) (DXGI \_ format \_ BC1 \_ untype, DXGI \_ format BC1 UNORM ou dxgi BC1 UNORM \_ \_ \_ \_ \_ sRGB) pour stocker les données de couleur à trois composants à l’aide d’une couleur 5:6:5 (5 bits rouge, 6 bits vert, 5 bits bleus).</span><span class="sxs-lookup"><span data-stu-id="ed682-195">Use the first block compression format (BC1) (either DXGI\_FORMAT\_BC1\_TYPELESS, DXGI\_FORMAT\_BC1\_UNORM, or DXGI\_BC1\_UNORM\_SRGB) to store three-component color data using a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue).</span></span> <span data-ttu-id="ed682-196">Cela est vrai même si les données contiennent également une valeur alpha de 1 bit.</span><span class="sxs-lookup"><span data-stu-id="ed682-196">This is true even if the data also contains 1-bit alpha.</span></span> <span data-ttu-id="ed682-197">En supposant une texture 4 × 4 utilisant le format de données le plus grand possible, le format BC1 réduit la mémoire requise de 48 octets (16 couleurs × 3 composants/couleur × 1 octet/composant) à 8 octets de mémoire.</span><span class="sxs-lookup"><span data-stu-id="ed682-197">Assuming a 4×4 texture using the largest data format possible, the BC1 format reduces the memory required from 48 bytes (16 colors × 3 components/color × 1 byte/component) to 8 bytes of memory.</span></span>

<span data-ttu-id="ed682-198">L’algorithme fonctionne sur 4 × 4 blocs de texels.</span><span class="sxs-lookup"><span data-stu-id="ed682-198">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="ed682-199">Au lieu de stocker 16 couleurs, l’algorithme enregistre 2 couleurs de référence (couleur \_ 0 et couleur \_ 1) et des index de couleurs 16 2 bits (bloque a – p), comme illustré dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="ed682-199">Instead of storing 16 colors, the algorithm saves 2 reference colors (color\_0 and color\_1) and 16 2-bit color indices (blocks a–p), as shown in the following diagram.</span></span>

![diagramme de la disposition de la compression BC1](images/d3d10-compression-bc1.png)

<span data-ttu-id="ed682-201">Les index de couleurs (a – p) sont utilisés pour rechercher les couleurs d’origine d’une table des couleurs.</span><span class="sxs-lookup"><span data-stu-id="ed682-201">The color indices (a–p) are used to look up the original colors from a color table.</span></span> <span data-ttu-id="ed682-202">La table des couleurs contient 4 couleurs.</span><span class="sxs-lookup"><span data-stu-id="ed682-202">The color table contains 4 colors.</span></span> <span data-ttu-id="ed682-203">Les deux premières couleurs (couleur \_ 0 et couleur \_ 1) représentent les couleurs minimales et maximales.</span><span class="sxs-lookup"><span data-stu-id="ed682-203">The first two colors—color\_0 and color\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="ed682-204">Les deux autres couleurs, Color \_ 2 et Color \_ 3, sont des couleurs intermédiaires calculées à l’aide d’une interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="ed682-204">The other two colors, color\_2 and color\_3, are intermediate colors calculated with linear interpolation.</span></span>


```
color_2 = 2/3*color_0 + 1/3*color_1
color_3 = 1/3*color_0 + 2/3*color_1
```



<span data-ttu-id="ed682-205">Les quatre couleurs reçoivent des valeurs d’index de 2 bits qui seront enregistrées dans les blocs a – p.</span><span class="sxs-lookup"><span data-stu-id="ed682-205">The four colors are assigned 2-bit index values that will be saved in blocks a–p.</span></span>


```
color_0 = 00
color_1 = 01
color_2 = 10
color_3 = 11
```



<span data-ttu-id="ed682-206">Enfin, chacune des couleurs des blocs a à p est comparée aux quatre couleurs de la table des couleurs, et l’index de la couleur la plus proche est stocké dans les blocs de 2 bits.</span><span class="sxs-lookup"><span data-stu-id="ed682-206">Finally, each of the colors in blocks a–p are compared with the four colors in the color table, and the index for the closest color is stored in the 2-bit blocks.</span></span>

<span data-ttu-id="ed682-207">Cet algorithme se prête aux données qui contiennent également une valeur alpha de 1 bit.</span><span class="sxs-lookup"><span data-stu-id="ed682-207">This algorithm lends itself to data that contains 1-bit alpha also.</span></span> <span data-ttu-id="ed682-208">La seule différence est que la couleur \_ 3 est définie sur 0 (qui représente une couleur transparente) et que la couleur \_ 2 est un mélange linéaire de la couleur \_ 0 et de la couleur \_ 1.</span><span class="sxs-lookup"><span data-stu-id="ed682-208">The only difference is that color\_3 is set to 0 (which represents a transparent color) and color\_2 is a linear blend of color\_0 and color\_1.</span></span>


```
color_2 = 1/2*color_0 + 1/2*color_1;
color_3 = 0;
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ed682-209">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="ed682-209">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="ed682-210">Ce format existe à la fois dans Direct3D 9 et 10.</span><span class="sxs-lookup"><span data-stu-id="ed682-210">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="ed682-211">Dans Direct3D 9, le format BC1 est appelé D3DFMT_DXT1.</span><span class="sxs-lookup"><span data-stu-id="ed682-211">In Direct3D 9, the BC1 format is called D3DFMT_DXT1.</span></span></li>
<li><span data-ttu-id="ed682-212">Dans Direct3D 10, le format BC1 est représenté par DXGI_FORMAT_BC1_UNORM ou DXGI_FORMAT_BC1_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="ed682-212">In Direct3D 10, the BC1 format is represented by DXGI_FORMAT_BC1_UNORM or DXGI_FORMAT_BC1_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc2"></a><span data-ttu-id="ed682-213">BC2</span><span class="sxs-lookup"><span data-stu-id="ed682-213">BC2</span></span>

<span data-ttu-id="ed682-214">Utilisez le format BC2 (DXGI \_ format \_ BC2 \_ sans type, DXGI format BC2 UNORM ou dxgi BC2 UNORM BC3 \_ \_ \_ \_ \_ \_ ) pour stocker les données qui contiennent des données de couleur et alpha avec une faible cohérence (utilisez [](#bc3) pour les données alpha hautement cohérentes).</span><span class="sxs-lookup"><span data-stu-id="ed682-214">Use the BC2 format (either DXGI\_FORMAT\_BC2\_TYPELESS, DXGI\_FORMAT\_BC2\_UNORM, or DXGI\_BC2\_UNORM\_SRGB) to store data that contains color and alpha data with low coherency (use [BC3](#bc3) for highly-coherent alpha data).</span></span> <span data-ttu-id="ed682-215">Le format BC2 stocke les données RVB sous la forme d’une couleur 5:6:5 (5 bits rouge, 6 bits vert, 5 bits bleus) et alpha comme valeur 4 bits distincte.</span><span class="sxs-lookup"><span data-stu-id="ed682-215">The BC2 format stores RGB data as a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha as a separate 4-bit value.</span></span> <span data-ttu-id="ed682-216">En supposant une texture 4 × 4 utilisant le plus grand format de données possible, cette technique de compression réduit la mémoire requise de 64 octets (16 couleurs × 4 composants/couleur × 1 octet/composant) à 16 octets de mémoire.</span><span class="sxs-lookup"><span data-stu-id="ed682-216">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="ed682-217">Le format BC2 stocke les couleurs avec le même nombre de bits et la même disposition de données que le format [BC1](#bc1) ; Toutefois, BC2 requiert une mémoire supplémentaire de 64 bits pour stocker les données alpha, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="ed682-217">The BC2 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC2 requires an additional 64-bits of memory to store the alpha data, as shown in the following diagram.</span></span>

![diagramme de la disposition de la compression BC2](images/d3d10-compression-bc2.png)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ed682-219">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="ed682-219">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="ed682-220">Ce format existe à la fois dans Direct3D 9 et 10.</span><span class="sxs-lookup"><span data-stu-id="ed682-220">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="ed682-221">Dans Direct3D 9, le format BC2 est appelé D3DFMT_DXT2 et D3DFMT_DXT3.</span><span class="sxs-lookup"><span data-stu-id="ed682-221">In Direct3D 9, the BC2 format is called D3DFMT_DXT2 and D3DFMT_DXT3.</span></span></li>
<li><span data-ttu-id="ed682-222">Dans Direct3D 10, le format BC2 est représenté par DXGI_FORMAT_BC2_UNORM ou DXGI_FORMAT_BC2_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="ed682-222">In Direct3D 10, the BC2 format is represented by DXGI_FORMAT_BC2_UNORM or DXGI_FORMAT_BC2_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc3"></a><span data-ttu-id="ed682-223">BC3</span><span class="sxs-lookup"><span data-stu-id="ed682-223">BC3</span></span>

<span data-ttu-id="ed682-224">Utilisez le format BC3 (DXGI \_ format \_ BC3 \_ sans type, DXGI format BC3 UNORM ou dxgi BC3 UNORM BC2 \_ \_ \_ \_ \_ \_ ) pour stocker des données de couleur hautement cohérentes (utilisez [](#bc2) avec des données alpha moins cohérentes).</span><span class="sxs-lookup"><span data-stu-id="ed682-224">Use the BC3 format (either DXGI\_FORMAT\_BC3\_TYPELESS, DXGI\_FORMAT\_BC3\_UNORM, or DXGI\_BC3\_UNORM\_SRGB) to store highly coherent color data (use [BC2](#bc2) with less coherent alpha data).</span></span> <span data-ttu-id="ed682-225">Le format BC3 stocke les données de couleur à l’aide de la couleur 5:6:5 (5 bits rouge, 6 bits vert, 5 bits bleus) et des données alpha à l’aide d’un octet.</span><span class="sxs-lookup"><span data-stu-id="ed682-225">The BC3 format stores color data using 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha data using one byte.</span></span> <span data-ttu-id="ed682-226">En supposant une texture 4 × 4 utilisant le plus grand format de données possible, cette technique de compression réduit la mémoire requise de 64 octets (16 couleurs × 4 composants/couleur × 1 octet/composant) à 16 octets de mémoire.</span><span class="sxs-lookup"><span data-stu-id="ed682-226">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="ed682-227">Le format BC3 stocke les couleurs avec le même nombre de bits et la même disposition de données que le format [BC1](#bc1) ; Toutefois, BC3 requiert une mémoire supplémentaire de 64 bits pour stocker les données alpha.</span><span class="sxs-lookup"><span data-stu-id="ed682-227">The BC3 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC3 requires an additional 64-bits of memory to store the alpha data.</span></span> <span data-ttu-id="ed682-228">Le format BC3 gère l’alpha en stockant deux valeurs de référence et en les interpolant entre elles (de la même façon que BC1 stocke la couleur RVB).</span><span class="sxs-lookup"><span data-stu-id="ed682-228">The BC3 format handles alpha by storing two reference values and interpolating between them (similarly to how BC1 stores RGB color).</span></span>

<span data-ttu-id="ed682-229">L’algorithme fonctionne sur 4 × 4 blocs de texels.</span><span class="sxs-lookup"><span data-stu-id="ed682-229">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="ed682-230">Au lieu de stocker 16 valeurs alpha, l’algorithme stocke 2 index alpha de référence (alpha \_ 0 et alpha \_ 1) et des index de couleur 16 3 bits (alpha a à p), comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="ed682-230">Instead of storing 16 alpha values, the algorithm stores 2 reference alphas (alpha\_0 and alpha\_1) and 16 3-bit color indices (alpha a through p), as shown in the following diagram.</span></span>

![diagramme de la disposition de la compression BC3](images/d3d10-compression-bc3.png)

<span data-ttu-id="ed682-232">Le format BC3 utilise les indices alpha (a – p) pour rechercher les couleurs d’origine d’une table de recherche qui contient 8 valeurs.</span><span class="sxs-lookup"><span data-stu-id="ed682-232">The BC3 format uses the alpha indices (a–p) to look up the original colors from a lookup table that contains 8 values.</span></span> <span data-ttu-id="ed682-233">Les deux premières valeurs (alpha \_ 0 et alpha \_ 1) sont les valeurs minimale et maximale ; les six autres valeurs intermédiaires sont calculées à l’aide d’une interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="ed682-233">The first two values—alpha\_0 and alpha\_1—are the minimum and maximum values; the other six intermediate values are calculated using linear interpolation.</span></span>

<span data-ttu-id="ed682-234">L’algorithme détermine le nombre de valeurs alpha interpolées en examinant les deux valeurs alpha de référence.</span><span class="sxs-lookup"><span data-stu-id="ed682-234">The algorithm determines the number of interpolated alpha values by examining the two reference alpha values.</span></span> <span data-ttu-id="ed682-235">Si alpha \_ 0 est supérieur à alpha \_ 1, BC3 interpole 6 valeurs alpha ; sinon, il interpole 4.</span><span class="sxs-lookup"><span data-stu-id="ed682-235">If alpha\_0 is greater than alpha\_1, then BC3 interpolates 6 alpha values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="ed682-236">Quand BC3 n’interpole que 4 valeurs alpha, il définit deux valeurs alpha supplémentaires (0 pour la transparence intégrale et 255 pour le total opaque).</span><span class="sxs-lookup"><span data-stu-id="ed682-236">When BC3 interpolates only 4 alpha values, it sets two additional alpha values (0 for fully transparent and 255 for fully opaque).</span></span> <span data-ttu-id="ed682-237">BC3 compresse les valeurs alpha dans la zone de Texel 4 × 4 en stockant le code binaire correspondant aux valeurs alpha interpolées qui correspond le mieux à l’alpha d’origine pour un Texel donné.</span><span class="sxs-lookup"><span data-stu-id="ed682-237">BC3 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values which most closely matches the original alpha for a given texel.</span></span>


```
if( alpha_0 > alpha_1 )
{
  // 6 interpolated alpha values.
  alpha_2 = 6/7*alpha_0 + 1/7*alpha_1; // bit code 010
  alpha_3 = 5/7*alpha_0 + 2/7*alpha_1; // bit code 011
  alpha_4 = 4/7*alpha_0 + 3/7*alpha_1; // bit code 100
  alpha_5 = 3/7*alpha_0 + 4/7*alpha_1; // bit code 101
  alpha_6 = 2/7*alpha_0 + 5/7*alpha_1; // bit code 110
  alpha_7 = 1/7*alpha_0 + 6/7*alpha_1; // bit code 111
}
else
{
  // 4 interpolated alpha values.
  alpha_2 = 4/5*alpha_0 + 1/5*alpha_1; // bit code 010
  alpha_3 = 3/5*alpha_0 + 2/5*alpha_1; // bit code 011
  alpha_4 = 2/5*alpha_0 + 3/5*alpha_1; // bit code 100
  alpha_5 = 1/5*alpha_0 + 4/5*alpha_1; // bit code 101
  alpha_6 = 0;                         // bit code 110
  alpha_7 = 255;                       // bit code 111
}
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ed682-238">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="ed682-238">Differences between Direct3D 9 and Direct3D 10:</span></span><br/>
<ul>
<li><span data-ttu-id="ed682-239">Dans Direct3D 9, le format BC3 est appelé D3DFMT_DXT4 et D3DFMT_DXT5.</span><span class="sxs-lookup"><span data-stu-id="ed682-239">In Direct3D 9, the BC3 format is called D3DFMT_DXT4 and D3DFMT_DXT5.</span></span></li>
<li><span data-ttu-id="ed682-240">Dans Direct3D 10, le format BC3 est représenté par DXGI_FORMAT_BC3_UNORM ou DXGI_FORMAT_BC3_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="ed682-240">In Direct3D 10, the BC3 format is represented by DXGI_FORMAT_BC3_UNORM or DXGI_FORMAT_BC3_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc4"></a><span data-ttu-id="ed682-241">TEXTURES BC4</span><span class="sxs-lookup"><span data-stu-id="ed682-241">BC4</span></span>

<span data-ttu-id="ed682-242">Utilisez le format textures BC4 pour stocker les données de couleur d’un composant à l’aide de 8 bits pour chaque couleur.</span><span class="sxs-lookup"><span data-stu-id="ed682-242">Use the BC4 format to store one-component color data using 8 bits for each color.</span></span> <span data-ttu-id="ed682-243">En raison de l’exactitude accrue (par rapport à [BC1](#bc1)), textures BC4 est idéal pour le stockage des données à virgule flottante dans la plage de \[ 0 à 1 à l' \] aide du format dxgi \_ \_ textures BC4 \_ UNORM et de \[ -1 à + 1 à l' \] aide du format dxgi \_ \_ textures BC4 \_ ronfler.</span><span class="sxs-lookup"><span data-stu-id="ed682-243">As a result of the increased accuracy (compared to [BC1](#bc1)), BC4 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC4\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC4\_SNORM format.</span></span> <span data-ttu-id="ed682-244">En supposant une texture 4 × 4 utilisant le plus grand format de données possible, cette technique de compression réduit la mémoire requise de 16 octets (16 couleurs × 1 composant/couleur × 1 octet/composant) à 8 octets.</span><span class="sxs-lookup"><span data-stu-id="ed682-244">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 16 bytes (16 colors × 1 components/color × 1 byte/component) to 8 bytes.</span></span>

<span data-ttu-id="ed682-245">L’algorithme fonctionne sur 4 × 4 blocs de texels.</span><span class="sxs-lookup"><span data-stu-id="ed682-245">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="ed682-246">Au lieu de stocker 16 couleurs, l’algorithme stocke 2 couleurs de référence (rouge \_ 0 et rouge \_ 1) et les index de couleurs 16 3 bits (rouge a à rouge p), comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="ed682-246">Instead of storing 16 colors, the algorithm stores 2 reference colors (red\_0 and red\_1) and 16 3-bit color indices (red a through red p), as shown in the following diagram.</span></span>

![diagramme de la disposition de la compression textures BC4](images/d3d10-compression-bc4.png)

<span data-ttu-id="ed682-248">L’algorithme utilise les index de 3 bits pour rechercher des couleurs dans une table de couleurs qui contient 8 couleurs.</span><span class="sxs-lookup"><span data-stu-id="ed682-248">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="ed682-249">Les deux premières couleurs (rouge \_ 0 et rouge \_ 1) représentent les couleurs minimales et maximales.</span><span class="sxs-lookup"><span data-stu-id="ed682-249">The first two colors—red\_0 and red\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="ed682-250">L’algorithme calcule les couleurs restantes à l’aide d’une interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="ed682-250">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="ed682-251">L’algorithme détermine le nombre de valeurs de couleur interpolées en examinant les deux valeurs de référence.</span><span class="sxs-lookup"><span data-stu-id="ed682-251">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="ed682-252">Si \_ le 0 rouge est supérieur à \_ 1 rouge, textures BC4 interpole 6 valeurs de couleur ; sinon, il interpole 4.</span><span class="sxs-lookup"><span data-stu-id="ed682-252">If red\_0 is greater than red\_1, then BC4 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="ed682-253">Quand textures BC4 n’interpole que 4 valeurs de couleur, il définit deux valeurs de couleur supplémentaires (0.0 f pour entièrement transparent et 1,0 f pour entièrement opaque).</span><span class="sxs-lookup"><span data-stu-id="ed682-253">When BC4 interpolates only 4 color values, it sets two additional color values (0.0f for fully transparent and 1.0f for fully opaque).</span></span> <span data-ttu-id="ed682-254">TEXTURES BC4 compresse les valeurs alpha dans la zone de Texel 4 × 4 en stockant le code binaire correspondant aux valeurs alpha interpolées qui correspond le mieux à l’alpha d’origine pour un Texel donné.</span><span class="sxs-lookup"><span data-stu-id="ed682-254">BC4 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values that most closely matches the original alpha for a given texel.</span></span>

-   [<span data-ttu-id="ed682-255">TEXTURES BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="ed682-255">BC4\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="ed682-256">TEXTURES BC4 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="ed682-256">BC4\_SNORM</span></span>](/windows)

### <a name="bc4_unorm"></a><span data-ttu-id="ed682-257">TEXTURES BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="ed682-257">BC4\_UNORM</span></span>

<span data-ttu-id="ed682-258">L’interpolation des données à composant unique s’effectue comme dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ed682-258">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="ed682-259">Les index de 3 bits sont affectés aux couleurs de référence (000 – 111, car il y a 8 valeurs), qui seront enregistrées dans des blocs de a à rouge p au cours de la compression.</span><span class="sxs-lookup"><span data-stu-id="ed682-259">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc4_snorm"></a><span data-ttu-id="ed682-260">TEXTURES BC4 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="ed682-260">BC4\_SNORM</span></span>

<span data-ttu-id="ed682-261">Le \_ format dxgi \_ textures BC4 \_ ronfler est exactement le même, sauf que les données sont encodées dans une plage de ronflements et lorsque 4 valeurs de couleur sont interpolées.</span><span class="sxs-lookup"><span data-stu-id="ed682-261">The DXGI\_FORMAT\_BC4\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 color values are interpolated.</span></span> <span data-ttu-id="ed682-262">L’interpolation des données à composant unique s’effectue comme dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ed682-262">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                     // bit code 110
  red_7 =  1.0f;                     // bit code 111
}
```



<span data-ttu-id="ed682-263">Les index de 3 bits sont affectés aux couleurs de référence (000 – 111, car il y a 8 valeurs), qui seront enregistrées dans des blocs de a à rouge p au cours de la compression.</span><span class="sxs-lookup"><span data-stu-id="ed682-263">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5"></a><span data-ttu-id="ed682-264">BC5</span><span class="sxs-lookup"><span data-stu-id="ed682-264">BC5</span></span>

<span data-ttu-id="ed682-265">Utilisez le format BC5 pour stocker les données de couleur à deux composants à l’aide de 8 bits pour chaque couleur.</span><span class="sxs-lookup"><span data-stu-id="ed682-265">Use the BC5 format to store two-component color data using 8 bits for each color.</span></span> <span data-ttu-id="ed682-266">En raison de l’exactitude accrue (par rapport à [BC1](#bc1)), BC5 est idéal pour le stockage des données à virgule flottante dans la plage de \[ 0 à 1 à l' \] aide du format dxgi \_ \_ BC5 \_ UNORM et de \[ -1 à + 1 à l' \] aide du format dxgi \_ \_ BC5 \_ ronfler.</span><span class="sxs-lookup"><span data-stu-id="ed682-266">As a result of the increased accuracy (compared to [BC1](#bc1)), BC5 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC5\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC5\_SNORM format.</span></span> <span data-ttu-id="ed682-267">En supposant une texture 4 × 4 utilisant le plus grand format de données possible, cette technique de compression réduit la mémoire requise de 32 octets (16 couleurs × 2 composants/couleur × 1 octet/composant) à 16 octets.</span><span class="sxs-lookup"><span data-stu-id="ed682-267">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 32 bytes (16 colors × 2 components/color × 1 byte/component) to 16 bytes.</span></span>

<span data-ttu-id="ed682-268">L’algorithme fonctionne sur 4 × 4 blocs de texels.</span><span class="sxs-lookup"><span data-stu-id="ed682-268">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="ed682-269">Au lieu de stocker 16 couleurs pour les deux composants, l’algorithme stocke 2 couleurs de référence pour chaque composant (rouge \_ 0, rouge \_ 1, vert \_ 0 et vert \_ 1) et les index de couleurs 16 3 bits pour chaque composant (rouge a à p rouge et vert a à vert p), comme illustré dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="ed682-269">Instead of storing 16 colors for both components, the algorithm stores 2 reference colors for each component (red\_0, red\_1, green\_0, and green\_1) and 16 3-bit color indices for each component (red a through red p and green a through green p), as shown in the following diagram.</span></span>

![diagramme de la disposition de la compression BC5](images/d3d10-compression-bc5.png)

<span data-ttu-id="ed682-271">L’algorithme utilise les index de 3 bits pour rechercher des couleurs dans une table de couleurs qui contient 8 couleurs.</span><span class="sxs-lookup"><span data-stu-id="ed682-271">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="ed682-272">Les deux premières couleurs (rouge \_ 0 et rouge \_ 1 (ou vert \_ 0 et vert \_ 1) sont les couleurs minimales et maximales.</span><span class="sxs-lookup"><span data-stu-id="ed682-272">The first two colors—red\_0 and red\_1 (or green\_0 and green\_1)—are the minimum and maximum colors.</span></span> <span data-ttu-id="ed682-273">L’algorithme calcule les couleurs restantes à l’aide d’une interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="ed682-273">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="ed682-274">L’algorithme détermine le nombre de valeurs de couleur interpolées en examinant les deux valeurs de référence.</span><span class="sxs-lookup"><span data-stu-id="ed682-274">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="ed682-275">Si \_ le 0 rouge est supérieur à \_ 1 rouge, BC5 interpole 6 valeurs de couleur ; sinon, il interpole 4.</span><span class="sxs-lookup"><span data-stu-id="ed682-275">If red\_0 is greater than red\_1, then BC5 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="ed682-276">Quand BC5 interpole uniquement 4 valeurs de couleur, il définit les deux autres valeurs de couleur à 0.0 f et 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="ed682-276">When BC5 interpolates only 4 color values, it sets the remaining two color values at 0.0f and 1.0f.</span></span>

-   [<span data-ttu-id="ed682-277">BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="ed682-277">BC5\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="ed682-278">BC5 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="ed682-278">BC5\_SNORM</span></span>](/windows)

### <a name="bc5_unorm"></a><span data-ttu-id="ed682-279">BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="ed682-279">BC5\_UNORM</span></span>

<span data-ttu-id="ed682-280">L’interpolation des données à composant unique s’effectue comme dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ed682-280">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="ed682-281">Les calculs pour les composants verts sont similaires.</span><span class="sxs-lookup"><span data-stu-id="ed682-281">The calculations for the green components are similar.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="ed682-282">Les index de 3 bits sont affectés aux couleurs de référence (000 – 111, car il y a 8 valeurs), qui seront enregistrées dans des blocs de a à rouge p au cours de la compression.</span><span class="sxs-lookup"><span data-stu-id="ed682-282">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5_snorm"></a><span data-ttu-id="ed682-283">BC5 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="ed682-283">BC5\_SNORM</span></span>

<span data-ttu-id="ed682-284">Le \_ format dxgi \_ BC5 \_ ronfler est exactement le même, sauf que les données sont encodées dans une plage de ronflements et lorsque 4 valeurs de données sont interpolées, les deux valeurs supplémentaires sont-1.0 f et 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="ed682-284">The DXGI\_FORMAT\_BC5\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 data values are interpolated, the two additional values are -1.0f and 1.0f.</span></span> <span data-ttu-id="ed682-285">L’interpolation des données à composant unique s’effectue comme dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ed682-285">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="ed682-286">Les calculs pour les composants verts sont similaires.</span><span class="sxs-lookup"><span data-stu-id="ed682-286">The calculations for the green components are similar.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                    // bit code 110
  red_7 =  1.0f;                    // bit code 111
}
```



<span data-ttu-id="ed682-287">Les index de 3 bits sont affectés aux couleurs de référence (000 – 111, car il y a 8 valeurs), qui seront enregistrées dans des blocs de a à rouge p au cours de la compression.</span><span class="sxs-lookup"><span data-stu-id="ed682-287">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

## <a name="format-conversion-using-direct3d-101"></a><span data-ttu-id="ed682-288">Conversion de format à l’aide de Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="ed682-288">Format Conversion Using Direct3D 10.1</span></span>

<span data-ttu-id="ed682-289">Direct3D 10,1 permet de copier les textures de type préstructurées et les textures compressées par bloc des mêmes largeurs de bits.</span><span class="sxs-lookup"><span data-stu-id="ed682-289">Direct3D 10.1 enables copies between prestructured-typed textures and block-compressed textures of the same bit widths.</span></span> <span data-ttu-id="ed682-290">Les fonctions qui peuvent y parvenir sont [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) et [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).</span><span class="sxs-lookup"><span data-stu-id="ed682-290">The functions that can accomplish this are [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).</span></span>

<span data-ttu-id="ed682-291">À partir de Direct3D 10,1, vous pouvez utiliser [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) et [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) pour effectuer une copie entre quelques types de format.</span><span class="sxs-lookup"><span data-stu-id="ed682-291">Beginning with Direct3D 10.1, you can use [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) to copy between a few format types.</span></span> <span data-ttu-id="ed682-292">Ce type d’opération de copie effectue un type de conversion de format qui réinterprète les données de ressources comme un type de format différent.</span><span class="sxs-lookup"><span data-stu-id="ed682-292">This type of copy operation performs a type of format conversion that reinterprets resource data as a different format type.</span></span> <span data-ttu-id="ed682-293">Prenons l’exemple suivant qui illustre la différence entre la réinterprétation des données et le comportement d’un type de conversion plus classique :</span><span class="sxs-lookup"><span data-stu-id="ed682-293">Consider this example that shows the difference between reinterpreting data with the way a more typical type of conversion behaves:</span></span>


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



<span data-ttu-id="ed682-294">Pour réinterpréter « f » comme type de « u », utilisez [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):</span><span class="sxs-lookup"><span data-stu-id="ed682-294">To reinterpret ‘f’ as the type of ‘u’, use [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):</span></span>


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



<span data-ttu-id="ed682-295">Dans la réinterprétation précédente, la valeur sous-jacente des données ne change pas. [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) réinterprète le float comme un entier non signé.</span><span class="sxs-lookup"><span data-stu-id="ed682-295">In the preceding reinterpretation, the underlying value of the data doesn’t change; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterprets the float as an unsigned integer.</span></span>

<span data-ttu-id="ed682-296">Pour effectuer le type de conversion le plus courant, utilisez l’assignation :</span><span class="sxs-lookup"><span data-stu-id="ed682-296">To perform the more typical type of conversion, use assignment:</span></span>


```
    u = f; // ‘u’ becomes 1.
```



<span data-ttu-id="ed682-297">Dans la conversion précédente, la valeur sous-jacente des données change.</span><span class="sxs-lookup"><span data-stu-id="ed682-297">In the preceding conversion, the underlying value of the data changes.</span></span>

<span data-ttu-id="ed682-298">Le tableau suivant répertorie les formats autorisés de source et de destination que vous pouvez utiliser dans ce type de réinterprétation de conversion de format.</span><span class="sxs-lookup"><span data-stu-id="ed682-298">The following table lists the allowable source and destination formats that you can use in this reinterpretation type of format conversion.</span></span> <span data-ttu-id="ed682-299">Vous devez encoder les valeurs correctement pour que la réinterprétation fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="ed682-299">You must encode the values properly for the reinterpretation to work as expected.</span></span>



| <span data-ttu-id="ed682-300">Largeur de bit</span><span class="sxs-lookup"><span data-stu-id="ed682-300">Bit Width</span></span> | <span data-ttu-id="ed682-301">Ressource non compressée</span><span class="sxs-lookup"><span data-stu-id="ed682-301">Uncompressed Resource</span></span>                                                                                                                                               | <span data-ttu-id="ed682-302">Ressource Block-Compressed</span><span class="sxs-lookup"><span data-stu-id="ed682-302">Block-Compressed Resource</span></span>                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed682-303">32</span><span class="sxs-lookup"><span data-stu-id="ed682-303">32</span></span>        | <span data-ttu-id="ed682-304">DXGI \_ format \_ R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="ed682-304">DXGI\_FORMAT\_R32\_UINT</span></span><br/> <span data-ttu-id="ed682-305">\_Format dxgi \_ R32 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="ed682-305">DXGI\_FORMAT\_R32\_SINT</span></span><br/>                                                                                               | <span data-ttu-id="ed682-306">DXGI \_ format \_ R9G9B9E5 \_ SHAREDEXP</span><span class="sxs-lookup"><span data-stu-id="ed682-306">DXGI\_FORMAT\_R9G9B9E5\_SHAREDEXP</span></span>                                                                                                                                   |
| <span data-ttu-id="ed682-307">64</span><span class="sxs-lookup"><span data-stu-id="ed682-307">64</span></span>        | <span data-ttu-id="ed682-308">DXGI \_ format \_ R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="ed682-308">DXGI\_FORMAT\_R16G16B16A16\_UINT</span></span><br/> <span data-ttu-id="ed682-309">\_Format dxgi \_ R16G16B16A16 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="ed682-309">DXGI\_FORMAT\_R16G16B16A16\_SINT</span></span><br/> <span data-ttu-id="ed682-310">DXGI \_ format \_ R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="ed682-310">DXGI\_FORMAT\_R32G32\_UINT</span></span><br/> <span data-ttu-id="ed682-311">\_Format dxgi \_ R32G32 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="ed682-311">DXGI\_FORMAT\_R32G32\_SINT</span></span><br/> | <span data-ttu-id="ed682-312">DXGI \_ format \_ BC1 \_ UNORM \[ \_ sRVB\]</span><span class="sxs-lookup"><span data-stu-id="ed682-312">DXGI\_FORMAT\_BC1\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="ed682-313">DXGI \_ format \_ textures BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="ed682-313">DXGI\_FORMAT\_BC4\_UNORM</span></span><br/> <span data-ttu-id="ed682-314">\_Format dxgi \_ textures BC4 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="ed682-314">DXGI\_FORMAT\_BC4\_SNORM</span></span><br/>                                               |
| <span data-ttu-id="ed682-315">128</span><span class="sxs-lookup"><span data-stu-id="ed682-315">128</span></span>       | <span data-ttu-id="ed682-316">DXGI \_ format \_ R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="ed682-316">DXGI\_FORMAT\_R32G32B32A32\_UINT</span></span><br/> <span data-ttu-id="ed682-317">\_Format dxgi \_ R32G32B32A32 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="ed682-317">DXGI\_FORMAT\_R32G32B32A32\_SINT</span></span><br/>                                                                             | <span data-ttu-id="ed682-318">DXGI \_ format \_ BC2 \_ UNORM \[ \_ sRVB\]</span><span class="sxs-lookup"><span data-stu-id="ed682-318">DXGI\_FORMAT\_BC2\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="ed682-319">DXGI \_ format \_ BC3 \_ UNORM \[ \_ sRVB\]</span><span class="sxs-lookup"><span data-stu-id="ed682-319">DXGI\_FORMAT\_BC3\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="ed682-320">DXGI \_ format \_ BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="ed682-320">DXGI\_FORMAT\_BC5\_UNORM</span></span><br/> <span data-ttu-id="ed682-321">\_Format dxgi \_ BC5 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="ed682-321">DXGI\_FORMAT\_BC5\_SNORM</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ed682-322">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ed682-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed682-323">Ressources (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ed682-323">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
