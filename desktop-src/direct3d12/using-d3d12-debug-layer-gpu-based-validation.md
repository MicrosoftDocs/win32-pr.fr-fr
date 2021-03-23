---
title: Validation basée sur GPU et couche de débogage Direct3D 12
description: Cette rubrique explique comment tirer le meilleur parti de la couche de débogage Direct3D 12. La validation basée sur GPU (GBV) active des scénarios de validation sur la chronologie GPU qui ne sont pas possibles lors des appels d’API sur le processeur.
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 3160df3faf994df2abf9cf878088e84564bb5fe1
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548587"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a><span data-ttu-id="190d6-104">Validation basée sur GPU et couche de débogage Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="190d6-104">GPU-based validation and the Direct3D 12 Debug Layer</span></span>

<span data-ttu-id="190d6-105">Cette rubrique explique comment tirer le meilleur parti de la couche de débogage Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="190d6-105">This topic describes how to make best use of the Direct3D 12 Debug Layer.</span></span> <span data-ttu-id="190d6-106">La validation basée sur GPU (GBV) active des scénarios de validation sur la chronologie GPU qui ne sont pas possibles lors des appels d’API sur le processeur.</span><span class="sxs-lookup"><span data-stu-id="190d6-106">GPU-based validation (GBV) enables validation scenarios on the GPU timeline that are not possible during API calls on the CPU.</span></span> <span data-ttu-id="190d6-107">GBV est disponible à partir de la mise à jour anniversaire des outils Graphics pour Windows 10.</span><span class="sxs-lookup"><span data-stu-id="190d6-107">GBV is available starting with the Graphics Tools for Windows 10 Anniversary Update.</span></span>

## <a name="purpose-of-gpu-based-validation"></a><span data-ttu-id="190d6-108">Objectif de la validation basée sur GPU</span><span class="sxs-lookup"><span data-stu-id="190d6-108">Purpose of GPU-based validation</span></span>

<span data-ttu-id="190d6-109">La validation basée sur GPU permet d’identifier les erreurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="190d6-109">GPU-based validation helps to identify the following errors:</span></span>

- <span data-ttu-id="190d6-110">Utilisation de descripteurs non initialisés ou incompatibles dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="190d6-110">Use of uninitialized or incompatible descriptors in a shader.</span></span>
- <span data-ttu-id="190d6-111">Utilisation de descripteurs référençant les ressources supprimées dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="190d6-111">Use of descriptors referencing deleted Resources in a shader.</span></span>
- <span data-ttu-id="190d6-112">Validation des États des ressources promues et de la dégradation de l’état des ressources.</span><span class="sxs-lookup"><span data-stu-id="190d6-112">Validation of promoted resource states and resource state decay.</span></span>
- <span data-ttu-id="190d6-113">Indexation au-delà de la fin du tas du descripteur dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="190d6-113">Indexing beyond the end of the descriptor heap in a shader.</span></span>
- <span data-ttu-id="190d6-114">Accès du nuanceur des ressources dans un État incompatible.</span><span class="sxs-lookup"><span data-stu-id="190d6-114">Shader accesses of resources in incompatible state.</span></span>
- <span data-ttu-id="190d6-115">Utilisation d’échantillonneurs non initialisés ou incompatibles dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="190d6-115">Use of uninitialized or incompatible Samplers in a shader.</span></span>

<span data-ttu-id="190d6-116">GBV fonctionne en créant des nuanceurs corrigés qui ont une validation ajoutée directement au nuanceur.</span><span class="sxs-lookup"><span data-stu-id="190d6-116">GBV works by creating patched shaders that have validation added directly to the shader.</span></span> <span data-ttu-id="190d6-117">Les nuanceurs corrigés inspectent les arguments racine et les ressources accessibles pendant l’exécution du nuanceur et signalent les erreurs dans un tampon de journal.</span><span class="sxs-lookup"><span data-stu-id="190d6-117">The patched shaders inspect root arguments and resources accessed during shader execution and report errors to a log buffer.</span></span> <span data-ttu-id="190d6-118">GBV injecte également des opérations supplémentaires et des appels de répartition dans les listes de commandes de l’application pour valider et suivre les modifications apportées à l’état des ressources imposées par la liste de commandes sur la chronologie du GPU.</span><span class="sxs-lookup"><span data-stu-id="190d6-118">GBV also injects extra operations and Dispatch calls into the application command lists to validate and track changes to resource state imposed by the command list on the GPU-timeline.</span></span>

<span data-ttu-id="190d6-119">Comme GBV nécessite la possibilité d’exécuter des nuanceurs, les listes de commandes de copie sont émulées par une liste de commandes de calcul.</span><span class="sxs-lookup"><span data-stu-id="190d6-119">Because GBV requires the ability to execute shaders, COPY command lists are emulated by a COMPUTE command list.</span></span> <span data-ttu-id="190d6-120">Cela peut modifier la manière dont le matériel effectue des copies même si le résultat final ne doit pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="190d6-120">This may potentially change how hardware performs copies though the end result should not be changed.</span></span> <span data-ttu-id="190d6-121">L’application percevra toujours qu’il s’agit de listes de commandes de copie et que la couche de débogage les validera comme telle.</span><span class="sxs-lookup"><span data-stu-id="190d6-121">The application will still perceive these are COPY command lists and the debug layer will validate them as such.</span></span>

