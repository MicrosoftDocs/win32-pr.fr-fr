---
description: Le brouillard de pixel obtient son nom du fait qu’il est calculé en fonction de chaque pixel dans le pilote de périphérique.
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: Brouillard de pixel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f62a597820fa009207d8dda7836d161cdf34c88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845734"
---
# <a name="pixel-fog-direct3d-9"></a><span data-ttu-id="fc639-103">Brouillard de pixel (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fc639-103">Pixel Fog (Direct3D 9)</span></span>

<span data-ttu-id="fc639-104">Le brouillard de pixel obtient son nom du fait qu’il est calculé en fonction de chaque pixel dans le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="fc639-104">Pixel fog gets its name from the fact that it is calculated on a per-pixel basis in the device driver.</span></span> <span data-ttu-id="fc639-105">Cela est différent du brouillard de vertex, qui est calculé par le pipeline pendant les calculs de transformation et d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="fc639-105">This is different from vertex fog, which is computed by the pipeline during transformation and lighting calculations.</span></span> <span data-ttu-id="fc639-106">Le brouillard de pixel est parfois appelé « voile de table », car certains pilotes utilisent une table de recherche précalculée pour déterminer le facteur de brouillard, en utilisant la profondeur de chaque pixel à appliquer dans le calcul de la fusion.</span><span class="sxs-lookup"><span data-stu-id="fc639-106">Pixel fog is sometimes called table fog because some drivers use a precalculated lookup table to determine the fog factor, using the depth of each pixel to apply in blending computations.</span></span> <span data-ttu-id="fc639-107">Elle peut être appliquée à l’aide de toute formule de brouillard identifiée par les membres du type énuméré [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="fc639-107">It can be applied using any fog formula identified by members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="fc639-108">Les implémentations de ces formules sont spécifiques au pilote.</span><span class="sxs-lookup"><span data-stu-id="fc639-108">The implementations of these formulas are driver-specific.</span></span> <span data-ttu-id="fc639-109">Si un pilote ne prend pas en charge une formule de brouillard complexe, il doit se dégrader par une formule moins complexe.</span><span class="sxs-lookup"><span data-stu-id="fc639-109">If a driver doesn't support a complex fog formula, it should degrade to a less complex formula.</span></span>

## <a name="eye-relative-vs-z-based-depth"></a><span data-ttu-id="fc639-110">Eye-Relative différences par rapport à la profondeur Z</span><span class="sxs-lookup"><span data-stu-id="fc639-110">Eye-Relative vs. Z-Based Depth</span></span>

<span data-ttu-id="fc639-111">Pour atténuer les artefacts graphiques liés au brouillard provoqués par une répartition inégale des valeurs z dans un tampon de profondeur, la plupart des périphériques matériels utilisent une profondeur relative à l’oeil au lieu des valeurs de profondeur basées sur z pour le brouillard de pixel.</span><span class="sxs-lookup"><span data-stu-id="fc639-111">To alleviate fog-related graphic artifacts caused by uneven distribution of z-values in a depth buffer, most hardware devices use eye-relative depth instead of z-based depth values for pixel fog.</span></span> <span data-ttu-id="fc639-112">La profondeur relative à l’oeil est essentiellement l’élément w d’un jeu de coordonnées homogène.</span><span class="sxs-lookup"><span data-stu-id="fc639-112">Eye-relative depth is essentially the w element from a homogeneous coordinate set.</span></span> <span data-ttu-id="fc639-113">Microsoft Direct3D prend la réciproque de l’élément RHW à partir d’un jeu de coordonnées de l’espace de l’appareil pour reproduire true w.</span><span class="sxs-lookup"><span data-stu-id="fc639-113">Microsoft Direct3D takes the reciprocal of the RHW element from a device space coordinate set to reproduce true w.</span></span> <span data-ttu-id="fc639-114">Si un appareil prend en charge le brouillard relatif à Eye, il définit l’indicateur **D3DPRASTERCAPS \_ WFOG** dans le membre RasterCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) lorsque vous appelez la méthode [**IDirect3DDevice9 :: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="fc639-114">If a device supports eye-relative fog, it sets the **D3DPRASTERCAPS\_WFOG** flag in the RasterCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="fc639-115">À l’exception du rastériseur de référence, les périphériques logiciels utilisent toujours z pour calculer les effets de brouillard de pixel.</span><span class="sxs-lookup"><span data-stu-id="fc639-115">With the exception of the reference rasterizer, software devices always use z to calculate pixel fog effects.</span></span>

<span data-ttu-id="fc639-116">Lorsque le brouillard relatif à l’oeil est pris en charge, le système utilise automatiquement la profondeur relative à l’oeil plutôt que la profondeur basée sur z Si la matrice de projection fournie produit des valeurs z dans l’espace universel qui sont équivalentes aux valeurs w dans l’espace de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fc639-116">When eye-relative fog is supported, the system automatically uses eye-relative depth rather than z-based depth if the provided projection matrix produces z-values in world space that are equivalent to w-values in device space.</span></span> <span data-ttu-id="fc639-117">Vous définissez la matrice de projection en appelant la méthode [**IDirect3DDevice9 :: setTransform**](/windows/desktop/api) , en utilisant la \_ valeur de projection D3DTS et en passant une structure [**D3DMATRIX**](d3dmatrix.md) qui représente la matrice souhaitée.</span><span class="sxs-lookup"><span data-stu-id="fc639-117">You set the projection matrix by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method, using the D3DTS\_PROJECTION value and passing a [**D3DMATRIX**](d3dmatrix.md) structure that represents the desired matrix.</span></span> <span data-ttu-id="fc639-118">Si la matrice de projection n’est pas conforme à cette exigence, les effets de brouillard ne sont pas appliqués correctement.</span><span class="sxs-lookup"><span data-stu-id="fc639-118">If the projection matrix isn't compliant with this requirement, fog effects are not applied properly.</span></span> <span data-ttu-id="fc639-119">Pour plus d’informations sur la génération d’une matrice conforme, consultez [projection Transform (Direct3D 9)](projection-transform.md).</span><span class="sxs-lookup"><span data-stu-id="fc639-119">For details about producing a compliant matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

<span data-ttu-id="fc639-120">Direct3D utilise la matrice de projection actuellement définie dans ses calculs de profondeur basés sur w.</span><span class="sxs-lookup"><span data-stu-id="fc639-120">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="fc639-121">Par conséquent, une application doit définir une matrice de projection conforme pour recevoir les fonctionnalités w souhaitées, même si elle n’utilise pas le pipeline de transformation Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fc639-121">As a result, an application must set a compliant projection matrix to receive the desired w-based features, even if it does not use the Direct3D transformation pipeline.</span></span>

<span data-ttu-id="fc639-122">Direct3D vérifie la quatrième colonne de la matrice de projection.</span><span class="sxs-lookup"><span data-stu-id="fc639-122">Direct3D checks the fourth column of the projection matrix.</span></span> <span data-ttu-id="fc639-123">Si les coefficients sont 0, 0, \[ 0, 1 \] (pour une projection affine), le système utilise des valeurs de profondeur basées sur z pour le brouillard.</span><span class="sxs-lookup"><span data-stu-id="fc639-123">If the coefficients are \[0,0,0,1\] (for an affine projection) the system will use z-based depth values for fog.</span></span> <span data-ttu-id="fc639-124">Dans ce cas, vous devez également spécifier les distances de début et de fin pour les effets de brouillard linéaires dans l’espace de l’appareil, qui s’étend de 0,0 au point le plus proche de l’utilisateur, et 1,0 au point le plus éloigné.</span><span class="sxs-lookup"><span data-stu-id="fc639-124">In this case, you must also specify the start and end distances for linear fog effects in device space, which ranges from 0.0 at the nearest point to the user, and 1.0 at the farthest point.</span></span>

## <a name="using-pixel-fog"></a><span data-ttu-id="fc639-125">Utilisation du brouillard de pixel</span><span class="sxs-lookup"><span data-stu-id="fc639-125">Using Pixel Fog</span></span>

<span data-ttu-id="fc639-126">Utilisez les étapes suivantes pour activer le brouillard de pixel dans votre application.</span><span class="sxs-lookup"><span data-stu-id="fc639-126">Use the following steps to enable pixel fog in your application.</span></span>

1.  <span data-ttu-id="fc639-127">Activez la fusion de brouillard en affectant \_ à l’état de rendu D3DRS FOGENABLE la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="fc639-127">Enable fog blending by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span>
2.  <span data-ttu-id="fc639-128">Définissez la couleur de brouillard souhaitée dans l' \_ État de rendu D3DRS FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="fc639-128">Set the desired fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="fc639-129">Choisissez la formule de brouillard à utiliser en affectant \_ à l’état de rendu D3DRS FOGTABLEMODE le membre correspondant du type énuméré [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="fc639-129">Choose the fog formula to use by setting the D3DRS\_FOGTABLEMODE render state to the corresponding member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="fc639-130">Définissez les paramètres de brouillard comme vous le souhaitez pour le mode de brouillard sélectionné dans les États de rendu associés.</span><span class="sxs-lookup"><span data-stu-id="fc639-130">Set the fog parameters as desired for the selected fog mode in the associated render states.</span></span> <span data-ttu-id="fc639-131">Cela comprend les distances de début et de fin pour le brouillard linéaire et la densité de brouillard pour le mode de brouillard exponentiel.</span><span class="sxs-lookup"><span data-stu-id="fc639-131">This includes the start and end distances for linear fog, and fog density for exponential fog mode.</span></span>

<span data-ttu-id="fc639-132">L’exemple suivant montre à quoi ces étapes peuvent ressembler dans le code.</span><span class="sxs-lookup"><span data-stu-id="fc639-132">The following example shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupPixelFog(DWORD Color, DWORD Mode)
{
    float Start   = 0.5f;    // For linear mode
    float End     = 0.8f;
    float Density = 0.66f;   // For exponential modes
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if( Mode == D3DFOG_LINEAR )
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }
```



<span data-ttu-id="fc639-133">Certains paramètres de brouillard sont requis comme valeurs à virgule flottante, même si la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte uniquement des valeurs DWORD dans le deuxième paramètre.</span><span class="sxs-lookup"><span data-stu-id="fc639-133">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts only DWORD values in the second parameter.</span></span> <span data-ttu-id="fc639-134">L’exemple précédent fournit les valeurs à virgule flottante à **IDirect3DDevice9 :: SetRenderState** sans traduction de données en convertissant les adresses des variables à virgule flottante en pointeurs DWORD, puis en les déréférençant.</span><span class="sxs-lookup"><span data-stu-id="fc639-134">The preceding example provides the floating-point values to **IDirect3DDevice9::SetRenderState** without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc639-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc639-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc639-136">Types de brouillard</span><span class="sxs-lookup"><span data-stu-id="fc639-136">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
