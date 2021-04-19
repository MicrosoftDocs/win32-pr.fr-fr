---
description: Les fonctionnalités suivantes ont été modifiées dans Microsoft Direct3D 9. Si vous utilisez ces fonctionnalités, consultez les modifications répertoriées ci-dessous pour vous aider à migrer votre application vers Direct3D 9.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Conversion en Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becdb878ad462bfc0157fb15b3c9c1ef2ba158dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515573"
---
# <a name="converting-to-direct3d-9"></a><span data-ttu-id="8045c-104">Conversion en Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="8045c-104">Converting to Direct3D 9</span></span>

<span data-ttu-id="8045c-105">Les fonctionnalités suivantes ont été modifiées dans Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="8045c-105">The following features were changed in Microsoft Direct3D 9.</span></span> <span data-ttu-id="8045c-106">Si vous utilisez ces fonctionnalités, consultez les modifications répertoriées ci-dessous pour vous aider à migrer votre application vers Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="8045c-106">If you are using these features, see the changes listed below to help you port your application to Direct3D 9.</span></span>

-   [<span data-ttu-id="8045c-107">Modifications de BaseVertexIndex</span><span class="sxs-lookup"><span data-stu-id="8045c-107">BaseVertexIndex Changes</span></span>](#basevertexindex-changes)
-   [<span data-ttu-id="8045c-108">Modifications de CreateImageSurface</span><span class="sxs-lookup"><span data-stu-id="8045c-108">CreateImageSurface Changes</span></span>](#createimagesurface-changes)
-   [<span data-ttu-id="8045c-109">D3DENUM \_ aucune \_ \_ modification du niveau WHQL</span><span class="sxs-lookup"><span data-stu-id="8045c-109">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>](/windows)
-   [<span data-ttu-id="8045c-110">Créer des modifications de ressources</span><span class="sxs-lookup"><span data-stu-id="8045c-110">Create Resource Changes</span></span>](#create-resource-changes)
-   [<span data-ttu-id="8045c-111">Modifications de EnumAdapterModes</span><span class="sxs-lookup"><span data-stu-id="8045c-111">EnumAdapterModes Changes</span></span>](#enumadaptermodes-changes)
-   [<span data-ttu-id="8045c-112">\_Modifications apportées à SetStreamSource</span><span class="sxs-lookup"><span data-stu-id="8045c-112">Get/SetStreamSource\_Changes</span></span>](#getsetstreamsource-changes)
-   [<span data-ttu-id="8045c-113">Modifications de la qualité d’échantillonnage multiple</span><span class="sxs-lookup"><span data-stu-id="8045c-113">Multisampling Quality Changes</span></span>](#multisampling-quality-changes)
-   [<span data-ttu-id="8045c-114">Modifications de ResourceManagerDiscardBytes</span><span class="sxs-lookup"><span data-stu-id="8045c-114">ResourceManagerDiscardBytes Changes</span></span>](#resourcemanagerdiscardbytes-changes)
-   [<span data-ttu-id="8045c-115">Modifications de SetSoftwareVertexProcessing</span><span class="sxs-lookup"><span data-stu-id="8045c-115">SetSoftwareVertexProcessing Changes</span></span>](#setsoftwarevertexprocessing-changes)
-   [<span data-ttu-id="8045c-116">Modifications de l’échantillonneur de texture</span><span class="sxs-lookup"><span data-stu-id="8045c-116">Texture Sampler Changes</span></span>](#texture-sampler-changes)
-   [<span data-ttu-id="8045c-117">Modifications de déclaration de vertex</span><span class="sxs-lookup"><span data-stu-id="8045c-117">Vertex Declaration Changes</span></span>](#vertex-declaration-changes)
-   [<span data-ttu-id="8045c-118">Intervalles \_ et \_ modifications SwapEffects \_</span><span class="sxs-lookup"><span data-stu-id="8045c-118">Intervals,\_and\_SwapEffects\_Changes</span></span>](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a><span data-ttu-id="8045c-119">Modifications de BaseVertexIndex</span><span class="sxs-lookup"><span data-stu-id="8045c-119">BaseVertexIndex Changes</span></span>

<span data-ttu-id="8045c-120">Dans DirectX 8. x, IDirect3DDevice8 :: SetIndices nécessitait un pointeur vers la mémoire tampon d’index et un BaseVertexIndex pour la position de départ dans la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="8045c-120">In DirectX 8.x, IDirect3DDevice8::SetIndices required a pointer to the index buffer and a BaseVertexIndex for the starting position in the vertex buffer.</span></span> <span data-ttu-id="8045c-121">Une application qui effectue un traitement par lot de différents objets dans la mémoire tampon de vertex devait basculer le tampon d’index (ou appeler IDirect3DDevice8 :: SetIndices) avant d’appeler IDirect3DDevice8 ::D rawIndexedPrimitive.</span><span class="sxs-lookup"><span data-stu-id="8045c-121">An application batching different objects into the vertex buffer had to switch the index buffer (or make a call to IDirect3DDevice8::SetIndices) before calling IDirect3DDevice8::DrawIndexedPrimitive.</span></span>

<span data-ttu-id="8045c-122">Dans Direct3D 9, la position de départ dans la mémoire tampon de vertex, *BaseVertexIndex*, a été déplacée vers IDirect3DDevice9 ::D rawindexedprimitive et son type de données est passé d’un DWORD à un entier.</span><span class="sxs-lookup"><span data-stu-id="8045c-122">In Direct3D 9, the starting position in the vertex buffer, *BaseVertexIndex*, has been moved to IDirect3DDevice9::DrawIndexedPrimitive, and its data type changed from a DWORD to an INT.</span></span>


```
HRESULT IDirect3DDevice9::DrawIndexedPrimitive( 
    D3DPRIMITIVETYPE PrimType, 
    INT BaseVertexIndex, 
    UINT minIndex, 
    UINT NumVertices, 
    UINT startIndex, 
    UINT primCount); 

HRESULT SetIndices(IDirect3DIndexBuffer9* pIndexData); 
```



## <a name="createimagesurface-changes"></a><span data-ttu-id="8045c-123">Modifications de CreateImageSurface</span><span class="sxs-lookup"><span data-stu-id="8045c-123">CreateImageSurface Changes</span></span>

<span data-ttu-id="8045c-124">IDirect3DDevice8 :: CreateImageSurface a été renommé [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface).</span><span class="sxs-lookup"><span data-stu-id="8045c-124">IDirect3DDevice8::CreateImageSurface was renamed [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface).</span></span> <span data-ttu-id="8045c-125">Un paramètre supplémentaire qui prend un type D3DPOOL a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="8045c-125">An additional parameter that takes a D3DPOOL type was added.</span></span> <span data-ttu-id="8045c-126">D3DPOOL \_ Scratch retourne une surface qui a des caractéristiques identiques à une surface créée par IDirect3DDevice8 :: CreateImageSurface.</span><span class="sxs-lookup"><span data-stu-id="8045c-126">D3DPOOL\_SCRATCH will return a surface that has identical characteristics to a surface created by IDirect3DDevice8::CreateImageSurface.</span></span> <span data-ttu-id="8045c-127">D3DPOOL \_ par défaut est le pool approprié à utiliser avec [**StretchRect**](/windows/desktop/api) et [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).</span><span class="sxs-lookup"><span data-stu-id="8045c-127">D3DPOOL\_DEFAULT is the appropriate pool for use with [**StretchRect**](/windows/desktop/api) and [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).</span></span>

## <a name="d3denum_no_whql_level-changes"></a><span data-ttu-id="8045c-128">D3DENUM \_ aucune \_ \_ modification du niveau WHQL</span><span class="sxs-lookup"><span data-stu-id="8045c-128">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>

<span data-ttu-id="8045c-129">Les applications doivent maintenant demander explicitement Microsoft Windows Hardware Quality Labs (WHQL), car la réponse est relativement longue (quelques secondes).</span><span class="sxs-lookup"><span data-stu-id="8045c-129">Applications now have to explicitly ask for the Microsoft Windows Hardware Quality Labs (WHQL) because the response takes relatively long (a few seconds).</span></span> <span data-ttu-id="8045c-130">D3DENUM \_ aucun \_ niveau WHQL n' \_ a été supprimé et le \_ niveau D3DENUM WHQL \_ a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="8045c-130">D3DENUM\_NO\_WHQL\_LEVEL has been removed and D3DENUM\_WHQL\_LEVEL has been added.</span></span>

## <a name="create-resource-changes"></a><span data-ttu-id="8045c-131">Créer des modifications de ressources</span><span class="sxs-lookup"><span data-stu-id="8045c-131">Create Resource Changes</span></span>

<span data-ttu-id="8045c-132">Un descripteur a été ajouté à plusieurs méthodes et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="8045c-132">A handle has been added to several methods and should be set to **NULL**.</span></span> <span data-ttu-id="8045c-133">Les méthodes affectées sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8045c-133">The methods affected include:</span></span>

-   [<span data-ttu-id="8045c-134">**CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="8045c-134">**CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="8045c-135">**CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="8045c-135">**CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [<span data-ttu-id="8045c-136">**CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="8045c-136">**CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="8045c-137">**CreateVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="8045c-137">**CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [<span data-ttu-id="8045c-138">**CreateIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="8045c-138">**CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [<span data-ttu-id="8045c-139">**CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="8045c-139">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [<span data-ttu-id="8045c-140">**CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="8045c-140">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="8045c-141">**CreateOffscreenPlainSurface**</span><span class="sxs-lookup"><span data-stu-id="8045c-141">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a><span data-ttu-id="8045c-142">Modifications de EnumAdapterModes</span><span class="sxs-lookup"><span data-stu-id="8045c-142">EnumAdapterModes Changes</span></span>

<span data-ttu-id="8045c-143">Le [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) prend maintenant un D3DFORMAT.</span><span class="sxs-lookup"><span data-stu-id="8045c-143">The [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) now takes a D3DFORMAT.</span></span>


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



<span data-ttu-id="8045c-144">Le format prend en charge un ensemble étendu de modes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="8045c-144">The format supports an expanding set of display modes.</span></span> <span data-ttu-id="8045c-145">Pour protéger les applications des formats d’énumération qui n’ont pas été inventés lors de la livraison de l’application, l’application doit indiquer à Direct3D le format des modes d’affichage à énumérer.</span><span class="sxs-lookup"><span data-stu-id="8045c-145">To protect applications from enumerating formats that were not invented when the application shipped, the application must tell Direct3D the format for the display modes that should be enumerated.</span></span> <span data-ttu-id="8045c-146">Le tableau résultant de modes d’affichage diffère uniquement par la largeur, la hauteur et la fréquence d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="8045c-146">The resulting array of display modes will differ only by width, height, and refresh rate.</span></span>

<span data-ttu-id="8045c-147">L’application spécifie un format de pixel et l’énumération est limitée aux modes d’affichage qui correspondent exactement au format.</span><span class="sxs-lookup"><span data-stu-id="8045c-147">The application specifies a pixel format and the enumeration is restricted to those display modes that exactly match the format.</span></span> <span data-ttu-id="8045c-148">La liste suivante répertorie les formats autorisés :</span><span class="sxs-lookup"><span data-stu-id="8045c-148">The following is a list of the allowed formats:</span></span>

-   <span data-ttu-id="8045c-149">D3DFMT \_ A1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="8045c-149">D3DFMT\_A1R5G5B5</span></span>
-   <span data-ttu-id="8045c-150">D3DFMT \_ A2B10G10R10</span><span class="sxs-lookup"><span data-stu-id="8045c-150">D3DFMT\_A2B10G10R10</span></span>
-   <span data-ttu-id="8045c-151">D3DFMT \_ A8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="8045c-151">D3DFMT\_A8R8G8B8</span></span>
-   <span data-ttu-id="8045c-152">D3DFMT \_ R5G6B5</span><span class="sxs-lookup"><span data-stu-id="8045c-152">D3DFMT\_R5G6B5</span></span>
-   <span data-ttu-id="8045c-153">D3DFMT \_ X1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="8045c-153">D3DFMT\_X1R5G5B5</span></span>
-   <span data-ttu-id="8045c-154">D3DFMT \_ X8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="8045c-154">D3DFMT\_X8R8G8B8</span></span>

<span data-ttu-id="8045c-155">L’énumération est équivalente pour les versions alpha et non alpha du même format.</span><span class="sxs-lookup"><span data-stu-id="8045c-155">Enumeration is equivalent for alpha and nonalpha versions of the same format.</span></span> <span data-ttu-id="8045c-156">Le format retourné sera toujours rempli avec le même format que celui fourni par l’application.</span><span class="sxs-lookup"><span data-stu-id="8045c-156">The returned Format will always be filled with the same format supplied by the application.</span></span>

<span data-ttu-id="8045c-157">Cette méthode traite 565 et 555 comme équivalents, et retourne la version correcte au format.</span><span class="sxs-lookup"><span data-stu-id="8045c-157">This method treats 565 and 555 as equivalent, and returns the correct version in the Format.</span></span> <span data-ttu-id="8045c-158">La différence entre en jeu uniquement lorsque l’application verrouille la mémoire tampon d’arrière-plan, et qu’il existe un indicateur explicite que l’application doit définir afin d’y parvenir.</span><span class="sxs-lookup"><span data-stu-id="8045c-158">The difference comes into play only when the application locks the back buffer, and there is an explicit flag that the application must set in order to accomplish this.</span></span>

## <a name="getsetstreamsource-changes"></a><span data-ttu-id="8045c-159">Modifications apportées à SetStreamSource</span><span class="sxs-lookup"><span data-stu-id="8045c-159">Get/SetStreamSource Changes</span></span>

<span data-ttu-id="8045c-160">Un paramètre a été ajouté aux méthodes [**GetStreamSource**](/windows/desktop/api) et [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) .</span><span class="sxs-lookup"><span data-stu-id="8045c-160">One parameter has been added to the [**GetStreamSource**](/windows/desktop/api) and [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) methods.</span></span> <span data-ttu-id="8045c-161">Le décalage est le nombre d’octets entre le début du flux et le début des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="8045c-161">The offset is the number of bytes between the beginning of the stream and the beginning of the vertex data.</span></span> <span data-ttu-id="8045c-162">Elle est mesurée en octets.</span><span class="sxs-lookup"><span data-stu-id="8045c-162">It is measured in bytes.</span></span> <span data-ttu-id="8045c-163">Cela permet au pipeline de prendre en charge les décalages de flux.</span><span class="sxs-lookup"><span data-stu-id="8045c-163">This enables the pipeline to support stream offsets.</span></span> <span data-ttu-id="8045c-164">Pour déterminer si l’appareil prend en charge les décalages de flux, consultez D3DDEVCAPS2 \_ STREAMOFFSET.</span><span class="sxs-lookup"><span data-stu-id="8045c-164">To find out if the device supports stream offsets, see D3DDEVCAPS2\_STREAMOFFSET.</span></span>


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a><span data-ttu-id="8045c-165">Modifications de la qualité d’échantillonnage multiple</span><span class="sxs-lookup"><span data-stu-id="8045c-165">Multisampling Quality Changes</span></span>

<span data-ttu-id="8045c-166">Auparavant, il existait uniquement l' \_ énumération de type D3DMULTISAMPLE.</span><span class="sxs-lookup"><span data-stu-id="8045c-166">Previously, there was only the D3DMULTISAMPLE\_TYPE enumeration.</span></span> <span data-ttu-id="8045c-167">Direct3D 9 conserve cette énumération et ajoute l’idée d’un niveau de qualité pour chaque élément de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="8045c-167">Direct3D 9 retains this enumeration and adds the idea of a quality level for each element of the enumeration.</span></span> <span data-ttu-id="8045c-168">Le niveau de qualité indique un compromis entre la qualité visuelle et les performances en indiquant le nombre d’échantillons masquables (au sens de D3DRS \_ MULTISAMPLEMASK).</span><span class="sxs-lookup"><span data-stu-id="8045c-168">The quality level indicates a trade-off between visual quality and performance by indicating the number of maskable samples (in the sense of D3DRS\_MULTISAMPLEMASK).</span></span>

<span data-ttu-id="8045c-169">Une application doit choisir le nombre d’exemples masquables requis, puis consulter pQualityLevels.</span><span class="sxs-lookup"><span data-stu-id="8045c-169">An application should choose how many maskable samples it requires, and then consult pQualityLevels.</span></span> <span data-ttu-id="8045c-170">Si la valeur est différente de zéro, cette valeur indique le nombre de niveaux de qualité que l’application peut passer aux différentes fonctions de création par le biais de MultiSampleQuality.</span><span class="sxs-lookup"><span data-stu-id="8045c-170">If nonzero, this value indicates the number of quality levels the application can pass to the various creation functions through MultiSampleQuality.</span></span> <span data-ttu-id="8045c-171">Étant donné que les pilotes exposent tous les schémas d’échantillonnage multiple comme des niveaux de qualité à D3DMULTISAMPLE \_ non masquables, vous pouvez énumérer tous les schémas d’échantillonnage multiple disponibles à l’aide de ce type si votre application n’a pas besoin de masquer des exemples.</span><span class="sxs-lookup"><span data-stu-id="8045c-171">Because drivers expose all their multisample schemes as quality levels at D3DMULTISAMPLE\_NONMASKABLE, you can enumerate all available multisampling schemes through this one type if your application does not need to mask samples.</span></span>

<span data-ttu-id="8045c-172">Le \_ bit D3DPRASTERCAPS STRETCHBLTMULTISAMPLE Cap a été retiré.</span><span class="sxs-lookup"><span data-stu-id="8045c-172">The D3DPRASTERCAPS\_STRETCHBLTMULTISAMPLE caps bit has been retired.</span></span> <span data-ttu-id="8045c-173">Ce bit est utilisé pour signifier que la méthode d’échantillonnage multiple ne prenait pas en charge les masques d’écriture et n’a pas pu être activée/désactivée entre [**BeginScene**](/windows/desktop/api) et [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene).</span><span class="sxs-lookup"><span data-stu-id="8045c-173">This bit used to mean that the multisampling method did not support write masks, and could not be toggled on and off between [**BeginScene**](/windows/desktop/api) and [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene).</span></span> <span data-ttu-id="8045c-174">Ces méthodes non masquées sont désormais exposées via D3DMULTISAMPLE non \_ MASKABLE.</span><span class="sxs-lookup"><span data-stu-id="8045c-174">Such nonmaskable methods are now exposed through D3DMULTISAMPLE\_NONMASKABLE.</span></span>


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



<span data-ttu-id="8045c-175">Il existe une valeur maximale différente pour chaque nombre d’échantillons masquables.</span><span class="sxs-lookup"><span data-stu-id="8045c-175">There is a different maximum for each number of maskable samples.</span></span> <span data-ttu-id="8045c-176">Par exemple, les \_ exemples D3DMULTISAMPLE 4 \_ peuvent avoir trois niveaux de qualité, tandis que les \_ exemples D3DMULTISAMPLE 2 ne peuvent en \_ avoir qu’un seul.</span><span class="sxs-lookup"><span data-stu-id="8045c-176">For example, D3DMULTISAMPLE\_4\_SAMPLES might have three levels of quality, while D3DMULTISAMPLE\_2\_SAMPLES might have only one.</span></span> <span data-ttu-id="8045c-177">Il y a au plus huit niveaux de qualité pour chaque nombre d’échantillons pouvant être masqués (le pilote n’est pas autorisé à exprimer davantage).</span><span class="sxs-lookup"><span data-stu-id="8045c-177">There are at most eight levels of quality for each number of maskable samples (the driver is not allowed to express more).</span></span> <span data-ttu-id="8045c-178">La qualité est comprise entre zéro et ( \* pQualityLevels-1).</span><span class="sxs-lookup"><span data-stu-id="8045c-178">The quality ranges from zero to (\*pQualityLevels - 1).</span></span>

## <a name="resourcemanagerdiscardbytes-changes"></a><span data-ttu-id="8045c-179">Modifications de ResourceManagerDiscardBytes</span><span class="sxs-lookup"><span data-stu-id="8045c-179">ResourceManagerDiscardBytes Changes</span></span>

<span data-ttu-id="8045c-180">ResourceManagerDiscardBytes a été remplacé par IDirect3DDevice9 :: EvictManagedResources.</span><span class="sxs-lookup"><span data-stu-id="8045c-180">ResourceManagerDiscardBytes has been replaced by IDirect3DDevice9::EvictManagedResources.</span></span> <span data-ttu-id="8045c-181">Il peut supprimer toutes les ressources, à la fois Direct3D et les ressources du pilote.</span><span class="sxs-lookup"><span data-stu-id="8045c-181">It can evict all resources, both Direct3D and driver resources.</span></span>

<span data-ttu-id="8045c-182">Le gestionnaire de ressources est désormais consulté lorsqu’une ressource (qu’elle soit gérée ou non) ne peut pas être créée car la mémoire vidéo est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="8045c-182">The resource manager is now consulted when a resource (whether managed or nonmanaged) fails creation because there is insufficient video memory.</span></span> <span data-ttu-id="8045c-183">Le responsable sera automatiquement invité à libérer suffisamment de ressources pour que la création aboutisse.</span><span class="sxs-lookup"><span data-stu-id="8045c-183">The manager will automatically be asked to free enough resources for the creation to succeed.</span></span> <span data-ttu-id="8045c-184">Dans DirectX 8,0, il ne s’agissait pas d’un processus automatisé.</span><span class="sxs-lookup"><span data-stu-id="8045c-184">In DirectX 8.0, this was not an automated process.</span></span>

## <a name="setsoftwarevertexprocessing-changes"></a><span data-ttu-id="8045c-185">Modifications de SetSoftwareVertexProcessing</span><span class="sxs-lookup"><span data-stu-id="8045c-185">SetSoftwareVertexProcessing Changes</span></span>

<span data-ttu-id="8045c-186">Une application peut créer un appareil en mode mixte pour utiliser le traitement des vertex logiciels et matériels.</span><span class="sxs-lookup"><span data-stu-id="8045c-186">An application can create a mixed-mode device to use software and hardware vertex processing.</span></span>

<span data-ttu-id="8045c-187">Pour basculer entre les deux modes de traitement de vertex dans DirectX 8. x, appelez IDirect3DDevice8 :: SetRenderState.</span><span class="sxs-lookup"><span data-stu-id="8045c-187">To switch between the two vertex processing modes in DirectX 8.x, call IDirect3DDevice8::SetRenderState.</span></span> <span data-ttu-id="8045c-188">Il a été remplacé par [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) pour faciliter les problèmes causés par les blocs d’État.</span><span class="sxs-lookup"><span data-stu-id="8045c-188">This has been replaced with [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) to ease problems caused by state blocks.</span></span> <span data-ttu-id="8045c-189">Cette nouvelle méthode n’est pas enregistrée par les blocs d’État.</span><span class="sxs-lookup"><span data-stu-id="8045c-189">This new method is not recorded by state blocks.</span></span>

## <a name="texture-sampler-changes"></a><span data-ttu-id="8045c-190">Modifications de l’échantillonneur de texture</span><span class="sxs-lookup"><span data-stu-id="8045c-190">Texture Sampler Changes</span></span>

<span data-ttu-id="8045c-191">Direct3D 9 prend en charge jusqu’à seize surfaces de texture en une seule passe à l’aide du modèle de nuanceur de pixels 2 \_ 0 ; Toutefois, le nombre de coordonnées de texture reste limité à huit.</span><span class="sxs-lookup"><span data-stu-id="8045c-191">Direct3D 9 supports up to sixteen texture surfaces in one pass using the pixel shader 2\_0 model; however, the number of texture coordinates remains limited to eight.</span></span> <span data-ttu-id="8045c-192">L’état de l’étape de texture est associé aux surfaces, aux jeux de coordonnées, au traitement des vertex et au traitement des pixels.</span><span class="sxs-lookup"><span data-stu-id="8045c-192">Texture stage state is associated with surfaces, coordinate sets, vertex processing, and pixel processing.</span></span> <span data-ttu-id="8045c-193">Pour gérer ces différences au moment de la compilation, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) a été divisé en deux méthodes :</span><span class="sxs-lookup"><span data-stu-id="8045c-193">To manage these differences at compile time, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) has been broken into two methods:</span></span>

-   <span data-ttu-id="8045c-194">IDirect3DDevice9 :: SetTextureStageState sera toujours utilisé pour l’état de coordonnée de texture, comme les modes de retour à la ligne et la génération de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="8045c-194">IDirect3DDevice9::SetTextureStageState will still be used for texture coordinate state, such as wrap modes and texture coordinate generation.</span></span>
-   <span data-ttu-id="8045c-195">[**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) a été ajouté et sera désormais utilisé pour le filtrage, la juxtaposition, le serrage, le MIPLOD, etc.</span><span class="sxs-lookup"><span data-stu-id="8045c-195">[**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) has been added and will now be used for filtering, tiling, clamping, MIPLOD, and so forth.</span></span> <span data-ttu-id="8045c-196">Cela fonctionnera pour seize échantillonneurs au maximum.</span><span class="sxs-lookup"><span data-stu-id="8045c-196">This will work for up to sixteen samplers.</span></span>

### <a name="settexturestagestate-changes"></a><span data-ttu-id="8045c-197">Modifications de SetTextureStageState</span><span class="sxs-lookup"><span data-stu-id="8045c-197">SetTextureStageState Changes</span></span>

<span data-ttu-id="8045c-198">IDirect3DDevice9 :: SetTextureStageState définit maintenant les États suivants :</span><span class="sxs-lookup"><span data-stu-id="8045c-198">IDirect3DDevice9::SetTextureStageState now sets the following states:</span></span>

-   <span data-ttu-id="8045c-199">Correction de l’état du traitement des vertex de fonction.</span><span class="sxs-lookup"><span data-stu-id="8045c-199">Fixed function vertex processing state.</span></span> <span data-ttu-id="8045c-200">Cet État contrôle la manipulation des coordonnées de texture D3DTSS \_ TEXTURETRANSFORMFLAGS et D3DTSS \_ TEXCOORDINDEX.</span><span class="sxs-lookup"><span data-stu-id="8045c-200">This state controls the manipulation of texture coordinates D3DTSS\_TEXTURETRANSFORMFLAGS and D3DTSS\_TEXCOORDINDEX.</span></span> <span data-ttu-id="8045c-201">Jusqu’à huit de chaque peuvent être définis (car huit coordonnées de texture sont toujours prises en charge).</span><span class="sxs-lookup"><span data-stu-id="8045c-201">Up to eight of each can be set (because eight texture coordinates are always supported).</span></span> <span data-ttu-id="8045c-202">D3DTSS \_ TEXCOORDINDEX est un état de traitement de vertex de fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="8045c-202">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="8045c-203">Si un nuanceur de sommet programmable est utilisé, cet État est ignoré.</span><span class="sxs-lookup"><span data-stu-id="8045c-203">If a programmable vertex shader is used, this state is ignored.</span></span>
-   <span data-ttu-id="8045c-204">Correction de l’état du nuanceur de pixels de fonction (TextureStageState hérité).</span><span class="sxs-lookup"><span data-stu-id="8045c-204">Fixed function pixel shader state (the legacy TextureStageState).</span></span>

    -   <span data-ttu-id="8045c-205">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="8045c-205">D3DTSS\_ALPHAARG0</span></span>
    -   <span data-ttu-id="8045c-206">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="8045c-206">D3DTSS\_ALPHAARG1</span></span>
    -   <span data-ttu-id="8045c-207">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="8045c-207">D3DTSS\_ALPHAARG2</span></span>
    -   <span data-ttu-id="8045c-208">D3DTSS \_ ALPHAOP</span><span class="sxs-lookup"><span data-stu-id="8045c-208">D3DTSS\_ALPHAOP</span></span>
    -   <span data-ttu-id="8045c-209">D3DTSS \_ BUMPENVLOFFSET</span><span class="sxs-lookup"><span data-stu-id="8045c-209">D3DTSS\_BUMPENVLOFFSET</span></span>
    -   <span data-ttu-id="8045c-210">D3DTSS \_ BUMPENVLSCALE</span><span class="sxs-lookup"><span data-stu-id="8045c-210">D3DTSS\_BUMPENVLSCALE</span></span>
    -   <span data-ttu-id="8045c-211">D3DTSS \_ BUMPENVMAT00</span><span class="sxs-lookup"><span data-stu-id="8045c-211">D3DTSS\_BUMPENVMAT00</span></span>
    -   <span data-ttu-id="8045c-212">D3DTSS \_ BUMPENVMAT01</span><span class="sxs-lookup"><span data-stu-id="8045c-212">D3DTSS\_BUMPENVMAT01</span></span>
    -   <span data-ttu-id="8045c-213">D3DTSS \_ BUMPENVMAT10</span><span class="sxs-lookup"><span data-stu-id="8045c-213">D3DTSS\_BUMPENVMAT10</span></span>
    -   <span data-ttu-id="8045c-214">D3DTSS \_ BUMPENVMAT11</span><span class="sxs-lookup"><span data-stu-id="8045c-214">D3DTSS\_BUMPENVMAT11</span></span>
    -   <span data-ttu-id="8045c-215">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="8045c-215">D3DTSS\_COLORARG0</span></span>
    -   <span data-ttu-id="8045c-216">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="8045c-216">D3DTSS\_COLORARG1</span></span>
    -   <span data-ttu-id="8045c-217">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="8045c-217">D3DTSS\_COLORARG2</span></span>
    -   <span data-ttu-id="8045c-218">D3DTSS \_ COLOROP</span><span class="sxs-lookup"><span data-stu-id="8045c-218">D3DTSS\_COLOROP</span></span>
    -   <span data-ttu-id="8045c-219">D3DTSS \_ RESULTARG</span><span class="sxs-lookup"><span data-stu-id="8045c-219">D3DTSS\_RESULTARG</span></span>

    <span data-ttu-id="8045c-220">Le nombre d’États de nuanceur de pixels de fonction fixes qui peuvent être définis est inférieur ou égal au nombre représenté par MaxTextureBlendStages.</span><span class="sxs-lookup"><span data-stu-id="8045c-220">The number of fixed function pixel shader states that can be set is less than or equal to the number represented by MaxTextureBlendStages.</span></span>

<span data-ttu-id="8045c-221">Le nombre d’échantillonneurs de texture disponibles pour l’application est déterminé par la version du nuanceur de pixels, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8045c-221">The number of texture samplers available to the application is determined by the pixel shader version, as indicated in the following table.</span></span>



| <span data-ttu-id="8045c-222">Nom</span><span class="sxs-lookup"><span data-stu-id="8045c-222">Name</span></span>                    | <span data-ttu-id="8045c-223">Number</span><span class="sxs-lookup"><span data-stu-id="8045c-223">Number</span></span>                                                         |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="8045c-224">PS \_ 1 \_ 1 à PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8045c-224">ps\_1\_1 to ps\_1\_3</span></span>    | <span data-ttu-id="8045c-225">4 échantillonneurs de texture</span><span class="sxs-lookup"><span data-stu-id="8045c-225">4 texture samplers</span></span>                                             |
| <span data-ttu-id="8045c-226">PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="8045c-226">ps\_1\_4</span></span>                | <span data-ttu-id="8045c-227">6 échantillonneurs de texture</span><span class="sxs-lookup"><span data-stu-id="8045c-227">6 texture samplers</span></span>                                             |
| <span data-ttu-id="8045c-228">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8045c-228">ps\_2\_0</span></span>                | <span data-ttu-id="8045c-229">16 échantillonneurs de texture</span><span class="sxs-lookup"><span data-stu-id="8045c-229">16 texture samplers</span></span>                                            |
| <span data-ttu-id="8045c-230">pipeline de fonction fixe</span><span class="sxs-lookup"><span data-stu-id="8045c-230">fixed function pipeline</span></span> | <span data-ttu-id="8045c-231">Échantillonneurs de texture MaxTextureBlendStages/MaxSimultaneousTextures</span><span class="sxs-lookup"><span data-stu-id="8045c-231">MaxTextureBlendStages/MaxSimultaneousTextures texture samplers</span></span> |



 

<span data-ttu-id="8045c-232">Les appareils qui prennent en charge le mappage de déplacement dans Direct3D 9 prennent en charge un échantillonneur supplémentaire (D3DDMAPSAMPLER), qui échantillonne les mappages de déplacement dans l’unité du paveur.</span><span class="sxs-lookup"><span data-stu-id="8045c-232">Devices that support displacement mapping in Direct3D 9 will support an additional sampler (D3DDMAPSAMPLER), which samples the displacement maps in the tessellator unit.</span></span>

### <a name="setsamplerstate-changes"></a><span data-ttu-id="8045c-233">Modifications de SetSamplerState</span><span class="sxs-lookup"><span data-stu-id="8045c-233">SetSamplerState Changes</span></span>

<span data-ttu-id="8045c-234">IDirect3DDevice9 :: SetSamplerState définit l’état de l’échantillonneur (y compris celui utilisé dans l’unité du paveur pour échantillonner les mappages de déplacement).</span><span class="sxs-lookup"><span data-stu-id="8045c-234">IDirect3DDevice9::SetSamplerState sets the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="8045c-235">Ils ont été renommés avec un \_ préfixe D3DSAMP pour permettre la détection des erreurs au moment de la compilation lors du Portage à partir de DirectX 8. x.</span><span class="sxs-lookup"><span data-stu-id="8045c-235">These have been renamed with a D3DSAMP\_ prefix to enable compile-time error detection when porting from DirectX 8.x.</span></span> <span data-ttu-id="8045c-236">Les États sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="8045c-236">The states include:</span></span>

-   <span data-ttu-id="8045c-237">\_Adresse D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="8045c-237">D3DSAMP\_ADDRESSU</span></span>
-   <span data-ttu-id="8045c-238">D3DSAMP \_ ADDRESSV</span><span class="sxs-lookup"><span data-stu-id="8045c-238">D3DSAMP\_ADDRESSV</span></span>
-   <span data-ttu-id="8045c-239">D3DSAMP \_ ADDRESSW</span><span class="sxs-lookup"><span data-stu-id="8045c-239">D3DSAMP\_ADDRESSW</span></span>
-   <span data-ttu-id="8045c-240">D3DSAMP \_ BORDERCOLOR</span><span class="sxs-lookup"><span data-stu-id="8045c-240">D3DSAMP\_BORDERCOLOR</span></span>
-   <span data-ttu-id="8045c-241">D3DSAMP \_ MAGFILTER</span><span class="sxs-lookup"><span data-stu-id="8045c-241">D3DSAMP\_MAGFILTER</span></span>
-   <span data-ttu-id="8045c-242">D3DSAMP \_ MAXANISOTROPY</span><span class="sxs-lookup"><span data-stu-id="8045c-242">D3DSAMP\_MAXANISOTROPY</span></span>
-   <span data-ttu-id="8045c-243">D3DSAMP \_ MAXMIPLEVEL</span><span class="sxs-lookup"><span data-stu-id="8045c-243">D3DSAMP\_MAXMIPLEVEL</span></span>
-   <span data-ttu-id="8045c-244">D3DSAMP \_ MINFILTER</span><span class="sxs-lookup"><span data-stu-id="8045c-244">D3DSAMP\_MINFILTER</span></span>
-   <span data-ttu-id="8045c-245">D3DSAMP \_ MIPFILTER</span><span class="sxs-lookup"><span data-stu-id="8045c-245">D3DSAMP\_MIPFILTER</span></span>
-   <span data-ttu-id="8045c-246">D3DSAMP \_ MIPMAPLODBIAS</span><span class="sxs-lookup"><span data-stu-id="8045c-246">D3DSAMP\_MIPMAPLODBIAS</span></span>

## <a name="vertex-declaration-changes"></a><span data-ttu-id="8045c-247">Modifications de déclaration de vertex</span><span class="sxs-lookup"><span data-stu-id="8045c-247">Vertex Declaration Changes</span></span>

<span data-ttu-id="8045c-248">Les déclarations de vertex sont maintenant dissociées de la création du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="8045c-248">Vertex declarations are now decoupled from vertex shader creation.</span></span> <span data-ttu-id="8045c-249">Les déclarations de vertex utilisent désormais une interface COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="8045c-249">Vertex declarations now use a Component Object Model (COM) interface.</span></span>

<span data-ttu-id="8045c-250">Pour DirectX 8. x, les déclarations de vertex sont liées aux nuanceurs de vertex.</span><span class="sxs-lookup"><span data-stu-id="8045c-250">For DirectX 8.x, vertex declarations are tied to vertex shaders.</span></span>

-   <span data-ttu-id="8045c-251">Pour le pipeline de fonction fixe, appelez [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) avec le code de format de vertex flexible de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="8045c-251">For the fixed function pipeline, call [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) with the flexible vertex format (FVF) code of the vertex buffer.</span></span>
-   <span data-ttu-id="8045c-252">Pour les nuanceurs vertex, appelez IDirect3DDevice9 :: SetVertexShader avec un handle vers un nuanceur de sommets créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="8045c-252">For vertex shaders, call IDirect3DDevice9::SetVertexShader with a handle to a previously create vertex shader.</span></span> <span data-ttu-id="8045c-253">Le nuanceur comprend une déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="8045c-253">The shader includes a vertex declaration.</span></span>

<span data-ttu-id="8045c-254">Pour Direct3D 9, les déclarations de vertex sont dissociées des nuanceurs de vertex et peuvent être utilisées avec le pipeline de fonction fixe ou avec les nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="8045c-254">For Direct3D 9, vertex declarations are decoupled from vertex shaders and they can be used with either the fixed function pipeline or with shaders.</span></span>

-   <span data-ttu-id="8045c-255">Pour le pipeline de fonction fixe, il n’est pas nécessaire d’appeler IDirect3DDevice9 :: SetVertexShader.</span><span class="sxs-lookup"><span data-stu-id="8045c-255">For the fixed function pipeline, there is no need to call IDirect3DDevice9::SetVertexShader.</span></span> <span data-ttu-id="8045c-256">Toutefois, si vous souhaitez basculer vers le pipeline de fonctions fixe et que vous avez précédemment utilisé un nuanceur de sommets, appelez IDirect3DDevice9 :: SetVertexShader (**null**).</span><span class="sxs-lookup"><span data-stu-id="8045c-256">If, however, you want to switch to the fixed function pipeline and have previously used a vertex shader, call IDirect3DDevice9::SetVertexShader(**NULL**).</span></span> <span data-ttu-id="8045c-257">Une fois cette opération effectuée, vous devrez toujours appeler [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) pour déclarer le code de la Commission.</span><span class="sxs-lookup"><span data-stu-id="8045c-257">When this is done, you will still need to call [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) to declare the FVF code.</span></span>
-   <span data-ttu-id="8045c-258">Quand vous utilisez des nuanceurs vertex, appelez IDirect3DDevice9 :: SetVertexShader avec l’objet vertex shader.</span><span class="sxs-lookup"><span data-stu-id="8045c-258">When using vertex shaders, call IDirect3DDevice9::SetVertexShader with the vertex shader object.</span></span> <span data-ttu-id="8045c-259">En outre, appelez IDirect3DDevice9 :: SetFVF pour configurer une déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="8045c-259">Additionally, call IDirect3DDevice9::SetFVF to set up a vertex declaration.</span></span> <span data-ttu-id="8045c-260">Cela utilise les informations implicites dans le prix de la Commission.</span><span class="sxs-lookup"><span data-stu-id="8045c-260">This uses the information implicit in the FVF.</span></span> <span data-ttu-id="8045c-261">[**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) peut être appelé à la place de IDirect3DDevice9 :: SetFVF, car il prend en charge les déclarations de vertex qui ne peuvent pas être exprimées avec une Commission de la Commission.</span><span class="sxs-lookup"><span data-stu-id="8045c-261">[**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) can be called in place of IDirect3DDevice9::SetFVF because it supports vertex declarations that cannot be expressed with an FVF.</span></span>

## <a name="intervals-and-swapeffects-changes"></a><span data-ttu-id="8045c-262">Intervalles et modifications SwapEffects</span><span class="sxs-lookup"><span data-stu-id="8045c-262">Intervals, and SwapEffects Changes</span></span>

<span data-ttu-id="8045c-263">Plusieurs modifications ont été apportées pour permettre à l’utilisateur de mieux contrôler la fréquence d’actualisation du moniteur, le taux de présentation et le tampon avant et le dessin de la mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="8045c-263">Several changes were made to give the user more control over monitor refresh rate, presentation rate, and front-buffer versus back-buffer drawing.</span></span> <span data-ttu-id="8045c-264">Les voici :</span><span class="sxs-lookup"><span data-stu-id="8045c-264">They are as follows:</span></span>

-   <span data-ttu-id="8045c-265">Suppression d’un effet d’échange, D3DSWAPEFFECT \_ Copy \_ Vsync et d’un taux de présentation, D3DPRESENT \_ rate \_ Unlimited.</span><span class="sxs-lookup"><span data-stu-id="8045c-265">Removed one swap effect, D3DSWAPEFFECT\_COPY\_VSYNC, and one presentation rate, D3DPRESENT\_RATE\_UNLIMITED.</span></span>
-   <span data-ttu-id="8045c-266">Les paramètres D3DPRESENT ont été renommés \_ . PresentationInterval plein écran \_ à PresentationIntervals.</span><span class="sxs-lookup"><span data-stu-id="8045c-266">Renamed D3DPRESENT\_PARAMETERS.FullScreen\_PresentationInterval to PresentationIntervals.</span></span>
-   <span data-ttu-id="8045c-267">Ajout de l' \_ intervalle D3DPRESENT \_ immédiat, ce qui signifie que la présentation n’est pas synchronisée avec la synchronisation verticale. Comme dans DirectX 8. x, la \_ valeur par défaut de l’intervalle D3DPRESENT \_ est définie comme égale à zéro et est équivalente à D3DPRESENT \_ Interval \_ .</span><span class="sxs-lookup"><span data-stu-id="8045c-267">Added D3DPRESENT\_INTERVAL\_IMMEDIATE, which means that the presentation is not synchronized with the vertical sync. As in DirectX 8.x, D3DPRESENT\_INTERVAL\_DEFAULT is defined as zero and is equivalent to D3DPRESENT\_INTERVAL\_ONE.</span></span> <span data-ttu-id="8045c-268">\_ \_ La valeur par défaut de l’intervalle D3DPRESENT est pratique pour initialiser les \_ paramètres D3DPRESENT à zéro.</span><span class="sxs-lookup"><span data-stu-id="8045c-268">D3DPRESENT\_INTERVAL\_DEFAULT is a convenience for initializing D3DPRESENT\_PARAMETERS to zero.</span></span>

<span data-ttu-id="8045c-269">Pour obtenir une explication détaillée des modes et des intervalles pris en charge, consultez D3DPRESENT.</span><span class="sxs-lookup"><span data-stu-id="8045c-269">For a detailed explanation of the modes and the intervals that are supported, see D3DPRESENT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8045c-270">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8045c-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8045c-271">Graphiques Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="8045c-271">Direct3D 9 Graphics</span></span>](dx9-graphics.md)
</dt> </dl>

 

 
