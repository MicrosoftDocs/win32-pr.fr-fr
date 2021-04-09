---
description: Gestion de la qualité vidéo
ms.assetid: 3617adf2-ed7b-4788-abce-58bc22a14511
title: Gestion de la qualité vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233ccd54cfcb98742abef9a91241e903c07ba549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951473"
---
# <a name="video-quality-management"></a><span data-ttu-id="5c57d-103">Gestion de la qualité vidéo</span><span class="sxs-lookup"><span data-stu-id="5c57d-103">Video Quality Management</span></span>

<span data-ttu-id="5c57d-104">Cette rubrique décrit certaines améliorations apportées au pipeline vidéo dans Windows 7, pour Microsoft Media Foundation et Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5c57d-104">This topic describes some improvements to the video pipeline in Windows 7, both for Microsoft Media Foundation and Microsoft DirectShow.</span></span>

<span data-ttu-id="5c57d-105">Dans un monde parfait, la vidéo ne se détournerait jamais, quelle que soit la résolution vidéo ou la charge de l’UC/GPU.</span><span class="sxs-lookup"><span data-stu-id="5c57d-105">In a perfect world, video would never glitch, regardless of the video resolution or the CPU/GPU load.</span></span> <span data-ttu-id="5c57d-106">En réalité, bien entendu, le pipeline vidéo doit être capable de faire face aux ressources matérielles limitées et il doit pouvoir adapter la lecture à l’environnement système de manière adaptative.</span><span class="sxs-lookup"><span data-stu-id="5c57d-106">In reality, of course, the video pipeline must be able to cope with finite hardware resources, and it must adaptively tailor playback to the system environment.</span></span> <span data-ttu-id="5c57d-107">Les objectifs de la gestion de la qualité vidéo sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="5c57d-107">The goals for video quality management are to:</span></span>

-   <span data-ttu-id="5c57d-108">Réduire les problèmes (images abandonnées ou tardives).</span><span class="sxs-lookup"><span data-stu-id="5c57d-108">Reduce glitching (dropped or late frames).</span></span>
-   <span data-ttu-id="5c57d-109">Réduisez l’utilisation de la mémoire, en particulier dans le GPU.</span><span class="sxs-lookup"><span data-stu-id="5c57d-109">Reduce memory usage, especially in the GPU.</span></span>
-   <span data-ttu-id="5c57d-110">Réduisez la consommation d’énergie, en particulier sur les ordinateurs portables fonctionnant sur batterie.</span><span class="sxs-lookup"><span data-stu-id="5c57d-110">Reduce power consumption, especially in laptops running on battery power.</span></span>
-   <span data-ttu-id="5c57d-111">Obtenir la meilleure qualité d’image possible, en fonction des contraintes de ressources.</span><span class="sxs-lookup"><span data-stu-id="5c57d-111">Get the best image quality possible, given resource constraints.</span></span>
-   <span data-ttu-id="5c57d-112">Conservez la vidéo synchronisée avec l’audio.</span><span class="sxs-lookup"><span data-stu-id="5c57d-112">Keep video synchronized with audio.</span></span>

<span data-ttu-id="5c57d-113">Certains de ces objectifs sont contraires, en particulier sur les systèmes bas de gamme.</span><span class="sxs-lookup"><span data-stu-id="5c57d-113">Some of these goals are contrary, particularly on low-end systems.</span></span> <span data-ttu-id="5c57d-114">En général, il existe un compromis entre la vitesse et la qualité.</span><span class="sxs-lookup"><span data-stu-id="5c57d-114">Generally there is a trade-off between speed and quality.</span></span> <span data-ttu-id="5c57d-115">Le problème est plus répréhensible que la réduction modérée de la qualité visuelle.</span><span class="sxs-lookup"><span data-stu-id="5c57d-115">Glitching is more objectionable than moderate reductions in visual quality.</span></span> <span data-ttu-id="5c57d-116">L’importance relative de la consommation d’énergie varie en fonction de l’environnement. sur un ordinateur portable fonctionnant sur batterie, il est très important.</span><span class="sxs-lookup"><span data-stu-id="5c57d-116">The relative importance of power consumption varies with the environment; in a laptop running on battery power, it is very important.</span></span>

