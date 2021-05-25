---
description: Consultez une combinaison d’un ou plusieurs indicateurs qui contrôlent le comportement de création de l’appareil.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d89043ac49b72bccf6279ef3c9c8fa2c856c775
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343226"
---
# <a name="d3dcreate"></a><span data-ttu-id="41b36-103">D3DCREATE</span><span class="sxs-lookup"><span data-stu-id="41b36-103">D3DCREATE</span></span>

<span data-ttu-id="41b36-104">Combinaison d’un ou de plusieurs indicateurs qui contrôlent le comportement de création de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="41b36-104">A combination of one or more flags that control the device create behavior.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41b36-105">#définition</span><span class="sxs-lookup"><span data-stu-id="41b36-105">#define</span></span></td>
<td><span data-ttu-id="41b36-106">Description</span><span class="sxs-lookup"><span data-stu-id="41b36-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41b36-107">D3DCREATE_ADAPTERGROUP_DEVICE</span><span class="sxs-lookup"><span data-stu-id="41b36-107">D3DCREATE_ADAPTERGROUP_DEVICE</span></span></td>
<td><span data-ttu-id="41b36-108">L’application demande à l’appareil de piloter tous les en-têtes détenus par cet adaptateur maître.</span><span class="sxs-lookup"><span data-stu-id="41b36-108">Application asks the device to drive all the heads that this master adapter owns.</span></span> <span data-ttu-id="41b36-109">L’indicateur n’est pas conforme sur les adaptateurs non maîtres.</span><span class="sxs-lookup"><span data-stu-id="41b36-109">The flag is illegal on nonmaster adapters.</span></span> <span data-ttu-id="41b36-110">Si cet indicateur est défini, les paramètres de présentation passés à <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> doivent pointer vers un tableau de <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="41b36-110">If this flag is set, the presentation parameters passed to <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> should point to an array of <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span></span> <span data-ttu-id="41b36-111">Le nombre d’éléments dans <strong>D3DPRESENT_PARAMETERS</strong> doit être égal au nombre d’adaptateurs défini par le membre NumberOfAdaptersInGroup de la structure <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="41b36-111">The number of elements in <strong>D3DPRESENT_PARAMETERS</strong> should equal the number of adapters defined by the NumberOfAdaptersInGroup member of the <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> structure.</span></span> <span data-ttu-id="41b36-112">Le runtime DirectX assignera chaque élément à chaque tête dans l’ordre numérique spécifié par le membre AdapterOrdinalInGroup de <strong>D3DCAPS9</strong>.</span><span class="sxs-lookup"><span data-stu-id="41b36-112">The DirectX runtime will assign each element to each head in the numerical order specified by the AdapterOrdinalInGroup member of <strong>D3DCAPS9</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41b36-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="41b36-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span></span></td>
<td><span data-ttu-id="41b36-114">Direct3D gérera les ressources au lieu du pilote.</span><span class="sxs-lookup"><span data-stu-id="41b36-114">Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="41b36-115">Les appels Direct3D n’échoueront pas pour les erreurs de ressources telles que la mémoire vidéo insuffisante.</span><span class="sxs-lookup"><span data-stu-id="41b36-115">Direct3D calls will not fail for resource errors such as insufficient video memory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41b36-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span><span class="sxs-lookup"><span data-stu-id="41b36-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span></span></td>
<td><span data-ttu-id="41b36-117">Comme D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D gère les ressources au lieu du pilote.</span><span class="sxs-lookup"><span data-stu-id="41b36-117">Like D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="41b36-118">Contrairement à D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX renvoie des erreurs pour des conditions telles qu’une mémoire vidéo insuffisante.</span><span class="sxs-lookup"><span data-stu-id="41b36-118">Unlike D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX will return errors for conditions such as insufficient video memory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41b36-119">D3DCREATE_DISABLE_PRINTSCREEN</span><span class="sxs-lookup"><span data-stu-id="41b36-119">D3DCREATE_DISABLE_PRINTSCREEN</span></span></td>
<td><span data-ttu-id="41b36-120">Le runtime n’enregistre pas les touches d’accès rapide pour printscreen, Ctrl-Printscreen et Alt-Printscreen pour capturer le contenu du bureau ou de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="41b36-120">Causes the runtime not register hotkeys for Printscreen, Ctrl-Printscreen and Alt-Printscreen to capture the desktop or window content.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41b36-121">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="41b36-121">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="41b36-122">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="41b36-122">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41b36-123">D3DCREATE_DISABLE_PSGP_THREADING</span><span class="sxs-lookup"><span data-stu-id="41b36-123">D3DCREATE_DISABLE_PSGP_THREADING</span></span></td>
<td><span data-ttu-id="41b36-124">Limitez le calcul au thread d’application principal.</span><span class="sxs-lookup"><span data-stu-id="41b36-124">Restrict computation to the main application thread.</span></span> <span data-ttu-id="41b36-125">Si l’indicateur n’est pas défini, le runtime peut effectuer le traitement du vertex logiciel et d’autres calculs dans le thread de travail afin d’améliorer les performances sur les systèmes multiprocesseurs.</span><span class="sxs-lookup"><span data-stu-id="41b36-125">If the flag is not set, the runtime may perform software vertex processing and other computations in worker thread to improve performance on multi-processor systems.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41b36-126">Différences entre Windows XP et Windows Vista :</span><span class="sxs-lookup"><span data-stu-id="41b36-126">Differences between Windows XP and Windows Vista:</span></span><br/> <span data-ttu-id="41b36-127">Cet indicateur est disponible sur Windows Vista, Windows Server 2008 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="41b36-127">This flag is available on Windows Vista, Windows Server 2008, and Windows 7.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41b36-128">D3DCREATE_ENABLE_PRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="41b36-128">D3DCREATE_ENABLE_PRESENTSTATS</span></span></td>
<td><span data-ttu-id="41b36-129">Active la collecte des statistiques actuelles sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="41b36-129">Enables the gathering of present statistics on the device.</span></span> <span data-ttu-id="41b36-130">Les appels à <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> retournent des données valides.</span><span class="sxs-lookup"><span data-stu-id="41b36-130">Calls to <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> will return valid data.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41b36-131">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="41b36-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="41b36-132">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="41b36-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41b36-133">D3DCREATE_FPU_PRESERVE</span><span class="sxs-lookup"><span data-stu-id="41b36-133">D3DCREATE_FPU_PRESERVE</span></span></td>
<td><span data-ttu-id="41b36-134">Définissez la précision des calculs en virgule flottante Direct3D sur la précision utilisée par le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="41b36-134">Set the precision for Direct3D floating-point calculations to the precision used by the calling thread.</span></span> <span data-ttu-id="41b36-135">Si vous ne spécifiez pas cet indicateur, Direct3D passe par défaut au mode d’aller-à-proche simple précision pour deux raisons :</span><span class="sxs-lookup"><span data-stu-id="41b36-135">If you do not specify this flag, Direct3D defaults to single-precision round-to-nearest mode for two reasons:</span></span>
<ul>
<li><span data-ttu-id="41b36-136">Le mode double précision réduit les performances Direct3D.</span><span class="sxs-lookup"><span data-stu-id="41b36-136">Double-precision mode will reduce Direct3D performance.</span></span></li>
<li><span data-ttu-id="41b36-137">Des portions de Direct3D supposent que les exceptions d’unité à virgule flottante sont masquées ; le démasquage de ces exceptions peut entraîner un comportement indéfini.</span><span class="sxs-lookup"><span data-stu-id="41b36-137">Portions of Direct3D assume floating-point unit exceptions are masked; unmasking these exceptions may result in undefined behavior.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41b36-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="41b36-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="41b36-139">Spécifie le traitement du vertex matériel.</span><span class="sxs-lookup"><span data-stu-id="41b36-139">Specifies hardware vertex processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41b36-140">D3DCREATE_MIXED_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="41b36-140">D3DCREATE_MIXED_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="41b36-141">Spécifie le traitement des vertex mixtes (logiciels et matériels).</span><span class="sxs-lookup"><span data-stu-id="41b36-141">Specifies mixed (both software and hardware) vertex processing.</span></span> <span data-ttu-id="41b36-142">Pour Windows 10, version 1607 et versions ultérieures, l’utilisation de ce paramètre n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="41b36-142">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="41b36-143">Consultez D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="41b36-143">See D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41b36-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="41b36-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="41b36-145">Spécifie le traitement du vertex logiciel.</span><span class="sxs-lookup"><span data-stu-id="41b36-145">Specifies software vertex processing.</span></span> <span data-ttu-id="41b36-146">Pour Windows 10, version 1607 et versions ultérieures, l’utilisation de ce paramètre n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="41b36-146">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="41b36-147">Utilisez D3DCREATE_HARDWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="41b36-147">Use D3DCREATE_HARDWARE_VERTEXPROCESSING.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="41b36-148">Sauf si le traitement du vertex matériel n’est pas disponible, l’utilisation du traitement du vertex logiciel n’est pas recommandée dans Windows 10, version 1607 (et versions ultérieures), car l’efficacité du traitement du vertex logiciel a été considérablement réduite, tout en améliorant la sécurité de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="41b36-148">Unless hardware vertex processing is not available, the usage of software vertex processing is not recommended in Windows 10, version 1607 (and later versions) because the efficiency of software vertex processing was significantly reduced while improving the security of the implementation.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41b36-149">D3DCREATE_MULTITHREADED</span><span class="sxs-lookup"><span data-stu-id="41b36-149">D3DCREATE_MULTITHREADED</span></span></td>
<td><span data-ttu-id="41b36-150">Indique que l’application demande à Direct3D d’être de sécurité multithread.</span><span class="sxs-lookup"><span data-stu-id="41b36-150">Indicates that the application requests Direct3D to be multithread safe.</span></span> <span data-ttu-id="41b36-151">Cela permet à un thread Direct3D de prendre possession de sa <a href="/windows/desktop/Sync/critical-section-objects">section critique</a> globale plus fréquemment, ce qui peut dégrader les performances.</span><span class="sxs-lookup"><span data-stu-id="41b36-151">This makes a Direct3D thread take ownership of its global <a href="/windows/desktop/Sync/critical-section-objects">critical section</a> more frequently, which can degrade performance.</span></span> <span data-ttu-id="41b36-152">Si une application traite des messages de fenêtre dans un thread lors de l’exécution d’appels d’API Direct3D dans un autre, l’application doit utiliser cet indicateur lors de la création de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="41b36-152">If an application processes window messages in one thread while making Direct3D API calls in another, the application must use this flag when creating the device.</span></span> <span data-ttu-id="41b36-153">Cette fenêtre doit également être détruite avant de décharger d3d9.dll.</span><span class="sxs-lookup"><span data-stu-id="41b36-153">This window must also be destroyed before unloading d3d9.dll.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41b36-154">D3DCREATE_NOWINDOWCHANGES</span><span class="sxs-lookup"><span data-stu-id="41b36-154">D3DCREATE_NOWINDOWCHANGES</span></span></td>
<td><span data-ttu-id="41b36-155">Indique que Direct3D ne doit pas modifier la fenêtre de focus de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="41b36-155">Indicates that Direct3D must not alter the focus window in any way.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="41b36-156">Si cet indicateur est défini, l’application doit prendre entièrement en charge tous les événements de gestion de focus, tels que ALT + TAB et les événements de clic de souris.</span><span class="sxs-lookup"><span data-stu-id="41b36-156">If this flag is set, the application must fully support all focus management events, such as ALT+TAB and mouse click events.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41b36-157">D3DCREATE_PUREDEVICE</span><span class="sxs-lookup"><span data-stu-id="41b36-157">D3DCREATE_PUREDEVICE</span></span></td>
<td><span data-ttu-id="41b36-158">Spécifie que Direct3D ne prend pas en charge les appels d’extraction \* pour tout ce qui peut être stocké dans des blocs d’État.</span><span class="sxs-lookup"><span data-stu-id="41b36-158">Specifies that Direct3D does not support Get\* calls for anything that can be stored in state blocks.</span></span> <span data-ttu-id="41b36-159">Il indique également à Direct3D de ne pas fournir de services d’émulation pour le traitement des vertex.</span><span class="sxs-lookup"><span data-stu-id="41b36-159">It also tells Direct3D not to provide any emulation services for vertex processing.</span></span> <span data-ttu-id="41b36-160">Cela signifie que si l’appareil ne prend pas en charge le traitement des vertex, l’application ne peut utiliser que des sommets convertis.</span><span class="sxs-lookup"><span data-stu-id="41b36-160">This means that if the device does not support vertex processing, then the application can use only post-transformed vertices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41b36-161">D3DCREATE_SCREENSAVER</span><span class="sxs-lookup"><span data-stu-id="41b36-161">D3DCREATE_SCREENSAVER</span></span></td>
<td><span data-ttu-id="41b36-162">Permet d’obtenir des économiseurs d’écran pendant une application en plein écran.</span><span class="sxs-lookup"><span data-stu-id="41b36-162">Allows screensavers during a fullscreen application.</span></span> <span data-ttu-id="41b36-163">Sans cet indicateur, Direct3D désactivera les économiseurs d’écran tant que l’application appelante est en plein écran.</span><span class="sxs-lookup"><span data-stu-id="41b36-163">Without this flag, Direct3D will disable screensavers for as long as the calling application is fullscreen.</span></span> <span data-ttu-id="41b36-164">Si l’application appelante est déjà un économiseur d’écran, cet indicateur n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="41b36-164">If the calling application is already a screensaver, this flag has no effect.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41b36-165">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="41b36-165">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="41b36-166">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="41b36-166">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="41b36-167">\_Les D3DCREATE matériels \_ VERTEXPROCESSING, D3DCREATE \_ Mixed \_ VERTEXPROCESSING et D3DCREATE \_ Software \_ VERTEXPROCESSING sont des indicateurs mutuellement exclusifs.</span><span class="sxs-lookup"><span data-stu-id="41b36-167">D3DCREATE\_HARDWARE\_VERTEXPROCESSING, D3DCREATE\_MIXED\_VERTEXPROCESSING, and D3DCREATE\_SOFTWARE\_VERTEXPROCESSING are mutually exclusive flags.</span></span> <span data-ttu-id="41b36-168">Au moins un de ces indicateurs de traitement de vertex doit être spécifié lors de l’appel de [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span><span class="sxs-lookup"><span data-stu-id="41b36-168">At least one of these vertex processing flags must be specified when calling [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span>

## <a name="constant-information"></a><span data-ttu-id="41b36-169">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="41b36-169">Constant Information</span></span>



| <span data-ttu-id="41b36-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41b36-170">Requirement</span></span>                         |  <span data-ttu-id="41b36-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="41b36-171">Value</span></span>          |
|--------------------------|------------|
| <span data-ttu-id="41b36-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="41b36-172">Header</span></span>                   | <span data-ttu-id="41b36-173">D3D9. h</span><span class="sxs-lookup"><span data-stu-id="41b36-173">D3D9.h</span></span>     |
| <span data-ttu-id="41b36-174">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="41b36-174">Minimum operating system</span></span> | <span data-ttu-id="41b36-175">Windows 98</span><span class="sxs-lookup"><span data-stu-id="41b36-175">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="41b36-176">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41b36-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41b36-177">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="41b36-177">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
