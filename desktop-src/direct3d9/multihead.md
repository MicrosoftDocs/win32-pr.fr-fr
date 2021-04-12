---
description: Les cartes multitête sont celles qui ont une mémoire tampon de frame et un accélérateur communs, des convertisseurs numériques-analogiques (DAC) indépendants et des sorties de surveillance.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Multitête (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4617666ca623795d33bf1dafcaafeabe73323253
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481297"
---
# <a name="multihead-direct3d-9"></a><span data-ttu-id="85cdf-103">Multitête (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85cdf-103">Multihead (Direct3D 9)</span></span>

<span data-ttu-id="85cdf-104">Les cartes multitête sont celles qui ont une mémoire tampon de frame et un accélérateur communs, des convertisseurs numériques-analogiques (DAC) indépendants et des sorties de surveillance.</span><span class="sxs-lookup"><span data-stu-id="85cdf-104">Multihead cards are those that have a common frame buffer and accelerator, independent digital-to-analog converters (DACs), and monitor outputs.</span></span> <span data-ttu-id="85cdf-105">Ces appareils peuvent offrir une prise en charge de plusieurs moniteurs plus utilisable qu’un nombre similaire de cartes d’affichage hétérogènes.</span><span class="sxs-lookup"><span data-stu-id="85cdf-105">Such devices can offer much more usable multiple monitor support than a similar number of heterogeneous display adapters.</span></span>

<span data-ttu-id="85cdf-106">Les cartes multitêtes sont exposées dans l’API en tant qu’appareil unique au niveau de l’API qui peut générer plusieurs chaînes de permutation plein écran.</span><span class="sxs-lookup"><span data-stu-id="85cdf-106">Multihead cards are exposed in the API as a single API-level device that can drive several full-screen swap chains.</span></span> <span data-ttu-id="85cdf-107">Par conséquent, toutes les ressources sont partagées avec tous les en-têtes, et chaque tête a exactement les mêmes fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="85cdf-107">Consequently, all resources are shared with all the heads, and each head has exactly the same capabilities.</span></span> <span data-ttu-id="85cdf-108">Chaque tête peut être définie en mode d’affichage indépendant.</span><span class="sxs-lookup"><span data-stu-id="85cdf-108">Each head can be set to independent display modes.</span></span> <span data-ttu-id="85cdf-109">Vous pouvez utiliser des appels distincts à [**IDirect3DSwapChain9 ::P renvoyés**](/windows/desktop/api) pour actualiser chaque tête.</span><span class="sxs-lookup"><span data-stu-id="85cdf-109">You can use separate calls to [**IDirect3DSwapChain9::Present**](/windows/desktop/api) to refresh each head.</span></span> <span data-ttu-id="85cdf-110">Vous pouvez également utiliser un appel à [**IDirect3DDevice9 ::P renvoyé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) pour actualiser chaque tête de manière séquentielle.</span><span class="sxs-lookup"><span data-stu-id="85cdf-110">You can also use one call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) to refresh each head sequentially.</span></span>