<span data-ttu-id="5c57d-117">Dans Windows 7, le rendu vidéo amélioré (EVR) offre une meilleure prise en charge de la gestion de la qualité vidéo.</span><span class="sxs-lookup"><span data-stu-id="5c57d-117">In Windows 7, the enhanced video renderer (EVR) has better support for video quality management.</span></span> <span data-ttu-id="5c57d-118">Le pipeline Media Foundation et le pipeline DirectShow ont été mis à jour pour tirer parti de ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="5c57d-118">Both the Media Foundation pipeline and the DirectShow pipeline have been updated to take advantage of these capabilities.</span></span> <span data-ttu-id="5c57d-119">Une approche à deux branches est utilisée :</span><span class="sxs-lookup"><span data-stu-id="5c57d-119">A two-pronged approach is used:</span></span>

-   <span data-ttu-id="5c57d-120">Avant le démarrage de la lecture, le pipeline peut effectuer des optimisations statiques, en fonction des paramètres de gestion de l’alimentation de l’utilisateur et des informations sur le matériel.</span><span class="sxs-lookup"><span data-stu-id="5c57d-120">Before playback starts, the pipeline can perform static optimizations, based on the user's power management settings and information about the hardware.</span></span>
-   <span data-ttu-id="5c57d-121">Après le démarrage de la lecture, le pipeline peut appliquer des optimisations dynamiques, en fonction des performances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5c57d-121">After playback starts, the pipeline can apply dynamic optimizations, based on run-time performance.</span></span>

## <a name="quality-management-in-media-foundation"></a><span data-ttu-id="5c57d-122">Gestion de la qualité dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5c57d-122">Quality Management in Media Foundation</span></span>

