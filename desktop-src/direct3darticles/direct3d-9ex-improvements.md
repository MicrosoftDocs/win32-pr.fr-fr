---
title: Améliorations de Direct3D 9Ex
description: Cette rubrique décrit la prise en charge intégrée de Windows 7 pour le mode de basculement présent et les statistiques actuelles associées dans Direct3D 9Ex et Gestionnaire de fenêtrage.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42eef10b6caaa959cb750f073c97a0f665384463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382413"
---
# <a name="direct3d-9ex-improvements"></a><span data-ttu-id="c9022-103">Améliorations de Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="c9022-103">Direct3D 9Ex improvements</span></span>

<span data-ttu-id="c9022-104">Cette rubrique décrit la prise en charge intégrée de Windows 7 pour le mode de basculement présent et les statistiques actuelles associées dans Direct3D 9Ex et Gestionnaire de fenêtrage.</span><span class="sxs-lookup"><span data-stu-id="c9022-104">This topic describes Windows 7's added support for Flip Mode Present and its associated present statistics in Direct3D 9Ex and Desktop Window Manager.</span></span> <span data-ttu-id="c9022-105">Les applications cibles incluent des vidéos ou des applications de présentation basées sur la fréquence des images.</span><span class="sxs-lookup"><span data-stu-id="c9022-105">Target applications include video or frame rate-based presentation applications.</span></span> <span data-ttu-id="c9022-106">Les applications qui utilisent le mode de basculement Direct3D 9Ex présentent réduisent la charge des ressources système lorsque DWM est activé.</span><span class="sxs-lookup"><span data-stu-id="c9022-106">Applications that use Direct3D 9Ex Flip Mode Present reduce the system resource load when DWM is enabled.</span></span> <span data-ttu-id="c9022-107">La présentation des améliorations des statistiques associées au mode de basculement présente permet aux applications Direct3D 9Ex de mieux contrôler le taux de présentation en fournissant des mécanismes de commentaires et de correction en temps réel.</span><span class="sxs-lookup"><span data-stu-id="c9022-107">Present statistics enhancements associated with Flip Mode Present enable Direct3D 9Ex applications to better control the rate of presentation by providing real-time feedback and correction mechanisms.</span></span> <span data-ttu-id="c9022-108">Des explications détaillées et des pointeurs vers des exemples de ressources sont inclus.</span><span class="sxs-lookup"><span data-stu-id="c9022-108">Detailed explanations and pointers to sample resources are included.</span></span>

