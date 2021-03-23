---
title: Compteurs UAV
description: Vous pouvez utiliser des compteurs non ordonnés-Access-View (UAV) pour associer un compteur Atomic 32 bits à un mode d’accès non ordonné (UAV).
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: 94bc1492e3b984d96c76788430d2e63c0672ca76
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104548529"
---
# <a name="uav-counters"></a>Compteurs UAV
Vous pouvez utiliser des compteurs non ordonnés-Access-View (UAV) pour associer un compteur Atomic 32 bits à un mode d’accès non ordonné (UAV).

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a>Différences entre les compteurs UAV de Direct3D 11 et Direct3D 12
Les applications Direct3D 12 et Direct3D 11 utilisent toutes les deux les mêmes fonctions de nuanceur HLSL (High-Level Shader Language) pour accéder aux compteurs UAV.

-   **IncrementCounter**
-   **DecrementCounter**
-   **Append**
-   **Utiliser**

### <a name="direct3d-12"></a>Direct3D 12
Dans Direct3D 12, les valeurs 32 bits sont allouées par l’application. par conséquent, les valeurs 32 bits peuvent être lues et écrites par le processeur ou le GPU, comme n’importe quelle autre ressource Direct3D 12.

### <a name="direct3d-11"></a>Direct3D 11
En dehors des nuanceurs, avec Direct3D 11, vous devez appeler les méthodes d’API pour accéder aux compteurs (par exemple, [ID3D11DeviceContext :: CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).

## <a name="using-uav-counters"></a>Utilisation des compteurs UAV
Votre application est chargée d’allouer 32 bits de stockage pour les compteurs UAV. Ce stockage peut être alloué dans une ressource différente de celle qui contient les données accessibles via le UAV.

Reportez-vous à [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12 \_ buffer \_ UAV \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) et [**D3D12 \_ buffer \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).

Si *pCounterResource* est spécifié dans l’appel à [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), alors un compteur est associé au UAV. Dans ce cas :

-   *StructureByteStride* doit être supérieur à zéro
-   Le format du format doit être DXGI \_ \_ inconnu
-   L’indicateur brut ne doit pas être défini
-   Les deux ressources doivent être des mémoires tampons
-   *CounterOffsetInBytes* doit être un multiple de 4 octets
-   *CounterOffsetInBytes* doit se trouver dans la plage de la ressource de compteur
-   *pDesc* ne peut pas être null
-   la *présource* ne peut pas être null

Et notez les cas d’utilisation suivants :

-   Si *pCounterResource* n’est pas spécifié, *CounterOffsetInBytes* doit avoir la valeur 0.
-   Si l’indicateur brut est défini, le format doit être DXGI \_ format \_ R32 sans \_ type et la ressource UAV doit être une mémoire tampon.
-   Si *pCounterResource* n’est pas défini, *CounterOffsetInBytes* doit avoir la valeur 0.
-   Si l’indicateur brut n’est pas défini et que *StructureByteStride* = 0, le format doit être un format UAV valide.

Direct3D 12 supprime la distinction entre les UAVs d’ajout et de compteur (bien que la distinction existe toujours dans le bytecode HLSL).

Le runtime principal valide ces restrictions dans [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).

Lors du traçage/Dispatch, la ressource de compteur doit être dans l’état [**D3D12 \_ accès non \_ \_ ordonné \_ à l’État**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)de la ressource. En outre, dans un appel de dessin/distribution unique, il n’est pas valide pour une application d’accéder au même emplacement de mémoire 32 bits via deux compteurs UAV distincts. La couche de débogage génère des erreurs si l’une ou l’autre est détectée.

Il n’existe pas de méthode « SetUnorderedAccessViewCounterValue » ou « CopyStructureCount », car les applications peuvent simplement copier des données vers et à partir de la valeur de compteur directement.

L’indexation dynamique de UAVs avec des compteurs est prise en charge.

Si un nuanceur tente d’accéder au compteur d’un UAV qui n’a pas de compteur associé, la couche de débogage émet un avertissement et une erreur de page GPU se produit et entraîne la suppression de l’appareil des applications.

Les compteurs UAV sont pris en charge dans tous les types de tas (par défaut, upload, readback).

## <a name="related-topics"></a>Rubriques connexes

* [Compteurs et requêtes](counters-and-queries.md)