---
description: Le modèle traditionnel pour la prise en charge de multiprocesseur est le multiprocesseur symétrique (SMP). Dans ce modèle, chaque processeur a un accès égal à la mémoire et aux e/s. Au fur et à mesure de l’ajout de processeurs, le bus de processeur devient une limite pour les performances du système.
ms.assetid: a1263968-2b26-45cc-bdd7-6aa354821a5a
title: Prise en charge de NUMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503b64f6f18779fb66a87fc3c45b682fcb97248c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479425"
---
# <a name="numa-support"></a>Prise en charge de NUMA

Le modèle traditionnel pour la prise en charge de multiprocesseur est le multiprocesseur symétrique (SMP). Dans ce modèle, chaque processeur a un accès égal à la mémoire et aux e/s. Au fur et à mesure de l’ajout de processeurs, le bus de processeur devient une limite pour les performances du système.

Les concepteurs de systèmes utilisent l’accès mémoire non uniforme (NUMA) pour augmenter la vitesse du processeur sans augmenter la charge sur le bus du processeur. L’architecture n’est pas uniforme, car chaque processeur est proche de certaines parties de la mémoire et plus éloignées des autres parties de la mémoire. Le processeur obtient rapidement l’accès à la mémoire à proximité, alors qu’il peut prendre plus de temps pour accéder à la mémoire qui est plus éloignée.

Dans un système NUMA, les processeurs sont disposés dans des systèmes plus petits appelés *nœuds*. Chaque nœud possède ses propres processeurs et sa mémoire, et est connecté au système plus grand via un bus d’interconnexion cohérent du cache.

Le système tente d’améliorer les performances en planifiant des threads sur les processeurs qui se trouvent dans le même nœud que la mémoire utilisée. Il tente de satisfaire les demandes d’allocation de mémoire à partir du nœud, mais alloue de la mémoire à partir d’autres nœuds si nécessaire. Il fournit également une API pour rendre la topologie du système disponible pour les applications. Vous pouvez améliorer les performances de vos applications à l’aide des fonctions NUMA pour optimiser la planification et l’utilisation de la mémoire.

Tout d’abord, vous devrez déterminer la disposition des nœuds dans le système. Pour récupérer le nœud portant le numéro le plus élevé dans le système, utilisez la fonction [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber) . Notez qu’il n’est pas garanti que ce nombre soit égal au nombre total de nœuds dans le système. En outre, il n’est pas garanti que les nœuds avec des nombres séquentiels soient proches les uns des autres. Pour récupérer la liste des processeurs sur le système, utilisez la fonction [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) . Vous pouvez déterminer le nœud pour chaque processeur de la liste à l’aide de la fonction [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode) . Pour récupérer une liste de tous les processeurs dans un nœud, vous pouvez également utiliser la fonction [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask) .

Une fois que vous avez déterminé quels processeurs appartiennent aux nœuds, vous pouvez optimiser les performances de votre application. Pour vous assurer que tous les threads de votre processus s’exécutent sur le même nœud, utilisez la fonction [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) avec un masque d’affinité de processus qui spécifie les processeurs dans le même nœud. Cela augmente l’efficacité des applications dont les threads ont besoin d’accéder à la même mémoire. Pour limiter le nombre de threads sur chaque nœud, vous pouvez également utiliser la fonction [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) .

Les applications gourmandes en mémoire doivent optimiser leur utilisation de la mémoire. Pour récupérer la quantité de mémoire disponible pour un nœud, utilisez la fonction [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode) . La fonction [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) permet à l’application de spécifier un nœud préféré pour l’allocation de mémoire. **VirtualAllocExNuma** n’alloue pas de pages physiques, si bien que les pages sont disponibles sur ce nœud ou ailleurs dans le système. Les pages physiques sont allouées à la demande. Si le nœud préféré ne dispose pas de suffisamment de pages, le gestionnaire de mémoire utilise les pages des autres nœuds. Si la mémoire est paginée, le même processus est utilisé lors de son retour.

### <a name="numa-support-on-systems-with-more-than-64-logical-processors"></a>Prise en charge de NUMA sur les systèmes avec plus de 64 processeurs logiques

