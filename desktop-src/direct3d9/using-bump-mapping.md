---
description: Utilisation du mappage de relief (Direct3D 9)
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: Utilisation du mappage de relief (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4bc96f78ffb19dda04ff6b2bc3d0e46800b04b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482673"
---
# <a name="using-bump-mapping-direct3d-9"></a><span data-ttu-id="ccc46-103">Utilisation du mappage de relief (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ccc46-103">Using Bump Mapping (Direct3D 9)</span></span>

## <a name="detecting-support-for-bump-mapping"></a><span data-ttu-id="ccc46-104">Détection de la prise en charge du mappage de relief</span><span class="sxs-lookup"><span data-stu-id="ccc46-104">Detecting Support for Bump Mapping</span></span>

<span data-ttu-id="ccc46-105">Un appareil peut effectuer un mappage de relief s’il prend en charge l' \_ opération de fusion de texture D3DTOP BUMPENVMAP ou D3DTOP \_ BUMPENVMAPLUMINANCE.</span><span class="sxs-lookup"><span data-stu-id="ccc46-105">A device can perform bump mapping if it supports either the D3DTOP\_BUMPENVMAP or D3DTOP\_BUMPENVMAPLUMINANCE texture blending operation.</span></span> <span data-ttu-id="ccc46-106">Utilisez [**IDirect3D9 :: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) avec \_ la requête D3DUSAGE \_ LEGACYBUMPMAP pour voir si un format est pris en charge pour le mappage de relief.</span><span class="sxs-lookup"><span data-stu-id="ccc46-106">Use [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_LEGACYBUMPMAP to see if a format is supported for bump mapping.</span></span>

<span data-ttu-id="ccc46-107">En outre, les applications doivent vérifier les fonctionnalités de l’appareil pour s’assurer que l’appareil prend en charge un nombre approprié d’étapes de fusion, en général au moins trois, et expose au moins un format de pixel de mappage de rugosité.</span><span class="sxs-lookup"><span data-stu-id="ccc46-107">Additionally, applications should check the device capabilities to make sure the device supports an appropriate number of blending stages, usually at least three, and exposes at least one bump-mapping pixel format.</span></span>

<span data-ttu-id="ccc46-108">L’exemple de code suivant vérifie les fonctionnalités de l’appareil pour détecter la prise en charge du mappage de relief dans le périphérique actuel, à l’aide des critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="ccc46-108">The following code example checks device capabilities to detect support for bump mapping in the current device, using the given criteria.</span></span>


```
BOOL SupportsBumpMapping()
{
    D3DCAPS9 d3dCaps;

    d3dDevice->GetDeviceCaps( &d3dCaps );

    // Does this device support the two bump mapping blend operations?
    if ( 0 == d3dCaps.TextureOpCaps & ( D3DTEXOPCAPS_BUMPENVMAP |
                                            D3DTEXOPCAPS_BUMPENVMAPLUMINANCE ))
        return FALSE;

    // Does this device support up to three blending stages?
    if( d3dCaps.MaxTextureBlendStages < 3 )
        return FALSE;

    return TRUE;
}
```



## <a name="creating-a-bump-map-texture"></a><span data-ttu-id="ccc46-109">Création d’une texture de placage de relief</span><span class="sxs-lookup"><span data-stu-id="ccc46-109">Creating a Bump Map Texture</span></span>

<span data-ttu-id="ccc46-110">Vous créez une texture de placage de relief comme n’importe quelle autre texture.</span><span class="sxs-lookup"><span data-stu-id="ccc46-110">You create a bump map texture like any other texture.</span></span> <span data-ttu-id="ccc46-111">Votre application vérifie la prise en charge du mappage de relief et récupère un format de pixel valide, comme indiqué dans détection de la prise en charge du mappage de relief.</span><span class="sxs-lookup"><span data-stu-id="ccc46-111">Your application verifies support for bump mapping and retrieves a valid pixel format, as discussed in Detecting Support for Bump Mapping.</span></span>

<span data-ttu-id="ccc46-112">Une fois la surface créée, vous pouvez charger chaque pixel avec les valeurs Delta appropriées et la luminance, si le format de surface comprend la luminance.</span><span class="sxs-lookup"><span data-stu-id="ccc46-112">After the surface is created, you can load each pixel with the appropriate delta values, and luminance, if the surface format includes luminance.</span></span> <span data-ttu-id="ccc46-113">Les valeurs de chaque composant de pixel sont décrites dans formats de pixel de la [carte de relief (Direct3D 9)](bump-map-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="ccc46-113">The values for each pixel component are described in [Bump Map Pixel Formats (Direct3D 9)](bump-map-pixel-formats.md).</span></span>

## <a name="configuring-bump-mapping-parameters"></a><span data-ttu-id="ccc46-114">Configuration des paramètres de mappage de relief</span><span class="sxs-lookup"><span data-stu-id="ccc46-114">Configuring Bump Mapping Parameters</span></span>

<span data-ttu-id="ccc46-115">Lorsque votre application a créé une carte de relief et défini le contenu de chaque pixel, vous pouvez préparer le rendu en configurant des paramètres de mappage de relief.</span><span class="sxs-lookup"><span data-stu-id="ccc46-115">When your application has created a bump map and set the contents of each pixel, you can prepare for rendering by configuring bump mapping parameters.</span></span> <span data-ttu-id="ccc46-116">Les paramètres de mappage de relief incluent la définition des textures requises et leurs opérations de fusion, ainsi que des contrôles de transformation et de luminance pour le placage de relief lui-même.</span><span class="sxs-lookup"><span data-stu-id="ccc46-116">Bump mapping parameters include setting the required textures and their blending operations, as well as the transformation and luminance controls for the bump map itself.</span></span>

1.  <span data-ttu-id="ccc46-117">Définir la carte de texture de base si elle est utilisée, le mappage de relief et les textures de la carte d’environnement en étapes de fusion de texture.</span><span class="sxs-lookup"><span data-stu-id="ccc46-117">Set the base texture map if used, bump map, and environment map textures into texture blending stages.</span></span>
2.  <span data-ttu-id="ccc46-118">Définissez la couleur et les opérations de fusion alpha pour chaque étape de texture.</span><span class="sxs-lookup"><span data-stu-id="ccc46-118">Set the color and alpha blending operations for each texture stage.</span></span>
3.  <span data-ttu-id="ccc46-119">Définissez la matrice de transformation de la carte de relief.</span><span class="sxs-lookup"><span data-stu-id="ccc46-119">Set the bump map transformation matrix.</span></span>
4.  <span data-ttu-id="ccc46-120">Définissez les valeurs de l’échelle de luminance et du décalage en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="ccc46-120">Set the luminance scale and offset values as needed.</span></span>

<span data-ttu-id="ccc46-121">L’exemple de code suivant définit trois textures (la carte de texture de base, la carte de relief et une carte d’environnement spéculaire) sur les étapes de fusion de texture appropriées.</span><span class="sxs-lookup"><span data-stu-id="ccc46-121">The following code example sets three textures (the base texture map, the bump map, and a specular environment map) to the appropriate texture blending stages.</span></span>


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



<span data-ttu-id="ccc46-122">Après avoir défini les textures à leurs étapes de fusion, l’exemple de code suivant prépare les opérations de fusion et les arguments pour chaque étape.</span><span class="sxs-lookup"><span data-stu-id="ccc46-122">After setting the textures to their blending stages, the following code example prepares the blending operations and arguments for each stage.</span></span>


```
// Set the color operations and arguments to prepare for
//   bump mapping.

// Stage 0: The base texture
d3dDevice->SetTextureStageState( 0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAOP, D3DTOP_SELECTARG1 );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE ); 
d3dDevice->SetTextureStageState( 0, D3DTSS_TEXCOORDINDEX, 1 );

// Stage 1: The bump map - Use luminance for this example.
d3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_BUMPENVMAPLUMINANCE);
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Stage 2: A specular environment map
d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX, 0 );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



<span data-ttu-id="ccc46-123">Lorsque les arguments et opérations de fusion sont définis, l’exemple de code suivant définit la matrice de mappage de rugosité 2x2 sur la matrice d’identité en définissant les \_ membres D3DTSS BUMPENVMAPMAT00 et D3DTSS \_ BUMPENVMAPMAT11 de [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="ccc46-123">When the blending operations and arguments are set, the following code example sets the 2x2 bump mapping matrix to the identity matrix by setting the D3DTSS\_BUMPENVMAPMAT00 and the D3DTSS\_BUMPENVMAPMAT11 members of [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) to 1.0.</span></span> <span data-ttu-id="ccc46-124">Si vous affectez à la matrice l’identité, le système utilise les valeurs Delta de la carte de relief non modifiées, mais cela n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ccc46-124">Setting the matrix to the identity causes the system to use the delta values in the bump map unmodified, but this is not a requirement.</span></span>


```
// Set the bump mapping matrix.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT00, F2DW(1.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT01, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT10, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT11, F2DW(1.0f) );
```



<span data-ttu-id="ccc46-125">Si vous définissez l’opération de mappage de bosselage pour inclure la luminance (D3DTOP \_ BUMPENVMAPLUMINANCE), vous devez définir les contrôles de luminance.</span><span class="sxs-lookup"><span data-stu-id="ccc46-125">If you set the bump mapping operation to include luminance (D3DTOP\_BUMPENVMAPLUMINANCE), you must set the luminance controls.</span></span> <span data-ttu-id="ccc46-126">Les commandes de luminance configurent la façon dont le système calcule la luminance avant de moduler la couleur à partir de la texture à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="ccc46-126">The luminance controls configure how the system computes luminance before modulating the color from the texture in the next stage.</span></span> <span data-ttu-id="ccc46-127">Pour plus d’informations, consultez [formules de mappage de relief (Direct3D 9)](bump-mapping-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="ccc46-127">For details, see [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md).</span></span>


```
// Set luminance controls. This is only needed when using
// a bump map that contains luminance, and when the 
// D3DTOP_BUMPENVMAPLUMINANCE texture blending operation is
// being used.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLSCALE, F2DW(0.5f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLOFFSET, F2DW(0.0f) );
```



<span data-ttu-id="ccc46-128">Une fois que votre application a configuré les paramètres de mappage de bosselage, elle peut s’afficher normalement, et les polygones rendus en relief.</span><span class="sxs-lookup"><span data-stu-id="ccc46-128">After your application configures bump mapping parameters, it can render as normal, and the rendered polygons receive bump mapping effects.</span></span>

<span data-ttu-id="ccc46-129">Notez que l’exemple précédent montre les paramètres définis pour le mappage d’environnement spéculaire.</span><span class="sxs-lookup"><span data-stu-id="ccc46-129">Note that the preceding example shows parameters set for specular environment mapping.</span></span> <span data-ttu-id="ccc46-130">Lors de l’exécution d’un mappage de lumière diffuse, les applications définissent l’opération de fusion de texture pour la dernière étape en \_ modulant D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="ccc46-130">When performing diffuse light mapping, applications set the texture blending operation for the last stage to D3DTOP\_MODULATE.</span></span> <span data-ttu-id="ccc46-131">Pour plus d’informations, consultez les [cartes de lumière diffuse (Direct3D 9)](diffuse-light-maps.md).</span><span class="sxs-lookup"><span data-stu-id="ccc46-131">For more information, see [Diffuse Light Maps (Direct3D 9)](diffuse-light-maps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccc46-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ccc46-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccc46-133">Placage de relief</span><span class="sxs-lookup"><span data-stu-id="ccc46-133">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 