<span data-ttu-id="c9022-109">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c9022-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c9022-110">Améliorations de Direct3D 9Ex pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="c9022-110">What's Improved about Direct3D 9Ex for Windows 7</span></span>](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [<span data-ttu-id="c9022-111">Présentation du mode de basculement de Direct3D 9EX</span><span class="sxs-lookup"><span data-stu-id="c9022-111">Direct3D 9EX Flip Mode Presentation</span></span>](#direct3d-9ex-flip-mode-presentation)
-   [<span data-ttu-id="c9022-112">Modèle de programmation et API</span><span class="sxs-lookup"><span data-stu-id="c9022-112">Programming Model and APIs</span></span>](#programming-model-and-apis)
    -   [<span data-ttu-id="c9022-113">Comment s’abonner au modèle de basculement Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="c9022-113">How to Opt Into the Direct3D 9Ex Flip Model</span></span>](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [<span data-ttu-id="c9022-114">Instructions de conception pour les applications de basculement Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="c9022-114">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="c9022-115">Synchronisation des frames des applications Direct3D 9Ex Flip Model</span><span class="sxs-lookup"><span data-stu-id="c9022-115">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="c9022-116">Synchronisation des frames pour les applications Windows lorsque DWM est désactivé</span><span class="sxs-lookup"><span data-stu-id="c9022-116">Frame Synchronization for Windowed Applications When DWM is Off</span></span>](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [<span data-ttu-id="c9022-117">Guide pas à pas d’un modèle de basculement Direct3D 9Ex et présentation de l’exemple de statistiques</span><span class="sxs-lookup"><span data-stu-id="c9022-117">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [<span data-ttu-id="c9022-118">Résumé des recommandations de programmation pour la synchronisation de frames</span><span class="sxs-lookup"><span data-stu-id="c9022-118">Summary of Programming Recommendations for Frame Synchronization</span></span>](#summary-of-programming-recommendations-for-frame-synchronization)
-   [<span data-ttu-id="c9022-119">Conclusion sur les améliorations Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="c9022-119">Conclusion about Direct3D 9Ex Improvements</span></span>](#conclusion-about-direct3d-9ex-improvements)
-   [<span data-ttu-id="c9022-120">Appel à l’action</span><span class="sxs-lookup"><span data-stu-id="c9022-120">Call to Action</span></span>](#call-to-action)
-   [<span data-ttu-id="c9022-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9022-121">Related topics</span></span>](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a><span data-ttu-id="c9022-122">Améliorations de Direct3D 9Ex pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="c9022-122">What's Improved about Direct3D 9Ex for Windows 7</span></span>

<span data-ttu-id="c9022-123">La présentation en mode Flip de Direct3D 9Ex est un mode amélioré de présentation d’images dans Direct3D 9Ex qui transmet efficacement les images rendues à Windows 7 Gestionnaire de fenêtrage (DWM) pour la composition.</span><span class="sxs-lookup"><span data-stu-id="c9022-123">Flip Mode Presentation of Direct3D 9Ex is an improved mode of presenting images in Direct3D 9Ex that efficiently hands off rendered images to Windows 7 Desktop Window Manager (DWM) for composition.</span></span> <span data-ttu-id="c9022-124">À compter de Windows Vista, DWM compose la totalité du bureau.</span><span class="sxs-lookup"><span data-stu-id="c9022-124">Beginning in Windows Vista, DWM composes the entire Desktop.</span></span> <span data-ttu-id="c9022-125">Lorsque DWM est activé, les applications en mode fenêtre présentent leur contenu sur le Bureau à l’aide d’une méthode appelée mode BLT présente dans DWM (ou le modèle BLT).</span><span class="sxs-lookup"><span data-stu-id="c9022-125">When DWM is enabled, windowed mode applications present their contents on the Desktop by using a method called Blt Mode Present to DWM (or Blt Model).</span></span> <span data-ttu-id="c9022-126">Avec le modèle BLT, DWM conserve une copie de la surface de rendu Direct3D 9Ex pour la composition du bureau.</span><span class="sxs-lookup"><span data-stu-id="c9022-126">With Blt Model, DWM maintains a copy of the Direct3D 9Ex rendered surface for Desktop composition.</span></span> <span data-ttu-id="c9022-127">Lorsque l’application est mise à jour, le nouveau contenu est copié vers la surface DWM via un BLT.</span><span class="sxs-lookup"><span data-stu-id="c9022-127">When the application updates, the new content is copied to the DWM surface through a blt.</span></span> <span data-ttu-id="c9022-128">Pour les applications qui contiennent du contenu Direct3D et GDI, les données GDI sont également copiées sur la surface DWM.</span><span class="sxs-lookup"><span data-stu-id="c9022-128">For applications that contain Direct3D and GDI content, the GDI data is also copied onto the DWM surface.</span></span>

<span data-ttu-id="c9022-129">Disponible dans Windows 7, le mode Flip présent dans DWM (ou Flip Model) est une nouvelle méthode de présentation qui permet essentiellement de passer les descripteurs des surfaces d’application entre les applications en mode fenêtre et le DWM.</span><span class="sxs-lookup"><span data-stu-id="c9022-129">Available in Windows 7, Flip Mode Present to DWM (or Flip Model) is a new presentation method that essentially enables passing handles of application surfaces between windowed mode applications and DWM.</span></span> <span data-ttu-id="c9022-130">Outre l’enregistrement des ressources, l’inversion du modèle prend en charge les statistiques actuelles améliorées.</span><span class="sxs-lookup"><span data-stu-id="c9022-130">In addition to saving resources, Flip Model supports enhanced present statistics.</span></span>

<span data-ttu-id="c9022-131">Les statistiques présentent les informations de minutage des trames que les applications peuvent utiliser pour synchroniser les flux vidéo et audio et récupérer des problèmes de lecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="c9022-131">Present statistics are frame-timing information that applications can use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="c9022-132">Les informations de minutage de trame dans les statistiques actuelles permettent aux applications d’ajuster la vitesse de présentation de leurs images vidéo pour une présentation plus lisse.</span><span class="sxs-lookup"><span data-stu-id="c9022-132">The frame-timing information in present statistics allows applications to adjust the presentation rate of their video frames for smoother presentation.</span></span> <span data-ttu-id="c9022-133">Dans Windows Vista, où DWM conserve une copie correspondante de la surface de cadre pour la composition du bureau, les applications peuvent utiliser les statistiques fournies par DWM.</span><span class="sxs-lookup"><span data-stu-id="c9022-133">In Windows Vista, where DWM maintains a corresponding copy of the frame surface for Desktop composition, applications can use present statistics provided by DWM.</span></span> <span data-ttu-id="c9022-134">Cette méthode d’obtention des statistiques actuelles sera toujours disponible dans Windows 7 pour les applications existantes.</span><span class="sxs-lookup"><span data-stu-id="c9022-134">This method of obtaining present statistics will still be available in Windows 7 for existing applications.</span></span>

<span data-ttu-id="c9022-135">Dans Windows 7, les applications Direct3D 9Ex qui adoptent le modèle de basculement doivent utiliser des API D3D9Ex pour obtenir les statistiques actuelles.</span><span class="sxs-lookup"><span data-stu-id="c9022-135">In Windows 7, Direct3D 9Ex-based applications that adopt Flip Model should use D3D9Ex APIs to obtain present statistics.</span></span> <span data-ttu-id="c9022-136">Lorsque DWM est activé, les applications en mode fenêtre et en mode exclusif Direct3D 9Ex peuvent attendre les mêmes informations sur les statistiques lors de l’utilisation de Flip Model.</span><span class="sxs-lookup"><span data-stu-id="c9022-136">When DWM is enabled, windowed mode and full-screen exclusive mode Direct3D 9Ex applications can expect the same present statistics information when using Flip Model.</span></span> <span data-ttu-id="c9022-137">Direct3D 9Ex Flip Model sent Statistics permet aux applications d’interroger les statistiques actuelles en temps réel, plutôt qu’une fois que le frame a été affiché à l’écran. les mêmes informations statistiques sont disponibles pour les applications en mode fenêtre Flip-Model activées en tant qu’applications plein écran. un indicateur ajouté dans les API D3D9Ex permet aux applications de retournement de supprimer efficacement les trames tardives au moment de la présentation.</span><span class="sxs-lookup"><span data-stu-id="c9022-137">Direct3D 9Ex Flip Model present statistics enable applications to query for present statistics in real time, rather than after the frame has been shown on screen; the same present statistics information is available for windowed-mode Flip-Model enabled applications as full-screen applications; an added flag in D3D9Ex APIs allows Flip Model applications to effectively discard late frames at presentation time.</span></span>

<span data-ttu-id="c9022-138">Le modèle de retournement de Direct3D 9Ex doit être utilisé par les nouvelles applications vidéo ou de présentation basées sur la fréquence des images qui ciblent Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c9022-138">Direct3D 9Ex Flip Model should be used by new video or frame rate-based presentation applications that target Windows 7.</span></span> <span data-ttu-id="c9022-139">En raison de la synchronisation entre le DWM et le runtime Direct3D 9Ex, les applications qui utilisent Flip Model doivent spécifier entre 2 et 4 mémoires tampons pour garantir une présentation fluide.</span><span class="sxs-lookup"><span data-stu-id="c9022-139">Because of the synchronization between DWM and the Direct3D 9Ex runtime, applications that use Flip Model should specify between 2 to 4 backbuffers to ensure smooth presentation.</span></span> <span data-ttu-id="c9022-140">Les applications qui utilisent les informations de statistiques actuelles tireront parti de l’amélioration des statistiques de retournement activé.</span><span class="sxs-lookup"><span data-stu-id="c9022-140">Those applications that use present statistics information will benefit from using Flip Model enabled present statistics enhancements.</span></span>

## <a name="direct3d-9ex-flip-mode-presentation"></a><span data-ttu-id="c9022-141">Présentation du mode de basculement de Direct3D 9EX</span><span class="sxs-lookup"><span data-stu-id="c9022-141">Direct3D 9EX Flip Mode Presentation</span></span>

<span data-ttu-id="c9022-142">Les améliorations des performances du mode de basculement de Direct3D 9Ex sont importantes sur le système lorsque DWM est activé et lorsque l’application est en mode fenêtre, plutôt qu’en mode exclusif plein écran.</span><span class="sxs-lookup"><span data-stu-id="c9022-142">Performance improvements of Direct3D 9Ex Flip Mode Present are significant on the system when DWM is on and when the application is in windowed mode, rather than in full screen exclusive mode.</span></span> <span data-ttu-id="c9022-143">Le tableau et l’illustration suivantes présentent une comparaison simplifiée des utilisations de la bande passante de la mémoire et des lectures et écritures système des applications Windows qui choisissent le modèle Flip Model et le modèle BLT d’utilisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="c9022-143">The following table and illustration show a simplified comparison of memory bandwidth usages and system reads and writes of windowed applications that choose Flip Model versus the default usage Blt Model.</span></span>



| <span data-ttu-id="c9022-144">Mode BLT présent dans DWM</span><span class="sxs-lookup"><span data-stu-id="c9022-144">Blt mode present to DWM</span></span>                                                                                                 | <span data-ttu-id="c9022-145">Mode de basculement de D3D9Ex présent dans DWM</span><span class="sxs-lookup"><span data-stu-id="c9022-145">D3D9Ex Flip Mode Present to DWM</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="c9022-146">1. l’application met à jour son Frame (écriture)</span><span class="sxs-lookup"><span data-stu-id="c9022-146">1. The application updates its frame (Write)</span></span><br/>                                                                 | <span data-ttu-id="c9022-147">1. l’application met à jour son Frame (écriture)</span><span class="sxs-lookup"><span data-stu-id="c9022-147">1. The application updates its frame (Write)</span></span><br/>                     |
| <span data-ttu-id="c9022-148">2. le runtime Direct3D copie le contenu de la surface dans une surface de redirection DWM (lecture, écriture)</span><span class="sxs-lookup"><span data-stu-id="c9022-148">2. Direct3D runtime copies surface contents to a DWM redirection surface (Read, Write)</span></span><br/>                       | <span data-ttu-id="c9022-149">2. le runtime Direct3D passe l’aire de l’application à DWM</span><span class="sxs-lookup"><span data-stu-id="c9022-149">2. Direct3D runtime passes the application surface to DWM</span></span><br/>        |
| <span data-ttu-id="c9022-150">3. une fois la copie de la surface partagée terminée, DWM restitue l’aire de l’application sur l’écran (lecture, écriture)</span><span class="sxs-lookup"><span data-stu-id="c9022-150">3. After the shared surface copy is completed, DWM renders the application surface onto screen (Read, Write)</span></span><br/> | <span data-ttu-id="c9022-151">3. DWM affiche l’aire de l’application sur l’écran (lecture, écriture)</span><span class="sxs-lookup"><span data-stu-id="c9022-151">3. DWM renders the application surface onto screen (Read, Write)</span></span><br/> |



 

![illustration d’une comparaison entre le modèle BLT et le modèle Flip](images/blt-flip-mode-present.png)

<span data-ttu-id="c9022-153">Le mode de basculement présent réduit l’utilisation de la mémoire système en réduisant le nombre de lectures et d’écritures par le runtime Direct3D pour la composition de frame avec fenêtres par DWM.</span><span class="sxs-lookup"><span data-stu-id="c9022-153">Flip Mode Present reduces system memory usage by reducing the number of reads and writes by the Direct3D runtime for the windowed frame composition by DWM.</span></span> <span data-ttu-id="c9022-154">Cela réduit la consommation d’énergie du système et l’utilisation de la mémoire globale.</span><span class="sxs-lookup"><span data-stu-id="c9022-154">This reduces the system power consumption and overall memory usage.</span></span>

<span data-ttu-id="c9022-155">Les applications peuvent tirer parti du mode de basculement Direct3D 9Ex présentent des améliorations des statistiques lorsque DWM est activé, que l’application soit en mode fenêtre ou en mode exclusif plein écran.</span><span class="sxs-lookup"><span data-stu-id="c9022-155">Applications can take advantage of Direct3D 9Ex Flip Mode present statistics enhancements when DWM is on, regardless of whether the application is in windowed mode or in full screen exclusive mode.</span></span>

## <a name="programming-model-and-apis"></a><span data-ttu-id="c9022-156">Modèle de programmation et API</span><span class="sxs-lookup"><span data-stu-id="c9022-156">Programming Model and APIs</span></span>

<span data-ttu-id="c9022-157">Les nouvelles applications vidéo ou de fréquence d’images qui utilisent des API Direct3D 9Ex sur Windows 7 peuvent tirer parti de la mémoire et des économies d’énergie, ainsi que de la présentation améliorée proposée par le mode Flip sur Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c9022-157">New video or frame rate-gauging applications that use Direct3D 9Ex APIs on Windows 7 can take advantage of the memory and power savings and of the improved presentation offered by Flip Mode Present when running on Windows 7.</span></span> <span data-ttu-id="c9022-158">(En cas d’exécution sur des versions précédentes de Windows, le runtime Direct3D utilise par défaut le mode BLT pour l’application.)</span><span class="sxs-lookup"><span data-stu-id="c9022-158">(When running on previous Windows versions, the Direct3D runtime defaults the application to Blt Mode Present.)</span></span>

<span data-ttu-id="c9022-159">Le mode de basculement présente que l’application peut tirer parti des mécanismes de commentaires et de correction des statistiques en temps réel lorsque DWM est activé.</span><span class="sxs-lookup"><span data-stu-id="c9022-159">Flip Mode Present entails that the application can take advantage of real-time present statistics feedback and correction mechanisms when DWM is on.</span></span> <span data-ttu-id="c9022-160">Toutefois, les applications qui utilisent le mode Flip doivent être conscientes des limitations lorsqu’elles utilisent le rendu simultané de l’API GDI.</span><span class="sxs-lookup"><span data-stu-id="c9022-160">However, applications that use Flip Mode Present should be aware of limitations when they use concurrent GDI API rendering.</span></span>

<span data-ttu-id="c9022-161">Vous pouvez modifier les applications existantes pour tirer parti du mode de basculement, avec les mêmes avantages et les mêmes avertissements que les applications récemment développées.</span><span class="sxs-lookup"><span data-stu-id="c9022-161">You can modify existing applications to take advantage of Flip Mode Present, with the same benefits and caveats as the newly developed applications.</span></span>

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a><span data-ttu-id="c9022-162">Comment s’abonner au modèle de basculement Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="c9022-162">How to Opt Into the Direct3D 9Ex Flip Model</span></span>

<span data-ttu-id="c9022-163">Les applications Direct3D 9Ex qui ciblent Windows 7 peuvent s’abonner au modèle de basculement en créant la chaîne de permutation avec la valeur d’énumération [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) .</span><span class="sxs-lookup"><span data-stu-id="c9022-163">Direct3D 9Ex applications that target Windows 7 can opt into the Flip Model by creating the swap chain with the [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) enumeration value.</span></span> <span data-ttu-id="c9022-164">Pour s’abonner au modèle Flip, les applications spécifient la structure de [**\_ paramètres D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) , puis passent un pointeur vers cette structure lorsqu’ils appellent l’API [**IDirect3D9Ex :: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) .</span><span class="sxs-lookup"><span data-stu-id="c9022-164">To opt into the Flip Model, applications specify the [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) structure, and then pass a pointer to this structure when they call the [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) API.</span></span> <span data-ttu-id="c9022-165">Cette section décrit comment les applications qui ciblent Windows 7 utilisent **IDirect3D9Ex :: CreateDeviceEx** pour s’abonner au modèle de retournement.</span><span class="sxs-lookup"><span data-stu-id="c9022-165">This section describes how applications that target Windows 7 use **IDirect3D9Ex::CreateDeviceEx** to opt into the Flip Model.</span></span> <span data-ttu-id="c9022-166">Pour plus d’informations sur l’API **IDirect3D9Ex :: CreateDeviceEx** , consultez **IDirect3D9Ex :: CreateDeviceEx sur MSDN**.</span><span class="sxs-lookup"><span data-stu-id="c9022-166">For more information about the **IDirect3D9Ex::CreateDeviceEx** API, see **IDirect3D9Ex::CreateDeviceEx on MSDN**.</span></span>

<span data-ttu-id="c9022-167">Pour plus de commodité, la syntaxe des [**\_ paramètres D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) et [**IDirect3D9Ex :: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) sont répétées ici.</span><span class="sxs-lookup"><span data-stu-id="c9022-167">For convenience, the syntax of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) and [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

<span data-ttu-id="c9022-168">Lorsque vous modifiez les applications Direct3D 9Ex pour Windows 7 afin d’accepter le modèle de basculement, vous devez prendre en compte les éléments suivants concernant les membres spécifiés des [**\_ paramètres D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters):</span><span class="sxs-lookup"><span data-stu-id="c9022-168">When you modify Direct3D 9Ex applications for Windows 7 to opt into the Flip Model, you should consider the following items about the specified members of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters):</span></span>

<dl> <dt>

<span data-ttu-id="c9022-169">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="c9022-169">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="c9022-170">(Windows 7 uniquement)</span><span class="sxs-lookup"><span data-stu-id="c9022-170">(Windows 7 Only)</span></span>

<span data-ttu-id="c9022-171">Quand **SwapEffect** est défini sur le nouveau \_ type d’effet de chaîne d’échange FLIPEX D3DSWAPEFFECT, le nombre de mémoires tampons d’arrière-plan doit être égal ou supérieur à 2, pour empêcher une baisse des performances de l’application en raison de l’attente de la libération de la mémoire tampon précédente précédente par DWM.</span><span class="sxs-lookup"><span data-stu-id="c9022-171">When **SwapEffect** is set to the new D3DSWAPEFFECT\_FLIPEX swap chain effect type, the back buffer count should be equal or greater than 2, to prevent an application performance penalty as a result of waiting on the previous Present buffer to be released by DWM.</span></span>

<span data-ttu-id="c9022-172">Lorsque l’application utilise également les statistiques actuelles associées à D3DSWAPEFFECT \_ FLIPEX, nous vous recommandons de définir le nombre de mémoires tampons d’arrière-plan sur une valeur comprise entre 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="c9022-172">When the application also uses present statistics associated with D3DSWAPEFFECT\_FLIPEX, we recommend that you set the back buffer count to from 2 to 4.</span></span>

<span data-ttu-id="c9022-173">L’utilisation de D3DSWAPEFFECT \_ FLIPEX sur Windows Vista ou des versions de système d’exploitation précédentes retourne Fail à partir de [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="c9022-173">Using D3DSWAPEFFECT\_FLIPEX on Windows Vista or previous operating system versions will return fail from [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

<span data-ttu-id="c9022-174">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="c9022-174">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="c9022-175">(Windows 7 uniquement)</span><span class="sxs-lookup"><span data-stu-id="c9022-175">(Windows 7 Only)</span></span>

<span data-ttu-id="c9022-176">Le nouveau \_ type d’effet de chaîne de permutation D3DSWAPEFFECT FLIPEX désigne le moment où une application adopte le mode Flip présent dans DWM.</span><span class="sxs-lookup"><span data-stu-id="c9022-176">The new D3DSWAPEFFECT\_FLIPEX swap chain effect type designates when an application is adopting Flip Mode Present to DWM.</span></span> <span data-ttu-id="c9022-177">Il permet à l’application d’utiliser plus efficacement la mémoire et la puissance, et permet également à l’application de tirer parti des statistiques de présentation en plein écran en mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c9022-177">It allows the application more efficient usage of memory and power, and also enables the application to take advantage of full-screen present statistics in windowed mode.</span></span> <span data-ttu-id="c9022-178">Le comportement de l’application en plein écran n’est pas affecté.</span><span class="sxs-lookup"><span data-stu-id="c9022-178">Full-screen application behavior is not affected.</span></span> <span data-ttu-id="c9022-179">Si Windowed a la valeur **true** et que **SwapEffect** a la valeur D3DSWAPEFFECT \_ FLIPEX, le runtime crée une mémoire tampon d’arrière-plan supplémentaire et fait pivoter le handle qui appartient à la mémoire tampon qui devient la mémoire tampon d’arrière-plan au moment de la présentation.</span><span class="sxs-lookup"><span data-stu-id="c9022-179">If Windowed is set to **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIPEX, the runtime creates one extra back buffer and rotates whichever handle belongs to the buffer that becomes the front buffer at presentation time.</span></span>

</dd> <dt>

<span data-ttu-id="c9022-180">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="c9022-180">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="c9022-181">(Windows 7 uniquement)</span><span class="sxs-lookup"><span data-stu-id="c9022-181">(Windows 7 Only)</span></span>

<span data-ttu-id="c9022-182">L’indicateur de [ \_ \_ mémoire tampon D3DPRESENTFLAG verrouillable](/windows/desktop/direct3d9/d3dpresentflag) ne peut pas être défini si **SwapEffect** est défini sur le nouveau type d’effet de chaîne de permutation [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) .</span><span class="sxs-lookup"><span data-stu-id="c9022-182">The [D3DPRESENTFLAG\_LOCKABLE\_BACKBUFFER](/windows/desktop/direct3d9/d3dpresentflag) flag cannot be set if **SwapEffect** is set to the new [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chain effect type.</span></span>

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="c9022-183">Instructions de conception pour les applications de basculement Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="c9022-183">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="c9022-184">Utilisez les instructions des sections suivantes pour concevoir vos applications Direct3D 9Ex Flip Model.</span><span class="sxs-lookup"><span data-stu-id="c9022-184">Use the guidelines in the following sections to design your Direct3D 9Ex Flip Model applications.</span></span>

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a><span data-ttu-id="c9022-185">Utiliser le mode Flip présent dans un HWND distinct du mode BLT présent</span><span class="sxs-lookup"><span data-stu-id="c9022-185">Use Flip Mode Present in a Separate HWND from Blt Mode Present</span></span>

<span data-ttu-id="c9022-186">Les applications doivent utiliser le mode de basculement de Direct3D 9Ex présent dans un HWND qui n’est pas également ciblé par d’autres API, y compris le mode BLT présente Direct3D 9Ex, d’autres versions de Direct3D ou GDI.</span><span class="sxs-lookup"><span data-stu-id="c9022-186">Applications should use Direct3D 9Ex Flip Mode Present in an HWND that is not also targeted by other APIs, including Blt Mode Present Direct3D 9Ex, other versions of Direct3D, or GDI.</span></span> <span data-ttu-id="c9022-187">Le mode de basculement présent peut être utilisé pour présenter des fenêtres enfants. autrement dit, les applications peuvent utiliser Flip Model lorsqu’elles ne sont pas mélangées avec le modèle BLT dans le même HWND, comme indiqué dans les illustrations suivantes.</span><span class="sxs-lookup"><span data-stu-id="c9022-187">Flip Mode Present can be used to present to child windows; that is, applications can use Flip Model when it is not mixed with Blt Model in the same HWND, as shown in the following illustrations.</span></span>

![illustration de la fenêtre parente Direct3D et d’une fenêtre enfant GDI, chacune avec son propre HWND](images/parent-d3d.png)

![illustration de la fenêtre parente GDI et d’une fenêtre enfant Direct3D, chacune avec son propre HWND](images/parent-gdi.png)

<span data-ttu-id="c9022-190">Étant donné que le modèle BLT gère une copie supplémentaire de la surface, GDI et d’autres contenus Direct3D peuvent être ajoutés au même HWND par le biais de mises à jour fragmentées de Direct3D et GDI.</span><span class="sxs-lookup"><span data-stu-id="c9022-190">Because Blt Model maintains an additional copy of the surface, GDI and other Direct3D contents can be added to the same HWND through piecemeal updates from Direct3D and GDI.</span></span> <span data-ttu-id="c9022-191">À l’aide du modèle de retournement, seul le contenu Direct3D 9Ex dans les chaînes de permutation [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) transmises à DWM sera visible.</span><span class="sxs-lookup"><span data-stu-id="c9022-191">Using the Flip Model, only Direct3D 9Ex content in [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chains that are passed to DWM will be visible.</span></span> <span data-ttu-id="c9022-192">Toutes les autres mises à jour de contenu Direct3D ou GDI du modèle BLT seront ignorées, comme indiqué dans les illustrations suivantes.</span><span class="sxs-lookup"><span data-stu-id="c9022-192">All other Blt Model Direct3D or GDI content updates will be ignored, as shown in the following illustrations.</span></span>

![illustration du texte GDI qui peut ne pas s’afficher si l’utilisation de l’opération Flip Model est utilisée et que le contenu Direct3D et GDI se trouvent dans le même HWND](images/d3d-gdi-same-hwnd.png)

![illustration du contenu Direct3D et GDI dans lequel DWM est activé et l’application est en mode fenêtre](images/d3d-gdinotext-same-hwnd.png)

<span data-ttu-id="c9022-195">Par conséquent, le modèle de retournement doit être activé pour les surfaces de tampon de chaîne de permutation où le modèle de basculement Direct3D 9Ex est rendu seul au HWND entier.</span><span class="sxs-lookup"><span data-stu-id="c9022-195">Therefore, Flip Model should be enabled for swap chain buffers surfaces where the Direct3D 9Ex Flip Model alone renders to the entire HWND.</span></span>

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a><span data-ttu-id="c9022-196">N’utilisez pas Flip Model avec ScrollWindow ou ScrollWindowEx de GDI</span><span class="sxs-lookup"><span data-stu-id="c9022-196">Do Not Use Flip Model with GDI's ScrollWindow or ScrollWindowEx</span></span>

<span data-ttu-id="c9022-197">Certaines applications Direct3D 9Ex utilisent les fonctions ScrollWindow ou ScrollWindowEx de GDI pour mettre à jour le contenu de la fenêtre lorsqu’un événement de défilement utilisateur est déclenché.</span><span class="sxs-lookup"><span data-stu-id="c9022-197">Some Direct3D 9Ex applications use GDI's ScrollWindow or ScrollWindowEx functions to update window contents when a user scroll event is triggered.</span></span> <span data-ttu-id="c9022-198">ScrollWindow et ScrollWindowEx effectuent la blts du contenu des fenêtres à l’écran lors du défilement d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c9022-198">ScrollWindow and ScrollWindowEx perform blts of window contents on screen as a window is scrolled.</span></span> <span data-ttu-id="c9022-199">Ces fonctions nécessitent également des mises à jour du modèle BLT pour le contenu GDI et Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c9022-199">These functions also require Blt Model updates for GDI and Direct3D 9Ex content.</span></span> <span data-ttu-id="c9022-200">Les applications qui utilisent l’une ou l’autre des fonctions n’affichent pas nécessairement l’affichage du contenu de la fenêtre visible à l’écran quand l’application est en mode fenêtre et que DWM est activé.</span><span class="sxs-lookup"><span data-stu-id="c9022-200">Applications that use either function will not necessarily display visible window contents scrolling on screen when the application is in windowed mode and DWM is enabled.</span></span> <span data-ttu-id="c9022-201">Nous vous recommandons de ne pas utiliser les API ScrollWindow et ScrollWindowEx de GDI dans vos applications, et de redessiner à la place leur contenu à l’écran en réponse au défilement.</span><span class="sxs-lookup"><span data-stu-id="c9022-201">We recommend that you not use GDI's ScrollWindow and ScrollWindowEx APIs in your applications, and instead redraw their contents on screen in response to scrolling.</span></span>

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a><span data-ttu-id="c9022-202">Utiliser une \_ chaîne de permutation D3DSWAPEFFECT FLIPEX par HWND</span><span class="sxs-lookup"><span data-stu-id="c9022-202">Use One D3DSWAPEFFECT\_FLIPEX Swap Chain per HWND</span></span>

<span data-ttu-id="c9022-203">Les applications qui utilisent Flip Model ne doivent pas utiliser plusieurs chaînes de permutation de modèle ciblant le même HWND.</span><span class="sxs-lookup"><span data-stu-id="c9022-203">Applications that use Flip Model should not use multiple Flip Model swap chains targeting the same HWND.</span></span>

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="c9022-204">Synchronisation des frames des applications Direct3D 9Ex Flip Model</span><span class="sxs-lookup"><span data-stu-id="c9022-204">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="c9022-205">Les statistiques présentent les informations de minutage des frames utilisées par les applications multimédias pour synchroniser les flux vidéo et audio et récupérer des défauts de lecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="c9022-205">Present statistics are frame timing information that media applications use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="c9022-206">Pour activer la disponibilité des statistiques, l’application Direct3D 9Ex doit s’assurer que le paramètre *BehaviorFlags* transmis par l’application à [**IDirect3D9Ex :: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contient l’indicateur de comportement de l’appareil [D3DCREATE \_ Enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).</span><span class="sxs-lookup"><span data-stu-id="c9022-206">To enable present statistics availability, the Direct3D 9Ex application must ensure that the *BehaviorFlags* parameter that the application passes to [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contains the device behavior flag [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).</span></span>

<span data-ttu-id="c9022-207">Pour plus de commodité, la syntaxe de [**IDirect3D9Ex :: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) est répétée ici.</span><span class="sxs-lookup"><span data-stu-id="c9022-207">For convenience, the syntax of [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

<span data-ttu-id="c9022-208">Le modèle de basculement Direct3D 9Ex ajoute l’indicateur de présentation [D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) qui applique le comportement de l’indicateur de présentation [ \_ \_ immédiate intervalle D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) .</span><span class="sxs-lookup"><span data-stu-id="c9022-208">Direct3D 9Ex Flip Model adds the [D3DPRESENT\_FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation flag that enforces the [D3DPRESENT\_INTERVAL\_IMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation-flag behavior.</span></span> <span data-ttu-id="c9022-209">L’application Direct3D 9Ex spécifie ces indicateurs de présentation dans le paramètre *dwFlags* que l’application transmet à [**IDirect3DDevice9Ex ::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), comme illustré ici.</span><span class="sxs-lookup"><span data-stu-id="c9022-209">The Direct3D 9Ex application specifies these presentation flags in the *dwFlags* parameter that the application passes to [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), as shown here.</span></span>

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

<span data-ttu-id="c9022-210">Lorsque vous modifiez votre application Direct3D 9Ex pour Windows 7, vous devez tenir compte des informations suivantes sur les indicateurs de présentation [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) spécifiés :</span><span class="sxs-lookup"><span data-stu-id="c9022-210">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the specified [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) presentation flags:</span></span>

<dl> <dt>

[<span data-ttu-id="c9022-211">D3DPRESENT \_ DONOTFLIP</span><span class="sxs-lookup"><span data-stu-id="c9022-211">D3DPRESENT\_DONOTFLIP</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="c9022-212">Cet indicateur est disponible uniquement en mode plein écran ou</span><span class="sxs-lookup"><span data-stu-id="c9022-212">This flag is available only in full-screen mode or</span></span>

<span data-ttu-id="c9022-213">(Windows 7 uniquement)</span><span class="sxs-lookup"><span data-stu-id="c9022-213">(Windows 7 Only)</span></span>

<span data-ttu-id="c9022-214">Lorsque l’application définit le membre **SwapEffect** des [**\_ paramètres D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) sur [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) dans un appel à [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="c9022-214">when the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

[<span data-ttu-id="c9022-215">D3DPRESENT \_ FORCEIMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="c9022-215">D3DPRESENT\_FORCEIMMEDIATE</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="c9022-216">(Windows 7 uniquement)</span><span class="sxs-lookup"><span data-stu-id="c9022-216">(Windows 7 Only)</span></span>

<span data-ttu-id="c9022-217">Cet indicateur peut être spécifié uniquement si l’application définit le membre **SwapEffect** des [**\_ paramètres D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) sur [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) dans un appel à [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="c9022-217">This flag can be specified only if the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span> <span data-ttu-id="c9022-218">L’application peut utiliser cet indicateur pour mettre immédiatement à jour une surface avec plusieurs frames plus loin dans la file d’attente de DWM présente, en ignorant essentiellement les frames intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="c9022-218">The application can use this flag to immediately update a surface with several frames later in the DWM Present queue, essentially skipping intermediate frames.</span></span>

<span data-ttu-id="c9022-219">Les applications FlipEx avec fenêtres peuvent utiliser cet indicateur pour mettre immédiatement à jour une surface avec un frame qui est plus tard dans la file d’attente présente dans le DWM, en ignorant les frames intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="c9022-219">Windowed FlipEx-enabled applications can use this flag to immediately update a surface with a frame that is later in the DWM Present queue, skipping intermediate frames.</span></span> <span data-ttu-id="c9022-220">Cela s’avère particulièrement utile pour les applications multimédias qui souhaitent ignorer les trames qui ont été détectées en retard et présentent les trames suivantes au moment de la composition.</span><span class="sxs-lookup"><span data-stu-id="c9022-220">This is especially useful for media applications that want to discard frames that have been detected as late and present subsequent frames at composition time.</span></span> <span data-ttu-id="c9022-221">[**IDirect3DDevice9Ex ::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) retourne une erreur de paramètre non valide si cet indicateur n’est pas correctement spécifié.</span><span class="sxs-lookup"><span data-stu-id="c9022-221">[**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) returns invalid parameter error if this flag is improperly specified.</span></span>

</dd> </dl>

<span data-ttu-id="c9022-222">Pour obtenir les informations de statistiques actuelles, l’application obtient la structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) en appelant l’API [**IDirect3DSwapChain9Ex :: GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c9022-222">To obtain present statistics information, the application obtains the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure by calling the [**IDirect3DSwapChain9Ex::GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) API.</span></span>

<span data-ttu-id="c9022-223">La structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) contient des statistiques sur [**IDirect3DDevice9Ex ::P**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) les appels resentex.</span><span class="sxs-lookup"><span data-stu-id="c9022-223">The [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure contains statistics about [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span> <span data-ttu-id="c9022-224">L’appareil doit être créé à l’aide d’un appel de [**IDirect3D9Ex :: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) avec l’indicateur [D3DCREATE \_ Enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) .</span><span class="sxs-lookup"><span data-stu-id="c9022-224">The device must be created by using a [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) call with the [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) flag.</span></span> <span data-ttu-id="c9022-225">Sinon, les données retournées par [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="c9022-225">Otherwise, the data returned by [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is undefined.</span></span> <span data-ttu-id="c9022-226">Une chaîne de permutation Direct3D 9Ex avec basculement de modèle fournit les informations de statistiques en mode fenêtre et en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="c9022-226">A Flip-Model-enabled Direct3D 9Ex swap chain provides present statistics information in both windowed and full-screen modes.</span></span>

<span data-ttu-id="c9022-227">Pour les chaînes de permutation Direct3D 9Ex compatibles avec le modèle BLT en mode fenêtre, toutes les valeurs de la structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) sont des zéros.</span><span class="sxs-lookup"><span data-stu-id="c9022-227">For Blt-Model-enabled Direct3D 9Ex swap chains in windowed mode, all [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure values will be zeroes.</span></span>

<span data-ttu-id="c9022-228">Pour FlipEx présente les statistiques, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) retourne \_ D3DERR \_ présente \_ des statistiques disjointes dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9022-228">For FlipEx present statistics, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) returns D3DERR\_PRESENT\_STATISTICS\_DISJOINT in the following situations:</span></span>

-   <span data-ttu-id="c9022-229">Premier appel à [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) jamais, qui indique le début d’une séquence</span><span class="sxs-lookup"><span data-stu-id="c9022-229">First call to [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ever, which indicates the beginning of a sequence</span></span>
-   <span data-ttu-id="c9022-230">Conversion DWM de on à OFF</span><span class="sxs-lookup"><span data-stu-id="c9022-230">DWM transition from on to off</span></span>
-   <span data-ttu-id="c9022-231">Changement de mode : mode avec fenêtre, en mode plein écran ou plein écran pour les transitions en plein écran</span><span class="sxs-lookup"><span data-stu-id="c9022-231">Mode change: either windowed mode to or from full screen or full screen to full screen transitions</span></span>

<span data-ttu-id="c9022-232">Pour plus de commodité, la syntaxe de [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) est répétée ici.</span><span class="sxs-lookup"><span data-stu-id="c9022-232">For convenience, the syntax of [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is repeated here.</span></span>

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

<span data-ttu-id="c9022-233">La méthode [**IDirect3DSwapChain9Ex :: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) retourne le dernier PresentCount, autrement dit, l’ID actuel du dernier appel présent réussi qui a été effectué par un périphérique d’affichage associé à la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="c9022-233">The [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) method returns the last PresentCount, that is, the Present ID of the last successful Present call that was made by a display device that is associated with the swap chain.</span></span> <span data-ttu-id="c9022-234">Cet ID est la valeur du membre **PresentCount** de la structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) .</span><span class="sxs-lookup"><span data-stu-id="c9022-234">This Present ID is the value of the **PresentCount** member of the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure.</span></span> <span data-ttu-id="c9022-235">Pour les chaînes de permutation Direct3D 9Ex compatibles avec le modèle BLT, en mode fenêtre, toutes les valeurs de la structure **D3DPRESENTSTATS** sont des zéros.</span><span class="sxs-lookup"><span data-stu-id="c9022-235">For Blt-Model-enabled Direct3D 9Ex swap chains, while in windowed mode, all **D3DPRESENTSTATS** structure values will be zeroes.</span></span>

<span data-ttu-id="c9022-236">Pour plus de commodité, la syntaxe de [**IDirect3DSwapChain9Ex :: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) est répétée ici.</span><span class="sxs-lookup"><span data-stu-id="c9022-236">For convenience, the syntax of [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) is repeated here.</span></span>

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

<span data-ttu-id="c9022-237">Lorsque vous modifiez votre application Direct3D 9Ex pour Windows 7, vous devez prendre en compte les informations suivantes sur la structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) :</span><span class="sxs-lookup"><span data-stu-id="c9022-237">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure:</span></span>

-   <span data-ttu-id="c9022-238">La valeur PresentCount renvoyée par [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) n’est pas mise à jour lorsqu’un appel [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) avec D3DPRESENT \_ DONOTWAIT spécifié dans le paramètre *dwFlags* retourne un échec.</span><span class="sxs-lookup"><span data-stu-id="c9022-238">The PresentCount value that [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) returns does not update when a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) call with D3DPRESENT\_DONOTWAIT specified in the *dwFlags* parameter returns failure.</span></span>
-   <span data-ttu-id="c9022-239">Quand [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) est appelé avec D3DPRESENT \_ DONOTFLIP, un appel [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) se déroule correctement, mais ne retourne pas de structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) mise à jour lorsque l’application est en mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c9022-239">When [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) is called with D3DPRESENT\_DONOTFLIP, a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>
-   <span data-ttu-id="c9022-240">**PresentRefreshCount** et **SyncRefreshCount** dans [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):</span><span class="sxs-lookup"><span data-stu-id="c9022-240">**PresentRefreshCount** versus **SyncRefreshCount** in [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):</span></span>
    -   <span data-ttu-id="c9022-241">**PresentRefreshCount** est égal à **SyncRefreshCount** lorsque l’application s’affiche sur chaque Vsync.</span><span class="sxs-lookup"><span data-stu-id="c9022-241">**PresentRefreshCount** is equal to **SyncRefreshCount** when the application presents on every vsync.</span></span>
    -   <span data-ttu-id="c9022-242">**SyncRefreshCount** est obtenu à l’intervalle Vsync lorsque le présent a été envoyé, **SyncQPCTime** est approximativement l’heure associée à l’intervalle de Vsync.</span><span class="sxs-lookup"><span data-stu-id="c9022-242">**SyncRefreshCount** is obtained on the vsync interval when the present was submitted, **SyncQPCTime** is approximately the time associated with the vsync interval.</span></span>

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a><span data-ttu-id="c9022-243">Synchronisation des frames pour les applications Windows lorsque DWM est désactivé</span><span class="sxs-lookup"><span data-stu-id="c9022-243">Frame Synchronization for Windowed Applications When DWM is Off</span></span>

<span data-ttu-id="c9022-244">Lorsque DWM est désactivé, les applications en fenêtre s’affichent directement sur l’écran du moniteur sans passer par une chaîne de basculement.</span><span class="sxs-lookup"><span data-stu-id="c9022-244">When DWM is off, windowed applications display directly to the monitor screen without going through a flip chain.</span></span> <span data-ttu-id="c9022-245">Dans Windows Vista, il n’existe pas de prise en charge pour l’obtention d’informations de statistiques de frame pour les applications avec fenêtres lorsque DWM est désactivé.</span><span class="sxs-lookup"><span data-stu-id="c9022-245">In Windows Vista, there is no support for obtaining frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="c9022-246">Pour gérer une API dans laquelle les applications n’ont pas besoin de prendre en charge le DWM, Windows 7 retourne des statistiques de frames pour les applications avec fenêtres lorsque DWM est désactivé.</span><span class="sxs-lookup"><span data-stu-id="c9022-246">To maintain an API where applications need not be DWM- aware, Windows 7 will return frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="c9022-247">Les statistiques de frame retournées lorsque DWM est désactivé sont des estimations uniquement.</span><span class="sxs-lookup"><span data-stu-id="c9022-247">The frame statistics returned when DWM is off are estimations only.</span></span>

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a><span data-ttu-id="c9022-248">Walk-Through d’un modèle de basculement et de présentation des statistiques Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="c9022-248">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>

<span data-ttu-id="c9022-249">**Pour choisir FlipEx Presentation pour Direct3D 9Ex, exemple**</span><span class="sxs-lookup"><span data-stu-id="c9022-249">**To opt into FlipEx presentation for Direct3D 9Ex sample**</span></span>

1.  <span data-ttu-id="c9022-250">Vérifiez que l’exemple d’application s’exécute sur la version du système d’exploitation Windows 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c9022-250">Ensure the sample application is running on Windows 7 or later operating system version.</span></span>
2.  <span data-ttu-id="c9022-251">Définissez le membre **SwapEffect** des [**\_ paramètres D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) sur [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) dans un appel à [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="c9022-251">Set the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



<span data-ttu-id="c9022-252">**Pour s’abonner également aux statistiques de présentation de FlipEx associées à Direct3D 9Ex, exemple**</span><span class="sxs-lookup"><span data-stu-id="c9022-252">**To also opt into FlipEx associated Present Statistics for Direct3D 9Ex sample**</span></span>

-   <span data-ttu-id="c9022-253">Définissez [D3DCREATE \_ Enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) dans le paramètre *BehaviorFlags* de [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="c9022-253">Set [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) in the *BehaviorFlags* parameter of [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



<span data-ttu-id="c9022-254">**Pour éviter, détecter et récupérer des problèmes**</span><span class="sxs-lookup"><span data-stu-id="c9022-254">**To avoid, detect and recover from glitches**</span></span>

1.  <span data-ttu-id="c9022-255">Appels présents dans la file d’attente : le nombre de tampons en mémoire recommandée est compris entre 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="c9022-255">Queue Present calls: recommended backbuffer count is from 2 to 4.</span></span>
2.  <span data-ttu-id="c9022-256">L’exemple Direct3D 9Ex ajoute une mémoire tampon de base implicite, la longueur réelle de la file d’attente est le nombre de tampons de la mémoire \ + 1.</span><span class="sxs-lookup"><span data-stu-id="c9022-256">Direct3D 9Ex sample adds an implicit backbuffer, actual Present queue length is backbuffer count + 1.</span></span>
3.  <span data-ttu-id="c9022-257">Créer une structure d’application d’assistance présente la structure de file d’attente pour stocker tous les ID présents de présent de la présente (PresentCount) et les PresentRefreshCount associés, calculés/attendus.</span><span class="sxs-lookup"><span data-stu-id="c9022-257">Create helper Present queue structure to store all successfully submitted Present's Present ID (PresentCount) and associated, calculated/expected PresentRefreshCount.</span></span>
4.  <span data-ttu-id="c9022-258">Pour détecter une occurrence de problème :</span><span class="sxs-lookup"><span data-stu-id="c9022-258">To detect glitch occurrence:</span></span>

    -   <span data-ttu-id="c9022-259">Appelez [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c9022-259">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).</span></span>
    -   <span data-ttu-id="c9022-260">Obtenez l’ID actuel (PresentCount) et le nombre de Vsync où le frame est affiché (PresentRefreshCount) du frame dont les statistiques actuelles sont obtenues.</span><span class="sxs-lookup"><span data-stu-id="c9022-260">Get the Present ID (PresentCount) and vsync count where the frame is shown (PresentRefreshCount) of the frame whose present statistics is obtained.</span></span>
    -   <span data-ttu-id="c9022-261">Récupérez le PresentRefreshCount attendu (TargetRefresh dans l’exemple de code) associé à l’ID présent.</span><span class="sxs-lookup"><span data-stu-id="c9022-261">Retrieve the expected PresentRefreshCount (TargetRefresh in sample code) associated with the Present ID.</span></span>
    -   <span data-ttu-id="c9022-262">Si le PresentRefreshCount réel est plus tard que prévu, un problème s’est produit.</span><span class="sxs-lookup"><span data-stu-id="c9022-262">If actual PresentRefreshCount is later than expected, a glitch has occurred.</span></span>

5.  <span data-ttu-id="c9022-263">Pour effectuer une récupération suite à un problème :</span><span class="sxs-lookup"><span data-stu-id="c9022-263">To recover from glitch:</span></span>

    -   <span data-ttu-id="c9022-264">Calculez le nombre de frames à ignorer ( \_ variable g iImmediates dans l’exemple de code).</span><span class="sxs-lookup"><span data-stu-id="c9022-264">Calculate how many frames to skip (g\_ iImmediates variable in sample code).</span></span>
    -   <span data-ttu-id="c9022-265">Présentez les frames ignorés avec l’intervalle D3DPRESENT \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="c9022-265">Present the skipped frames with interval D3DPRESENT\_FORCEIMMEDIATE.</span></span>

<span data-ttu-id="c9022-266">**Considérations relatives à la détection et à la récupération des problèmes**</span><span class="sxs-lookup"><span data-stu-id="c9022-266">**Considerations for glitch detection and recovery**</span></span>

1.  <span data-ttu-id="c9022-267">La récupération de problème prend la variable N (g \_ iQueueDelay dans l’exemple de code) nombre d’appels présents où N (g \_ iQueueDelay) est égal à g \_ iImmediates plus la longueur de la file d’attente actuelle, c’est-à-dire :</span><span class="sxs-lookup"><span data-stu-id="c9022-267">Glitch recovery takes N (g\_iQueueDelay variable in sample code) number of Present calls where N (g\_iQueueDelay) equals g\_iImmediates plus length of the Present queue, that is:</span></span>

    -   <span data-ttu-id="c9022-268">Frames ignorés avec l’intervalle présent D3DPRESENT \_ FORCEIMMEDIATE, plus</span><span class="sxs-lookup"><span data-stu-id="c9022-268">Skipping frames with Present interval D3DPRESENT\_FORCEIMMEDIATE, plus</span></span>
    -   <span data-ttu-id="c9022-269">Mises en file d’attente qui doivent être traitées</span><span class="sxs-lookup"><span data-stu-id="c9022-269">Queued Presents that need to be processed</span></span>

2.  <span data-ttu-id="c9022-270">Définissez une limite sur la longueur du problème ( \_ \_ limite de récupération des problèmes dans l’exemple).</span><span class="sxs-lookup"><span data-stu-id="c9022-270">Set a limit to the glitch length (GLITCH\_RECOVERY\_LIMIT in sample).</span></span> <span data-ttu-id="c9022-271">Si l’exemple d’application ne peut pas récupérer à partir d’un problème trop long (par exemple, 1 seconde, ou 60 vsyncs sur 60 Hz), passez l’animation intermittente et réinitialisez la file d’attente d’assistance actuelle.</span><span class="sxs-lookup"><span data-stu-id="c9022-271">If the sample application cannot recover from a glitch that is too long (that is say, 1 second, or 60 vsyncs on 60Hz monitor), jump over the intermittent animation and reset the Present helper queue.</span></span>


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



<span data-ttu-id="c9022-272">**Exemple de scénario**</span><span class="sxs-lookup"><span data-stu-id="c9022-272">**Sample scenario**</span></span>

-   <span data-ttu-id="c9022-273">L’illustration suivante montre une application avec un nombre de tampons de mémoire tampon de 4.</span><span class="sxs-lookup"><span data-stu-id="c9022-273">The following illustration shows an application with backbuffer count of 4.</span></span> <span data-ttu-id="c9022-274">La longueur réelle de la file d’attente actuelle est donc 5.</span><span class="sxs-lookup"><span data-stu-id="c9022-274">The actual Present queue length is therefore 5.</span></span>

    ![illustration d’une mise en file d’attente d’appliances et de la file d’attente actuelle](images/sample-scenario.png)

    <span data-ttu-id="c9022-276">Le frame A est destiné à être affiché à l’écran sur le nombre d’intervalles de synchronisation de 1, mais a détecté qu’il a été affiché sur le nombre d’intervalles de synchronisation de 4.</span><span class="sxs-lookup"><span data-stu-id="c9022-276">Frame A is targeted to go on screen on sync interval count of 1 but was detected that it was shown on sync interval count of 4.</span></span> <span data-ttu-id="c9022-277">Par conséquent, un problème s’est produit.</span><span class="sxs-lookup"><span data-stu-id="c9022-277">Therefore a glitch has occurred.</span></span> <span data-ttu-id="c9022-278">Les 3 images suivantes sont présentées avec D3DPRESENT \_ Interval \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="c9022-278">Subsequent 3 frames are presented with D3DPRESENT\_INTERVAL\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="c9022-279">Le problème doit prendre un total de 8 appels présents avant de pouvoir être récupéré : le frame suivant sera affiché en fonction du nombre d’intervalles de synchronisation ciblés.</span><span class="sxs-lookup"><span data-stu-id="c9022-279">The glitch should take a total of 8 Present calls before it is recovered - the next frame will be shown as per its targeted sync interval count.</span></span>

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a><span data-ttu-id="c9022-280">Résumé des recommandations de programmation pour la synchronisation de frames</span><span class="sxs-lookup"><span data-stu-id="c9022-280">Summary of Programming Recommendations for Frame Synchronization</span></span>

-   <span data-ttu-id="c9022-281">Créez une liste de sauvegarde de tous les ID LastPresentCount (obtenus via [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) et des PresentRefreshCount estimés associés de tous les cadeaux soumis.</span><span class="sxs-lookup"><span data-stu-id="c9022-281">Create a backup list of all the LastPresentCount IDs (obtained via [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) and associated estimated PresentRefreshCount of all the Presents submitted.</span></span>
    > [!Note]  
    > <span data-ttu-id="c9022-282">Lorsque l’application appelle [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) avec D3DPRESENT \_ DONOTFLIP, l’appel [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) a échoué mais ne retourne pas de structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) mise à jour lorsque l’application est en mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c9022-282">When the application calls [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) with D3DPRESENT\_DONOTFLIP, the [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>

     

-   <span data-ttu-id="c9022-283">Appelez [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) pour obtenir le PresentRefreshCount réel associé à chaque ID actuel des frames affichés, pour vous assurer que l’application gère les retours d’échec de l’appel.</span><span class="sxs-lookup"><span data-stu-id="c9022-283">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) to obtain the actual PresentRefreshCount associated with each Present ID of frames shown, to make sure that the application handles failure returns from the call.</span></span>
-   <span data-ttu-id="c9022-284">Si le PresentRefreshCount réel est postérieur au PresentRefreshCount estimé, un problème est détecté.</span><span class="sxs-lookup"><span data-stu-id="c9022-284">If actual PresentRefreshCount is later than estimated PresentRefreshCount, a glitch is detected.</span></span> <span data-ttu-id="c9022-285">Compenser en envoyant des frames de retard» présent avec D3DPRESENT \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="c9022-285">Compensate by submitting lagging frames' Present with D3DPRESENT\_FORCEIMMEDIATE.</span></span>
-   <span data-ttu-id="c9022-286">Quand un frame est présenté en retard dans la file d’attente actuelle, tous les frames mis en file d’attente suivants sont présentés en retard.</span><span class="sxs-lookup"><span data-stu-id="c9022-286">When one frame is presented late in the Present queue, all subsequent queued frames will be presented late.</span></span> <span data-ttu-id="c9022-287">D3DPRESENT \_ FORCEIMMEDIATE corrigera uniquement le frame suivant qui sera présenté après tous les frames mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c9022-287">D3DPRESENT\_FORCEIMMEDIATE will correct only the next frame to be presented after all the queued frames.</span></span> <span data-ttu-id="c9022-288">Par conséquent, le nombre de files d’attente ou de mises en mémoire tampon actuelles ne doit pas être trop long. il y a donc moins de problèmes de trames à intercepter.</span><span class="sxs-lookup"><span data-stu-id="c9022-288">Therefore, the Present queue or backbuffer count should not be too long -- so there are less frame glitches to catch up with.</span></span> <span data-ttu-id="c9022-289">Le nombre optimal de mémoires tampons est de 2 à 4.</span><span class="sxs-lookup"><span data-stu-id="c9022-289">The optimal backbuffer count is 2 to 4.</span></span>
-   <span data-ttu-id="c9022-290">Si le PresentRefreshCount estimé est postérieur au PresentRefreshCount réel, la limitation DWM peut s’être produite.</span><span class="sxs-lookup"><span data-stu-id="c9022-290">If estimated PresentRefreshCount is later than the actual PresentRefreshCount, DWM throttling might have occurred.</span></span> <span data-ttu-id="c9022-291">Les solutions suivantes sont possibles :</span><span class="sxs-lookup"><span data-stu-id="c9022-291">The following solutions are possible:</span></span>

    -   <span data-ttu-id="c9022-292">réduction de la longueur actuelle de la file d’attente</span><span class="sxs-lookup"><span data-stu-id="c9022-292">reducing Present queue length</span></span>
    -   <span data-ttu-id="c9022-293">réduction des besoins en mémoire du GPU avec d’autres moyens, en plus de réduire la longueur de la file d’attente actuelle (autrement dit, la réduction de la qualité, la suppression des effets, etc.)</span><span class="sxs-lookup"><span data-stu-id="c9022-293">reducing GPU memory requirements with any other means besides reducing Present Queue length (that is, decreasing quality, removing effects, and so on)</span></span>
    -   <span data-ttu-id="c9022-294">spécification de [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) pour empêcher la limitation DWM en général</span><span class="sxs-lookup"><span data-stu-id="c9022-294">specifying [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) to prevent DWM throttling in general</span></span>

-   <span data-ttu-id="c9022-295">Vérifiez la fonctionnalité d’affichage de l’application et les performances des statistiques de frame dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="c9022-295">Verify application display functionality and frame statistics performance in the following scenarios:</span></span>

    -   <span data-ttu-id="c9022-296">avec DWM activé et désactivé</span><span class="sxs-lookup"><span data-stu-id="c9022-296">with DWM on and off</span></span>
    -   <span data-ttu-id="c9022-297">modes exclusif et avec fenêtre plein écran</span><span class="sxs-lookup"><span data-stu-id="c9022-297">fullscreen exclusive and windowed modes</span></span>
    -   <span data-ttu-id="c9022-298">matériel de capacité inférieure</span><span class="sxs-lookup"><span data-stu-id="c9022-298">lower capability hardware</span></span>

-   <span data-ttu-id="c9022-299">Lorsque les applications ne peuvent pas récupérer à partir d’un grand nombre de trames avec D3DPRESENT \_ FORCEIMMEDIATE présentes, elles peuvent potentiellement effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9022-299">When applications cannot recover from large numbers of glitched frames with D3DPRESENT\_FORCEIMMEDIATE Present, they can potentially perform the following operations:</span></span>

    -   <span data-ttu-id="c9022-300">Réduisez l’utilisation du processeur et du GPU en rendant moins de charge de travail.</span><span class="sxs-lookup"><span data-stu-id="c9022-300">reduce CPU and GPU usage by rendering with less workload.</span></span>
    -   <span data-ttu-id="c9022-301">en cas de décodage vidéo, décodez plus rapidement en réduisant la qualité et, par conséquent, l’utilisation du processeur et du GPU.</span><span class="sxs-lookup"><span data-stu-id="c9022-301">in the case of video decode, decode faster by reducing quality and, therefore, CPU and GPU usage.</span></span>

## <a name="conclusion-about-direct3d-9ex-improvements"></a><span data-ttu-id="c9022-302">Conclusion sur les améliorations Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="c9022-302">Conclusion about Direct3D 9Ex Improvements</span></span>

<span data-ttu-id="c9022-303">Sur Windows 7, les applications qui affichent la fréquence d’images vidéo ou de jauge pendant la présentation peuvent choisir de retourner le modèle.</span><span class="sxs-lookup"><span data-stu-id="c9022-303">On Windows 7, applications that display video or gauge frame rate during presentation can opt into Flip Model.</span></span> <span data-ttu-id="c9022-304">Les améliorations actuelles des statistiques associées à la fonction Flip Model Direct3D 9Ex peuvent tirer parti des applications qui synchronisent la présentation par fréquence d’images, avec des commentaires en temps réel sur la détection et la récupération des problèmes.</span><span class="sxs-lookup"><span data-stu-id="c9022-304">The present statistics improvements that are associated with Flip Model Direct3D 9Ex can benefit applications that synchronize presentation per frame rate, with real time feedback for glitch detection and recovery.</span></span> <span data-ttu-id="c9022-305">Les développeurs qui adoptent le modèle de basculement Direct3D 9Ex doivent prendre en compte un HWND distinct du contenu GDI et de la synchronisation de la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="c9022-305">Developers that adopt the Direct3D 9Ex Flip Model should take targeting a separate HWND from GDI content and frame rate synchronization into account.</span></span> <span data-ttu-id="c9022-306">Reportez-vous aux détails de cette rubrique et à la documentation MSDN.</span><span class="sxs-lookup"><span data-stu-id="c9022-306">Refer to details in this topic, and MSDN documentation.</span></span> <span data-ttu-id="c9022-307">Pour obtenir une documentation supplémentaire, consultez [le centre de développement DirectX sur MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="c9022-307">For additional documentation, see [DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).</span></span>

## <a name="call-to-action"></a><span data-ttu-id="c9022-308">À vous d’agir !</span><span class="sxs-lookup"><span data-stu-id="c9022-308">Call to Action</span></span>

<span data-ttu-id="c9022-309">Nous vous encourageons à utiliser le modèle de basculement Direct3D 9Ex et ses statistiques sur Windows 7 lorsque vous créez des applications qui tentent de synchroniser la fréquence des images de présentation ou de récupérer à partir de défauts d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c9022-309">We encourage you to use Direct3D 9Ex Flip Model and its present statistics on Windows 7 when you create applications that attempt to synchronize presentation frame rate or recover from display glitches.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9022-310">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9022-310">Related topics</span></span>

<span data-ttu-id="c9022-311">[Centre de développement DirectX sur MSDN](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="c9022-311">[DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> </dl>