Sur les systèmes avec plus de 64 processeurs logiques, les nœuds sont attribués aux [groupes de processeurs](processor-groups.md) en fonction de la capacité des nœuds. La capacité d’un nœud est le nombre de processeurs présents lorsque le système démarre avec tous les processeurs logiques supplémentaires qui peuvent être ajoutés pendant que le système est en cours d’exécution.

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Les groupes de processeurs ne sont pas pris en charge.

Chaque nœud doit être entièrement contenu dans un groupe. Si les capacités des nœuds sont relativement faibles, le système affecte plusieurs nœuds au même groupe, en choisissant des nœuds physiquement proches les uns des autres pour obtenir de meilleures performances. Si la capacité d’un nœud dépasse le nombre maximal de processeurs dans un groupe, le système fractionne le nœud en plusieurs nœuds plus petits, chacun étant suffisamment petit pour tenir dans un groupe.

Un nœud NUMA idéal pour un nouveau processus peut être demandé à l’aide de l’attribut étendu de [**\_ \_ \_ \_ nœud préféré de l’attribut proc thread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) lors de la création du processus. À l’instar d’un processeur idéal pour les threads, le nœud idéal est un indicateur du planificateur, qui assigne le nouveau processus au groupe qui contient le nœud demandé, si possible.

Les fonctions NUMA étendues [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex), [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex), [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)et [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex) diffèrent de leurs équivalents non étendus dans le fait que le numéro de nœud est une valeur **UShort** plutôt qu’un **UCHAR**, pour prendre en charge le nombre potentiellement plus élevé de nœuds sur un système avec plus de 64 processeurs logiques. En outre, le processeur spécifié avec ou récupéré par les fonctions étendues comprend le groupe de processeurs. le processeur spécifié avec ou récupéré par les fonctions non étendues est relatif au groupe. Pour plus d’informations, consultez les rubriques de référence sur les fonctions individuelles.

Une application prenant en charge les groupes peut attribuer tous ses threads à un nœud particulier de la même manière que celle décrite précédemment dans cette rubrique, à l’aide des fonctions NUMA étendues correspondantes. L’application utilise [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) pour récupérer la liste de tous les processeurs sur le système. Notez que l’application ne peut pas définir le masque d’affinité du processus à moins que le processus ne soit affecté à un seul groupe et que le nœud prévu se trouve dans ce groupe. En règle générale, l’application doit appeler [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity) pour limiter ses threads au nœud prévu.


### <a name="behavior-starting-with-windows-10-build-20348"></a>comportement commençant par Windows 10 Build 20348 

> [!NOTE]
> à partir de Windows 10 Build 20348, le comportement de cette fonction et d’autres fonctions NUMA a été modifié afin de mieux prendre en charge les systèmes avec des nœuds contenant plus de 64 processeurs.

la création de nœuds « factices » pour prendre en charge un mappage de 1:1 entre les groupes et les nœuds a entraîné des comportements confus où des nombres inattendus de nœuds NUMA sont signalés et, à partir de Windows 10 Build 20348, le système d’exploitation a changé pour permettre l’association de plusieurs groupes à un nœud  

Dans le cadre de ces modifications apportées au système d’exploitation, un certain nombre d’API NUMA ont été modifiées pour prendre en charge la création de rapports pour les plusieurs groupes qui peuvent désormais être associés à un seul nœud NUMA. Les API mises à jour et nouvelles sont étiquetées dans le tableau de la section **API NUMA** ci-dessous.

Étant donné que la suppression du fractionnement des nœuds peut avoir un impact sur les applications existantes, une valeur de Registre est disponible pour vous permettre de revenir au comportement de fractionnement des nœuds hérités. Vous pouvez réactiver le fractionnement des nœuds en créant une **REG_DWORD** valeur nommée « SplitLargeNodes » avec la valeur 1 sous HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\NUMA. Les modifications apportées à ce paramètre requièrent un redémarrage pour prendre effet.

```powershell
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\NUMA" /v SplitLargeNodes /t REG_DWORD /d 1
```

> [!NOTE]
> Les applications mises à jour pour utiliser la nouvelle fonctionnalité de l’API qui signale la véritable topologie NUMA continuent de fonctionner correctement sur les systèmes où le fractionnement de nœuds volumineux a été réactivé avec cette clé de registre.

