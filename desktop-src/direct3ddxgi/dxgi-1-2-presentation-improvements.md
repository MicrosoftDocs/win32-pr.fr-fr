---
title: Retourner le modèle, les rectangles modifiés, les zones défilantes
description: DXGI 1,2 prend en charge une nouvelle chaîne de permutation-modèle, des rectangles modifiés et des zones défilantes. Nous expliquons les avantages de l’utilisation de la nouvelle chaîne de permutation-modèle et de l’optimisation de la présentation en spécifiant des rectangles incorrects et des zones défilantes.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3abbb784de82f5bf647a4b66503497edcd4f89
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104552578"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a><span data-ttu-id="92fb4-104">Retourner le modèle, les rectangles modifiés, les zones défilantes</span><span class="sxs-lookup"><span data-stu-id="92fb4-104">Flip model, dirty rectangles, scrolled areas</span></span>

<span data-ttu-id="92fb4-105">DXGI 1,2 prend en charge une nouvelle chaîne de permutation-modèle, des rectangles modifiés et des zones défilantes.</span><span class="sxs-lookup"><span data-stu-id="92fb4-105">DXGI 1.2 supports a new flip-model swap chain, dirty rectangles, and scrolled areas.</span></span> <span data-ttu-id="92fb4-106">Nous expliquons les avantages de l’utilisation de la nouvelle chaîne de permutation-modèle et de l’optimisation de la présentation en spécifiant des rectangles incorrects et des zones défilantes.</span><span class="sxs-lookup"><span data-stu-id="92fb4-106">We explain the benefits of using the new flip-model swap chain and of optimizing presentation by specifying dirty rectangles and scrolled areas.</span></span>

## <a name="dxgi-flip-model-presentation"></a><span data-ttu-id="92fb4-107">Présentation DXGI Flip-Model</span><span class="sxs-lookup"><span data-stu-id="92fb4-107">DXGI flip-model presentation</span></span>

<span data-ttu-id="92fb4-108">DXGI 1,2 ajoute la prise en charge du modèle de retournement pour les API Direct3D 10 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="92fb4-108">DXGI 1.2 adds support for the flip presentation model for Direct3D 10 and later APIs.</span></span> <span data-ttu-id="92fb4-109">Dans Windows 7, Direct3D 9EX First a adopté la [Présentation Flip-Model](../direct3darticles/direct3d-9ex-improvements.md) pour éviter de copier inutilement la mémoire tampon de chaîne d’échange.</span><span class="sxs-lookup"><span data-stu-id="92fb4-109">In Windows 7, Direct3D 9EX first adopted [flip-model presentation](../direct3darticles/direct3d-9ex-improvements.md) to avoid unnecessarily copying the swap-chain buffer.</span></span> <span data-ttu-id="92fb4-110">En utilisant Flip Model, les mémoires tampons d’arrière-plan sont retournées entre le runtime et Gestionnaire de fenêtrage (DWM), de sorte que le DWM compose toujours directement à partir de la mémoire tampon d’arrière-plan au lieu de copier le contenu de la mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="92fb4-110">By using flip model, back buffers are flipped between the runtime and Desktop Window Manager (DWM), so DWM always composes directly from the back buffer instead of copying the back buffer content.</span></span>

