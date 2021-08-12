---
title: Niveau de fonctionnalité Direct3D 12 Core 1.0
description: Le niveau de fonctionnalité principal 1,0 est un sous-ensemble de l’ensemble de fonctionnalités Direct3D 12 complet.
ms.topic: article
ms.date: 11/05/2019
ms.openlocfilehash: 93eab39509074114bf2032cfb1cdea3e4e767dae9786241a34f970ca5cd51703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530719"
---
# <a name="the-direct3d-12-core-10-feature-level"></a>Niveau de fonctionnalité Direct3D 12 Core 1.0

Le niveau de fonctionnalité principal 1,0 est un sous-ensemble de l’ensemble de fonctionnalités Direct3D 12 complet. Le niveau de fonctionnalité principal 1,0 peut être exposé par une catégorie d’appareils appelés *appareils de calcul uniquement*. Le modèle de pilote global pour les appareils de calcul uniquement est le modèle de pilote de calcul Microsoft (MCDM). MCDM est un homologue mis à l’échelle de Windows modèle de pilote de périphérique (WDDM), qui a une plus grande portée.

Un appareil qui prend *uniquement* en charge les fonctionnalités au sein d’un niveau de fonctionnalité principal est appelé *appareil principal*.

> [!NOTE]
> L’appareil *de calcul uniquement*, l’appareil *MCDM*, l' *appareil de niveau de fonctionnalité principal* et l' *appareil de base* ont tous la même signification. Nous préférerons l' *appareil de base* pour des raisons de simplicité.

## <a name="creating-a-core-device"></a>Création d’un périphérique principal

En général, pour créer un appareil Direct3D 12, vous appelez la fonction [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) et spécifiez un niveau de fonctionnalité minimal.

Si vous spécifiez un niveau de fonctionnalité de 9 à 12, l’appareil retourné est un appareil riche en fonctionnalités, tel qu’un GPU traditionnel (qui prend en charge un sur-ensemble de la fonctionnalité d’un appareil principal). Un appareil principal n’est jamais retourné pour cette plage de niveaux de fonctionnalité.

