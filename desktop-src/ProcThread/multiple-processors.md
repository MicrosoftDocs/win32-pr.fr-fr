---
description: 'Les ordinateurs avec plusieurs processeurs sont généralement conçus pour l’une des deux architectures : l’accès mémoire non uniforme (NUMA) ou le multitraitement symétrique (SMP).'
ms.assetid: 3c9186c8-a54d-4536-8237-bfff78cc7d11
title: Plusieurs processeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0093404a0df653a153823915f1ac72b5e41d50c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519109"
---
# <a name="multiple-processors"></a>Plusieurs processeurs

Les ordinateurs avec plusieurs processeurs sont généralement conçus pour l’une des deux architectures : l’accès mémoire non uniforme (NUMA) ou le multitraitement symétrique (SMP).

Dans un ordinateur NUMA, chaque processeur est plus proche de certaines parties de la mémoire que d’autres, ce qui rend l’accès à la mémoire plus rapide pour certaines parties de la mémoire que d’autres parties. Dans le modèle NUMA, le système tente de planifier les threads sur les processeurs qui sont proches de la mémoire utilisée. Pour plus d’informations sur NUMA, consultez [prise en charge de Numa](numa-support.md).

Dans un ordinateur SMP, deux ou plusieurs processeurs ou cœurs identiques se connectent à une seule mémoire principale partagée. Dans le modèle SMP, tout thread peut être attribué à n’importe quel processeur. Par conséquent, la planification de threads sur un ordinateur SMP est similaire à la planification de threads sur un ordinateur avec un seul processeur. Toutefois, le planificateur a un pool de processeurs, afin qu’il puisse planifier l’exécution simultanée de threads. La planification est toujours déterminée par la priorité des threads, mais elle peut être influencée par la définition de l’affinité de thread et du processeur idéal pour les threads, comme indiqué dans cette rubrique.

## <a name="thread-affinity"></a>Affinité de thread

L' *affinité de thread* force l’exécution d’un thread sur un sous-ensemble spécifique de processeurs. La définition de l’affinité de thread doit généralement être évitée, car elle peut interférer avec la capacité du planificateur à planifier efficacement les threads entre les processeurs. Cela peut réduire les gains de performances générés par le traitement parallèle. Une utilisation appropriée de l’affinité de thread consiste à tester chaque processeur.

Le système représente l’affinité avec un masque de masque appelé masque d’affinité du processeur. Le masque d’affinité correspond à la taille du nombre maximal de processeurs dans le système, avec les bits définis pour identifier un sous-ensemble de processeurs. Initialement, le système détermine le sous-ensemble de processeurs dans le masque.

Vous pouvez obtenir l’affinité de thread actuelle pour tous les threads du processus en appelant la fonction [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) . Utilisez la fonction [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) pour spécifier l’affinité de thread pour tous les threads du processus. Pour définir l’affinité de thread pour un seul thread, utilisez la fonction [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) . L’affinité de thread doit être un sous-ensemble de l’affinité de processus.

Sur les systèmes dotés de plus de 64 processeurs, le masque d’affinité représente initialement des processeurs dans un seul groupe de processeurs. Toutefois, l’affinité de thread peut être définie sur un processeur d’un autre groupe, ce qui modifie le masque d’affinité du processus. Pour plus d’informations, consultez [groupes de processeurs](processor-groups.md).

## <a name="thread-ideal-processor"></a>Processeur idéal pour les threads

Lorsque vous spécifiez un *processeur idéal pour les threads*, le planificateur exécute le thread sur le processeur spécifié lorsque cela est possible. Utilisez la fonction [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor) pour spécifier un processeur préféré pour un thread. Cela ne garantit pas que le processeur idéal sera choisi, mais qu’il fournit un conseil utile au planificateur. Sur les systèmes dotés de plus de 64 processeurs, vous pouvez utiliser la fonction [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex) pour spécifier un processeur préféré dans un groupe de processeurs spécifique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge de NUMA](numa-support.md)
</dt> <dt>

[Groupes de processeurs](processor-groups.md)
</dt> </dl>

 

 
