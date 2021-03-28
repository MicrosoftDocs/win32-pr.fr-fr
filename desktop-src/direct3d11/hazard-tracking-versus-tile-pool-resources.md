---
title: Suivi des risques ou ressources d’un pool de vignettes
description: Pour les ressources qui ne sont pas en mosaïque, Direct3D peut empêcher certaines conditions de danger pendant le rendu, mais comme le suivi des risques se trouve au niveau de la mosaïque pour les ressources en mosaïque, le suivi des conditions de danger lors du rendu des ressources en mosaïque peut être trop onéreux.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75dcd11cb5e49f165105bd932854e36b37308cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379666"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a>Suivi des risques ou ressources d’un pool de vignettes

Pour les ressources qui ne sont pas en mosaïque, Direct3D peut empêcher certaines conditions de danger pendant le rendu, mais comme le suivi des risques se trouve au niveau de la mosaïque pour les ressources en mosaïque, le suivi des conditions de danger lors du rendu des ressources en mosaïque peut être trop onéreux.

Par exemple, pour les ressources non juxtaposées, le runtime n’autorise pas la liaison d’une sous-ressource donnée en tant qu’entrée (comme ShaderResourceView) et en tant que sortie (comme un RenderTargetView) en même temps. Si un tel cas est rencontré, le runtime dissocie l’entrée. Cette surcharge de suivi dans le runtime est peu coûteuse et est effectuée au niveau de la sous-ressource. L’un des avantages de cette surcharge de suivi est de réduire les risques d’applications par inadvertance en fonction de l’ordre d’exécution des nuanceurs matériels. L’ordre d’exécution du nuanceur de matériel peut varier s’il n’est pas sur une unité de traitement graphique (GPU) donnée, alors que sur différents GPU.

Le suivi de la façon dont les ressources sont liées peut être trop coûteux pour les ressources en mosaïque, car le suivi se fait au niveau de la mosaïque. De nouveaux problèmes se posent, tels que la validation éventuelle des tentatives de rendu sur un RenderTargetView avec une vignette mappée à plusieurs zones de la surface simultanément. S’il s’avère que ce suivi des risques par vignette est trop coûteux pour le runtime, l’idéal serait au moins une option dans la couche de débogage.

Une application doit informer le pilote d’affichage lorsqu’il a émis une opération d’écriture ou de lecture sur une ressource en mosaïque qui fait référence à la mémoire du pool de vignettes qui sera également référencée par des ressources en mosaïque distinctes dans les opérations de lecture ou d’écriture à venir, et que la première opération doit se terminer avant que les opérations suivantes puissent commencer. Pour plus d’informations sur cette condition, consultez la section Notes [**ID3D11DeviceContext2 :: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappages dans un pool de vignettes](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




