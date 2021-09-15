---
title: Minutage (Direct3D 12 Graphics)
description: Cette section traite de l’interrogation des horodateurs et de l’étalonnage des compteurs GPU et horodateur de l’UC.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403532"
---
# <a name="timing-direct3d-12-graphics"></a>Minutage (Direct3D 12 Graphics)

Cette section traite de l’interrogation des horodateurs et de l’étalonnage des compteurs GPU et horodateur de l’UC.

## <a name="timestamp-frequency"></a>Fréquence d’horodatage

Votre application peut interroger la fréquence d’horodatage du GPU en fonction de la file d’attente par commande (reportez-vous à la méthode [**ID3D12CommandQueue :: GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) ).

La fréquence retournée est mesurée en Hz (cycles/s). Si la file d’attente de commandes spécifiée ne prend pas en charge les horodateurs (voir le tableau dans la section [requêtes](queries.md) ), cette API échoue (et retourne **E_FAIL**). [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) et [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) prennent toujours en charge les horodateurs. [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) prend éventuellement en charge les horodatages si le membre [**D3D12_FEATURE_DATA_D3D12_OPTIONS3 :: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) a la **valeur true**.

## <a name="timestamp-calibration"></a>Étalonnage de l’horodateur

D3D12 permet aux applications de mettre en corrélation les résultats obtenus à partir des requêtes d’horodatage avec les résultats obtenus lors de l’appel de `QueryPerformanceCounter` . Cette option est activée par l’appel de [**ID3D12CommandQueue :: GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).

[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) échantillonne le compteur d’horodatage GPU pour une file d’attente de commandes donnée et échantillonne le compteur UC `QueryPerformanceCounter` à presque en même temps. Là encore, cette API échoue (en renvoyant E \_ Fail) si la file d’attente de commandes spécifiée ne prend pas en charge les horodateurs (voir le tableau dans la rubrique [requêtes](queries.md) ).

Notez que les compteurs du GPU et de l’horodateur de l’UC ne sont pas nécessairement directement liés à la fréquence d’horloge de ces processeurs, mais qu’ils fonctionnent à la place des graduations d’horodatage.

## <a name="timestamp-queries"></a>Requêtes d’horodatage

Vous pouvez obtenir des horodateurs dans le cadre d’une liste de commandes (au lieu d’un appel côté processeur sur une file d’attente de commandes) via des requêtes d’horodatage. (Pour plus d’informations sur les requêtes, consultez [requêtes](queries.md) en général). 

Toutes les requêtes d’horodatage utilisent le type [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) pour la requête réelle. Toutefois, en raison des limitations matérielles, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) et [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) utiliser un [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) différent de celui utilisé par [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) .

Les files d’attente de calcul et direct utilisent [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Les files d’attente de copie utilisent [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Les requêtes de file d’attente de copie sont prises en charge uniquement si le membre [**D3D12_FEATURE_DATA_D3D12_OPTIONS3 :: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) a la **valeur true**.

Les requêtes d’horodatage, une fois résolues via [**ID3D12GraphicsCommandList :: ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), sont des **uint64s** qui représentent des graduations, telles qu’elles sont retournées par [**ID3D12CommandQueue :: GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)et, par conséquent, elles doivent être divisées par la fréquence de la file d’attente pour obtenir la longueur en secondes.

> [!IMPORTANT]
> Pour plus de précision, utilisez l’arithmétique à virgule flottante lors du calcul des intervalles de seconde ou de milliseconde des horodateurs. Par exemple, utilisez `queriedTicks / (double)Frequency` au lieu de `queriedTicks / Frequency`.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Compteurs et requêtes](counters-and-queries.md)
</dt> <dt>

[**ID3D12Device::SetStablePowerState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[**ID3D12Object :: SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[Mesure des performances](performance-measurement.md)
</dt> </dl>