## <a name="turning-on-gpu-based-validation"></a><span data-ttu-id="190d6-122">Activation de la validation basée sur GPU</span><span class="sxs-lookup"><span data-stu-id="190d6-122">Turning on GPU-based validation</span></span>

<span data-ttu-id="190d6-123">GBV peut être forcé à l’aide du panneau de configuration DirectX (DXCPL) en forçant la couche de débogage Direct3D 12 et en forçant en outre la validation basée sur GPU (nouvel onglet dans le panneau de configuration).</span><span class="sxs-lookup"><span data-stu-id="190d6-123">GBV can be forced on using the DirectX Control Panel (DXCPL) by forcing on the Direct3D 12 Debug Layer and additionally forcing on GPU-based validation (new tab in the control panel).</span></span> <span data-ttu-id="190d6-124">Une fois activé, GBV reste activé jusqu’à la sortie de l’appareil Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="190d6-124">Once enabled, GBV will remain enabled until the Direct3D 12 device is released.</span></span> <span data-ttu-id="190d6-125">Sinon, GBV peut être activé par programme avant de créer l’appareil Direct3D 12 :</span><span class="sxs-lookup"><span data-stu-id="190d6-125">Alternatively, GBV can be enabled programmatically prior to creating the Direct3D 12 Device:</span></span>

```cpp
void EnableShaderBasedValidation()
{
    CComPtr<ID3D12Debug> spDebugController0;
    CComPtr<ID3D12Debug1> spDebugController1;
    VERIFY(D3D12GetDebugInterface(IID_PPV_ARGS(&spDebugController0)));
    VERIFY(spDebugController0->QueryInterface(IID_PPV_ARGS(&spDebugController1)));
    spDebugController1->SetEnableGPUBasedValidation(true);
}
```

## <a name="recommended-usage"></a><span data-ttu-id="190d6-126">Utilisation recommandée</span><span class="sxs-lookup"><span data-stu-id="190d6-126">Recommended usage</span></span>

<span data-ttu-id="190d6-127">En règle générale, vous devez exécuter votre code avec la couche de débogage activée la plupart du temps.</span><span class="sxs-lookup"><span data-stu-id="190d6-127">Generally, you should run your code with the debug layer enabled most of the time.</span></span> <span data-ttu-id="190d6-128">Toutefois, GBV peut ralentir considérablement les choses.</span><span class="sxs-lookup"><span data-stu-id="190d6-128">However, GBV can slow things down a lot.</span></span> <span data-ttu-id="190d6-129">Les développeurs peuvent envisager d’activer GBV avec des jeux de données plus petits (par exemple, des démonstrations de moteur ou des petits niveaux de jeu avec moins d’PSO et des ressources) ou lors de la mise en place d’une application précoce pour réduire les problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="190d6-129">Developers may consider enabling GBV with smaller data sets (for example, engine demos or small game levels with fewer PSO’s and resources) or during early application bring-up to reduce performance problems.</span></span> <span data-ttu-id="190d6-130">Avec un contenu de plus grande taille, envisagez d’activer GBV sur une ou deux machines de test dans un test nocturne.</span><span class="sxs-lookup"><span data-stu-id="190d6-130">With larger content consider turning on GBV on one or two test machines in a nightly test pass.</span></span>

## <a name="debug-output"></a><span data-ttu-id="190d6-131">Sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="190d6-131">Debug output</span></span>

<span data-ttu-id="190d6-132">GBV produit une sortie de débogage après qu’un appel à [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) termine l’exécution sur le GPU.</span><span class="sxs-lookup"><span data-stu-id="190d6-132">GBV produces debug output after a call to [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) completes execution on the GPU.</span></span> <span data-ttu-id="190d6-133">Étant donné qu’il s’agit de la chronologie du GPU, la sortie de débogage peut être asynchrone avec une autre validation de la chronologie de l’UC.</span><span class="sxs-lookup"><span data-stu-id="190d6-133">Since this is on the GPU-timeline the debug output may be asynchronous with other CPU-timeline validation.</span></span> <span data-ttu-id="190d6-134">Les développeurs d’applications peuvent souhaiter injecter leur propre attente-après-exécution pour synchroniser la sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="190d6-134">Application developers may want to inject their own wait-after-execute to synchronize debug output.</span></span>

<span data-ttu-id="190d6-135">La sortie de GBV identifie l’endroit où une erreur s’est produite dans un nuanceur, ainsi que le nombre actuel de dessins/dispatchs et les identités des objets associés (par exemple, liste de commandes, file d’attente, PSO, etc.).</span><span class="sxs-lookup"><span data-stu-id="190d6-135">GBV output identifies where in a shader an error occurred, along with the current draw/dispatch count and identities of related objects (e.g. command list, queue, PSO, etc).</span></span>

## <a name="example-debug-message"></a><span data-ttu-id="190d6-136">Exemple de message de débogage</span><span class="sxs-lookup"><span data-stu-id="190d6-136">Example debug message</span></span>

