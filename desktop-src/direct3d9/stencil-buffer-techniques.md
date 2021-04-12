---
description: Les applications utilisent la mémoire tampon de stencil pour masquer les pixels dans une image. Le masque détermine si le pixel est dessiné ou non. Certains des effets les plus courants sont présentés ci-dessous.
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: Techniques de tampon de stencil (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392883"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a><span data-ttu-id="4131c-105">Techniques de tampon de stencil (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4131c-105">Stencil Buffer Techniques (Direct3D 9)</span></span>

<span data-ttu-id="4131c-106">Les applications utilisent la mémoire tampon de stencil pour masquer les pixels dans une image.</span><span class="sxs-lookup"><span data-stu-id="4131c-106">Applications use the stencil buffer to mask pixels in an image.</span></span> <span data-ttu-id="4131c-107">Le masque détermine si le pixel est dessiné ou non.</span><span class="sxs-lookup"><span data-stu-id="4131c-107">The mask controls whether the pixel is drawn or not.</span></span> <span data-ttu-id="4131c-108">Certains des effets les plus courants sont présentés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4131c-108">Some of the more common effects are shown below.</span></span>

-   [<span data-ttu-id="4131c-109">Composition</span><span class="sxs-lookup"><span data-stu-id="4131c-109">Compositing</span></span>](compositing.md)
-   [<span data-ttu-id="4131c-110">Décalque</span><span class="sxs-lookup"><span data-stu-id="4131c-110">Decaling</span></span>](decaling.md)
-   [<span data-ttu-id="4131c-111">Dissoudre, fondu et balayage</span><span class="sxs-lookup"><span data-stu-id="4131c-111">Dissolves, Fades, and Swipes</span></span>](dissolves--fades--and-swipes.md)
-   [<span data-ttu-id="4131c-112">Plans et silhouettes</span><span class="sxs-lookup"><span data-stu-id="4131c-112">Outlines and Silhouettes</span></span>](outlines-and-silhouettes.md)
-   [<span data-ttu-id="4131c-113">Stencil recto-verso</span><span class="sxs-lookup"><span data-stu-id="4131c-113">Two-Sided Stencil</span></span>](two-sided-stencil.md)

<span data-ttu-id="4131c-114">La mémoire tampon de stencil active ou désactive le dessin sur la surface de la cible de rendu pixel par pixel.</span><span class="sxs-lookup"><span data-stu-id="4131c-114">The stencil buffer enables or disables drawing to the rendering target surface on a pixel-by-pixel basis.</span></span> <span data-ttu-id="4131c-115">À son niveau le plus fondamental, il permet aux applications de masquer les sections de l’image rendue afin qu’elles ne soient pas affichées.</span><span class="sxs-lookup"><span data-stu-id="4131c-115">At its most fundamental level, it enables applications to mask sections of the rendered image so that they are not displayed.</span></span> <span data-ttu-id="4131c-116">Les applications utilisent souvent des mémoires tampons stencil pour des effets spéciaux, tels que les dissolutions, le décalque et le mode plan.</span><span class="sxs-lookup"><span data-stu-id="4131c-116">Applications often use stencil buffers for special effects such as dissolves, decaling, and outlining.</span></span>

<span data-ttu-id="4131c-117">Les informations de tampon de stencil sont incorporées dans les données de la mémoire tampon z.</span><span class="sxs-lookup"><span data-stu-id="4131c-117">Stencil buffer information is embedded in the z-buffer data.</span></span> <span data-ttu-id="4131c-118">Votre application peut utiliser la méthode [**IDirect3D9 :: CheckDeviceFormat**](/windows/desktop/api) pour vérifier la prise en charge des stencils matériels, comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="4131c-118">Your application can use the [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) method to check for hardware stencil support, as shown in the following code example.</span></span>


```
// Reject devices that cannot perform 8-bit stencil buffering. 
// The following example assumes that pCaps is a valid pointer 
// to an initialized D3DCAPS9 structure. 

if( FAILED( m_pD3D->CheckDeviceFormat( pCaps->AdapterOrdinal,
                                       pCaps->DeviceType,  
                                       Format,  
                                       D3DUSAGE_DEPTHSTENCIL, 
                                       D3DRTYPE_SURFACE,
                                       D3DFMT_D24S8 ) ) )
return E_FAIL;
```



<span data-ttu-id="4131c-119">[**IDirect3D9 :: CheckDeviceFormat**](/windows/desktop/api) vous permet de choisir un appareil à créer en fonction des fonctionnalités de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="4131c-119">[**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) allows you to choose a device to create based on the capabilities of that device.</span></span> <span data-ttu-id="4131c-120">Dans ce cas, les appareils qui ne prennent pas en charge les mémoires tampons de stencil 8 bits sont rejetés.</span><span class="sxs-lookup"><span data-stu-id="4131c-120">In this case, devices that do not support 8-bit stencil buffers are rejected.</span></span> <span data-ttu-id="4131c-121">Notez qu’il ne s’agit que d’une seule utilisation possible pour **IDirect3D9 :: CheckDeviceFormat**; Pour plus d’informations, consultez Détermination de la [prise en charge matérielle (Direct3D 9)](determining-hardware-support.md).</span><span class="sxs-lookup"><span data-stu-id="4131c-121">Note that this is only one possible use for **IDirect3D9::CheckDeviceFormat**; for details see [Determining Hardware Support (Direct3D 9)](determining-hardware-support.md).</span></span>

## <a name="how-the-stencil-buffer-works"></a><span data-ttu-id="4131c-122">Fonctionnement de la mémoire tampon de stencil</span><span class="sxs-lookup"><span data-stu-id="4131c-122">How the Stencil Buffer Works</span></span>

<span data-ttu-id="4131c-123">Direct3D effectue un test sur le contenu de la mémoire tampon de stencil pixel par pixel.</span><span class="sxs-lookup"><span data-stu-id="4131c-123">Direct3D performs a test on the contents of the stencil buffer on a pixel-by-pixel basis.</span></span> <span data-ttu-id="4131c-124">Pour chaque pixel de la surface cible, il effectue un test à l’aide de la valeur correspondante dans la mémoire tampon du stencil, une valeur de référence du stencil et une valeur de masque du stencil.</span><span class="sxs-lookup"><span data-stu-id="4131c-124">For each pixel in the target surface, it performs a test using the corresponding value in the stencil buffer, a stencil reference value, and a stencil mask value.</span></span> <span data-ttu-id="4131c-125">Si le test réussit, Direct3D effectue une action.</span><span class="sxs-lookup"><span data-stu-id="4131c-125">If the test passes, Direct3D performs an action.</span></span> <span data-ttu-id="4131c-126">Le test est effectué à l’aide des étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4131c-126">The test is performed using the following steps.</span></span>

1.  <span data-ttu-id="4131c-127">Effectue une opération and au niveau du bit de la valeur de référence du stencil avec le masque du gabarit.</span><span class="sxs-lookup"><span data-stu-id="4131c-127">Perform a bitwise AND operation of the stencil reference value with the stencil mask.</span></span>
2.  <span data-ttu-id="4131c-128">Effectue une opération and au niveau du bit de la valeur de mémoire tampon du stencil pour le pixel actuel avec le masque de stencil.</span><span class="sxs-lookup"><span data-stu-id="4131c-128">Perform a bitwise AND operation of the stencil buffer value for the current pixel with the stencil mask.</span></span>
3.  <span data-ttu-id="4131c-129">Comparez le résultat de l’étape 1 au résultat de l’étape 2, à l’aide de la fonction de comparaison.</span><span class="sxs-lookup"><span data-stu-id="4131c-129">Compare the result of step 1 to the result of step 2, using the comparison function.</span></span>

<span data-ttu-id="4131c-130">Ces étapes sont présentées dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="4131c-130">These steps are shown in the following code example.</span></span>


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



<span data-ttu-id="4131c-131">est le contenu de la mémoire tampon de stencil pour le pixel actuel.</span><span class="sxs-lookup"><span data-stu-id="4131c-131">is the contents of the stencil buffer for the current pixel.</span></span> <span data-ttu-id="4131c-132">Cet exemple de code utilise le symbole esperluette (&) pour représenter l’opération and au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="4131c-132">This code example uses the ampersand (&) symbol to represent the bitwise AND operation.</span></span>


```
StencilMask
```



<span data-ttu-id="4131c-133">représente la valeur du masque de stencil, et</span><span class="sxs-lookup"><span data-stu-id="4131c-133">represents the value of the stencil mask, and</span></span>


```
StencilRef
```



<span data-ttu-id="4131c-134">représente la valeur de référence du stencil.</span><span class="sxs-lookup"><span data-stu-id="4131c-134">represents the stencil reference value.</span></span>


```
CompFunc
```



<span data-ttu-id="4131c-135">fonction de comparaison.</span><span class="sxs-lookup"><span data-stu-id="4131c-135">is the comparison function.</span></span>

<span data-ttu-id="4131c-136">Le pixel actuel est écrit dans la surface cible si le test du stencil réussit, et est ignoré dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4131c-136">The current pixel is written to the target surface if the stencil test passes, and is ignored otherwise.</span></span> <span data-ttu-id="4131c-137">Le comportement de comparaison par défaut consiste à écrire le pixel, quel que soit le mode de fonctionnement de chaque opération de bits (D3DCMP \_ Always).</span><span class="sxs-lookup"><span data-stu-id="4131c-137">The default comparison behavior is to write the pixel, no matter how each bitwise operation turns out (D3DCMP\_ALWAYS).</span></span> <span data-ttu-id="4131c-138">Vous pouvez modifier ce comportement en modifiant la valeur de l' \_ État de rendu D3DRS STENCILFUNC, en passant un membre du type énuméré [**D3DCMPFUNC**](./d3dcmpfunc.md) pour identifier la fonction de comparaison souhaitée.</span><span class="sxs-lookup"><span data-stu-id="4131c-138">You can change this behavior by changing the value of the D3DRS\_STENCILFUNC render state, passing a member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type to identify the desired comparison function.</span></span>

<span data-ttu-id="4131c-139">Votre application peut personnaliser le fonctionnement de la mémoire tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="4131c-139">Your application can customize the operation of the stencil buffer.</span></span> <span data-ttu-id="4131c-140">Elle peut définir la fonction de comparaison, le masque de stencil et la valeur de référence du stencil.</span><span class="sxs-lookup"><span data-stu-id="4131c-140">It can set the comparison function, the stencil mask, and the stencil reference value.</span></span> <span data-ttu-id="4131c-141">Il peut également contrôler l’action effectuée par Direct3D lorsque le test de stencil réussit ou échoue.</span><span class="sxs-lookup"><span data-stu-id="4131c-141">It can also control the action that Direct3D takes when the stencil test passes or fails.</span></span> <span data-ttu-id="4131c-142">Pour plus d’informations, consultez état de la [mémoire tampon des stencils (Direct3D 9)](stencil-buffer-state.md).</span><span class="sxs-lookup"><span data-stu-id="4131c-142">For more information, see [Stencil Buffer State (Direct3D 9)](stencil-buffer-state.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4131c-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="4131c-143">Examples</span></span>

<span data-ttu-id="4131c-144">Les exemples de code suivants illustrent la configuration de la mémoire tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="4131c-144">The following code examples demonstrate setting up the stencil buffer.</span></span>


```
// Enable stencil testing
pDevice->SetRenderState(D3DRS_STENCILENABLE, TRUE);

// Specify the stencil comparison function
pDevice->SetRenderState(D3DRS_STENCILFUNC, D3DCMP_EQUAL);

// Set the comparison reference value
pDevice->SetRenderState(D3DRS_STENCILREF, 0);

//  Specify a stencil mask 
pDevice->SetRenderState(D3DRS_STENCILMASK, 0);
```



<span data-ttu-id="4131c-145">Par défaut, la valeur de référence du stencil est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="4131c-145">By default, the stencil reference value is zero.</span></span> <span data-ttu-id="4131c-146">Toute valeur entière est valide.</span><span class="sxs-lookup"><span data-stu-id="4131c-146">Any integer value is valid.</span></span> <span data-ttu-id="4131c-147">Direct3D effectue une opération de bits AND de la valeur de référence du stencil et une valeur de masque de stencil avant le test du stencil.</span><span class="sxs-lookup"><span data-stu-id="4131c-147">Direct3D performs a bitwise AND of the stencil reference value and a stencil mask value before the stencil test.</span></span>

<span data-ttu-id="4131c-148">Vous pouvez contrôler les informations de pixels qui sont écrites en fonction de la comparaison du stencil.</span><span class="sxs-lookup"><span data-stu-id="4131c-148">You can control what pixel information is written out depending on the stencil comparison.</span></span>


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



<span data-ttu-id="4131c-149">Vous pouvez écrire votre propre formule pour la valeur que vous souhaitez écrire dans la mémoire tampon du stencil, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4131c-149">You can write your own formula for the value you want written into the stencil buffer as shown in the following example.</span></span>


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a><span data-ttu-id="4131c-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4131c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4131c-151">Pipeline de pixels</span><span class="sxs-lookup"><span data-stu-id="4131c-151">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
