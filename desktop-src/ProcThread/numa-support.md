---
description: Le modèle traditionnel pour la prise en charge de multiprocesseur est le multiprocesseur symétrique (SMP). Dans ce modèle, chaque processeur a un accès égal à la mémoire et aux e/s. Au fur et à mesure de l’ajout de processeurs, le bus de processeur devient une limite pour les performances du système.
ms.assetid: a1263968-2b26-45cc-bdd7-6aa354821a5a
title: Prise en charge de NUMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559df7d4e13571953f2826188bd80ccbc472b2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518472"
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

## <a name="numa-api"></a>API NUMA

Le tableau suivant décrit l’API NUMA.



| Fonction                                                                     | Description                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)      | Alloue des pages de mémoire physique à mapper et à démapper dans une région AWE ( [Address Windowing Extensions](../memory/address-windowing-extensions.md) ) d’un processus spécifié et spécifie le nœud NUMA pour la mémoire physique. |
| [**CreateFileMappingNuma**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingnumaw)                      | Crée ou ouvre un objet de mappage de fichier nommé ou sans nom pour un fichier spécifié et spécifie le nœud NUMA pour la mémoire physique.                                                                                              |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Récupère des informations sur les processeurs logiques et le matériel associé.                                                                                                                                                            |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Récupère des informations sur les relations entre les processeurs logiques et le matériel associé.                                                                                                                                       |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)             | Récupère la quantité de mémoire disponible dans le nœud spécifié.                                                                                                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)         | Récupère la quantité de mémoire disponible dans un nœud spécifié en tant que valeur **UShort** .                                                                                                                                             |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)                 | Récupère le nœud qui a actuellement le nombre le plus élevé.                                                                                                                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)                 | Récupère le masque de processeur pour le nœud spécifié.                                                                                                                                                                            |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)             | Récupère le masque de processeur pour un nœud spécifié sous la forme d’une valeur **UShort** .                                                                                                                                                        |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                         | Récupère le numéro de nœud pour le processeur spécifié.                                                                                                                                                                          |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                     | Récupère le nombre de nœuds sous la forme d’une valeur **UShort** pour le processeur spécifié.                                                                                                                                                    |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                         | Récupère le numéro de nœud pour l’identificateur de proximité spécifié.                                                                                                                                                               |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                     | Récupère le nombre de nœuds sous la forme d’une valeur **UShort** pour l’identificateur de proximité spécifié.                                                                                                                                         |
| [**MapViewOfFileExNuma**](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)                          | Mappe une vue d’un mappage de fichier dans l’espace d’adressage d’un processus appelant et spécifie le nœud NUMA pour la mémoire physique.                                                                                                 |
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

 

 