L’exemple suivant illustre tout d’abord les problèmes potentiels liés aux tables de builds qui mappent les processeurs à des nœuds NUMA à l’aide des API d’affinité héritée, qui ne fournissent plus de couverture complète de tous les processeurs du système, ce qui peut entraîner une table incomplète. Les implications d’une telle incomplète dépendent du contenu de la table. Si la table stocke simplement le numéro de nœud correspondant, il s’agit probablement d’un problème de performances avec des processeurs non couverts conservés dans le cadre du nœud 0. Toutefois, si la table contient des pointeurs vers une structure de contexte par nœud, cela peut entraîner des déréférencements NULL au moment de l’exécution.

L’exemple de code suivant illustre deux solutions de contournement pour le problème. La première consiste à migrer vers les API d’affinité de nœud à plusieurs groupes (en mode utilisateur et en mode noyau). La seconde consiste à utiliser **KeQueryLogicalProcessorRelationship** pour interroger directement le nœud NUMA associé à un numéro de processeur donné.

```cpp

//
// Problematic implementation using KeQueryNodeActiveAffinity.
//

USHORT CurrentNode;
USHORT HighestNodeNumber;
GROUP_AFFINITY NodeAffinity;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    KeQueryNodeActiveAffinity(CurrentNode, &NodeAffinity, NULL);
    while (NodeAffinity.Mask != 0) {

        ProcessorNumber.Group = NodeAffinity.Group;
        BitScanForward(&ProcessorNumber.Number, NodeAffinity.Mask);

        ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

        ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode;]

        NodeAffinity.Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
    }
}

//
// Resolution using KeQueryNodeActiveAffinity2.
//

USHORT CurrentIndex;
USHORT CurrentNode;
USHORT CurrentNodeAffinityCount;
USHORT HighestNodeNumber;
ULONG MaximumGroupCount;
PGROUP_AFFINITY NodeAffinityMasks;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

MaximumGroupCount = KeQueryMaximumGroupCount();
NodeAffinityMasks = ExAllocatePool2(POOL_FLAG_PAGED,
                                    sizeof(GROUP_AFFINITY) * MaximumGroupCount,
                                    'tseT');

if (NodeAffinityMasks == NULL) {
    return STATUS_NO_MEMORY;
}

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    Status = KeQueryNodeActiveAffinity2(CurrentNode,
                                        NodeAffinityMasks,
                                        MaximumGroupCount,
                                        &CurrentNodeAffinityCount);
    NT_ASSERT(NT_SUCCESS(Status));

    for (CurrentIndex = 0; CurrentIndex < CurrentNodeAffinityCount; CurrentIndex += 1) {

        CurrentAffinity = &NodeAffinityMasks[CurrentIndex];

        while (CurrentAffinity->Mask != 0) {

            ProcessorNumber.Group = CurrentAffinity.Group;
            BitScanForward(&ProcessorNumber.Number, CurrentAffinity->Mask);

            ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

            ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode];

            CurrentAffinity->Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
        }
    }
}

//
// Resolution using KeQueryLogicalProcessorRelationship.
//

ULONG ProcessorCount;
ULONG ProcessorIndex;
SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX ProcessorInformation;
ULONG ProcessorInformationSize;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

ProcessorCount = KeQueryActiveProcessorCountEx(ALL_PROCESSOR_GROUPS);

for (ProcessorIndex = 0; ProcessorIndex < ProcessorCount; ProcessorIndex += 1) {

    Status = KeGetProcessorNumberFromIndex(ProcessorIndex, &ProcessorNumber);
    NT_ASSERT(NT_SUCCESS(Status));

    ProcessorInformationSize = sizeof(ProcessorInformation);
    Status = KeQueryLogicalProcessorRelationship(&ProcessorNumber,
                                                    RelationNumaNode,
                                                    &ProcessorInformation,
                                                    &ProcesorInformationSize);
    NT_ASSERT(NT_SUCCESS(Status));

    NodeNumber = ProcessorInformation.NumaNode.NodeNumber;

    ProcessorNodeContexts[ProcessorIndex] = NodeContexts[NodeNumber];
}
```

## <a name="numa-api"></a>API NUMA

Le tableau suivant décrit l’API NUMA.



