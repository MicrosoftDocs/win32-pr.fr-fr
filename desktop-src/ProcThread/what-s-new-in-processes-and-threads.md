---
description: Windows 7 et Windows Server 2008 R2 incluent les nouveaux éléments de programmation suivants pour les processus et les threads.
ms.assetid: 69cd8713-b40c-4fec-a256-9c2ee3d73da5
title: Nouveautés des processus et des threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7dfb708a2890bab1fcd3fd66385f74bd8513b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865045"
---
# <a name="whats-new-in-processes-and-threads"></a>Nouveautés des processus et des threads

Windows 7 et Windows Server 2008 R2 incluent les nouveaux éléments de programmation suivants pour les processus et les threads.

## <a name="new-capabilities"></a>Nouvelles fonctionnalités

Les versions 64 bits de Windows 7 et Windows Server 2008 R2 prennent en charge plus de 64 processeurs logiques sur un seul ordinateur. Pour plus d’informations, consultez [groupes de processeurs](processor-groups.md).

La planification en mode utilisateur (UMS) est un mécanisme léger que les applications peuvent utiliser pour planifier leurs propres threads. Pour plus d’informations, consultez [planification en mode utilisateur](user-mode-scheduling.md).

## <a name="new-functions"></a>Nouvelles fonctions

Les nouvelles fonctions suivantes sont utilisées avec les processeurs et les groupes de processeurs.



| Fonction                                                                                | Description                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)<br/>                         | Crée un thread qui s’exécute dans l’espace d’adressage virtuel d’un autre processus et spécifie éventuellement des attributs étendus tels que l’affinité de groupe de processeurs.<br/> |
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)<br/>                   | Retourne le nombre de processeurs actifs dans un groupe de processeurs ou dans le système.<br/>                                                                            |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)<br/>         | Retourne le nombre de groupes de processeurs actifs dans le système.<br/>                                                                                              |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)<br/>           | Récupère le groupe de processeurs et le numéro du processeur logique dans lequel le thread appelant s’exécute.<br/>                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex)<br/> | Récupère des informations sur les relations entre les processeurs logiques et le matériel associé.<br/>                                                                 |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)<br/>                 | Retourne le nombre maximal de processeurs logiques qu’un groupe de processeurs ou le système peut avoir.<br/>                                                           |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)<br/>       | Retourne le nombre maximal de groupes de processeurs que le système peut avoir. <br/>                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)<br/>         | Récupère la quantité de mémoire disponible dans le nœud spécifié sous la forme d’une valeur USHORT.<br/>                                                                 |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)<br/>           | Récupère le nœud NUMA associé à l’appareil sous-jacent pour un handle de fichier.<br/>                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)<br/>             | Récupère le masque de processeur pour le nœud NUMA spécifié sous la forme d’une valeur USHORT.<br/>                                                                               |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)<br/>                     | Récupère le numéro de nœud du processeur logique spécifié sous la forme d’une valeur USHORT.<br/>                                                                           |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)<br/>                     | Récupère le nombre de nœuds sous la forme d’une valeur USHORT pour l’identificateur de proximité spécifié.<br/>                                                                       |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)<br/>                   | Récupère l’affinité de groupe de processeurs du processus spécifié.<br/>                                                                                          |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)<br/>           | Récupère le temps de cycle que chaque processeur dans le groupe spécifié a passé à exécuter des appels de procédure différés (DPC) et des routines de service d’interruption (routines).<br/>     |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)<br/>                     | Récupère l’affinité de groupe de processeurs du thread spécifié.<br/>                                                                                           |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)<br/>               | Récupère le numéro de processeur du processeur idéal pour le thread spécifié.<br/>                                                                           |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)<br/>       | Récupère la durée de cycle accumulée pour le thread inactif sur chaque processeur logique dans le groupe de processeurs spécifié. <br/>                                     |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)<br/>                     | Définit l’affinité de groupe de processeurs pour le thread spécifié.<br/>                                                                                               |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)<br/>               | Définit le processeur idéal pour le thread spécifié et récupère éventuellement le processeur idéal précédent.<br/>                                                  |



 

Les nouvelles fonctions suivantes sont utilisées avec les pools de threads.