> [!Note]  
> <span data-ttu-id="85cdf-111">L’actualisation de chaque tête ne se produit pas simultanément avec un seul appel à [**IDirect3DDevice9 ::P renvoyé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="85cdf-111">The refresh of each head does not occur simultaneously with a single call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="85cdf-112">Les statistiques présentes dans Direct3D 9Ex peuvent utiliser la structure [**D3DPRESENTSTATS**](d3dpresentstats.md) pour conserver les actualisations de chaque tête près les unes des autres afin de limiter les effets de déchirage sur plusieurs têtes de cartes.</span><span class="sxs-lookup"><span data-stu-id="85cdf-112">Present statistics in Direct3D 9Ex can use the [**D3DPRESENTSTATS**](d3dpresentstats.md) structure to keep the refreshes to each head close to each other to limit tearing effects across multiple heads of adapters.</span></span> <span data-ttu-id="85cdf-113">Pour plus d’informations sur la synchronisation des frames des applications Direct3D 9Ex Flip Model, consultez [améliorations de Direct3D 9Ex](../direct3darticles/direct3d-9ex-improvements.md).</span><span class="sxs-lookup"><span data-stu-id="85cdf-113">For information about synchronizing frames of Direct3D 9Ex flip model applications, see [Direct3D 9Ex Improvements](../direct3darticles/direct3d-9ex-improvements.md).</span></span>

 

<span data-ttu-id="85cdf-114">Chaque chaîne de permutation pour un appareil multitête doit être en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="85cdf-114">Each swap chain for a multihead device must be full screen.</span></span> <span data-ttu-id="85cdf-115">Quand un appareil est entré en mode multitête, il doit rester en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="85cdf-115">When a device has entered multihead mode, it must remain full screen.</span></span> <span data-ttu-id="85cdf-116">La transition vers le mode avec fenêtres nécessite la destruction de l’appareil (à l’exception de l’opération ALT normale + TAB-to-Minimize).</span><span class="sxs-lookup"><span data-stu-id="85cdf-116">The transition back to windowed mode requires the destruction of the device (except for the normal ALT+TAB-to-minimize operation).</span></span>

<span data-ttu-id="85cdf-117">L’ancienne méthode de division de la mémoire vidéo entre les têtes et le traitement de chaque tête en tant qu’accélérateur entièrement indépendant sera toujours un scénario d’utilisation courant.</span><span class="sxs-lookup"><span data-stu-id="85cdf-117">The old method of dividing video memory between the heads and treating each head as a fully independent accelerator will still be a common usage scenario.</span></span> <span data-ttu-id="85cdf-118">Cette proposition ne remplace pas ce mécanisme, sauf si l’application a été spécifiquement codée pour fonctionner en mode multitête Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="85cdf-118">This proposal does not replace that mechanism unless the application has been specifically coded to function in the Direct3D 9 multihead mode.</span></span>

<span data-ttu-id="85cdf-119">Les pilotes disposent d’une connaissance adéquate pour basculer entre les deux modes de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="85cdf-119">Drivers are given adequate knowledge to switch between the two modes of operation.</span></span>

<span data-ttu-id="85cdf-120">L’une des têtes est appelée tête principale et toutes les autres têtes sur la même carte sont appelées têtes subordonnées.</span><span class="sxs-lookup"><span data-stu-id="85cdf-120">One head will be called the master head, and all other heads on the same card be called subordinate heads.</span></span> <span data-ttu-id="85cdf-121">Si plus d’un adaptateur multitête est présent dans un système, le maître et ses subordonnés d’un adaptateur multitête sont appelés groupes.</span><span class="sxs-lookup"><span data-stu-id="85cdf-121">If more than one multihead adapter is present in a system, the master and its subordinates from one multihead adapter are called a group.</span></span> <span data-ttu-id="85cdf-122">Les groupes sont dénotés par l’ordinal d’adaptateur de leur en-tête maître.</span><span class="sxs-lookup"><span data-stu-id="85cdf-122">Groups are denoted by the adapter ordinal of their master head.</span></span>

<span data-ttu-id="85cdf-123">La structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) a été mise à jour pour exposer les nouvelles extrémités matérielles suivantes.</span><span class="sxs-lookup"><span data-stu-id="85cdf-123">The [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure has been updated to expose the following new hardware caps.</span></span>


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   <span data-ttu-id="85cdf-124">NumberOfAdaptersInGroup est égal à 1 pour les adaptateurs conventionnels et supérieur à 1 pour la carte maîtresse d’une carte multitête.</span><span class="sxs-lookup"><span data-stu-id="85cdf-124">NumberOfAdaptersInGroup is 1 for conventional adapters, and greater than 1 for the master adapter of a multihead card.</span></span> <span data-ttu-id="85cdf-125">La valeur sera 0 pour un adaptateur subordonné d’une carte multitête.</span><span class="sxs-lookup"><span data-stu-id="85cdf-125">The value will be 0 for a subordinate adapter of a multihead card.</span></span> <span data-ttu-id="85cdf-126">Chaque carte peut avoir au plus une base de référence, mais elle peut avoir de nombreux subordonnés.</span><span class="sxs-lookup"><span data-stu-id="85cdf-126">Each card can have at most one master, but might have many subordinates.</span></span>
-   <span data-ttu-id="85cdf-127">MasterAdapterOrdinal indique quel appareil est le maître de ce subordonné.</span><span class="sxs-lookup"><span data-stu-id="85cdf-127">MasterAdapterOrdinal indicates which device is the master for this subordinate.</span></span>
-   <span data-ttu-id="85cdf-128">AdapterOrdinalInGroup indique l’ordre dans lequel les têtes sont référencées par l’API.</span><span class="sxs-lookup"><span data-stu-id="85cdf-128">AdapterOrdinalInGroup indicates the order in which heads are referenced by the API.</span></span> <span data-ttu-id="85cdf-129">L’adaptateur maître a toujours le AdapterOrdinalInGroup 0.</span><span class="sxs-lookup"><span data-stu-id="85cdf-129">The master adapter always has AdapterOrdinalInGroup 0.</span></span> <span data-ttu-id="85cdf-130">Ces valeurs ne correspondent pas aux ordinaux des adaptateurs passés aux méthodes IDirect3D9, mais s’appliquent uniquement aux têtes d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="85cdf-130">These values do not correspond to the adapter ordinals passed to the IDirect3D9 methods, but apply only to heads within a group.</span></span>

<span data-ttu-id="85cdf-131">Cette définition permet aux cartes multitête de continuer à présenter plusieurs adaptateurs comme s’il s’agissait de cartes indépendantes, comme c’était le cas dans DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="85cdf-131">This definition allows multihead cards to continue to present multiple adapters as if they were independent cards, just as they did in DirectX 8.</span></span>

<span data-ttu-id="85cdf-132">Pour créer un périphérique multitête, spécifiez l’indicateur de comportement D3DCREATE \_ ADAPTERGROUP \_ Device dans [**IDirect3D9 :: CreateDevice**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="85cdf-132">To create a multihead device, specify the behavior flag D3DCREATE\_ADAPTERGROUP\_DEVICE in [**IDirect3D9::CreateDevice**](/windows/desktop/api).</span></span> <span data-ttu-id="85cdf-133">Les paramètres de présentation (un tableau [**de \_ paramètres D3DPRESENT**](d3dpresent-parameters.md)) doivent contenir des éléments NumberOfAdaptersInGroup.</span><span class="sxs-lookup"><span data-stu-id="85cdf-133">The presentation parameters (an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md)) should contain NumberOfAdaptersInGroup elements.</span></span> <span data-ttu-id="85cdf-134">Le runtime assignera chaque élément à chaque tête dans l’ordre numérique AdapterOrdinalInGroup.</span><span class="sxs-lookup"><span data-stu-id="85cdf-134">The runtime will assign each element to each head in AdapterOrdinalInGroup numerical order.</span></span> <span data-ttu-id="85cdf-135">Lorsque l' \_ appareil D3DCREATE ADAPTERGROUP \_ est défini, chaque paramètre de présentation doit avoir :</span><span class="sxs-lookup"><span data-stu-id="85cdf-135">When D3DCREATE\_ADAPTERGROUP\_DEVICE is set, each presentation parameter must have:</span></span>

-   <span data-ttu-id="85cdf-136">Le membre avec fenêtres a la valeur **false** (en d’autres termes, en mode plein écran).</span><span class="sxs-lookup"><span data-stu-id="85cdf-136">The Windowed member set to **FALSE** (in other words, be full screen).</span></span>
-   <span data-ttu-id="85cdf-137">La même valeur pour le membre EnableAutoDepthStencil des [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="85cdf-137">The same value for the EnableAutoDepthStencil member of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="85cdf-138">En outre, si EnableAutoDepthStencil a la valeur **true**, chacun des champs suivants doit avoir la même valeur pour chaque [**\_ paramètre D3DPRESENT**](d3dpresent-parameters.md):</span><span class="sxs-lookup"><span data-stu-id="85cdf-138">In addition, if EnableAutoDepthStencil is **TRUE**, then each of the following fields must have the same value for each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md):</span></span>

-   <span data-ttu-id="85cdf-139">AutoDepthStencilFormat</span><span class="sxs-lookup"><span data-stu-id="85cdf-139">AutoDepthStencilFormat</span></span>
-   <span data-ttu-id="85cdf-140">BackBufferWidth</span><span class="sxs-lookup"><span data-stu-id="85cdf-140">BackBufferWidth</span></span>
-   <span data-ttu-id="85cdf-141">BackBufferHeight</span><span class="sxs-lookup"><span data-stu-id="85cdf-141">BackBufferHeight</span></span>
-   <span data-ttu-id="85cdf-142">BackBufferFormat</span><span class="sxs-lookup"><span data-stu-id="85cdf-142">BackBufferFormat</span></span>

<span data-ttu-id="85cdf-143">Si la DAC est définie, les appels supplémentaires à [**IDirect3DDevice9 :: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) ne sont pas conformes.</span><span class="sxs-lookup"><span data-stu-id="85cdf-143">If DAC is set, additional calls to [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) are illegal.</span></span>

<span data-ttu-id="85cdf-144">Si l’appareil a été créé avec la DAC, [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) attend un tableau de [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="85cdf-144">If the device was created with the DAC, [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) will expect an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="85cdf-145">Chaque structure de [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md) transmise à [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) doit être en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="85cdf-145">Each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure passed to [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) must be full screen.</span></span> <span data-ttu-id="85cdf-146">Pour revenir au mode fenêtre, l’application doit détruire l’appareil et recréer un appareil non-en-tête en mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="85cdf-146">To switch back to windowed mode, the application must destroy the device and re-create a non-multihead device in windowed mode.</span></span>

<span data-ttu-id="85cdf-147">Voici un scénario d’utilisation de base :</span><span class="sxs-lookup"><span data-stu-id="85cdf-147">Here is a basic usage scenario:</span></span>


```
1. Create multihead device 
2. For each swap chain of device:
   3. Call GetBackBuffer for the i-th swapchain
   4. Call SetRenderTarget 
   5. Call DrawPrimitive 
   6. Optionally call swapchain::Present (or wait until 
all swap chains are drawn and present outside of loop)
7. End the for loop
8. Optionally present all swap chains with device::Present
```



<span data-ttu-id="85cdf-148">Pour plus d’informations, consultez [**IDirect3D9 :: CreateDevice**](/windows/desktop/api) et [**IDirect3DDevice9 :: GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).</span><span class="sxs-lookup"><span data-stu-id="85cdf-148">For more information, see [**IDirect3D9::CreateDevice**](/windows/desktop/api) and [**IDirect3DDevice9::GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).</span></span>

## <a name="related-topics"></a><span data-ttu-id="85cdf-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85cdf-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85cdf-150">Conseils de programmation</span><span class="sxs-lookup"><span data-stu-id="85cdf-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
