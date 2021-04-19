---
title: Niveau de fonctionnalité Direct3D 12 Core 1.0
description: Le niveau de fonctionnalité principal 1,0 est un sous-ensemble de l’ensemble de fonctionnalités Direct3D 12 complet.
ms.topic: article
ms.date: 11/05/2019
ms.openlocfilehash: 42d13b71c516e55ecce378cf9cb415c45e520ba9
ms.sourcegitcommit: bba068130240d16de8a3f3468b7cd72b2cd760f6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2020
ms.locfileid: "106513515"
---
# <a name="the-direct3d-12-core-10-feature-level"></a><span data-ttu-id="26c1d-103">Niveau de fonctionnalité Direct3D 12 Core 1.0</span><span class="sxs-lookup"><span data-stu-id="26c1d-103">The Direct3D 12 Core 1.0 Feature Level</span></span>

<span data-ttu-id="26c1d-104">Le niveau de fonctionnalité principal 1,0 est un sous-ensemble de l’ensemble de fonctionnalités Direct3D 12 complet.</span><span class="sxs-lookup"><span data-stu-id="26c1d-104">The Core 1.0 Feature Level is a subset of the full Direct3D 12 feature set.</span></span> <span data-ttu-id="26c1d-105">Le niveau de fonctionnalité principal 1,0 peut être exposé par une catégorie d’appareils appelés *appareils de calcul uniquement*.</span><span class="sxs-lookup"><span data-stu-id="26c1d-105">Core 1.0 Feature Level can be exposed by a category of devices known as *compute-only devices*.</span></span> <span data-ttu-id="26c1d-106">Le modèle de pilote global pour les appareils de calcul uniquement est le modèle de pilote de calcul Microsoft (MCDM).</span><span class="sxs-lookup"><span data-stu-id="26c1d-106">The overall driver model for compute-only devices is the Microsoft Compute Driver Model (MCDM).</span></span> <span data-ttu-id="26c1d-107">MCDM est un homologue mis à l’échelle du modèle WDDM (Windows Device Driver Model), qui a une plus grande portée.</span><span class="sxs-lookup"><span data-stu-id="26c1d-107">MCDM is a scaled-down peer of the Windows Device Driver Model (WDDM), which has a larger scope.</span></span>

<span data-ttu-id="26c1d-108">Un appareil qui prend *uniquement* en charge les fonctionnalités au sein d’un niveau de fonctionnalité principal est appelé *appareil principal*.</span><span class="sxs-lookup"><span data-stu-id="26c1d-108">A device that supports *only* the features within a Core Feature Level is known as a *Core device*.</span></span>

> [!NOTE]
> <span data-ttu-id="26c1d-109">L’appareil *de calcul uniquement*, l’appareil *MCDM*, l' *appareil de niveau de fonctionnalité principal* et l' *appareil de base* ont tous la même signification.</span><span class="sxs-lookup"><span data-stu-id="26c1d-109">*Compute-only device*, *MCDM device*, *Core Feature Level device*, and *Core device* all mean the same thing.</span></span> <span data-ttu-id="26c1d-110">Nous préférerons l' *appareil de base* pour des raisons de simplicité.</span><span class="sxs-lookup"><span data-stu-id="26c1d-110">We'll prefer *Core device* for simplicity.</span></span>

## <a name="creating-a-core-device"></a><span data-ttu-id="26c1d-111">Création d’un périphérique principal</span><span class="sxs-lookup"><span data-stu-id="26c1d-111">Creating a Core device</span></span>

<span data-ttu-id="26c1d-112">En général, pour créer un appareil Direct3D 12, vous appelez la fonction [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) et spécifiez un niveau de fonctionnalité minimal.</span><span class="sxs-lookup"><span data-stu-id="26c1d-112">In general, to create a Direct3D 12 device, you call the [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) function, and specify a minimum feature level.</span></span>

<span data-ttu-id="26c1d-113">Si vous spécifiez un niveau de fonctionnalité de 9 à 12, l’appareil retourné est un appareil riche en fonctionnalités, tel qu’un GPU traditionnel (qui prend en charge un sur-ensemble de la fonctionnalité d’un appareil principal).</span><span class="sxs-lookup"><span data-stu-id="26c1d-113">If you specify a feature level of 9 through 12, then the device that's returned is a feature-rich device, such as a traditional GPU (which supports a superset of the functionality of a Core device).</span></span> <span data-ttu-id="26c1d-114">Un appareil principal n’est jamais retourné pour cette plage de niveaux de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="26c1d-114">A Core device is never returned for that range of feature levels.</span></span>

