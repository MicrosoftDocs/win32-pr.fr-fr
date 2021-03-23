---
title: Barrières UAV et barrières de l’état des ressources dans DirectML
description: Décrit les avantages de l’exactitude des barrières et comment vous pouvez les utiliser dans DirectML.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 9bfc93d4fb28cff5d7d196287c6573e3e494d1d5
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548543"
---
# <a name="uav-barriers-and-resource-state-barriers-in-directml"></a>Barrières UAV et barrières de l’état des ressources dans DirectML

## <a name="unordered-access-view-uav-barrier-requirements"></a>Exigences en matière de barrière de vue d’accès non ordonné (UAV)

### <a name="uav-barriers-in-direct3d-12"></a>Obstacles UAV dans Direct3D 12

Dans Direct3D 12, les distributions de nuanceur de calcul adjacentes dans la même liste de commandes sont autorisées à s’exécuter en parallèle sur le GPU, sauf s’ils sont synchronisés avec un cloisonnement UAV (non ordonnéed Access View) intermédiaire. Cela peut améliorer les performances en renforçant l’utilisation du matériel GPU. Toutefois, par défaut, sans l’utilisation d’un cloisonnement UAV, l’exécution parallèle de deux distributions adjacentes peut provoquer une condition de concurrence s’il existe une dépendance de données entre les deux distributions ; ou si les deux distributions effectuent des écritures UAV dans les mêmes régions de mémoire.

Une barrière UAV force tous les distributions précédemment envoyées à terminer l’exécution de l’opération sur le GPU avant que les distributions suivantes puissent commencer. Les barrières UAV sont utilisées pour la synchronisation entre les distributions sur la même liste de commandes afin d’éviter les concurrences de données. Vous pouvez émettre un cloisonnement UAV à l’aide de la [méthode **ID3D12GraphicsCommandList :: ResourceBarrier**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).

### <a name="uav-barriers-in-directml"></a>Barrières UAV dans DirectML

Dans DirectML, les opérateurs sont distribués d’une manière similaire à la façon dont les nuanceurs de calcul sont distribués dans Direct3D 12. Autrement dit, les distributions adjacentes des opérateurs sont autorisées à s’exécuter en parallèle sur le GPU, sauf s’il existe une barrière UAV entre eux. Un modèle de Machine Learning classique contient des dépendances de données entre ses opérateurs. par exemple, la sortie d’un opérateur alimente l’entrée d’un autre. Il est donc important d’utiliser des barrières UAV pour synchroniser correctement les distributions.

DirectML garantit qu’il lira uniquement les dizaines d’entrées (et n’écrit jamais). Il garantit également qu’il ne fabriquera jamais d’écritures dans un tenseur de sortie en dehors de la plage du membre [**DML_BUFFER_TENSOR_DESC :: TotalTensorSizeInBytes**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) de tenseur. Cela signifie que les dépendances de données entre les opérateurs dans DirectML peuvent être motivées en examinant uniquement les liaisons d’entrée et de sortie d’un opérateur.

Par exemple, ces garanties vous permettent de distribuer deux opérateurs qui lient la même région d’une ressource en tant qu’entrée, sans avoir à émettre une barrière UAV intermédiaire. Cela est toujours sûr, car DirectML n’écrit jamais dans des dizaines d’entrées. Autre exemple : il est toujours possible de lier les dizaines de sortie de deux distributions d’opérateur simultanés à la même ressource Direct3D 12 (tant que leurs dizaines ne se chevauchent pas), car DirectML n’écrit jamais en dehors des limites d’un tenseur (comme défini par le DML_BUFFER_TENSOR_DESC de tenseur **:: TotalTensorSizeInBytes**).

Comme les barrières UAV sont une forme de synchronisation, l’utilisation inutile de barrières UAV peut avoir un impact négatif sur les performances. Par conséquent, il est préférable d’utiliser le nombre minimal de barrières UAV nécessaires pour synchroniser correctement les distributions dans une liste de commandes.

### <a name="example-1"></a>Exemple 1

Dans l’exemple suivant, la sortie d’un opérateur de convolution est alimentée dans une activation ReLU, suivie d’une normalisation par lots.

```console
    CONVOLUTION (conv1)
         |
  ACTIVATION_RELU (relu1)
         |
BATCH_NORMALIZATION (batch1)
```

Étant donné qu’il existe une dépendance de données entre les trois opérateurs, vous aurez besoin d’une barrière UAV entre chaque Dispatch successif (voir [**IDMLCommandRecorder :: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)).

1. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`
2. `d3d12CommandList->ResourceBarrier(`**Barrière UAV**`)`
3. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**relu1**`)`
4. `d3d12CommandList->ResourceBarrier(`**Barrière UAV**`)`
5. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**batch1**`)`

### <a name="example-2"></a>Exemple 2

```console
     MAX_POOLING (pool1)
        /    \
CONVOLUTION  CONVOLUTION
  (conv1)      (conv2)
        \    /
         JOIN (join1)
```

Ici, la sortie du regroupement est alimentée en deux convolutions, dont les sorties sont ensuite concaténées à l’aide de l’opérateur de jointure. Une dépendance de données existe entre et les deux et, ainsi qu' `pool1` `conv1` `conv2` entre `conv1` et `conv2` et `join1` . Voici une méthode valide pour exécuter ce graphique.

1. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**pool1**`)`
2. `d3d12CommandList->ResourceBarrier(`**Barrière UAV**`)`
3. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`
4. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**Conv2**`)`
5. `d3d12CommandList->ResourceBarrier(`**Barrière UAV**`)`
6. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**Join1**`)`

Dans ce cas, `conv1` et `conv2` sont en mesure de s’exécuter simultanément sur le GPU, ce qui peut améliorer les performances.

## <a name="resource-barrier-state-requirements"></a>Exigences relatives à l’état de la barrière des ressources

En tant qu’appelant, il vous incombe de vous assurer que toutes les ressources Direct3D 12 se trouvent dans l’état de barrière de ressources approprié avant d’exécuter des distributions DirectML sur le GPU. DirectML n’effectue pas de barrières de transition en votre nom.

Avant l’exécution de [**IDMLCommandRecorder :: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) sur le GPU, vous devez faire passer toutes les ressources liées à l’état **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** ou à un État pouvant être promu implicitement en **D3D12_RESOURCE_STATE_UNORDERED_ACCESS**, tel que **D3D12_RESOURCE_STATE_COMMON**. Une fois cet appel terminé, les ressources restent à l’état **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** . Pour plus d’informations, consultez [liaison dans DirectML](dml-binding.md).

## <a name="see-also"></a>Voir aussi

* [Utilisation de barrières de ressources pour synchroniser les États des ressources dans Direct3D 12](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
* [Liaison dans DirectML](dml-binding.md)
