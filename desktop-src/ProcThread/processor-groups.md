---
description: les versions 64 bits de Windows 7 et Windows Server 2008 R2 et versions ultérieures de Windows prennent en charge plus de 64 processeurs logiques sur un seul ordinateur. Cette fonctionnalité n’est pas disponible dans les versions 32 bits de Windows.
ms.assetid: c627ac0f-96e8-48b5-9103-4316f487e173
title: Groupes de processeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc5916faf3cf90bce7f8549834fe130f299f782d6b2534969c89d74df454ae9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119418669"
---
# <a name="processor-groups"></a>Groupes de processeurs

les versions 64 bits de Windows 7 et Windows Server 2008 R2 et versions ultérieures de Windows prennent en charge plus de 64 processeurs logiques sur un seul ordinateur. Cette fonctionnalité n’est pas disponible dans les versions 32 bits de Windows.

Les systèmes avec plusieurs processeurs physiques ou systèmes avec des processeurs physiques dotés de plusieurs cœurs fournissent le système d’exploitation avec plusieurs processeurs logiques. Un *processeur logique* est un moteur informatique logique du point de vue du système d’exploitation, de l’application ou du pilote. Un *noyau* est une unité de processeur, qui peut se composer d’un ou de plusieurs processeurs logiques. Un *processeur physique* peut se composer d’un ou de plusieurs cœurs. Un processeur physique est identique à un package de processeur, un socket ou un processeur.

La prise en charge des systèmes dotés de plus de 64 processeurs logiques est basée sur le concept de *groupe de processeurs*, qui est un ensemble statique de 64 processeurs logiques qui est traité comme une entité de planification unique. Les groupes de processeurs sont numérotés à partir de 0. Les systèmes avec moins de 64 processeurs logiques ont toujours un groupe unique, le groupe 0.

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Les groupes de processeurs ne sont pas pris en charge.

Lorsque le système démarre, le système d’exploitation crée des groupes de processeurs et affecte des processeurs logiques aux groupes. Si le système est capable d’ajouter des processeurs à chaud, le système d’exploitation autorise l’espace en groupes pour les processeurs qui peuvent arriver pendant que le système est en cours d’exécution. Le système d’exploitation minimise le nombre de groupes dans un système. Par exemple, un système avec des processeurs logiques 128 a deux groupes de processeurs avec 64 processeurs dans chaque groupe, et non quatre groupes avec des processeurs logiques de 32 dans chaque groupe.

Pour de meilleures performances, le système d’exploitation prend en compte la localité physique lors de l’affectation de processeurs logiques à des groupes. Tous les processeurs logiques d’un cœur, et tous les cœurs d’un processeur physique, sont affectés au même groupe, si possible. Les processeurs physiques qui sont physiquement proches les uns des autres sont affectés au même groupe. Un nœud NUMA est affecté à un seul groupe, sauf si la capacité du nœud dépasse la taille maximale du groupe. Pour plus d’informations, consultez [prise en charge de Numa](numa-support.md).

Sur les systèmes avec 64 ou moins de processeurs, les applications existantes fonctionneront correctement sans modification. Les applications qui n’appellent pas de fonctions qui utilisent des masques d’affinité de processeur ou des numéros de processeur fonctionnent correctement sur tous les systèmes, quel que soit le nombre de processeurs. Pour fonctionner correctement sur les systèmes avec plus de 64 processeurs logiques, les types d’applications suivants peuvent nécessiter des modifications :

-   Les applications qui gèrent, gèrent ou affichent des informations par processeur pour l’ensemble du système doivent être modifiées pour prendre en charge plus de 64 processeurs logiques. un exemple d’une telle application est Windows gestionnaire des tâches, qui affiche la charge de travail de chaque processeur dans le système.
-   Les applications dont les performances sont critiques et qui peuvent évoluer efficacement au-delà de 64 processeurs logiques doivent être modifiées pour s’exécuter sur ces systèmes. Par exemple, les applications de base de données peuvent tirer parti des modifications.
-   Si une application utilise une DLL avec des structures de données par processeur et que la DLL n’a pas été modifiée pour prendre en charge plus de 64 processeurs logiques, tous les threads de l’application qui appellent des fonctions exportées par la DLL doivent être affectés au même groupe.

Par défaut, une application est concédée à un seul groupe, qui doit fournir une capacité de traitement importante pour l’application typique. Le système d’exploitation affecte initialement chaque processus à un seul groupe de manière alternée entre les groupes du système. Un processus commence son exécution affectée à un groupe. Le premier thread d’un processus s’exécute initialement dans le groupe auquel le processus est assigné. Chaque thread nouvellement créé est affecté au même groupe que le thread qui l’a créé.

Une application qui requiert l’utilisation de plusieurs groupes afin qu’elle puisse s’exécuter sur plus de 64 processeurs doit déterminer explicitement où exécuter ses threads et est chargée de définir les affinités du processeur des threads sur les groupes souhaités. L’indicateur d' [ \_ \_ affinité parente hérite](process-creation-flags.md) peut être utilisé pour spécifier un processus parent (qui peut être différent du processus actuel) à partir duquel générer l’affinité pour un nouveau processus. Si le processus s’exécute dans un groupe unique, il peut lire et modifier son affinité à l’aide de [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) et [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) tout en restant dans le même groupe ; Si l’affinité de processus est modifiée, la nouvelle affinité est appliquée à ses threads.

L’affinité d’un thread peut être spécifiée lors de la création à l’aide de l’attribut étendu d’affinité de [](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) [**\_ \_ \_ groupe \_ d’attributs proc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) avec la fonction CreateRemoteThreadEx. Une fois le thread créé, son affinité peut être modifiée en appelant [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) ou [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity). Si un thread est assigné à un autre groupe que le processus, l’affinité du processus est mise à jour pour inclure l’affinité du thread et le processus devient un processus à plusieurs groupes. Des modifications d’affinité supplémentaires doivent être apportées pour les threads individuels. l’affinité d’un processus à plusieurs groupes ne peut pas être modifiée à l’aide de [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask). La fonction [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity) récupère l’ensemble des groupes auxquels un processus et ses threads sont assignés.

Pour spécifier l’affinité pour tous les processus associés à un objet de traitement, utilisez la fonction [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) avec la classe d’informations **JobObjectGroupInformation** ou **JobObjectGroupInformationEx** .

Un processeur logique est identifié par son numéro de groupe et son numéro de processeur relatif au groupe. Cela est représenté par une structure de [**\_ numéro de processeur**](/windows/desktop/api/WinNT/ns-winnt-processor_number) . Les numéros de processeur numériques utilisés par les fonctions héritées sont relatifs au groupe.

Pour plus d’informations sur les modifications apportées à l’architecture du système d’exploitation pour prendre en charge plus de 64 processeurs, consultez le livre blanc [prise en charge des systèmes dotés de plus de 64 processeurs](https://www.microsoft.com/whdc/system/Sysinternals/MoreThan64proc.mspx).

Pour obtenir la liste des nouvelles fonctions et structures qui prennent en charge les groupes de processeurs, consultez [Nouveautés des processus et des threads](what-s-new-in-processes-and-threads.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Plusieurs processeurs](multiple-processors.md)
</dt> <dt>

[Prise en charge de NUMA](numa-support.md)
</dt> </dl>

 

 