<span data-ttu-id="92fb4-111">Les API DXGI 1,2 incluent une interface révisée de la chaîne d’échange DXGI, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1).</span><span class="sxs-lookup"><span data-stu-id="92fb4-111">DXGI 1.2 APIs include a revised DXGI swap-chain interface, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="92fb4-112">Vous pouvez utiliser plusieurs méthodes d’interface [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) pour créer l’objet **IDXGISwapChain1** approprié à utiliser avec un handle [**HWND**](../winprog/windows-data-types.md) , un objet [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) , [DirectComposition](../directcomp/directcomposition-portal.md)ou le Framework [**Windows. UI. Xaml**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="92fb4-112">You can use multiple [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) interface methods to create the appropriate **IDXGISwapChain1** object to use with an [**HWND**](../winprog/windows-data-types.md) handle, a [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) object, [DirectComposition](../directcomp/directcomposition-portal.md), or the [**Windows.UI.Xaml**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) framework.</span></span>

<span data-ttu-id="92fb4-113">Vous sélectionnez le modèle de retournement de présentation en spécifiant l' [**effet d’échange dxgi retourner la valeur d’énumération \_ \_ \_ \_ séquentielle**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) dans le membre **SwapEffect** de la structure de la [**chaîne de \_ permutation dxgi \_ \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) et en définissant le membre **BufferCount** de la **\_ chaîne de permutation \_ \_** dxgi DESC1 sur un minimum de 2.</span><span class="sxs-lookup"><span data-stu-id="92fb4-113">You select the flip presentation model by specifying the [**DXGI\_SWAP\_EFFECT\_FLIP\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) enumeration value in the **SwapEffect** member of the [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) structure and by setting the **BufferCount** member of **DXGI\_SWAP\_CHAIN\_DESC1** to a minimum of 2.</span></span> <span data-ttu-id="92fb4-114">Pour plus d’informations sur l’utilisation de DXGI Flip Model, consultez [dxgi Flip Model](dxgi-flip-model.md).</span><span class="sxs-lookup"><span data-stu-id="92fb4-114">For more info about how to use DXGI flip model, see [DXGI flip model](dxgi-flip-model.md).</span></span> <span data-ttu-id="92fb4-115">En raison de la présentation fluide et des autres nouvelles fonctionnalités de retournement du modèle de présentation, nous vous recommandons d’utiliser l’outil retourner le modèle de présentation pour toutes les nouvelles applications que vous écrivez avec Direct3D 10 et les API ultérieures.</span><span class="sxs-lookup"><span data-stu-id="92fb4-115">Because of the flip presentation model's smoother presentation and other new functionality, we recommend that you use flip presentation model for all new apps that you write with Direct3D 10 and later APIs.</span></span>

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a><span data-ttu-id="92fb4-116">Utilisation de rectangles modifiés et du rectangle de défilement dans la présentation de la chaîne de permutation</span><span class="sxs-lookup"><span data-stu-id="92fb4-116">Using dirty rectangles and the scroll rectangle in swap chain presentation</span></span>

<span data-ttu-id="92fb4-117">En utilisant des rectangles incorrects et le rectangle de défilement dans la présentation de la chaîne de permutation, vous économisez l’utilisation de la bande passante de mémoire et l’utilisation associée de la puissance système, car la quantité de données de pixels dont le système d’exploitation a besoin pour dessiner le cadre suivant est réduite si le système d’exploitation n’a pas besoin de dessiner l’ensemble</span><span class="sxs-lookup"><span data-stu-id="92fb4-117">By using dirty rectangles and the scroll rectangle in swap chain presentation, you save on the usage of memory bandwidth and the related usage of system power because the amount of pixel data that the operating system needs to draw the next presented frame is reduced if the operating system doesn't need to draw the entire frame.</span></span> <span data-ttu-id="92fb4-118">Pour les applications qui sont souvent affichées via Connexion Bureau à distance et d’autres technologies d’accès à distance, les économies sont particulièrement perceptibles dans la qualité d’affichage, car ces technologies utilisent des rectangles incorrects et des métadonnées de défilement.</span><span class="sxs-lookup"><span data-stu-id="92fb4-118">For apps that are often displayed via Remote Desktop Connection and other remote-accessing technologies, the savings are particularly noticeable in the display quality because these technologies use dirty rectangles and scroll metadata.</span></span>

<span data-ttu-id="92fb4-119">Vous pouvez utiliser Scroll uniquement avec les chaînes de permutation DXGI qui s’exécutent dans le modèle de présentation Flip.</span><span class="sxs-lookup"><span data-stu-id="92fb4-119">You can use scroll only with DXGI swap chains that run in flip presentation model.</span></span> <span data-ttu-id="92fb4-120">Vous pouvez utiliser des rectangles modifiés avec les chaînes de permutation DXGI qui s’exécutent à la fois dans le modèle Flip et dans le modèle BitBlt (défini avec [**dxgi \_ swap \_ Effect \_ Sequential**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span><span class="sxs-lookup"><span data-stu-id="92fb4-120">You can use dirty rectangles with DXGI swap chains that run in both flip model and bitblt model (set with [**DXGI\_SWAP\_EFFECT\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span></span>

<span data-ttu-id="92fb4-121">Dans ce scénario et cette illustration, nous présentons les fonctionnalités d’utilisation des rectangles incorrects et de défilement.</span><span class="sxs-lookup"><span data-stu-id="92fb4-121">In this scenario and illustration we show the functionality of using dirty rectangles and scroll.</span></span> <span data-ttu-id="92fb4-122">Ici, une application défilante contient du texte et anime une vidéo.</span><span class="sxs-lookup"><span data-stu-id="92fb4-122">Here, a scrollable app contains text and animating video.</span></span> <span data-ttu-id="92fb4-123">L’application utilise des rectangles modifiés pour mettre à jour simplement la vidéo d’animation et la nouvelle ligne de la fenêtre, au lieu de mettre à jour la fenêtre entière.</span><span class="sxs-lookup"><span data-stu-id="92fb4-123">The app uses dirty rectangles to just update the animating video and new line for the window, instead of updating the entire window.</span></span> <span data-ttu-id="92fb4-124">Le rectangle de défilement permet au système d’exploitation de copier et de traduire le contenu précédemment rendu sur le nouveau Frame et de restituer uniquement la nouvelle ligne sur le nouveau Frame.</span><span class="sxs-lookup"><span data-stu-id="92fb4-124">The scroll rectangle allows the operating system to copy and translate the previously rendered content on the new frame and to render only the new line on the new frame.</span></span>

<span data-ttu-id="92fb4-125">L’application effectue une présentation en appelant la méthode [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) .</span><span class="sxs-lookup"><span data-stu-id="92fb4-125">The app performs presentation by calling the [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) method.</span></span> <span data-ttu-id="92fb4-126">Dans cet appel, l’application passe un pointeur vers une structure de [**\_ \_ paramètres dxgi présente**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) qui comprend des rectangles incorrects et le nombre de rectangles modifiés, ou le rectangle de défilement et le décalage de défilement associé, ou les deux rectangles de modification et le rectangle de défilement.</span><span class="sxs-lookup"><span data-stu-id="92fb4-126">In this call, the app passes a pointer to a [**DXGI\_PRESENT\_PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) structure that includes dirty rectangles and the number of dirty rectangles, or the scroll rectangle and the associated scroll offset, or both dirty rectangles and the scroll rectangle.</span></span> <span data-ttu-id="92fb4-127">Notre application passe 2 rectangles incorrects et le rectangle de défilement.</span><span class="sxs-lookup"><span data-stu-id="92fb4-127">Our app passes 2 dirty rectangles and the scroll rectangle.</span></span> <span data-ttu-id="92fb4-128">Le rectangle de défilement est la zone du frame précédent que le système d’exploitation doit copier dans le frame actuel avant de restituer le frame actuel.</span><span class="sxs-lookup"><span data-stu-id="92fb4-128">The scroll rectangle is the area of the previous frame that the operating system needs to copy to the current frame before it renders the current frame.</span></span> <span data-ttu-id="92fb4-129">L’application spécifie la vidéo animée et la nouvelle ligne en tant que rectangles modifiés, et le système d’exploitation les affiche sur le frame actuel.</span><span class="sxs-lookup"><span data-stu-id="92fb4-129">The app specifies the animating video and new line as dirty rectangles, and the operating system renders them on the current frame.</span></span>

![illustration du chevauchement des rectangles de défilement et de modification](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

<span data-ttu-id="92fb4-131">Le rectangle en pointillés affiche le rectangle de défilement dans le frame actuel.</span><span class="sxs-lookup"><span data-stu-id="92fb4-131">The dashed rectangle shows the scroll rectangle in the current frame.</span></span> <span data-ttu-id="92fb4-132">Le rectangle de défilement est spécifié par le membre **pScrollRect** des [**\_ \_ paramètres dxgi present**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters).</span><span class="sxs-lookup"><span data-stu-id="92fb4-132">The scroll rectangle is specified by the **pScrollRect** member of [**DXGI\_PRESENT\_PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters).</span></span> <span data-ttu-id="92fb4-133">La flèche affiche le décalage de défilement.</span><span class="sxs-lookup"><span data-stu-id="92fb4-133">The arrow shows the scroll offset.</span></span> <span data-ttu-id="92fb4-134">Le décalage de défilement est spécifié par le membre **pScrollOffset** des **\_ \_ paramètres dxgi present**.</span><span class="sxs-lookup"><span data-stu-id="92fb4-134">The scroll offset is specified by the **pScrollOffset** member of **DXGI\_PRESENT\_PARAMETERS**.</span></span> <span data-ttu-id="92fb4-135">Les rectangles pleins affichent les rectangles modifiés que l’application a mis à jour avec le nouveau contenu.</span><span class="sxs-lookup"><span data-stu-id="92fb4-135">Filled rectangles show dirty rectangles that the app updated with new content.</span></span> <span data-ttu-id="92fb4-136">Les rectangles remplis sont spécifiés par les membres **DirtyRectsCount** et **PDirtyRects** des **\_ \_ paramètres dxgi présents**.</span><span class="sxs-lookup"><span data-stu-id="92fb4-136">The filled rectangles are specified by the **DirtyRectsCount** and **pDirtyRects** members of **DXGI\_PRESENT\_PARAMETERS**.</span></span>

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a><span data-ttu-id="92fb4-137">Exemple 2 : chaîne de permutation du modèle de mise en mémoire tampon avec rectangles modifiés et rectangle de défilement</span><span class="sxs-lookup"><span data-stu-id="92fb4-137">Sample 2-buffer flip-model swap chain with dirty rectangles and scroll rectangle</span></span>

<span data-ttu-id="92fb4-138">L’illustration et la séquence suivantes montrent un exemple d’opération de présentation de DXGI Flip-Model qui utilise des rectangles modifiés et un rectangle de défilement.</span><span class="sxs-lookup"><span data-stu-id="92fb4-138">The next illustration and sequence shows an example of a DXGI flip-model presentation operation that uses dirty rectangles and a scroll rectangle.</span></span> <span data-ttu-id="92fb4-139">Dans cet exemple, nous utilisons le nombre minimal de mémoires tampons pour la présentation de retournement de modèle, qui est un nombre de tampons de deux, une mémoire tampon d’arrière-plan qui contient le contenu d’affichage de l’application et une mémoire tampon d’arrière-plan qui contient le frame actuel que l’application souhaite restituer.</span><span class="sxs-lookup"><span data-stu-id="92fb4-139">In this example we use the minimum number of buffers for flip-model presentation, which is a buffer count of two, one front buffer that contains the app display content and one back buffer that contains the current frame that the app wants to render.</span></span>

1.  <span data-ttu-id="92fb4-140">Comme indiqué dans le tampon d’avant au début du frame, l’application avec défilement affiche initialement un frame avec du texte et anime la vidéo.</span><span class="sxs-lookup"><span data-stu-id="92fb4-140">As shown in the front buffer at the beginning of the frame, the scrollable app initially shows a frame with some text and animating video.</span></span>
2.  <span data-ttu-id="92fb4-141">Pour afficher le frame suivant, l’application effectue le rendu sur la mémoire tampon d’arrière-plan des rectangles incorrects qui mettent à jour la vidéo d’animation et la nouvelle ligne pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="92fb4-141">To render the next frame, the app renders onto the back buffer the dirty rectangles that update the animating video and the new line for the window.</span></span>
3.  <span data-ttu-id="92fb4-142">Lorsque l’application appelle [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), elle spécifie les rectangles modifiés et le rectangle de défilement et le décalage.</span><span class="sxs-lookup"><span data-stu-id="92fb4-142">When the app calls [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), it specifies the dirty rectangles and the scroll rectangle and offset.</span></span> <span data-ttu-id="92fb4-143">Le runtime copie ensuite le rectangle de défilement du frame précédent moins les rectangles modifiés mis à jour dans la mémoire tampon d’arrière-plan actuelle.</span><span class="sxs-lookup"><span data-stu-id="92fb4-143">The runtime next copies the scroll rectangle from the previous frame minus the updated dirty rectangles onto the current back buffer.</span></span>
4.  <span data-ttu-id="92fb4-144">Le runtime échange enfin les mémoires tampons d’arrière-plan et d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="92fb4-144">The runtime finally swaps the front and back buffers.</span></span>

![exemple de chaîne de permutation de modèle avec rectangles défilant et incorrects](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a><span data-ttu-id="92fb4-146">Suivi des rectangles de modification et des rectangles de défilement sur plusieurs frames</span><span class="sxs-lookup"><span data-stu-id="92fb4-146">Tracking dirty rectangles and scroll rectangles across multiple frames</span></span>

<span data-ttu-id="92fb4-147">Lorsque vous utilisez des rectangles modifiés dans votre application, vous devez effectuer le suivi des rectangles modifiés pour prendre en charge le rendu incrémentiel.</span><span class="sxs-lookup"><span data-stu-id="92fb4-147">When you use dirty rectangles in your app, you must track the dirty rectangles to support incremental rendering.</span></span> <span data-ttu-id="92fb4-148">Quand votre application appelle [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) avec des rectangles incorrects, vous devez vous assurer que chaque pixel dans les rectangles incorrects est à jour.</span><span class="sxs-lookup"><span data-stu-id="92fb4-148">When your app calls [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) with dirty rectangles, you must ensure that every pixel within the dirty rectangles is up to date.</span></span> <span data-ttu-id="92fb4-149">Si vous ne rerendez pas complètement la totalité de la zone du rectangle modifié ou si vous ne savez pas quelles sont les zones modifiées, vous devez copier les données de la mémoire tampon d’arrière-plan entièrement cohérente précédente dans la mémoire tampon d’arrière-plan actuelle et obsolète avant de commencer le rendu.</span><span class="sxs-lookup"><span data-stu-id="92fb4-149">If you aren't completely re-rendering the whole area of the dirty rectangle or if you can’t know for certain the areas that are dirtied, you must copy some data from the previous fully coherent back buffer to the current, stale back buffer before you start rendering.</span></span>

<span data-ttu-id="92fb4-150">Le runtime copie uniquement les différences entre les zones mises à jour du frame précédent et les zones mises à jour du frame actuel sur la mémoire tampon d’arrière-plan actuelle.</span><span class="sxs-lookup"><span data-stu-id="92fb4-150">The runtime copies only the differences between updated areas of the previous frame and updated areas of the current frame onto the current back buffer.</span></span> <span data-ttu-id="92fb4-151">Si ces zones se croisent, le runtime copie uniquement la différence entre elles.</span><span class="sxs-lookup"><span data-stu-id="92fb4-151">If these areas intersect, the runtime copies only the difference between them.</span></span> <span data-ttu-id="92fb4-152">Comme vous pouvez le voir dans le diagramme et la séquence suivants, vous devez copier l’intersection entre le rectangle de modification de l’image 1 et le rectangle de modification de l’image 2 dans le rectangle de modification de l’image 2.</span><span class="sxs-lookup"><span data-stu-id="92fb4-152">As you can see in the following diagram and sequence, you must copy the intersection between the dirty rectangle from frame 1 and the dirty rectangle from frame 2 into frame 2’s dirty rectangle.</span></span>

1.  <span data-ttu-id="92fb4-153">Présente le rectangle sale dans le frame 1.</span><span class="sxs-lookup"><span data-stu-id="92fb4-153">Present dirty rectangle in frame 1.</span></span>
2.  <span data-ttu-id="92fb4-154">Copiez l’intersection entre le rectangle modifié du frame 1 et le rectangle modifié du frame 2 dans le rectangle de modification du frame 2.</span><span class="sxs-lookup"><span data-stu-id="92fb4-154">Copy intersection between the dirty rectangle from frame 1 and the dirty rectangle from frame 2 into frame 2’s dirty rectangle.</span></span>
3.  <span data-ttu-id="92fb4-155">Présente le rectangle sale dans le frame 2.</span><span class="sxs-lookup"><span data-stu-id="92fb4-155">Present dirty rectangle in frame 2.</span></span>

![suivi des rectangles de défilement et de modification sur plusieurs frames](images/track-dirty-rects-scroll-rects.png)

<span data-ttu-id="92fb4-157">Pour généraliser, pour une chaîne de permutation avec N mémoires tampons, la zone que le runtime copie à partir du dernier frame jusqu’au frame actuel sur le présent du frame actuel est :</span><span class="sxs-lookup"><span data-stu-id="92fb4-157">To generalize, for a swap chain with N buffers, the area that the runtime copies from the last frame to the current frame on the current frame’s present is:</span></span>

![équation pour calculer la zone copiée par le Runtime](images/runtime-copy-equation.png)

<span data-ttu-id="92fb4-159">où buffer indique l’index de mémoire tampon dans une chaîne de permutation, en commençant par l’index de la mémoire tampon actuel à zéro.</span><span class="sxs-lookup"><span data-stu-id="92fb4-159">where buffer indicates the buffer index in a swap chain, starting with current buffer index at zero.</span></span>

<span data-ttu-id="92fb4-160">Vous pouvez effectuer le suivi de toute intersection entre le frame précédent et les rectangles non intègres du frame actuel en conservant une copie des rectangles incorrects du frame précédent ou en rerendant les rectangles incorrects du nouveau Frame avec le contenu approprié à partir de l’image précédente.</span><span class="sxs-lookup"><span data-stu-id="92fb4-160">You can keep track of any intersections between the previous frame and the current frame’s dirty rectangles by keeping a copy of the previous frame’s dirty rectangles or by re-rendering the new frame’s dirty rectangles with the appropriate content from the previous frame.</span></span>

<span data-ttu-id="92fb4-161">De même, dans les cas où la chaîne de permutation contient plus de 2 mémoires tampons d’arrière-plan, vous devez vous assurer que les zones qui se chevauchent entre les rectangles de modification de la mémoire tampon active et les rectangles incorrects de tous les frames précédents sont copiées ou ré-restituées.</span><span class="sxs-lookup"><span data-stu-id="92fb4-161">Similarly, in the cases where the swap chain has more than 2 back buffers, you must ensure that overlapping areas between the current buffer’s dirty rectangles and the dirty rectangles of all previous frame’s are copied or re-rendered.</span></span>

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a><span data-ttu-id="92fb4-162">Suivi d’une seule intersection entre 2 rectangles incorrects</span><span class="sxs-lookup"><span data-stu-id="92fb4-162">Tracking a single intersection between 2 dirty rectangles</span></span>

<span data-ttu-id="92fb4-163">Dans le cas le plus simple, lorsque vous mettez à jour un rectangle de modification unique par trame, les rectangles modifiés entre deux frames peuvent se croiser.</span><span class="sxs-lookup"><span data-stu-id="92fb4-163">In the simplest case, when you update a single dirty rectangle per frame, the dirty rectangles across two frames might intersect.</span></span> <span data-ttu-id="92fb4-164">Pour déterminer si le rectangle de modification du frame précédent et le rectangle de modification du frame actuel se chevauchent, vous devez vérifier si le rectangle modifié du frame précédent croise le rectangle modifié du frame actuel.</span><span class="sxs-lookup"><span data-stu-id="92fb4-164">To find out whether the dirty rectangle of the previous frame and the dirty rectangle of the current frame overlap, you need to verify whether the dirty rectangle of the previous frame intersects with the dirty rectangle of the current frame.</span></span> <span data-ttu-id="92fb4-165">Vous pouvez appeler la fonction GDI [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) pour déterminer si deux structures [**Rect**](/previous-versions//dd162897(v=vs.85)) qui représentent les deux rectangles incorrects se croisent.</span><span class="sxs-lookup"><span data-stu-id="92fb4-165">You can call the GDI [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) function to determine whether two [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that represent the two dirty rectangles intersect.</span></span>

<span data-ttu-id="92fb4-166">Dans cet extrait de code, un appel à [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) retourne l’intersection de deux rectangles incorrects dans un autre [**Rect**](/previous-versions//dd162897(v=vs.85)) appelé dirtyRectCopy.</span><span class="sxs-lookup"><span data-stu-id="92fb4-166">In this code snippet, a call to [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) returns the intersection of two dirty rectangles in another [**RECT**](/previous-versions//dd162897(v=vs.85)) called dirtyRectCopy.</span></span> <span data-ttu-id="92fb4-167">Une fois que l’extrait de code a déterminé que les deux rectangles incorrects se croisent, il appelle la méthode [**ID3D11DeviceContext1 :: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) pour copier la région d’intersection dans le frame actuel.</span><span class="sxs-lookup"><span data-stu-id="92fb4-167">After the code snippet determines that the two dirty rectangles intersect, it calls the [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) method to copy the region of intersection into the current frame.</span></span>

```
RECT dirtyRectPrev, dirtyRectCurrent, dirtyRectCopy;
 
if (IntersectRect( &dirtyRectCopy, &dirtyRectPrev, &dirtyRectCurrent ))
{
       D3D11_BOX intersectBox;
       intersectBox.left    = dirtyRectCopy.left;
       intersectBox.top     = dirtyRectCopy.top;
       intersectBox.front   = 0;
       intersectBox.right   = dirtyRectCopy.right;
       intersectBox.bottom  = dirtyRectCopy.bottom;
       intersectBox.back    = 1;
 
       d3dContext->CopySubresourceRegion1(pBackbuffer,
                                    0,
                                    0,
                                    0,
                                    0,
                                    pPrevBackbuffer,
                                    0,
                                    &intersectBox,
                                    0
                                    );
}

// Render additional content to the current pBackbuffer and call Present1.
```

<span data-ttu-id="92fb4-168">Si vous utilisez cet extrait de code dans votre application, l’application est alors prête à appeler [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) pour mettre à jour le frame actuel avec le rectangle de modification actuel.</span><span class="sxs-lookup"><span data-stu-id="92fb4-168">If you use this code snippet in your application, the app will then be ready to call [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) to update the current frame with the current dirty rectangle.</span></span>

### <a name="tracking-intersections-between-n-dirty-rectangles"></a><span data-ttu-id="92fb4-169">Suivi des intersections entre N rectangles incorrects</span><span class="sxs-lookup"><span data-stu-id="92fb4-169">Tracking intersections between N dirty rectangles</span></span>

<span data-ttu-id="92fb4-170">Si vous spécifiez plusieurs rectangles incorrects, qui peuvent inclure un rectangle impropre pour la ligne de défilement récemment révélée, par trame, vous devez vérifier et suivre les chevauchements qui peuvent se produire entre tous les rectangles de modification de l’image précédente et tous les rectangles incorrects du frame actuel.</span><span class="sxs-lookup"><span data-stu-id="92fb4-170">If you specify multiple dirty rectangles, which can include a dirty rectangle for the newly revealed scroll line, per frame, you need to verify and track any overlaps that might occur between all the dirty rectangles of the previous frame and all the dirty rectangles of the current frame.</span></span> <span data-ttu-id="92fb4-171">Pour calculer les intersections entre les rectangles modifiés du frame précédent et les rectangles modifiés du frame actuel, vous pouvez regrouper les rectangles incorrects dans des régions.</span><span class="sxs-lookup"><span data-stu-id="92fb4-171">To calculate the intersections between the dirty rectangles of the previous frame and the dirty rectangles of the current frame, you can group the dirty rectangles into regions.</span></span>

<span data-ttu-id="92fb4-172">Dans cet extrait de code, nous appelons la fonction GDI [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) pour convertir chaque rectangle sale en une région rectangulaire, puis nous appelons la fonction GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) pour combiner toutes les régions rectangulaires incorrectes dans un groupe.</span><span class="sxs-lookup"><span data-stu-id="92fb4-172">In this code snippet, we call the GDI [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) function to convert each dirty rectangle into a rectangular region and then we call the GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) function to combine all the dirty rectangular regions into a group.</span></span>

```
HRGN hDirtyRgnPrev, hDirtyRgnCurrent, hRectRgn; // Handles to regions 
// Save all the dirty rectangles from the previous frame.
 
RECT dirtyRect[N]; // N is the number of dirty rectangles in current frame, which includes newly scrolled area.
 
int iReturn;
SetRectRgn(hDirtyRgnCurrent, 
       dirtyRect[0].left, 
       dirtyRect[0].top, 
       dirtyRect[0].right, 
       dirtyRect[0].bottom 
       );

for (int i = 1; i<N; i++)
{
   SetRectRgn(hRectRgn, 
          dirtyRect[0].left, 
          dirtyRect[0].top, 
          dirtyRect[0].right, 
          dirtyRect[0].bottom 
          );

   iReturn = CombineRgn(hDirtyRgnCurrent,
                        hDirtyRgnCurrent,
                        hRectRgn,
                        RGN_OR
                        );
   // Handle the error that CombineRgn returns for iReturn.
}
```

<span data-ttu-id="92fb4-173">Vous pouvez maintenant utiliser la fonction GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) pour déterminer l’intersection entre la région modifiée du frame précédent et la région modifiée du frame actuel.</span><span class="sxs-lookup"><span data-stu-id="92fb4-173">You can now use the GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) function to determine the intersection between the dirty region of the previous frame and the dirty region of the current frame.</span></span> <span data-ttu-id="92fb4-174">Une fois que vous avez obtenu la région d’intersection, appelez la fonction GDI [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) pour obtenir chaque rectangle de la région d’intersection, puis appelez la méthode [**ID3D11DeviceContext1 :: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) pour copier chaque rectangle d’intersection dans la mémoire tampon d’arrière-plan actuelle.</span><span class="sxs-lookup"><span data-stu-id="92fb4-174">After you obtain the intersecting region, call the GDI [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) function to obtain each individual rectangle from the intersecting region and then call the [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) method to copy each intersecting rectangle into the current back buffer.</span></span> <span data-ttu-id="92fb4-175">L’extrait de code suivant montre comment utiliser ces fonctions GDI et Direct3D.</span><span class="sxs-lookup"><span data-stu-id="92fb4-175">The next code snippet shows how to use these GDI and Direct3D functions.</span></span>

```
HRGN hIntersectRgn;
bool bRegionsIntersect;
iReturn = CombineRgn(hIntersectRgn, hDirtyRgnCurrent, hDirtyRgnPrev, RGN_AND);
if (iReturn == ERROR)
{
       // Handle error.
}
else if(iReturn == NULLREGION)
{
       bRegionsIntersect = false;
}
else
{
       bRegionsIntersect = true;
}
 
if (bRegionsIntersect)
{
       int rgnDataSize = GetRegionData(hIntersectRgn, 0, NULL);
       if (rgnDataSize)
       {
              char pMem[] = new char[size];
              RGNDATA* pRgnData = reinterpret_cast<RGNDATA*>(pMem);
              iReturn = GetRegionData(hIntersectRgn, rgnDataSize, pRgnData);
              // Handle iReturn failure.
 
              for (int rectcount = 0; rectcount < pRgnData->rdh.nCount; ++r)
              {
                     const RECT* pIntersectRect = reinterpret_cast<RECT*>(pRgnData->Buffer) +                                            
                                                  rectcount;                
                     D3D11_BOX intersectBox;
                     intersectBox.left    = pIntersectRect->left;
                     intersectBox.top     = pIntersectRect->top;
                     intersectBox.front   = 0;
                     intersectBox.right   = pIntersectRect->right;
                     intersectBox.bottom  = pIntersectRect->bottom;
                     intersectBox.back    = 1;
 
                     d3dContext->CopySubresourceRegion1(pBackbuffer,
                                                      0,
                                                      0,
                                                      0,
                                                      0,
                                                      pPrevBackbuffer,
                                                      0,
                                                      &intersectBox,
                                                      0
                                                      );
              }

              delete [] pMem;
       }
}
```

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a><span data-ttu-id="92fb4-176">Chaîne d’échange de modèle BitBlt avec rectangles modifiés</span><span class="sxs-lookup"><span data-stu-id="92fb4-176">Bitblt model swap chain with dirty rectangles</span></span>

<span data-ttu-id="92fb4-177">Vous pouvez utiliser des rectangles modifiés avec les chaînes de permutation DXGI qui s’exécutent dans le modèle BitBlt (défini avec l' [**\_ effet d’échange dxgi \_ \_ séquentiel**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span><span class="sxs-lookup"><span data-stu-id="92fb4-177">You can use dirty rectangles with DXGI swap chains that run in bitblt model (set with [**DXGI\_SWAP\_EFFECT\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span></span> <span data-ttu-id="92fb4-178">Les chaînes d’échange de modèle BitBlt qui utilisent plusieurs mémoires tampons doivent également suivre les rectangles de modification qui se chevauchent entre les frames de la même façon que celle décrite dans [suivi des rectangles incorrects et des rectangles de défilement sur plusieurs frames](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) pour les chaînes de permutation du modèle.</span><span class="sxs-lookup"><span data-stu-id="92fb4-178">Bitblt model swap chains that use more than one buffer must also track overlapping dirty rectangles across frames in the same way as described in [Tracking dirty rectangles and scroll rectangles across multiple frames](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) for flip model swap chains.</span></span> <span data-ttu-id="92fb4-179">Les chaînes d’échange de modèle BitBlt avec une seule mémoire tampon n’ont pas besoin de suivre les rectangles de modification qui se chevauchent, car la mémoire tampon entière est redessinée à chaque trame.</span><span class="sxs-lookup"><span data-stu-id="92fb4-179">Bitblt model swap chains with just one buffer need not track overlapping dirty rectangles because the entire buffer is redrawn every frame.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92fb4-180">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92fb4-180">Related topics</span></span>

[<span data-ttu-id="92fb4-181">Améliorations de DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="92fb4-181">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