| Fonction                                                                     | Description                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)      | Alloue des pages de mémoire physique à mapper et à démapper dans une région AWE ( [Address Windowing Extensions](../memory/address-windowing-extensions.md) ) d’un processus spécifié et spécifie le nœud NUMA pour la mémoire physique. |
| [**CreateFileMappingNuma**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingnumaw)                      | Crée ou ouvre un objet de mappage de fichier nommé ou sans nom pour un fichier spécifié et spécifie le nœud NUMA pour la mémoire physique.                                                                                              |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | mise à jour dans Windows 10 Build 20348. Récupère des informations sur les processeurs logiques et le matériel associé.                                                                                                                                                            |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | mise à jour dans Windows 10 Build 20348. Récupère des informations sur les relations entre les processeurs logiques et le matériel associé.                                                                                                                                       |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)             | Récupère la quantité de mémoire disponible dans le nœud spécifié.                                                                                                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)         | Récupère la quantité de mémoire disponible dans un nœud spécifié en tant que valeur **UShort** .                                                                                                                                             |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)                 | Récupère le nœud qui a actuellement le nombre le plus élevé.                                                                                                                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)                 | mise à jour dans Windows 10 Build 20348. Récupère le masque de processeur pour le nœud spécifié.                                                                                                                                                                            |
| [**GetNumaNodeProcessorMask2**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormask2)                         | nouveauté de Windows 10 Build 20348. Récupère le masque de processeur à plusieurs groupes du nœud spécifié.                                                                                                                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)             | mise à jour dans Windows 10 Build 20348. Récupère le masque de processeur pour un nœud spécifié sous la forme d’une valeur **UShort** .                                                                                                                                                        |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                         | Récupère le numéro de nœud pour le processeur spécifié.                                                                                                                                                                          |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                     | Récupère le nombre de nœuds sous la forme d’une valeur **UShort** pour le processeur spécifié.                                                                                                                                                    |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                         | Récupère le numéro de nœud pour l’identificateur de proximité spécifié.                                                                                                                                                               |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                     | Récupère le nombre de nœuds sous la forme d’une valeur **UShort** pour l’identificateur de proximité spécifié.                                                                                                                                         |
| [**GetProcessDefaultCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessdefaultcpusetmasks)                     | nouveauté de Windows 10 Build 20348. Récupère la liste des ensembles d’UC dans l’ensemble de processus par défaut qui a été défini par SetProcessDefaultCpuSetMasks ou SetProcessDefaultCpuSets.                                                                                                                                         |
| [**GetThreadSelectedCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadselectedcpusetmasks)                     | nouveauté de Windows 10 Build 20348. Définit l’affectation de jeux d’UC sélectionnée pour le thread spécifié. Cette assignation remplace l’attribution de processus par défaut, si celle-ci est définie.                                                                                                                                          |
| [**MapViewOfFileExNuma**](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)                          | Cartes une vue d’un mappage de fichier dans l’espace d’adressage d’un processus appelant, et spécifie le nœud NUMA pour la mémoire physique.                                                                                                 |
| [**SetProcessDefaultCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessdefaultcpusetmasks)                     | nouveauté de Windows 10 Build 20348. Définit l’affectation de jeux d’UC par défaut pour les threads dans le processus spécifié.                                                                                                                                          |
| [**SetThreadSelectedCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadselectedcpusetmasks)                     | nouveauté de Windows 10 Build 20348. Définit l’affectation de jeux d’UC sélectionnée pour le thread spécifié. Cette assignation remplace l’attribution de processus par défaut, si celle-ci est définie.                                                                                                                                          |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                            | Réserve ou valide une zone de mémoire dans l’espace d’adressage virtuel du processus spécifié et spécifie le nœud NUMA pour la mémoire physique.                                                                          |



 

La fonction [**QueryWorkingSetEx**](/windows/win32/api/psapi/nf-psapi-queryworkingsetex) peut être utilisée pour récupérer le nœud NUMA sur lequel une page est allouée. Pour obtenir un exemple, consultez [allocation de mémoire à partir d’un nœud NUMA](../memory/allocating-memory-from-a-numa-node.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Allocation de mémoire à partir d’un nœud NUMA](../memory/allocating-memory-from-a-numa-node.md)
</dt> <dt>

[Plusieurs processeurs](multiple-processors.md)
</dt> <dt>

[Groupes de processeurs](processor-groups.md)
</dt> </dl>

 

 