En revanche, si vous spécifiez un niveau de fonctionnalité principal (par exemple, [**D3D_FEATURE_LEVEL ::D 3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), l’appareil retourné peut être riche en fonctionnalités, ou il peut s’agir d’un appareil de base.

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

Si vous spécifiez un `_CORE` niveau de fonctionnalité, la couche Runtime/Debug vérifie que les fonctionnalités utilisées par votre application sont autorisées par ce `_CORE` niveau de fonctionnalité. Cet ensemble de fonctionnalités est défini plus loin dans cette rubrique.

## <a name="shader-model-for-core-devices"></a>Modèle de nuanceur pour les périphériques centraux

Un périphérique de base prend en charge le modèle de nuanceur 5.0 +.

Le Runtime effectue la conversion des modèles de nuanceur 5. x non DXIL en 6,0 DXIL. Ainsi, le pilote doit uniquement prendre en charge 6. x.

## <a name="resource-management-model-for-core-devices"></a>Modèle de gestion des ressources pour les périphériques de base

- Dimensions de ressources prises en charge : mémoires tampons brutes et structurées uniquement (aucune mémoire tampon typée, texture1d/2D, etc.)
- Aucune prise en charge des ressources réservées (en mosaïque)
- Aucune prise en charge des tas personnalisés
- Aucun de ces indicateurs de tas n’est pris en charge :
  - D3D12_HEAP_FLAG_HARDWARE_PROTECTED
  - D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH
  - D3D12_HEAP_FLAG_ALLOW_DISPLAY
  - D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (Notez que le nuanceur atomiques est obligatoire, cet indicateur est destiné à une autre fonctionnalité, à des atomices d’adaptateurs croisés)

## <a name="resource-binding-model-for-core-devices"></a>Modèle de liaison de ressources pour les périphériques centraux

- Prise en charge du niveau de liaison de ressources 1 uniquement
- Exceptions :
  - Pas de prise en charge des échantillonneurs de texture
  - Prise en charge de 64 UAVs comme niveau de fonctionnalité 11.1 + (contrairement à 8 uniquement)
  - Les implémentations n’ont pas besoin d’implémenter la vérification des limites sur les accès du nuanceur aux ressources par le biais de descripteurs, les accès hors limites produisent un comportement indéfini.
    - En tant que sous-ensemble, l’indicateur de plage de descripteurs D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS dans les signatures racines n’est pas pris en charge.
- Les descripteurs UAV/CBV ne peuvent être créés que sur des ressources à partir de tas par défaut (aucun tas upload/readback). Cela oblige votre application à effectuer des copies pour récupérer des données sur le processeur< >GPU.
- Bien qu’il s’agit du niveau de capacité de liaison le plus bas, il existe toujours des fonctionnalités requises, même dans ce niveau qui mérite d’être appelé :
  - Les tas de descripteurs peuvent être mis à jour après l’enregistrement des listes de commandes (voir D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE dans les spécifications de liaison de ressources)
  - Les descripteurs racine sont fondamentalement des pointeurs GPUVA
    - Même s’il n’y a pas de prise en charge de MMU/VA, le SAV de mémoire tampon utilisé dans les descripteurs racine peut être émulé par les implémentations en procédant à une mise à jour corrective des adresses.

### <a name="structured-buffer-restrictions"></a>Restrictions de mémoire tampon structurées

Les mémoires tampons structurées doivent avoir une adresse de base qui est alignée sur 4 octets et STRIDE doit être 2 ou un multiple de 4. Le cas d’une Stride de 2 est destiné aux applications avec des données 16 bits, en particulier en raison de l’absence de prise en charge des mémoires tampons typées dans D3D_FEATURE_LEVEL_1_0_CORE.

La Stride spécifiée dans les descripteurs doit correspondre au Stride spécifié en HLSL.  

## <a name="command-queue-support-for-core-devices"></a>Prise en charge des files d’attente de commandes pour les périphériques principaux

Calculez et copiez les files d’attente uniquement (aucune file d’attente 3D, vidéo, etc.).

## <a name="shader-support-for-core-devices"></a>Prise en charge des nuanceurs pour les périphériques centraux

Les nuanceurs de calcul uniquement, aucun nuanceur de graphiques (vertex, nuanceurs de pixels, etc.) ou toutes les fonctionnalités associées, telles que les cibles de rendu, les chaînes de permutation, l’assembleur d’entrée.

### <a name="arithmetic-precision"></a>Précision arithmétique

Les périphériques centraux n’ont pas besoin de prendre en charge les dénormes pour les opérations à virgule flottante 16 bits.

## <a name="supported-apis-for-core-devices"></a>API prises en charge pour les périphériques centraux

La liste ci-dessous représente le sous-ensemble pris en charge de l’interface de programmation d’applications complète (les API qui ne sont *pas* prises en charge dans le niveau de fonctionnalité Core 1,0 ne sont *pas* répertoriées).

### <a name="id3d12device-methods"></a>Méthodes ID3D12Device

* [ID3D12Device::CheckFeatureSupport](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [ID3D12Device::CopyDescriptors](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [ID3D12Device::CopyDescriptorsSimple](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [ID3D12Device::CreateCommandAllocator](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [ID3D12Device::CreateCommandList](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [ID3D12Device::CreateCommandQueue](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [ID3D12Device::CreateCommandSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [ID3D12Device::CreateCommittedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [ID3D12Device::CreateComputePipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [ID3D12Device::CreateConstantBufferView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [ID3D12Device::CreateDescriptorHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [ID3D12Device::CreateFence](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [ID3D12Device :: CreateHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [ID3D12Device::CreatePlacedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [ID3D12Device::CreateQueryHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [ID3D12Device::CreateRootSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [ID3D12Device::CreateShaderResourceView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [ID3D12Device::CreateSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [ID3D12Device::CreateUnorderedAccessView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [ID3D12Device :: expulsion](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [ID3D12Device::GetAdapterLuid](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [ID3D12Device :: GetCopyableFootprints](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [ID3D12Device::GetCustomHeapProperties](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [ID3D12Device::GetDescriptorHandleIncrementSize](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [ID3D12Device::GetDeviceRemovedReason](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [ID3D12Device::GetNodeCount](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [ID3D12Device::GetResourceAllocationInfo](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [ID3D12Device::MakeResident](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [ID3D12Device::OpenSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [ID3D12Device::OpenSharedHandleByName](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [ID3D12Device::SetStablePowerState](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a>Méthodes ID3D12Device1

* [ID3D12Device1::CreatePipelineLibrary](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [ID3D12Device1::SetEventOnMultipleFenceCompletion](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a>Méthodes ID3D12Device2

* [ID3D12Device2::CreatePipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a>Méthodes ID3D12Device3

* [ID3D12Device3::OpenExistingHeapFromAddress](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* [ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))
* [ID3D12Device3::EnqueueMakeResident](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a>Méthodes ID3D12Device4

* [ID3D12Device4::GetResourceAllocationInfo1](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a>Méthodes ID3D12Device5

* [ID3D12Device5::CreateMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [ID3D12Device5::CreateStateObject](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [ID3D12Device5::EnumerateMetaCommandParameters](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [ID3D12Device5::EnumerateMetaCommands](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [ID3D12Device5::RemoveDevice](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a>Méthodes ID3D12CommandQueue

* [ID3D12CommandQueue::BeginEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [ID3D12CommandQueue::EndEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [ID3D12CommandQueue::ExecuteCommandLists](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [ID3D12CommandQueue::GetClockCalibration](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [ID3D12CommandQueue::GetDesc](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [ID3D12CommandQueue::GetTimestampFrequency](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [ID3D12CommandQueue :: SetMarker](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [ID3D12CommandQueue :: signal](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [ID3D12CommandQueue :: wait](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a>Méthodes ID3D12CommandList

* [ID3D12CommandList :: GetType](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a>Méthodes ID3D12GraphicsCommandList

* [ID3D12GraphicsCommandList::BeginEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [ID3D12GraphicsCommandList::BeginQuery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [ID3D12GraphicsCommandList::ClearState](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [ID3D12GraphicsCommandList :: Close](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [ID3D12GraphicsCommandList::CopyBufferRegion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [ID3D12GraphicsCommandList::CopyResource](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [ID3D12GraphicsCommandList::CopyTextureRegion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [ID3D12GraphicsCommandList ::D ispatch](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [ID3D12GraphicsCommandList::EndEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [ID3D12GraphicsCommandList::EndQuery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [ID3D12GraphicsCommandList :: Reset](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [ID3D12GraphicsCommandList::ResolveQueryData](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [ID3D12GraphicsCommandList::ResourceBarrier](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstant](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstants](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [ID3D12GraphicsCommandList::SetComputeRootConstantBufferView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [ID3D12GraphicsCommandList::SetComputeRootDescriptorTable](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [ID3D12GraphicsCommandList::SetComputeRootShaderResourceView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [ID3D12GraphicsCommandList::SetComputeRootSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [ID3D12GraphicsCommandList::SetDescriptorHeaps](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [ID3D12GraphicsCommandList :: SetMarker](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [ID3D12GraphicsCommandList::SetPipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [ID3D12GraphicsCommandList::SetPredication](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a>Méthodes ID3D12GraphicsCommandList1

* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a>Méthodes ID3D12GraphicsCommandList2

* [ID3D12GraphicsCommandList2::WriteBufferImmediate](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a>Méthodes ID3D12GraphicsCommandList4

* [ID3D12GraphicsCommandList4::ExecuteMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [ID3D12GraphicsCommandList4::InitializeMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)
