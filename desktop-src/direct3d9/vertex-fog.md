---
description: Lorsque le système exécute un sommet, il applique des calculs de brouillard à chaque vertex d’un polygone, puis interpole les résultats sur la face du polygone pendant la pixellisation.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: Brouillard du vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35cd880bda7ebffd36bd95bec5f8565e104eaa15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108391"
---
# <a name="vertex-fog-direct3d-9"></a><span data-ttu-id="1a6b5-103">Brouillard du vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1a6b5-103">Vertex Fog (Direct3D 9)</span></span>

<span data-ttu-id="1a6b5-104">Lorsque le système exécute un sommet, il applique des calculs de brouillard à chaque vertex d’un polygone, puis interpole les résultats sur la face du polygone pendant la pixellisation.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-104">When the system performs vertex fogging, it applies fog calculations at each vertex in a polygon, and then interpolates the results across the face of the polygon during rasterization.</span></span> <span data-ttu-id="1a6b5-105">Les effets de brouillard du vertex sont calculés par le moteur de transformation et l’éclairage Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-105">Vertex fog effects are computed by the Direct3D lighting and transformation engine.</span></span> <span data-ttu-id="1a6b5-106">Pour plus d’informations, consultez [paramètres de brouillard (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1a6b5-106">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="1a6b5-107">Si votre application n’utilise pas Direct3D pour la transformation et l’éclairage, l’application doit effectuer des calculs de brouillard.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-107">If your application does not use Direct3D for transformation and lighting, the application must perform fog calculations.</span></span> <span data-ttu-id="1a6b5-108">Dans ce cas, placez le facteur de brouillard calculé dans le composant alpha de la couleur spéculaire pour chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-108">In this case, place the fog factor that is computed in the alpha component of the specular color for each vertex.</span></span> <span data-ttu-id="1a6b5-109">Vous êtes libre d’utiliser les formules que vous souhaitez, volumétriques ou autres.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-109">You are free to use whatever formulas you want - range-based, volumetric, or otherwise.</span></span> <span data-ttu-id="1a6b5-110">Direct3D utilise le facteur de brouillard fourni pour effectuer une interpolation sur la face de chaque polygone.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-110">Direct3D uses the supplied fog factor to interpolate across the face of each polygon.</span></span> <span data-ttu-id="1a6b5-111">Les applications qui effectuent leur propre transformation et éclairage doivent également effectuer leurs propres calculs de brouillard de vertex.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-111">Applications that perform their own transformation and lighting must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="1a6b5-112">Par conséquent, une telle application a besoin uniquement d’activer la fusion de brouillard et de définir la couleur du brouillard via les États de rendu associés, comme décrit dans [mélange de brouillards (Direct3D 9)](fog-blending.md) et [couleur de brouillard (Direct3D 9)](fog-color.md).</span><span class="sxs-lookup"><span data-stu-id="1a6b5-112">As a result, such an application need only enable fog blending and set the fog color through the associated render states, as described in [Fog Blending (Direct3D 9)](fog-blending.md) and [Fog Color (Direct3D 9)](fog-color.md).</span></span>

> [!Note]  
> <span data-ttu-id="1a6b5-113">Quand vous utilisez un nuanceur de sommets, vous devez utiliser le brouillard de vertex.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-113">When using a vertex shader, you must use vertex fog.</span></span> <span data-ttu-id="1a6b5-114">Pour ce faire, utilisez le nuanceur de sommets pour écrire l’intensité de brouillard par vertex dans le registre oFog.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-114">This is accomplished by using the vertex shader to write the per-vertex fog intensity to the oFog register.</span></span> <span data-ttu-id="1a6b5-115">Une fois le nuanceur de pixels terminé, les données oFog sont utilisées pour effectuer une interpolation linéaire avec la couleur de brouillard.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-115">After the pixel shader completes, the oFog data is used to linearly interpolate with the fog color.</span></span> <span data-ttu-id="1a6b5-116">Cette intensité n’est pas disponible dans un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-116">This intensity is not available in a pixel shader.</span></span>

 

## <a name="range-based-fog"></a><span data-ttu-id="1a6b5-117">Brouillard Range-Based</span><span class="sxs-lookup"><span data-stu-id="1a6b5-117">Range-Based Fog</span></span>

> [!Note]  
> <span data-ttu-id="1a6b5-118">Direct3D utilise des calculs de brouillard basés sur une plage uniquement lors de l’utilisation du brouillard de vertex avec la transformation et le moteur d’éclairage Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-118">Direct3D uses range-based fog calculations only when using vertex fog with the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="1a6b5-119">Cela est dû au fait que le brouillard de pixel est implémenté dans le pilote de périphérique et qu’il n’existe pas de matériel pour prendre en charge le brouillard basé sur une plage par pixel.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-119">This is because pixel fog is implemented in the device driver, and no hardware currently exists to support per-pixel range-based fog.</span></span> <span data-ttu-id="1a6b5-120">Si votre application effectue sa propre transformation et éclairage, elle doit effectuer ses propres calculs de brouillard, en fonction de la plage ou dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-120">If your application performs its own transformation and lighting, it must perform its own fog calculations, range-based or otherwise.</span></span>

 

<span data-ttu-id="1a6b5-121">Parfois, l’utilisation de brouillard peut introduire des artefacts graphiques qui entraînent la fusion des objets avec la couleur de brouillard de manière peu intuitive.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-121">Sometimes, using fog can introduce graphic artifacts that cause objects to be blended with the fog color in nonintuitive ways.</span></span> <span data-ttu-id="1a6b5-122">Par exemple, Imaginez une scène dans laquelle il y a deux objets visibles : un qui est suffisamment éloigné pour être affecté par le brouillard, et l’autre presque suffisamment pour ne pas être affecté.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-122">For example, imagine a scene in which there are two visible objects: one distant enough to be affected by fog, and the other near enough to be unaffected.</span></span> <span data-ttu-id="1a6b5-123">Si la zone d’affichage pivote sur place, les effets de brouillard apparent peuvent changer, même si les objets sont stationnaires.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-123">If the viewing area rotates in place, the apparent fog effects can change, even if the objects are stationary.</span></span> <span data-ttu-id="1a6b5-124">Le diagramme suivant montre une vue verticale d’une telle situation.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-124">The following diagram shows a top-down view of such a situation.</span></span>

![diagramme de deux points de vue et de la façon dont ils affectent le brouillard pour deux objets](images/artifog.png)

<span data-ttu-id="1a6b5-126">Le brouillard basé sur une plage est un moyen plus précis et plus précis de déterminer les effets de brouillard.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-126">Range-based fog is another, more accurate, way to determine the fog effects.</span></span> <span data-ttu-id="1a6b5-127">Dans le brouillard basé sur une plage, Direct3D utilise la distance réelle entre le point de vue et un vertex pour ses calculs de brouillard.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-127">In range-based fog, Direct3D uses the actual distance from the viewpoint to a vertex for its fog calculations.</span></span> <span data-ttu-id="1a6b5-128">Direct3D augmente l’effet du brouillard au fur et à mesure que la distance entre les deux points augmente, plutôt que la profondeur du vertex dans la scène, évitant ainsi les artefacts de rotation.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-128">Direct3D increases the effect of fog as the distance between the two points increases, rather than the depth of the vertex within in the scene, thereby avoiding rotational artifacts.</span></span>

<span data-ttu-id="1a6b5-129">Si l’appareil actuel prend en charge le brouillard basé sur une plage, il définit la \_ valeur FOGRANGE D3DPRASTERCAPS dans le membre RasterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) lorsque vous appelez la méthode [**IDirect3DDevice9 :: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="1a6b5-129">If the current device supports range-based fog, it will set the D3DPRASTERCAPS\_FOGRANGE value in the RasterCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="1a6b5-130">Pour activer le brouillard basé sur une plage, définissez l' \_ État de rendu D3DRS RANGEFOGENABLE sur **true**.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-130">To enable range-based fog, set the D3DRS\_RANGEFOGENABLE render state to **TRUE**.</span></span>

<span data-ttu-id="1a6b5-131">Le brouillard basé sur une plage est calculé par Direct3D pendant la transformation et l’éclairage.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-131">Range-based fog is computed by Direct3D during transformation and lighting.</span></span> <span data-ttu-id="1a6b5-132">Les applications qui n’utilisent pas la transformation et le moteur d’éclairage Direct3D doivent également effectuer leurs propres calculs de brouillard de vertex.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-132">Applications that don't use the Direct3D transformation and lighting engine must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="1a6b5-133">Dans ce cas, fournissez le facteur de brouillard basé sur une plage dans le composant alpha du composant spéculaire pour chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-133">In this case, provide the range-based fog factor in the alpha component of the specular component for each vertex.</span></span>

## <a name="using-vertex-fog"></a><span data-ttu-id="1a6b5-134">Utilisation du brouillard du vertex</span><span class="sxs-lookup"><span data-stu-id="1a6b5-134">Using Vertex Fog</span></span>

<span data-ttu-id="1a6b5-135">Utilisez les étapes suivantes pour activer le brouillard de vertex dans votre application.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-135">Use the following steps to enable vertex fog in your application.</span></span>

1.  <span data-ttu-id="1a6b5-136">Activez la fusion de brouillard en affectant \_ à D3DRS FOGENABLE la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-136">Enable fog blending by setting D3DRS\_FOGENABLE to **TRUE**.</span></span>
2.  <span data-ttu-id="1a6b5-137">Définissez la couleur de brouillard dans l' \_ État de rendu D3DRS FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-137">Set the fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="1a6b5-138">Choisissez la formule de brouillard souhaitée en affectant \_ à l’état de rendu D3DRS FOGVERTEXMODE la valeur d’un membre du type énuméré [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="1a6b5-138">Choose the desired fog formula by setting the D3DRS\_FOGVERTEXMODE render state to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="1a6b5-139">Définissez les paramètres de brouillard comme vous le souhaitez pour la formule de brouillard sélectionnée dans les États de rendu.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-139">Set the fog parameters as desired for the selected fog formula in the render states.</span></span>

<span data-ttu-id="1a6b5-140">L’exemple suivant, écrit en C++, illustre ce que ces étapes peuvent ressembler dans le code.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-140">The following example, written in C++, shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupVertexFog(DWORD Color, DWORD Mode, BOOL UseRange, FLOAT Density)
{
    float Start = 0.5f,    // Linear fog distances
          End   = 0.8f;
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if(D3DFOG_LINEAR == Mode)
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }

    // Enable range-based fog if desired (only supported for
    //   vertex fog). For this example, it is assumed that UseRange
    //   is set to a nonzero value only if the driver exposes the 
    //   D3DPRASTERCAPS_FOGRANGE capability.
    // Note: This is slightly more performance intensive
    //   than non-range-based fog.
    if(UseRange)
        g_pDevice->SetRenderState(D3DRS_RANGEFOGENABLE, TRUE);
}
```



<span data-ttu-id="1a6b5-141">Certains paramètres de brouillard sont requis comme valeurs à virgule flottante, même si la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte uniquement des valeurs DWORD dans le deuxième paramètre.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-141">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method only accepts DWORD values in the second parameter.</span></span> <span data-ttu-id="1a6b5-142">Cet exemple fournit correctement les valeurs à virgule flottante à ces méthodes sans traduction de données en effectuant un cast des adresses des variables à virgule flottante en tant que pointeurs DWORD, puis en les déréférençant.</span><span class="sxs-lookup"><span data-stu-id="1a6b5-142">This example successfully provides the floating-point values to these methods without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a6b5-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a6b5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a6b5-144">Types de brouillard</span><span class="sxs-lookup"><span data-stu-id="1a6b5-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