<span data-ttu-id="5c57d-123">Pour activer les optimisations statiques, définissez l’attribut [ \_ \_ \_ \_ optimisations de la lecture statique de la topologie MF](mf-topology-static-playback-optimizations.md) sur la topologie partielle avant de résoudre la topologie.</span><span class="sxs-lookup"><span data-stu-id="5c57d-123">To enable static optimizations, set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute on the partial topology before resolving the topology.</span></span> <span data-ttu-id="5c57d-124">Le chargeur de topologie interroge cet attribut dans sa méthode [**IMFTopoLoader :: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .</span><span class="sxs-lookup"><span data-stu-id="5c57d-124">The topology loader queries this attribute in its [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="5c57d-125">Si vous activez les optimisations statiques, vous devez définir deux autres attributs sur la topologie :</span><span class="sxs-lookup"><span data-stu-id="5c57d-125">If you enable static optimizations, you should set two other attributes on the topology:</span></span>



| <span data-ttu-id="5c57d-126">Attribut</span><span class="sxs-lookup"><span data-stu-id="5c57d-126">Attribute</span></span>                                                                                                                                      | <span data-ttu-id="5c57d-127">Description</span><span class="sxs-lookup"><span data-stu-id="5c57d-127">Description</span></span>                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="5c57d-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>\_ \_ nombre maximal de lectures de la topologie \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="5c57d-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span><br/>   | <span data-ttu-id="5c57d-129">Spécifie la taille maximale de la fenêtre de lecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="5c57d-129">Specifies the maximum size of the video playback window.</span></span><br/> |
| <span data-ttu-id="5c57d-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>\_fréquence de lecture de \_ la topologie MF \_</span><span class="sxs-lookup"><span data-stu-id="5c57d-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span><br/> | <span data-ttu-id="5c57d-131">Spécifie la fréquence d’actualisation du moniteur.</span><span class="sxs-lookup"><span data-stu-id="5c57d-131">Specifies the monitor refresh rate.</span></span><br/>                      |



 

<span data-ttu-id="5c57d-132">Ces deux attributs aident le pipeline à calculer le paramètre le plus efficace pour la gestion de la qualité.</span><span class="sxs-lookup"><span data-stu-id="5c57d-132">These two attributes help the pipeline calculate the most effective setting for quality management.</span></span>

<span data-ttu-id="5c57d-133">Les optimisations dynamiques sont effectuées par le gestionnaire de qualité.</span><span class="sxs-lookup"><span data-stu-id="5c57d-133">Dynamic optimizations are performed by the quality manager.</span></span> <span data-ttu-id="5c57d-134">Vous n’avez rien à faire pour activer le gestionnaire de qualité ; elle est automatiquement activée.</span><span class="sxs-lookup"><span data-stu-id="5c57d-134">You do not need to do anything to enable the quality manager; it is automatically enabled.</span></span> <span data-ttu-id="5c57d-135">Le gestionnaire de qualité existait dans Windows Vista ; dans Windows 7, EVR peut répondre mieux aux messages du gestionnaire de qualité.</span><span class="sxs-lookup"><span data-stu-id="5c57d-135">The quality manager existed in Windows Vista; in Windows 7, the EVR can respond better to messages from the quality manager.</span></span>

## <a name="quality-management-in-directshow"></a><span data-ttu-id="5c57d-136">Gestion de la qualité dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="5c57d-136">Quality Management in DirectShow</span></span>

<span data-ttu-id="5c57d-137">DirectShow prend en charge les optimisations statiques et dynamiques pour la lecture de DVD.</span><span class="sxs-lookup"><span data-stu-id="5c57d-137">DirectShow supports static and dynamic optimizations for DVD playback.</span></span> <span data-ttu-id="5c57d-138">Pour activer ces optimisations dans une application de lecture de DVD, définissez les indicateurs suivants dans le paramètre *dwFlags* de la méthode **IDvdGraphBuilder :: RenderDvdVideoVolume** :</span><span class="sxs-lookup"><span data-stu-id="5c57d-138">To enable these optimizations in a DVD playback application, set the following flags in the *dwFlags* parameter of the **IDvdGraphBuilder::RenderDvdVideoVolume** method:</span></span>



| <span data-ttu-id="5c57d-139">Indicateur</span><span class="sxs-lookup"><span data-stu-id="5c57d-139">Flag</span></span>                  | <span data-ttu-id="5c57d-140">Description</span><span class="sxs-lookup"><span data-stu-id="5c57d-140">Description</span></span>                    |
|-----------------------|--------------------------------|
| <span data-ttu-id="5c57d-141">\_graphique des \_ adaptateurs de DVD am \_</span><span class="sxs-lookup"><span data-stu-id="5c57d-141">AM\_DVD\_ADAPT\_GRAPH</span></span> | <span data-ttu-id="5c57d-142">Active les optimisations statiques.</span><span class="sxs-lookup"><span data-stu-id="5c57d-142">Enables static optimizations.</span></span>  |
| <span data-ttu-id="5c57d-143">AM \_ DVD \_ EVR \_ QoS</span><span class="sxs-lookup"><span data-stu-id="5c57d-143">AM\_DVD\_EVR\_QOS</span></span>     | <span data-ttu-id="5c57d-144">Active les optimisations dynamiques.</span><span class="sxs-lookup"><span data-stu-id="5c57d-144">Enables dynamic optimizations.</span></span> |



 

<span data-ttu-id="5c57d-145">D’autres applications DirectShow peuvent activer des optimisations dynamiques en appelant la méthode [**IEVRFilterConfigEx :: SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) directement sur le filtre EVR.</span><span class="sxs-lookup"><span data-stu-id="5c57d-145">Other DirectShow applications can enable dynamic optimizations by calling the [**IEVRFilterConfigEx::SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) method directly on the EVR filter.</span></span> <span data-ttu-id="5c57d-146">Spécifiez l’indicateur **EVRFilterConfigPrefs \_ EnableQoS** .</span><span class="sxs-lookup"><span data-stu-id="5c57d-146">Specify the **EVRFilterConfigPrefs\_EnableQoS** flag.</span></span>

> [!Note]  
> <span data-ttu-id="5c57d-147">Les optimisations statiques dans DirectShow sont limitées à la lecture des DVD.</span><span class="sxs-lookup"><span data-stu-id="5c57d-147">Static optimizations in DirectShow are limited to DVD playback.</span></span>

 

## <a name="quality-management-in-the-evr"></a><span data-ttu-id="5c57d-148">Gestion de la qualité dans le EVR</span><span class="sxs-lookup"><span data-stu-id="5c57d-148">Quality Management in the EVR</span></span>

<span data-ttu-id="5c57d-149">EVR prend en charge de nouveaux indicateurs de configuration pour la gestion de la qualité.</span><span class="sxs-lookup"><span data-stu-id="5c57d-149">The EVR supports some new configuration flags for quality management.</span></span> <span data-ttu-id="5c57d-150">Si vous activez les optimisations de gestion de la qualité décrites précédemment, vous n’êtes pas obligé de définir ces indicateurs directement.</span><span class="sxs-lookup"><span data-stu-id="5c57d-150">If you enable the quality management optimizations described previously, you do not have to set these flags directly.</span></span> <span data-ttu-id="5c57d-151">Toutefois, elles sont documentées pour les applications qui souhaitent un contrôle plus granulaire sur les EVR.</span><span class="sxs-lookup"><span data-stu-id="5c57d-151">However, they are documented for applications that want more granular control over the EVR.</span></span>

<span data-ttu-id="5c57d-152">Définissez les indicateurs suivants sur le mélangeur EVR en appelant la méthode [**IMFVideoMixerControl2 :: SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) :</span><span class="sxs-lookup"><span data-stu-id="5c57d-152">Set the following flags on the EVR mixer by calling the [**IMFVideoMixerControl2::SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c57d-153">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="5c57d-153">Flags</span></span></th>
<th><span data-ttu-id="5c57d-154">Description</span><span class="sxs-lookup"><span data-stu-id="5c57d-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="5c57d-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="5c57d-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span></span></li>
<li><span data-ttu-id="5c57d-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="5c57d-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="5c57d-157">Ignorez le deuxième champ de chaque trame entrelacée.</span><span class="sxs-lookup"><span data-stu-id="5c57d-157">Skip the second field of every interlaced frame.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="5c57d-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span><span class="sxs-lookup"><span data-stu-id="5c57d-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span></span></li>
<li><span data-ttu-id="5c57d-159"><strong>MFVideoMixPrefs_ForceBob</strong></span><span class="sxs-lookup"><span data-stu-id="5c57d-159"><strong>MFVideoMixPrefs_ForceBob</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="5c57d-160">Utilisez la désentrelacement Bob, même si le pilote prend en charge un mode de désentrelacement de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="5c57d-160">Use bob deinterlacing, even if the driver supports a higher-quality deinterlace mode.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5c57d-161">Définissez les indicateurs suivants sur le présentateur EVR en appelant la méthode [**IMFVideoDisplayControl :: SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) :</span><span class="sxs-lookup"><span data-stu-id="5c57d-161">Set the following flags on the EVR presenter by calling the [**IMFVideoDisplayControl::SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c57d-162">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="5c57d-162">Flags</span></span></th>
<th><span data-ttu-id="5c57d-163">Description</span><span class="sxs-lookup"><span data-stu-id="5c57d-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="5c57d-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="5c57d-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span></span></li>
<li><span data-ttu-id="5c57d-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="5c57d-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="5c57d-166">Limiter la sortie pour correspondre à la bande passante GPU.</span><span class="sxs-lookup"><span data-stu-id="5c57d-166">Throttle output to match GPU bandwidth.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="5c57d-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span><span class="sxs-lookup"><span data-stu-id="5c57d-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span></span></li>
<li><span data-ttu-id="5c57d-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span><span class="sxs-lookup"><span data-stu-id="5c57d-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="5c57d-169">Batch Direct3D présente des appels.</span><span class="sxs-lookup"><span data-stu-id="5c57d-169">Batch Direct3D Present calls.</span></span> <span data-ttu-id="5c57d-170">Cette optimisation permet au système d’entrer les États inactifs plus fréquemment, ce qui peut réduire la consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="5c57d-170">This optimization enables the system to enter into idle states more frequently, which can reduce power consumption.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="5c57d-171">MFVideoRenderPrefs_ForceScaling</span><span class="sxs-lookup"><span data-stu-id="5c57d-171">MFVideoRenderPrefs_ForceScaling</span></span></li>
<li><span data-ttu-id="5c57d-172">MFVideoRenderPrefs_AllowScaling</span><span class="sxs-lookup"><span data-stu-id="5c57d-172">MFVideoRenderPrefs_AllowScaling</span></span></li>
</ul></td>
<td><span data-ttu-id="5c57d-173">Effectue un mixage vidéo à l’aide d’un rectangle plus petit que le rectangle de sortie.</span><span class="sxs-lookup"><span data-stu-id="5c57d-173">Perform video mixing using a rectangle smaller than the output rectangle.</span></span> <span data-ttu-id="5c57d-174">Mettez à l’échelle le résultat avec la taille de sortie correcte.</span><span class="sxs-lookup"><span data-stu-id="5c57d-174">Scale the result to the correct output size.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5c57d-175">En outre, le récepteur multimédia EVR prend en charge les attributs de configuration qui correspondent à chacun de ces indicateurs :</span><span class="sxs-lookup"><span data-stu-id="5c57d-175">In addition, the EVR media sink supports configuration attributes that correspond to each of these flags:</span></span>

-   [<span data-ttu-id="5c57d-176">EVRConfig \_ AllowBatching</span><span class="sxs-lookup"><span data-stu-id="5c57d-176">EVRConfig\_AllowBatching</span></span>](evrconfig-allowbatching.md)
-   [<span data-ttu-id="5c57d-177">EVRConfig \_ AllowDropToBob</span><span class="sxs-lookup"><span data-stu-id="5c57d-177">EVRConfig\_AllowDropToBob</span></span>](evrconfig-allowdroptobob.md)
-   [<span data-ttu-id="5c57d-178">EVRConfig \_ AllowDropToHalfInterlace</span><span class="sxs-lookup"><span data-stu-id="5c57d-178">EVRConfig\_AllowDropToHalfInterlace</span></span>](evrconfig-allowdroptohalfinterlace.md)
-   [<span data-ttu-id="5c57d-179">EVRConfig \_ AllowScaling</span><span class="sxs-lookup"><span data-stu-id="5c57d-179">EVRConfig\_AllowScaling</span></span>](evrconfig-allowscaling.md)
-   [<span data-ttu-id="5c57d-180">EVRConfig \_ AllowDropToThrottle</span><span class="sxs-lookup"><span data-stu-id="5c57d-180">EVRConfig\_AllowDropToThrottle</span></span>](evrconfig-allowdroptothrottle.md)
-   [<span data-ttu-id="5c57d-181">EVRConfig \_ ForceBatching</span><span class="sxs-lookup"><span data-stu-id="5c57d-181">EVRConfig\_ForceBatching</span></span>](evrconfig-forcebatching.md)
-   [<span data-ttu-id="5c57d-182">EVRConfig \_ ForceBob</span><span class="sxs-lookup"><span data-stu-id="5c57d-182">EVRConfig\_ForceBob</span></span>](evrconfig-forcebob.md)
-   [<span data-ttu-id="5c57d-183">EVRConfig \_ ForceHalfInterlace</span><span class="sxs-lookup"><span data-stu-id="5c57d-183">EVRConfig\_ForceHalfInterlace</span></span>](evrconfig-forcehalfinterlace.md)
-   [<span data-ttu-id="5c57d-184">EVRConfig \_ ForceScaling</span><span class="sxs-lookup"><span data-stu-id="5c57d-184">EVRConfig\_ForceScaling</span></span>](evrconfig-forcescaling.md)
-   [<span data-ttu-id="5c57d-185">EVRConfig \_ ForceThrottle</span><span class="sxs-lookup"><span data-stu-id="5c57d-185">EVRConfig\_ForceThrottle</span></span>](evrconfig-forcethrottle.md)

<span data-ttu-id="5c57d-186">Avant le démarrage de la lecture, vous pouvez définir ces attributs directement sur le récepteur multimédia EVR, au lieu d’appeler les méthodes [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) et [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="5c57d-186">Before playback starts, you can set these attributes directly on the EVR media sink, as an alternative to calling the [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) and [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) methods.</span></span> <span data-ttu-id="5c57d-187">Pour définir ces attributs, interrogez le récepteur multimédia EVR pour [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="5c57d-187">To set these attributes, query the EVR media sink for [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c57d-188">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c57d-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c57d-189">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="5c57d-189">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 