<span data-ttu-id="190d6-137">Le message d’erreur suivant indique qu’une ressource nommée « main Color buffer » a été accédée dans un nuanceur en tant que ressource de nuanceur, mais qu’elle était dans l’état d’accès non ordonné lorsque le nuanceur s’exécutait sur le GPU.</span><span class="sxs-lookup"><span data-stu-id="190d6-137">The following error message indicates that a resource named “Main Color Buffer” was accessed in a shader as a shader resource but was in the unordered access state when the shader ran on the GPU.</span></span> <span data-ttu-id="190d6-138">Des informations supplémentaires, telles que l’emplacement dans la source du nuanceur, le nom de la liste de commandes et le nombre de dessins (index de dessin), ainsi que les noms des objets d’interface D3D associés sont également fournis.</span><span class="sxs-lookup"><span data-stu-id="190d6-138">Additional information, such as the location in the shader source, the name of the command list and the Draw count (Draw Index), and the names of related D3D interface objects are also provided.</span></span>

```cmd
D3D12 ERROR: Incompatible resource state: Resource: 0x0000016F61A6EA80:'Main Color Buffer', 
Subresource Index: [0], 
Descriptor heap index: [0], 
Binding Type In Descriptor: SRV, 
Resource State: D3D12_RESOURCE_STATE_UNORDERED_ACCESS(0x8), 
Shader Stage: PIXEL, 
Root Parameter Index: [0], 
Draw Index: [0], 
Shader Code: E:\FileShare\MiniEngine_GitHub_160128\MiniEngine_GitHub\Core\Shaders\SharpeningUpsamplePS.hlsl(37,2-59), 
Asm Instruction Range: [0x138-0x16b], 
Asm Operand Index: [3], 
Command List: 0x0000016F6F75F740:'CommandList', SRV/UAV/CBV Descriptor Heap: 0x0000016F6F76F280:'Unnamed ID3D12DescriptorHeap Object', 
Sampler Descriptor Heap: <not set>, 
Pipeline State: 0x0000016F572C89F0:'Unnamed ID3D12PipelineState Object',  
[ EXECUTION ERROR #942: GPU_BASED_VALIDATION_INCOMPATIBLE_RESOURCE_STATE]
```

## <a name="debug-layer-apis"></a><span data-ttu-id="190d6-139">API de couche de débogage</span><span class="sxs-lookup"><span data-stu-id="190d6-139">Debug Layer APIs</span></span>

<span data-ttu-id="190d6-140">Pour activer la couche de débogage, appelez [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).</span><span class="sxs-lookup"><span data-stu-id="190d6-140">To enable the debug layer, call [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).</span></span>

<span data-ttu-id="190d6-141">Pour activer la validation basée sur GPU, appelez [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)et reportez-vous aux méthodes des interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="190d6-141">To enable GPU-based validation, call [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation), and refer to the methods of the following interfaces:</span></span>

- [<span data-ttu-id="190d6-142">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="190d6-142">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [<span data-ttu-id="190d6-143">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="190d6-143">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [<span data-ttu-id="190d6-144">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="190d6-144">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

<span data-ttu-id="190d6-145">Reportez-vous aux énumérations et structures suivantes :</span><span class="sxs-lookup"><span data-stu-id="190d6-145">Refer to the following enumerations and structures:</span></span>

- [<span data-ttu-id="190d6-146">**\_Type de \_ \_ paramètre de liste de commandes de débogage D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="190d6-146">**D3D12\_DEBUG\_COMMAND\_LIST\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [<span data-ttu-id="190d6-147">**TYPE de paramètre de l' \_ appareil de débogage D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="190d6-147">**D3D12\_DEBUG\_DEVICE\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [<span data-ttu-id="190d6-148">**Indicateurs de création de l' \_ \_ \_ État du \_ pipeline de validation \_ basé \_ sur \_ GPU D3D12**</span><span class="sxs-lookup"><span data-stu-id="190d6-148">**D3D12\_GPU\_BASED\_VALIDATION\_PIPELINE\_STATE\_CREATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [<span data-ttu-id="190d6-149">**\_Mode de \_ \_ Correction du \_ nuanceur de validation basé \_ sur GPU D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="190d6-149">**D3D12\_GPU\_BASED\_VALIDATION\_SHADER\_PATCH\_MODE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [<span data-ttu-id="190d6-150">**\_Liste de commandes de débogage D3D12 \_ \_ \_ \_ \_ paramètres de validation basés sur GPU \_**</span><span class="sxs-lookup"><span data-stu-id="190d6-150">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [<span data-ttu-id="190d6-151">**D3D12 \_ déboguer les \_ \_ \_ paramètres de validation basés sur GPU \_ \_**</span><span class="sxs-lookup"><span data-stu-id="190d6-151">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a><span data-ttu-id="190d6-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="190d6-152">Related topics</span></span>

* [<span data-ttu-id="190d6-153">Fonctionnement de la couche de débogage Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="190d6-153">Understanding the Direct3D 12 Debug Layer</span></span>](understanding-the-d3d12-debug-layer.md)