| Fonction                                                                              | Description                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)<br/> | Récupère la réserve de piles et les tailles de validation pour les threads dans le pool de threads spécifié.<br/>              |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)<br/> | Spécifie que le rappel doit s’exécuter sur un thread persistant.<br/>                                      |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)<br/>     | Spécifie la priorité d’une fonction de rappel par rapport à d’autres éléments de travail dans le même pool de threads.<br/> |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)<br/>     | Définit la réserve de piles et les tailles de validation pour les nouveaux threads dans le pool de threads spécifié. <br/>              |



 

Les nouvelles fonctions suivantes sont utilisées avec UMS.



| Fonction                                                                          | Description                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)<br/>             | Crée une liste de saisie semi-automatique UMS.<br/>                                                                     |
| [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)<br/>               | Crée un contexte de thread UMS pour représenter un thread de travail UMS.<br/>                                     |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)<br/>             | Supprime la liste de saisie semi-automatique UMS spécifiée. La liste doit être vide.<br/>                                 |
| [**DeleteUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)<br/>               | Supprime le contexte de thread UMS spécifié. Le thread doit être arrêté.<br/>                           |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems)<br/> | Récupère les threads de travail UMS de la liste de saisie semi-automatique UMS spécifiée.<br/>                               |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)<br/>               | Convertit le thread appelant en un thread de planificateur UMS.<br/>                                           |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)<br/>                           | Exécute le thread de travail UMS spécifié.<br/>                                                              |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)<br/>                     | Retourne le contexte de thread UMS du thread UMS appelant.<br/>                                          |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)<br/>                       | Retourne le contexte de thread UMS suivant dans une liste de contextes de thread UMS.<br/>                              |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)<br/>         | Récupère un handle vers l’événement associé à la liste de saisie semi-automatique UMS spécifiée.<br/>                 |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)<br/>         | Récupère des informations sur le thread de travail UMS spécifié.<br/>                                       |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)<br/>             | Définit des informations de contexte spécifiques à l’application pour le thread de travail UMS spécifié.<br/>                 |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)<br/>                             | Fonction de point d’entrée du planificateur UMS définie par l’application associée à une liste de saisie semi-automatique UMS. <br/> |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)<br/>                               | Donne le contrôle au thread UMS Scheduler sur lequel le thread de travail UMS appelant est en cours d’exécution.<br/>      |



 

## <a name="new-structures"></a>Nouvelles structures



| Structure                                                                                                 | Description                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**relation du CACHE \_**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)<br/>                                              | Décrit les attributs du cache. <br/>                                                             |
| [**affinité de groupe \_**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)<br/>                                                      | Contient une affinité spécifique au groupe de processeurs, telle que l’affinité d’un thread.<br/>          |
| [**relation de groupe \_**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)<br/>                                              | Contient des informations sur les groupes de processeurs. <br/>                                            |
| [**\_relation de nœud NUMA \_**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)<br/>                                     | Contient des informations sur un nœud NUMA dans un groupe de processeurs. <br/>                            |
| [**\_informations sur le groupe de processeurs \_**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)<br/>                                         | Contient le nombre et l’affinité des processeurs dans un groupe de processeurs.<br/>                     |
| [**Numéro de processeur \_**](/windows/desktop/api/WinNT/ns-winnt-processor_number)<br/>                                                  | Représente un processeur logique dans un groupe de processeurs.<br/>                                     |
| [**relation de processeur \_**](/windows/desktop/api/WinNT/ns-winnt-processor_relationship)<br/>                                      | Contient des informations sur l’affinité au sein d’un groupe de processeurs.<br/>                            |
| [**\_ \_ informations sur le processeur logique système \_ \_ ex**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)<br/> | Contient des informations sur les relations entre les processeurs logiques et le matériel associé.<br/> |
| [**\_attributs de création de \_ thread UMS \_**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)<br/>                        | Spécifie les attributs d’un thread de travail UMS. <br/>                                           |
| [**\_ \_ informations de démarrage du planificateur \_ UMS**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)<br/>                            | Spécifie les attributs d’un thread UMS Scheduler<br/>                                          |



 

 

 
