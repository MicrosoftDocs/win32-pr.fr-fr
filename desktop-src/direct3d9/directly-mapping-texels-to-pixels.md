---
description: Lors du rendu de la sortie 2D à l’aide de vertex prétransformés, vous devez veiller à ce que chaque zone Texel corresponde correctement à une zone de pixel unique, sinon une déformation de texture peut se produire.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Mappage direct des texels à des pixels (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f86e9d05acff402128ddb83fc97898ff6a21d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200766"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a><span data-ttu-id="1b580-103">Mappage direct des texels à des pixels (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1b580-103">Directly Mapping Texels to Pixels (Direct3D 9)</span></span>

<span data-ttu-id="1b580-104">Lors du rendu de la sortie 2D à l’aide de vertex prétransformés, vous devez veiller à ce que chaque zone Texel corresponde correctement à une zone de pixel unique, sinon une déformation de texture peut se produire.</span><span class="sxs-lookup"><span data-stu-id="1b580-104">When rendering 2D output using pre-transformed vertices, care must be taken to ensure that each texel area correctly corresponds to a single pixel area, otherwise texture distortion can occur.</span></span> <span data-ttu-id="1b580-105">En maîtrisant les principes de base du processus que Direct3D suit lors de la pixellisation et de la texturation des triangles, vous pouvez vous assurer que votre application Direct3D affiche correctement la sortie 2D.</span><span class="sxs-lookup"><span data-stu-id="1b580-105">By understanding the basics of the process that Direct3D follows when rasterizing and texturing triangles, you can ensure your Direct3D application correctly renders 2D output.</span></span>

![illustration d’un affichage de résolution de 6X6](images/maptex-fig1.png)

<span data-ttu-id="1b580-107">Le diagramme précédent montre les pixels modélisés comme des carrés.</span><span class="sxs-lookup"><span data-stu-id="1b580-107">The preceding diagram shows pixels that are modeled as squares.</span></span> <span data-ttu-id="1b580-108">En réalité, toutefois, les pixels sont des points, et non des carrés.</span><span class="sxs-lookup"><span data-stu-id="1b580-108">In reality, however, pixels are dots, not squares.</span></span> <span data-ttu-id="1b580-109">Chaque carré du diagramme précédent indique la zone allumée par le pixel, mais un pixel est toujours simplement un point au centre d’un carré.</span><span class="sxs-lookup"><span data-stu-id="1b580-109">Each square in the preceding diagram indicates the area lit by the pixel, but a pixel is always just a dot at the center of a square.</span></span> <span data-ttu-id="1b580-110">Cette distinction, bien qu’apparemment petite, est importante.</span><span class="sxs-lookup"><span data-stu-id="1b580-110">This distinction, though seemingly small, is important.</span></span> <span data-ttu-id="1b580-111">Une meilleure illustration du même affichage est illustrée dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="1b580-111">A better illustration of the same display is shown in the following diagram.</span></span>

![illustration d’un affichage constitué de pixels](images/maptex-fig2.png)

<span data-ttu-id="1b580-113">Le diagramme précédent montre correctement chaque pixel physique en tant que point au centre de chaque cellule.</span><span class="sxs-lookup"><span data-stu-id="1b580-113">The preceding diagram correctly shows each physical pixel as a point in the center of each cell.</span></span> <span data-ttu-id="1b580-114">La coordonnée de l’espace à l’écran (0,0) est située directement en haut à gauche du pixel, et par conséquent au centre de la cellule supérieure gauche.</span><span class="sxs-lookup"><span data-stu-id="1b580-114">The screen space coordinate (0, 0) is located directly at the top-left pixel, and therefore at the center of the top-left cell.</span></span> <span data-ttu-id="1b580-115">L’angle supérieur gauche de l’affichage est donc à (-0,5,-0,5), car il s’agit de 0,5 cellules à gauche et de 0,5 cellules en partant du pixel supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="1b580-115">The top-left corner of the display is therefore at (-0.5, -0.5) because it is 0.5 cells to the left and 0.5 cells up from the top-left pixel.</span></span> <span data-ttu-id="1b580-116">Direct3D affiche un quadruple avec des angles à (0, 0) et (4, 4), comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="1b580-116">Direct3D will render a quad with corners at (0, 0) and (4, 4), as shown in the following illustration.</span></span>

![illustration d’un plan d’un quadruple Quad non pixellisé entre (0, 0) et (4,4)](images/maptex-fig3.png)

<span data-ttu-id="1b580-118">L’illustration précédente montre où le quad mathématique est en rapport avec l’affichage, mais n’indique pas ce à quoi ressemblera une fois que Direct3D la pixellise et l’envoie à l’écran.</span><span class="sxs-lookup"><span data-stu-id="1b580-118">The preceding illustration shows where the mathematical quad is in relation to the display, but does not show what the quad will look like once Direct3D rasterizes it and sends it to the display.</span></span> <span data-ttu-id="1b580-119">En fait, il est impossible pour un affichage raster de remplir le quad exactement comme indiqué, car les bords du Quad ne coïncident pas avec les limites entre les cellules de pixels.</span><span class="sxs-lookup"><span data-stu-id="1b580-119">In fact, it is impossible for a raster display to fill the quad exactly as shown because the edges of the quad do not coincide with the boundaries between pixel cells.</span></span> <span data-ttu-id="1b580-120">En d’autres termes, étant donné que chaque pixel ne peut afficher qu’une seule couleur, chaque cellule de pixel est remplie avec une seule couleur ; Si l’affichage devait restituer le quad exactement comme indiqué, les cellules de pixels le long du bord de l’quadruple-mesure doivent afficher deux couleurs distinctes : bleu, qui est couvert par le quadruple et le blanc où seul l’arrière-plan est visible.</span><span class="sxs-lookup"><span data-stu-id="1b580-120">In other words, because each pixel can only display a single color, each pixel cell is filled with only a single color; if the display were to render the quad exactly as shown, the pixel cells along the quad's edge would need to show two distinct colors: blue where covered by the quad and white where only the background is visible.</span></span>

<span data-ttu-id="1b580-121">Au lieu de cela, le matériel graphique est chargé de déterminer les pixels à remplir pour rapprocher le quad.</span><span class="sxs-lookup"><span data-stu-id="1b580-121">Instead, the graphics hardware is tasked with determining which pixels should be filled to approximate the quad.</span></span> <span data-ttu-id="1b580-122">Ce processus est appelé pixellisation et est détaillé dans les [règles de pixellisation (Direct3D 9)](rasterization-rules.md).</span><span class="sxs-lookup"><span data-stu-id="1b580-122">This process is called rasterization, and is detailed in [Rasterization Rules (Direct3D 9)](rasterization-rules.md).</span></span> <span data-ttu-id="1b580-123">Pour ce cas particulier, le quad pixellisé est représenté dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="1b580-123">For this particular case, the rasterized quad is shown in the following illustration.</span></span>

![illustration d’un Quad non texturé dessiné de (0,0) à (4,4)](images/maptex-fig4.png)

<span data-ttu-id="1b580-125">Notez que le quad passé à Direct3D a des angles à (0, 0) et (4, 4), mais que la sortie pixellisée (l’illustration précédente) contient des angles à (-0.5,-0,5) et (3,5, 3.5).</span><span class="sxs-lookup"><span data-stu-id="1b580-125">Note that the quad passed to Direct3D has corners at (0, 0) and (4, 4), but the rasterized output (the preceding illustration) has corners at (-0.5,-0.5) and (3.5,3.5).</span></span> <span data-ttu-id="1b580-126">Comparez les deux illustrations précédentes pour le rendu des différences.</span><span class="sxs-lookup"><span data-stu-id="1b580-126">Compare the preceding two illustrations for rendering differences.</span></span> <span data-ttu-id="1b580-127">Vous pouvez voir que la taille du rendu de l’affichage est correcte, mais qu’elle a été décalée par les cellules-0,5 dans les directions x et y.</span><span class="sxs-lookup"><span data-stu-id="1b580-127">You can see that what the display actually renders is the correct size, but has been shifted by -0.5 cells in the x and y directions.</span></span> <span data-ttu-id="1b580-128">Toutefois, à l’exception des techniques d’échantillonnage multiple, il s’agit de la meilleure approximation possible du quadruple.</span><span class="sxs-lookup"><span data-stu-id="1b580-128">However, except for multi-sampling techniques, this is the best possible approximation to the quad.</span></span> <span data-ttu-id="1b580-129">(Voir l' [exemple antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) pour une couverture complète de l’échantillonnage multiple.) Sachez que si le rastériseur remplit chaque cellule du quadruple, la zone résultante serait de dimension 5 x 5 au lieu du 4 x 4 souhaité.</span><span class="sxs-lookup"><span data-stu-id="1b580-129">(See the [Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) for thorough coverage of multi-sampling.) Be aware that if the rasterizer filled every cell the quad crossed, the resulting area would be of dimension 5 x 5 instead of the desired 4 x 4.</span></span>

<span data-ttu-id="1b580-130">Si vous supposez que les coordonnées d’écran proviennent de l’angle supérieur gauche de la grille d’affichage au lieu du pixel supérieur gauche, le quadruple s’affiche exactement comme prévu.</span><span class="sxs-lookup"><span data-stu-id="1b580-130">If you assume that screen coordinates originate at the top-left corner of the display grid instead of the top-left pixel, the quad appears exactly as expected.</span></span> <span data-ttu-id="1b580-131">Toutefois, la différence devient évidente lorsque le quadruple reçoit une texture.</span><span class="sxs-lookup"><span data-stu-id="1b580-131">However, the difference becomes clear when the quad is given a texture.</span></span> <span data-ttu-id="1b580-132">L’illustration suivante montre la texture 4 x 4 que vous allez mapper directement sur le quadruple.</span><span class="sxs-lookup"><span data-stu-id="1b580-132">The following illustration shows the 4 x 4 texture you'll map directly onto the quad.</span></span>

![illustration d’une texture 4x4](images/maptex-fig5.png)

<span data-ttu-id="1b580-134">Étant donné que la texture est de 4 x 4 texels et que le quad est de 4 x 4 pixels, vous pouvez vous attendre à ce que le quad texturé apparaisse exactement comme la texture, quel que soit l’emplacement de l’écran où le quadruple est dessiné.</span><span class="sxs-lookup"><span data-stu-id="1b580-134">Because the texture is 4 x 4 texels and the quad is 4 x 4 pixels, you might expect the textured quad to appear exactly like the texture regardless of the location on the screen where the quad is drawn.</span></span> <span data-ttu-id="1b580-135">Toutefois, ce n’est pas le cas. même les modifications mineures de la position influencent le mode d’affichage de la texture.</span><span class="sxs-lookup"><span data-stu-id="1b580-135">However, this is not the case; even slight changes in position influence how the texture is displayed.</span></span> <span data-ttu-id="1b580-136">L’illustration suivante montre comment un quadruple entre (0, 0) et (4, 4) s’affiche après avoir été pixellisé et texturé.</span><span class="sxs-lookup"><span data-stu-id="1b580-136">The following illustration shows how a quad between (0, 0) and (4, 4) is displayed after being rasterized and textured.</span></span>

![illustration d’un Quad texturé dessiné à partir de (0,0) et (4, 4)](images/maptex-fig6.png)

<span data-ttu-id="1b580-138">Le quadruple représenté dans l’illustration précédente montre la sortie texturée (avec un mode de filtrage linéaire et un mode d’adressage de serrage) avec la structure pixellisée superposée.</span><span class="sxs-lookup"><span data-stu-id="1b580-138">The quad drawn in the preceding illustration shows the textured output (with a linear filtering mode and a clamp addressing mode) with the superimposed rasterized outline.</span></span> <span data-ttu-id="1b580-139">Le reste de cet article explique exactement pourquoi la sortie ressemble à la façon dont elle se présente au lieu de regarder la texture, mais pour ceux qui veulent la solution, voici : les bords de la quadruple entrée doivent se trouver sur les lignes limites entre les cellules de pixels.</span><span class="sxs-lookup"><span data-stu-id="1b580-139">The rest of this article explains exactly why the output looks the way it does instead of looking like the texture, but for those who want the solution, here it is: The edges of the input quad need to lie upon the boundary lines between pixel cells.</span></span> <span data-ttu-id="1b580-140">En décalant simplement les coordonnées x et y de-0,5 unités, les cellules texels couvre parfaitement les cellules de pixels et le quad peut être parfaitement recréé à l’écran.</span><span class="sxs-lookup"><span data-stu-id="1b580-140">By simply shifting the x and y quad coordinates by -0.5 units, texel cells will perfectly cover pixel cells and the quad can be perfectly recreated on the screen.</span></span> <span data-ttu-id="1b580-141">(La dernière illustration de cette rubrique montre le Quad aux coordonnées corrigées.)</span><span class="sxs-lookup"><span data-stu-id="1b580-141">(The last illustration in this topic shows the quad at the corrected coordinates.)</span></span>

<span data-ttu-id="1b580-142">Les détails de la raison pour laquelle la sortie pixellisée n’a que peu de similarité avec la texture d’entrée sont directement liés à la façon dont les adresses Direct3D et les textures d’échantillons.</span><span class="sxs-lookup"><span data-stu-id="1b580-142">The details of why the rasterized output only bears slight resemblance to the input texture are directly related to the way Direct3D addresses and samples textures.</span></span> <span data-ttu-id="1b580-143">Ce qui suit suppose que vous avez une bonne compréhension de l' [espace de coordonnées de texture](texture-coordinates.md) et du filtrage de [texture bilinéaire](bilinear-texture-filtering.md).</span><span class="sxs-lookup"><span data-stu-id="1b580-143">What follows assumes you have a good understanding of [texture coordinate space](texture-coordinates.md) And [bilinear texture filtering](bilinear-texture-filtering.md).</span></span>

<span data-ttu-id="1b580-144">En revenons à notre investigation sur la sortie de pixel étrange, il est judicieux de remonter la couleur de sortie vers le nuanceur de pixels : le nuanceur de pixels est appelé pour chaque pixel sélectionné pour faire partie de la forme pixellisée.</span><span class="sxs-lookup"><span data-stu-id="1b580-144">Getting back to our investigation of the strange pixel output, it makes sense to trace the output color back to the pixel shader: The pixel shader is called for each pixel selected to be part of the rasterized shape.</span></span> <span data-ttu-id="1b580-145">Le quadruple bleu plein représenté dans une illustration précédente peut avoir un nuanceur particulièrement simple :</span><span class="sxs-lookup"><span data-stu-id="1b580-145">The solid blue quad depicted in an earlier illustration could have a particularly simple shader:</span></span>


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



<span data-ttu-id="1b580-146">Pour le quad plaqué, le nuanceur de pixels doit être légèrement modifié :</span><span class="sxs-lookup"><span data-stu-id="1b580-146">For the textured quad, the pixel shader has to be changed slightly:</span></span>


```
texture MyTexture;

sampler MySampler = 
sampler_state 
{ 
    Texture = <MyTexture>;
    MinFilter = Linear;
    MagFilter = Linear;
    AddressU = Clamp;
    AddressV = Clamp;
};

float4 TextureLookupPS( float2 vTexCoord : TEXCOORD0 ) : COLOR
{
    return tex2D( MySampler, vTexCoord );
} 
```



<span data-ttu-id="1b580-147">Ce code suppose que la texture 4 x 4 est stockée dans MyTexture.</span><span class="sxs-lookup"><span data-stu-id="1b580-147">That code assumes the 4 x 4 texture is stored in MyTexture.</span></span> <span data-ttu-id="1b580-148">Comme indiqué, l’échantillon de texture MySampler est défini pour effectuer un filtrage bilinéaire sur MyTexture.</span><span class="sxs-lookup"><span data-stu-id="1b580-148">As shown, the MySampler texture sampler is set to perform bilinear filtering on MyTexture.</span></span> <span data-ttu-id="1b580-149">Le nuanceur de pixels est appelé une fois pour chaque pixel pixellisé, et chaque fois que la couleur retournée est la couleur de texture échantillonnée sur vTexCoord.</span><span class="sxs-lookup"><span data-stu-id="1b580-149">The pixel shader gets called once for each rasterized pixel, and each time the returned color is the sampled texture color at vTexCoord.</span></span> <span data-ttu-id="1b580-150">Chaque fois que le nuanceur de pixels est appelé, l’argument vTexCoord est défini sur les coordonnées de texture à ce pixel.</span><span class="sxs-lookup"><span data-stu-id="1b580-150">Each time the pixel shader is called, the vTexCoord argument is set to the texture coordinates at that pixel.</span></span> <span data-ttu-id="1b580-151">Cela signifie que le nuanceur demande à l’échantillonneur de texture la couleur de texture filtrée à l’emplacement exact du pixel, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="1b580-151">That means the shader is asking the texture sampler for the filtered texture color at the exact location of the pixel, as detailed in the following illustration.</span></span>

![illustration des emplacements d’échantillonnage des coordonnées de texture](images/maptex-fig7.png)

<span data-ttu-id="1b580-153">La texture (affichée superposée) est échantillonnée directement aux emplacements de pixels (représentés par des points noirs).</span><span class="sxs-lookup"><span data-stu-id="1b580-153">The texture (shown superimposed) is sampled directly at pixel locations (shown as black dots).</span></span> <span data-ttu-id="1b580-154">Les coordonnées de texture ne sont pas affectées par la pixellisation (elles restent dans l’espace de l’écran projeté du Quad d’origine).</span><span class="sxs-lookup"><span data-stu-id="1b580-154">Texture coordinates are not affected by rasterization (they remain in the projected screen-space of the original quad).</span></span> <span data-ttu-id="1b580-155">Les points noirs indiquent où se trouvent les pixels de pixellisation.</span><span class="sxs-lookup"><span data-stu-id="1b580-155">The black dots show where the rasterization pixels are.</span></span> <span data-ttu-id="1b580-156">Les coordonnées de texture à chaque pixel sont facilement déterminées en interpolant les coordonnées stockées à chaque vertex : le pixel à (0,0) coïncide avec le vertex à (0,0); par conséquent, les coordonnées de texture à ce pixel sont simplement les coordonnées de texture stockées sur ce vertex, UV (0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="1b580-156">The texture coordinates at each pixel are easily determined by interpolating the coordinates stored at each vertex: The pixel at (0,0) coincides with the vertex at (0, 0); therefore, the texture coordinates at that pixel are simply the texture coordinates stored at that vertex, UV (0.0, 0.0).</span></span> <span data-ttu-id="1b580-157">Pour le pixel à (3, 1), les coordonnées interpolées sont UV (0,75, 0,25), car ce pixel se situe à trois quarts de la largeur de la texture et d’un quart de sa hauteur.</span><span class="sxs-lookup"><span data-stu-id="1b580-157">For the pixel at (3, 1), the interpolated coordinates are UV (0.75, 0.25) because that pixel is located at three-fourths of the texture's width and one-fourth of its height.</span></span> <span data-ttu-id="1b580-158">Ces coordonnées interpolées sont celles qui sont passées au nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="1b580-158">These interpolated coordinates are what get passed to the pixel shader.</span></span>

<span data-ttu-id="1b580-159">Les texels ne sont pas alignés avec les pixels de cet exemple ; chaque pixel (et par conséquent, chaque point d’échantillonnage) est positionné à l’angle de quatre texels.</span><span class="sxs-lookup"><span data-stu-id="1b580-159">The texels do not line up with the pixels in this example; each pixel (and therefore each sampling point) is positioned at the corner of four texels.</span></span> <span data-ttu-id="1b580-160">Étant donné que le mode de filtrage est défini sur linéaire, l’échantillonneur calcule la moyenne des couleurs des quatre texels partageant cet angle.</span><span class="sxs-lookup"><span data-stu-id="1b580-160">Because the filtering mode is set to Linear, the sampler will average the colors of the four texels sharing that corner.</span></span> <span data-ttu-id="1b580-161">Cela explique pourquoi le pixel attendu est en fait trois-quarts gris plus un quart rouge, le pixel supposé être vert est un demi-gris plus un quart rouge plus un quart de vert, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="1b580-161">This explains why the pixel expected to be red is actually three-fourths gray plus one-fourth red, the pixel expected to be green is one-half gray plus one-fourth red plus one-fourth green, and so on.</span></span>

<span data-ttu-id="1b580-162">Pour résoudre ce problème, il vous suffit de mapper correctement le Quad aux pixels sur lesquels il sera pixellisé et de mapper correctement les texels sur les pixels.</span><span class="sxs-lookup"><span data-stu-id="1b580-162">To fix this problem, all you need to do is correctly map the quad to the pixels to which it will be rasterized, and thereby correctly map the texels to pixels.</span></span> <span data-ttu-id="1b580-163">L’illustration suivante montre les résultats du dessin du même quadruple entre (-0,5,-0,5) et (3,5, 3,5), qui est le quadruple à partir du début.</span><span class="sxs-lookup"><span data-stu-id="1b580-163">The following illustration shows the results of drawing the same quad between (-0.5, -0.5) and (3.5, 3.5), which is the quad intended from the outset.</span></span>

![illustration d’un Quad texturé qui correspond au Quad pixellisé](images/maptex-fig8.png)

<span data-ttu-id="1b580-165">L’illustration ci-dessus montre que le quad (indiqué dans (-0,5,-0,5) à (3,5, 3,5)) correspond exactement à la zone pixellisée.</span><span class="sxs-lookup"><span data-stu-id="1b580-165">The preceding illustration demonstrates that the quad (shown outlined from (-0.5, -0.5) to (3.5, 3.5)) exactly matches the rasterized area.</span></span>

## <a name="summary"></a><span data-ttu-id="1b580-166">Résumé</span><span class="sxs-lookup"><span data-stu-id="1b580-166">Summary</span></span>

<span data-ttu-id="1b580-167">En résumé, les pixels et les texels sont en fait des points, pas des blocs solides.</span><span class="sxs-lookup"><span data-stu-id="1b580-167">In summary, pixels and texels are actually points, not solid blocks.</span></span> <span data-ttu-id="1b580-168">L’espace à l’écran provient du pixel supérieur gauche, mais les coordonnées de texture proviennent de l’angle supérieur gauche de la grille de la texture.</span><span class="sxs-lookup"><span data-stu-id="1b580-168">Screen space originates at the top-left pixel, but texture coordinates originate at the top-left corner of the texture's grid.</span></span> <span data-ttu-id="1b580-169">Plus important encore, n’oubliez pas de soustraire 0,5 unités des composants x et y de vos positions de vertex lorsque vous travaillez dans un espace d’écran transformé afin d’aligner correctement les éléments de texture avec les pixels.</span><span class="sxs-lookup"><span data-stu-id="1b580-169">Most importantly, remember to subtract 0.5 units from the x and y components of your vertex positions when working in transformed screen space in order to correctly align texels with pixels.</span></span>

<span data-ttu-id="1b580-170">Le code suivant est un exemple de décalage des vertex d’un carré 256 par 256 pour afficher correctement une texture 256 par 256 dans l’espace d’écran transformé.</span><span class="sxs-lookup"><span data-stu-id="1b580-170">The following code is an example of offsetting the vertices of a 256 by 256 square to properly display a 256 by 256 texture in transformed screen space.</span></span>


```C++
//define FVF with vertex values in transformed screen space
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW|D3DFVF_TEX1)

struct CUSTOMVERTEX
{
    FLOAT x, y, z, rhw; // position
    FLOAT tu, tv;       // texture coordinates
};

//unadjusted vertex values
float left = 0.0f;
float right = 255.0f;
float top = 0.0f;
float bottom = 255.0f;


//256 by 256 rectangle matching 256 by 256 texture
CUSTOMVERTEX vertices[] =
{
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f}, // x, y, z, rhw, u, v
    { right, top,    0.5f, 1.0f, 1.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  bottom, 0.5f, 1.0f, 0.0f, 1.0f},
    
};
```




```C++
//adjust all the vertices to correctly line up texels with pixels 
for (int i=0; i<6; i++)
{
    vertices[i].x -= 0.5f;
    vertices[i].y -= 0.5f;
}
```



## <a name="related-topics"></a><span data-ttu-id="1b580-171">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b580-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b580-172">Coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="1b580-172">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