<span data-ttu-id="26c1d-115">En revanche, si vous spécifiez un niveau de fonctionnalité principal (par exemple, [**D3D_FEATURE_LEVEL ::D 3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), l’appareil retourné peut être riche en fonctionnalités, ou il peut s’agir d’un appareil de base.</span><span class="sxs-lookup"><span data-stu-id="26c1d-115">On the other hand, if you specify a Core feature level (for example, [**D3D_FEATURE_LEVEL::D3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), then the device that's returned could be feature-rich, or it could be a Core device.</span></span>

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

<span data-ttu-id="26c1d-116">Si vous spécifiez un `_CORE` niveau de fonctionnalité, la couche Runtime/Debug vérifie que les fonctionnalités utilisées par votre application sont autorisées par ce `_CORE` niveau de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="26c1d-116">If you specify a `_CORE` feature level, then the runtime/debug layer validates that the features your application uses are allowed by that `_CORE` feature level.</span></span> <span data-ttu-id="26c1d-117">Cet ensemble de fonctionnalités est défini plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="26c1d-117">That set of features is defined later in this topic.</span></span>

## <a name="shader-model-for-core-devices"></a><span data-ttu-id="26c1d-118">Modèle de nuanceur pour les périphériques centraux</span><span class="sxs-lookup"><span data-stu-id="26c1d-118">Shader model for Core devices</span></span>

<span data-ttu-id="26c1d-119">Un périphérique de base prend en charge le modèle de nuanceur 5.0 +.</span><span class="sxs-lookup"><span data-stu-id="26c1d-119">A Core device supports Shader Model 5.0+.</span></span>

<span data-ttu-id="26c1d-120">Le Runtime effectue la conversion des modèles de nuanceur 5. x non DXIL en 6,0 DXIL.</span><span class="sxs-lookup"><span data-stu-id="26c1d-120">The runtime performs conversion of 5.x non DXIL shader models to 6.0 DXIL.</span></span> <span data-ttu-id="26c1d-121">Ainsi, le pilote doit uniquement prendre en charge 6. x.</span><span class="sxs-lookup"><span data-stu-id="26c1d-121">So the driver need only support 6.x.</span></span>

## <a name="resource-management-model-for-core-devices"></a><span data-ttu-id="26c1d-122">Modèle de gestion des ressources pour les périphériques de base</span><span class="sxs-lookup"><span data-stu-id="26c1d-122">Resource management model for Core devices</span></span>

- <span data-ttu-id="26c1d-123">Dimensions de ressources prises en charge : mémoires tampons brutes et structurées uniquement (aucune mémoire tampon typée, texture1d/2D, etc.)</span><span class="sxs-lookup"><span data-stu-id="26c1d-123">Supported resource dimensions: raw and structured buffers only (no typed buffers, texture1d/2D, etc.)</span></span>
- <span data-ttu-id="26c1d-124">Aucune prise en charge des ressources réservées (en mosaïque)</span><span class="sxs-lookup"><span data-stu-id="26c1d-124">No support for reserved (tiled) resources</span></span>
- <span data-ttu-id="26c1d-125">Aucune prise en charge des tas personnalisés</span><span class="sxs-lookup"><span data-stu-id="26c1d-125">No support for custom heaps</span></span>
- <span data-ttu-id="26c1d-126">Aucun de ces indicateurs de tas n’est pris en charge :</span><span class="sxs-lookup"><span data-stu-id="26c1d-126">No support for any of these heap flags:</span></span>
  - <span data-ttu-id="26c1d-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span><span class="sxs-lookup"><span data-stu-id="26c1d-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span></span>
  - <span data-ttu-id="26c1d-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span><span class="sxs-lookup"><span data-stu-id="26c1d-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span></span>
  - <span data-ttu-id="26c1d-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span><span class="sxs-lookup"><span data-stu-id="26c1d-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span></span>
  - <span data-ttu-id="26c1d-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (Notez que le nuanceur atomiques est obligatoire, cet indicateur est destiné à une autre fonctionnalité, à des atomices d’adaptateurs croisés)</span><span class="sxs-lookup"><span data-stu-id="26c1d-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (note shader atomics are required, this flag is for another feature, cross adapter atomics)</span></span>

## <a name="resource-binding-model-for-core-devices"></a><span data-ttu-id="26c1d-131">Modèle de liaison de ressources pour les périphériques centraux</span><span class="sxs-lookup"><span data-stu-id="26c1d-131">Resource binding model for Core devices</span></span>

- <span data-ttu-id="26c1d-132">Prise en charge du niveau de liaison de ressources 1 uniquement</span><span class="sxs-lookup"><span data-stu-id="26c1d-132">Support for resource binding tier 1 only</span></span>
- <span data-ttu-id="26c1d-133">Exceptions :</span><span class="sxs-lookup"><span data-stu-id="26c1d-133">Exceptions:</span></span>
  - <span data-ttu-id="26c1d-134">Pas de prise en charge des échantillonneurs de texture</span><span class="sxs-lookup"><span data-stu-id="26c1d-134">No support for texture samplers</span></span>
  - <span data-ttu-id="26c1d-135">Prise en charge de 64 UAVs comme niveau de fonctionnalité 11.1 + (contrairement à 8 uniquement)</span><span class="sxs-lookup"><span data-stu-id="26c1d-135">Support for 64 UAVs like Feature Level 11.1+ (as opposed to only 8)</span></span>
  - <span data-ttu-id="26c1d-136">Les implémentations n’ont pas besoin d’implémenter la vérification des limites sur les accès du nuanceur aux ressources par le biais de descripteurs, les accès hors limites produisent un comportement indéfini.</span><span class="sxs-lookup"><span data-stu-id="26c1d-136">Implementations do not have to implement bounds checking on shader accesses to resources through descriptors, out of bounds accesses produce undefined behavior.</span></span>
    - <span data-ttu-id="26c1d-137">En tant que sous-ensemble, l’indicateur de plage de descripteurs D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS dans les signatures racines n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="26c1d-137">As a byproduct, the descriptor range flag D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS in root signatures is not supported.</span></span>
- <span data-ttu-id="26c1d-138">Les descripteurs UAV/CBV ne peuvent être créés que sur des ressources à partir de tas par défaut (aucun tas upload/readback).</span><span class="sxs-lookup"><span data-stu-id="26c1d-138">UAV/CBV descriptors can only be made on resources from default heaps (so no upload/readback heaps).</span></span> <span data-ttu-id="26c1d-139">Cela oblige votre application à effectuer des copies pour récupérer des données sur le processeur< >GPU.</span><span class="sxs-lookup"><span data-stu-id="26c1d-139">This forces your application to do copies to get data across CPU<->GPU.</span></span>
- <span data-ttu-id="26c1d-140">Bien qu’il s’agit du niveau de capacité de liaison le plus bas, il existe toujours des fonctionnalités requises, même dans ce niveau qui mérite d’être appelé :</span><span class="sxs-lookup"><span data-stu-id="26c1d-140">Despite being the lowest binding capability tier, there are still some features required even in this tier worth calling out:</span></span>
  - <span data-ttu-id="26c1d-141">Les tas de descripteurs peuvent être mis à jour après l’enregistrement des listes de commandes (voir D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE dans les spécifications de liaison de ressources)</span><span class="sxs-lookup"><span data-stu-id="26c1d-141">Descriptor heaps can be updated after command lists are recorded (see D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE in the resource binding spec)</span></span>
  - <span data-ttu-id="26c1d-142">Les descripteurs racine sont fondamentalement des pointeurs GPUVA</span><span class="sxs-lookup"><span data-stu-id="26c1d-142">Root descriptors are basically GPUVA pointers</span></span>
    - <span data-ttu-id="26c1d-143">Même s’il n’y a pas de prise en charge de MMU/VA, le SAV de mémoire tampon utilisé dans les descripteurs racine peut être émulé par les implémentations en procédant à une mise à jour corrective des adresses.</span><span class="sxs-lookup"><span data-stu-id="26c1d-143">Even though there is no MMU / VA support, buffer VAs that are used in root descriptors can be emulated by implementations by doing address patching.</span></span>

### <a name="structured-buffer-restrictions"></a><span data-ttu-id="26c1d-144">Restrictions de mémoire tampon structurées</span><span class="sxs-lookup"><span data-stu-id="26c1d-144">Structured buffer restrictions</span></span>

<span data-ttu-id="26c1d-145">Les mémoires tampons structurées doivent avoir une adresse de base qui est alignée sur 4 octets et STRIDE doit être 2 ou un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="26c1d-145">Structured buffers must have a base address that is 4 byte aligned, and stride must be 2 or a multiple of 4.</span></span> <span data-ttu-id="26c1d-146">Le cas d’une Stride de 2 est destiné aux applications avec des données 16 bits, en particulier en raison de l’absence de prise en charge des mémoires tampons typées dans D3D_FEATURE_LEVEL_1_0_CORE.</span><span class="sxs-lookup"><span data-stu-id="26c1d-146">The case for a stride of 2 is for apps with 16 bit data, particularly given there is no support for typed buffers in D3D_FEATURE_LEVEL_1_0_CORE.</span></span>

<span data-ttu-id="26c1d-147">La Stride spécifiée dans les descripteurs doit correspondre au Stride spécifié en HLSL.</span><span class="sxs-lookup"><span data-stu-id="26c1d-147">Stride specified in descriptors must match the stride specified in HLSL.</span></span>  

## <a name="command-queue-support-for-core-devices"></a><span data-ttu-id="26c1d-148">Prise en charge des files d’attente de commandes pour les périphériques principaux</span><span class="sxs-lookup"><span data-stu-id="26c1d-148">Command queue support for Core devices</span></span>

<span data-ttu-id="26c1d-149">Calculez et copiez les files d’attente uniquement (aucune file d’attente 3D, vidéo, etc.).</span><span class="sxs-lookup"><span data-stu-id="26c1d-149">Compute and copy queues only (no 3D, video, etc. queues).</span></span>

## <a name="shader-support-for-core-devices"></a><span data-ttu-id="26c1d-150">Prise en charge des nuanceurs pour les périphériques centraux</span><span class="sxs-lookup"><span data-stu-id="26c1d-150">Shader support for Core devices</span></span>

<span data-ttu-id="26c1d-151">Les nuanceurs de calcul uniquement, aucun nuanceur de graphiques (vertex, nuanceurs de pixels, etc.) ou toutes les fonctionnalités associées, telles que les cibles de rendu, les chaînes de permutation, l’assembleur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="26c1d-151">Compute shaders only, no graphics shaders (Vertex, Pixel Shaders, etc.) nor any related functionality such as render targets, swap chains, input assembler.</span></span>

### <a name="arithmetic-precision"></a><span data-ttu-id="26c1d-152">Précision arithmétique</span><span class="sxs-lookup"><span data-stu-id="26c1d-152">Arithmetic precision</span></span>

<span data-ttu-id="26c1d-153">Les périphériques centraux n’ont pas besoin de prendre en charge les dénormes pour les opérations à virgule flottante 16 bits.</span><span class="sxs-lookup"><span data-stu-id="26c1d-153">Core devices do not have to support denorms for 16 bit floating point operations.</span></span>

## <a name="supported-apis-for-core-devices"></a><span data-ttu-id="26c1d-154">API prises en charge pour les périphériques centraux</span><span class="sxs-lookup"><span data-stu-id="26c1d-154">Supported APIs for Core devices</span></span>

<span data-ttu-id="26c1d-155">La liste ci-dessous représente le sous-ensemble pris en charge de l’interface de programmation d’applications complète (les API qui ne sont *pas* prises en charge dans le niveau de fonctionnalité Core 1,0 ne sont *pas* répertoriées).</span><span class="sxs-lookup"><span data-stu-id="26c1d-155">The list below represents the supported subset of the full application programming interface (APIs that are *not* supported in Core 1.0 Feature Level are *not* listed).</span></span>

### <a name="id3d12device-methods"></a><span data-ttu-id="26c1d-156">Méthodes ID3D12Device</span><span class="sxs-lookup"><span data-stu-id="26c1d-156">ID3D12Device methods</span></span>

* [<span data-ttu-id="26c1d-157">ID3D12Device::CheckFeatureSupport</span><span class="sxs-lookup"><span data-stu-id="26c1d-157">ID3D12Device::CheckFeatureSupport</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [<span data-ttu-id="26c1d-158">ID3D12Device::CopyDescriptors</span><span class="sxs-lookup"><span data-stu-id="26c1d-158">ID3D12Device::CopyDescriptors</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [<span data-ttu-id="26c1d-159">ID3D12Device::CopyDescriptorsSimple</span><span class="sxs-lookup"><span data-stu-id="26c1d-159">ID3D12Device::CopyDescriptorsSimple</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [<span data-ttu-id="26c1d-160">ID3D12Device::CreateCommandAllocator</span><span class="sxs-lookup"><span data-stu-id="26c1d-160">ID3D12Device::CreateCommandAllocator</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [<span data-ttu-id="26c1d-161">ID3D12Device::CreateCommandList</span><span class="sxs-lookup"><span data-stu-id="26c1d-161">ID3D12Device::CreateCommandList</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [<span data-ttu-id="26c1d-162">ID3D12Device::CreateCommandQueue</span><span class="sxs-lookup"><span data-stu-id="26c1d-162">ID3D12Device::CreateCommandQueue</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [<span data-ttu-id="26c1d-163">ID3D12Device::CreateCommandSignature</span><span class="sxs-lookup"><span data-stu-id="26c1d-163">ID3D12Device::CreateCommandSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [<span data-ttu-id="26c1d-164">ID3D12Device::CreateCommittedResource</span><span class="sxs-lookup"><span data-stu-id="26c1d-164">ID3D12Device::CreateCommittedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [<span data-ttu-id="26c1d-165">ID3D12Device::CreateComputePipelineState</span><span class="sxs-lookup"><span data-stu-id="26c1d-165">ID3D12Device::CreateComputePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [<span data-ttu-id="26c1d-166">ID3D12Device::CreateConstantBufferView</span><span class="sxs-lookup"><span data-stu-id="26c1d-166">ID3D12Device::CreateConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [<span data-ttu-id="26c1d-167">ID3D12Device::CreateDescriptorHeap</span><span class="sxs-lookup"><span data-stu-id="26c1d-167">ID3D12Device::CreateDescriptorHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [<span data-ttu-id="26c1d-168">ID3D12Device::CreateFence</span><span class="sxs-lookup"><span data-stu-id="26c1d-168">ID3D12Device::CreateFence</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [<span data-ttu-id="26c1d-169">ID3D12Device :: CreateHeap</span><span class="sxs-lookup"><span data-stu-id="26c1d-169">ID3D12Device::CreateHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [<span data-ttu-id="26c1d-170">ID3D12Device::CreatePlacedResource</span><span class="sxs-lookup"><span data-stu-id="26c1d-170">ID3D12Device::CreatePlacedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [<span data-ttu-id="26c1d-171">ID3D12Device::CreateQueryHeap</span><span class="sxs-lookup"><span data-stu-id="26c1d-171">ID3D12Device::CreateQueryHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [<span data-ttu-id="26c1d-172">ID3D12Device::CreateRootSignature</span><span class="sxs-lookup"><span data-stu-id="26c1d-172">ID3D12Device::CreateRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [<span data-ttu-id="26c1d-173">ID3D12Device::CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="26c1d-173">ID3D12Device::CreateShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [<span data-ttu-id="26c1d-174">ID3D12Device::CreateSharedHandle</span><span class="sxs-lookup"><span data-stu-id="26c1d-174">ID3D12Device::CreateSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [<span data-ttu-id="26c1d-175">ID3D12Device::CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="26c1d-175">ID3D12Device::CreateUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [<span data-ttu-id="26c1d-176">ID3D12Device :: expulsion</span><span class="sxs-lookup"><span data-stu-id="26c1d-176">ID3D12Device::Evict</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [<span data-ttu-id="26c1d-177">ID3D12Device::GetAdapterLuid</span><span class="sxs-lookup"><span data-stu-id="26c1d-177">ID3D12Device::GetAdapterLuid</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [<span data-ttu-id="26c1d-178">ID3D12Device :: GetCopyableFootprints</span><span class="sxs-lookup"><span data-stu-id="26c1d-178">ID3D12Device::GetCopyableFootprints</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [<span data-ttu-id="26c1d-179">ID3D12Device::GetCustomHeapProperties</span><span class="sxs-lookup"><span data-stu-id="26c1d-179">ID3D12Device::GetCustomHeapProperties</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [<span data-ttu-id="26c1d-180">ID3D12Device::GetDescriptorHandleIncrementSize</span><span class="sxs-lookup"><span data-stu-id="26c1d-180">ID3D12Device::GetDescriptorHandleIncrementSize</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [<span data-ttu-id="26c1d-181">ID3D12Device::GetDeviceRemovedReason</span><span class="sxs-lookup"><span data-stu-id="26c1d-181">ID3D12Device::GetDeviceRemovedReason</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [<span data-ttu-id="26c1d-182">ID3D12Device::GetNodeCount</span><span class="sxs-lookup"><span data-stu-id="26c1d-182">ID3D12Device::GetNodeCount</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [<span data-ttu-id="26c1d-183">ID3D12Device::GetResourceAllocationInfo</span><span class="sxs-lookup"><span data-stu-id="26c1d-183">ID3D12Device::GetResourceAllocationInfo</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [<span data-ttu-id="26c1d-184">ID3D12Device::MakeResident</span><span class="sxs-lookup"><span data-stu-id="26c1d-184">ID3D12Device::MakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [<span data-ttu-id="26c1d-185">ID3D12Device::OpenSharedHandle</span><span class="sxs-lookup"><span data-stu-id="26c1d-185">ID3D12Device::OpenSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [<span data-ttu-id="26c1d-186">ID3D12Device::OpenSharedHandleByName</span><span class="sxs-lookup"><span data-stu-id="26c1d-186">ID3D12Device::OpenSharedHandleByName</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [<span data-ttu-id="26c1d-187">ID3D12Device::SetStablePowerState</span><span class="sxs-lookup"><span data-stu-id="26c1d-187">ID3D12Device::SetStablePowerState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a><span data-ttu-id="26c1d-188">Méthodes ID3D12Device1</span><span class="sxs-lookup"><span data-stu-id="26c1d-188">ID3D12Device1 methods</span></span>

* [<span data-ttu-id="26c1d-189">ID3D12Device1::CreatePipelineLibrary</span><span class="sxs-lookup"><span data-stu-id="26c1d-189">ID3D12Device1::CreatePipelineLibrary</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [<span data-ttu-id="26c1d-190">ID3D12Device1::SetEventOnMultipleFenceCompletion</span><span class="sxs-lookup"><span data-stu-id="26c1d-190">ID3D12Device1::SetEventOnMultipleFenceCompletion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [<span data-ttu-id="26c1d-191">ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority</span><span class="sxs-lookup"><span data-stu-id="26c1d-191">ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a><span data-ttu-id="26c1d-192">Méthodes ID3D12Device2</span><span class="sxs-lookup"><span data-stu-id="26c1d-192">ID3D12Device2 methods</span></span>

* [<span data-ttu-id="26c1d-193">ID3D12Device2::CreatePipelineState</span><span class="sxs-lookup"><span data-stu-id="26c1d-193">ID3D12Device2::CreatePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a><span data-ttu-id="26c1d-194">Méthodes ID3D12Device3</span><span class="sxs-lookup"><span data-stu-id="26c1d-194">ID3D12Device3 methods</span></span>

* [<span data-ttu-id="26c1d-195">ID3D12Device3::OpenExistingHeapFromAddress</span><span class="sxs-lookup"><span data-stu-id="26c1d-195">ID3D12Device3::OpenExistingHeapFromAddress</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* <span data-ttu-id="26c1d-196">[ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span><span class="sxs-lookup"><span data-stu-id="26c1d-196">[ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span></span>
* [<span data-ttu-id="26c1d-197">ID3D12Device3::EnqueueMakeResident</span><span class="sxs-lookup"><span data-stu-id="26c1d-197">ID3D12Device3::EnqueueMakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a><span data-ttu-id="26c1d-198">Méthodes ID3D12Device4</span><span class="sxs-lookup"><span data-stu-id="26c1d-198">ID3D12Device4 methods</span></span>

* [<span data-ttu-id="26c1d-199">ID3D12Device4::GetResourceAllocationInfo1</span><span class="sxs-lookup"><span data-stu-id="26c1d-199">ID3D12Device4::GetResourceAllocationInfo1</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a><span data-ttu-id="26c1d-200">Méthodes ID3D12Device5</span><span class="sxs-lookup"><span data-stu-id="26c1d-200">ID3D12Device5 methods</span></span>

* [<span data-ttu-id="26c1d-201">ID3D12Device5::CreateMetaCommand</span><span class="sxs-lookup"><span data-stu-id="26c1d-201">ID3D12Device5::CreateMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [<span data-ttu-id="26c1d-202">ID3D12Device5::CreateStateObject</span><span class="sxs-lookup"><span data-stu-id="26c1d-202">ID3D12Device5::CreateStateObject</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [<span data-ttu-id="26c1d-203">ID3D12Device5::EnumerateMetaCommandParameters</span><span class="sxs-lookup"><span data-stu-id="26c1d-203">ID3D12Device5::EnumerateMetaCommandParameters</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [<span data-ttu-id="26c1d-204">ID3D12Device5::EnumerateMetaCommands</span><span class="sxs-lookup"><span data-stu-id="26c1d-204">ID3D12Device5::EnumerateMetaCommands</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [<span data-ttu-id="26c1d-205">ID3D12Device5::RemoveDevice</span><span class="sxs-lookup"><span data-stu-id="26c1d-205">ID3D12Device5::RemoveDevice</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a><span data-ttu-id="26c1d-206">Méthodes ID3D12CommandQueue</span><span class="sxs-lookup"><span data-stu-id="26c1d-206">ID3D12CommandQueue methods</span></span>

* [<span data-ttu-id="26c1d-207">ID3D12CommandQueue::BeginEvent</span><span class="sxs-lookup"><span data-stu-id="26c1d-207">ID3D12CommandQueue::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [<span data-ttu-id="26c1d-208">ID3D12CommandQueue::EndEvent</span><span class="sxs-lookup"><span data-stu-id="26c1d-208">ID3D12CommandQueue::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [<span data-ttu-id="26c1d-209">ID3D12CommandQueue::ExecuteCommandLists</span><span class="sxs-lookup"><span data-stu-id="26c1d-209">ID3D12CommandQueue::ExecuteCommandLists</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [<span data-ttu-id="26c1d-210">ID3D12CommandQueue::GetClockCalibration</span><span class="sxs-lookup"><span data-stu-id="26c1d-210">ID3D12CommandQueue::GetClockCalibration</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [<span data-ttu-id="26c1d-211">ID3D12CommandQueue::GetDesc</span><span class="sxs-lookup"><span data-stu-id="26c1d-211">ID3D12CommandQueue::GetDesc</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [<span data-ttu-id="26c1d-212">ID3D12CommandQueue::GetTimestampFrequency</span><span class="sxs-lookup"><span data-stu-id="26c1d-212">ID3D12CommandQueue::GetTimestampFrequency</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [<span data-ttu-id="26c1d-213">ID3D12CommandQueue :: SetMarker</span><span class="sxs-lookup"><span data-stu-id="26c1d-213">ID3D12CommandQueue::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [<span data-ttu-id="26c1d-214">ID3D12CommandQueue :: signal</span><span class="sxs-lookup"><span data-stu-id="26c1d-214">ID3D12CommandQueue::Signal</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [<span data-ttu-id="26c1d-215">ID3D12CommandQueue :: wait</span><span class="sxs-lookup"><span data-stu-id="26c1d-215">ID3D12CommandQueue::Wait</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a><span data-ttu-id="26c1d-216">Méthodes ID3D12CommandList</span><span class="sxs-lookup"><span data-stu-id="26c1d-216">ID3D12CommandList methods</span></span>

* [<span data-ttu-id="26c1d-217">ID3D12CommandList :: GetType</span><span class="sxs-lookup"><span data-stu-id="26c1d-217">ID3D12CommandList::GetType</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a><span data-ttu-id="26c1d-218">Méthodes ID3D12GraphicsCommandList</span><span class="sxs-lookup"><span data-stu-id="26c1d-218">ID3D12GraphicsCommandList methods</span></span>

* [<span data-ttu-id="26c1d-219">ID3D12GraphicsCommandList::BeginEvent</span><span class="sxs-lookup"><span data-stu-id="26c1d-219">ID3D12GraphicsCommandList::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [<span data-ttu-id="26c1d-220">ID3D12GraphicsCommandList::BeginQuery</span><span class="sxs-lookup"><span data-stu-id="26c1d-220">ID3D12GraphicsCommandList::BeginQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [<span data-ttu-id="26c1d-221">ID3D12GraphicsCommandList::ClearState</span><span class="sxs-lookup"><span data-stu-id="26c1d-221">ID3D12GraphicsCommandList::ClearState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [<span data-ttu-id="26c1d-222">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="26c1d-222">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [<span data-ttu-id="26c1d-223">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="26c1d-223">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [<span data-ttu-id="26c1d-224">ID3D12GraphicsCommandList :: Close</span><span class="sxs-lookup"><span data-stu-id="26c1d-224">ID3D12GraphicsCommandList::Close</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [<span data-ttu-id="26c1d-225">ID3D12GraphicsCommandList::CopyBufferRegion</span><span class="sxs-lookup"><span data-stu-id="26c1d-225">ID3D12GraphicsCommandList::CopyBufferRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [<span data-ttu-id="26c1d-226">ID3D12GraphicsCommandList::CopyResource</span><span class="sxs-lookup"><span data-stu-id="26c1d-226">ID3D12GraphicsCommandList::CopyResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [<span data-ttu-id="26c1d-227">ID3D12GraphicsCommandList::CopyTextureRegion</span><span class="sxs-lookup"><span data-stu-id="26c1d-227">ID3D12GraphicsCommandList::CopyTextureRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [<span data-ttu-id="26c1d-228">ID3D12GraphicsCommandList ::D ispatch</span><span class="sxs-lookup"><span data-stu-id="26c1d-228">ID3D12GraphicsCommandList::Dispatch</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [<span data-ttu-id="26c1d-229">ID3D12GraphicsCommandList::EndEvent</span><span class="sxs-lookup"><span data-stu-id="26c1d-229">ID3D12GraphicsCommandList::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [<span data-ttu-id="26c1d-230">ID3D12GraphicsCommandList::EndQuery</span><span class="sxs-lookup"><span data-stu-id="26c1d-230">ID3D12GraphicsCommandList::EndQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [<span data-ttu-id="26c1d-231">ID3D12GraphicsCommandList :: Reset</span><span class="sxs-lookup"><span data-stu-id="26c1d-231">ID3D12GraphicsCommandList::Reset</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [<span data-ttu-id="26c1d-232">ID3D12GraphicsCommandList::ResolveQueryData</span><span class="sxs-lookup"><span data-stu-id="26c1d-232">ID3D12GraphicsCommandList::ResolveQueryData</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [<span data-ttu-id="26c1d-233">ID3D12GraphicsCommandList::ResourceBarrier</span><span class="sxs-lookup"><span data-stu-id="26c1d-233">ID3D12GraphicsCommandList::ResourceBarrier</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [<span data-ttu-id="26c1d-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span><span class="sxs-lookup"><span data-stu-id="26c1d-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [<span data-ttu-id="26c1d-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span><span class="sxs-lookup"><span data-stu-id="26c1d-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [<span data-ttu-id="26c1d-236">ID3D12GraphicsCommandList::SetComputeRootConstantBufferView</span><span class="sxs-lookup"><span data-stu-id="26c1d-236">ID3D12GraphicsCommandList::SetComputeRootConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [<span data-ttu-id="26c1d-237">ID3D12GraphicsCommandList::SetComputeRootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="26c1d-237">ID3D12GraphicsCommandList::SetComputeRootDescriptorTable</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [<span data-ttu-id="26c1d-238">ID3D12GraphicsCommandList::SetComputeRootShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="26c1d-238">ID3D12GraphicsCommandList::SetComputeRootShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [<span data-ttu-id="26c1d-239">ID3D12GraphicsCommandList::SetComputeRootSignature</span><span class="sxs-lookup"><span data-stu-id="26c1d-239">ID3D12GraphicsCommandList::SetComputeRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [<span data-ttu-id="26c1d-240">ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="26c1d-240">ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [<span data-ttu-id="26c1d-241">ID3D12GraphicsCommandList::SetDescriptorHeaps</span><span class="sxs-lookup"><span data-stu-id="26c1d-241">ID3D12GraphicsCommandList::SetDescriptorHeaps</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [<span data-ttu-id="26c1d-242">ID3D12GraphicsCommandList :: SetMarker</span><span class="sxs-lookup"><span data-stu-id="26c1d-242">ID3D12GraphicsCommandList::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [<span data-ttu-id="26c1d-243">ID3D12GraphicsCommandList::SetPipelineState</span><span class="sxs-lookup"><span data-stu-id="26c1d-243">ID3D12GraphicsCommandList::SetPipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [<span data-ttu-id="26c1d-244">ID3D12GraphicsCommandList::SetPredication</span><span class="sxs-lookup"><span data-stu-id="26c1d-244">ID3D12GraphicsCommandList::SetPredication</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a><span data-ttu-id="26c1d-245">Méthodes ID3D12GraphicsCommandList1</span><span class="sxs-lookup"><span data-stu-id="26c1d-245">ID3D12GraphicsCommandList1 methods</span></span>

* [<span data-ttu-id="26c1d-246">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT</span><span class="sxs-lookup"><span data-stu-id="26c1d-246">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [<span data-ttu-id="26c1d-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span><span class="sxs-lookup"><span data-stu-id="26c1d-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a><span data-ttu-id="26c1d-248">Méthodes ID3D12GraphicsCommandList2</span><span class="sxs-lookup"><span data-stu-id="26c1d-248">ID3D12GraphicsCommandList2 methods</span></span>

* [<span data-ttu-id="26c1d-249">ID3D12GraphicsCommandList2::WriteBufferImmediate</span><span class="sxs-lookup"><span data-stu-id="26c1d-249">ID3D12GraphicsCommandList2::WriteBufferImmediate</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a><span data-ttu-id="26c1d-250">Méthodes ID3D12GraphicsCommandList4</span><span class="sxs-lookup"><span data-stu-id="26c1d-250">ID3D12GraphicsCommandList4 methods</span></span>

* [<span data-ttu-id="26c1d-251">ID3D12GraphicsCommandList4::ExecuteMetaCommand</span><span class="sxs-lookup"><span data-stu-id="26c1d-251">ID3D12GraphicsCommandList4::ExecuteMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [<span data-ttu-id="26c1d-252">ID3D12GraphicsCommandList4::InitializeMetaCommand</span><span class="sxs-lookup"><span data-stu-id="26c1d-252">ID3D12GraphicsCommandList4::InitializeMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)
