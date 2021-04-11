---
description: Cette rubrique décrit les fonctions de processus et de thread.
ms.assetid: 8c8e8af0-bf50-4a4b-945c-83bae1eff7dd
title: Fonctions de processus et de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97d871c7fc3635734ce79ba5cbf231e6955e59d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202851"
---
# <a name="process-and-thread-functions"></a>Fonctions de processus et de thread

Cette rubrique décrit les fonctions de processus et de thread.

-   [Fonction de file d’attente Dispatch](#dispatch-queue-function)
-   [Traiter les fonctions](#process-functions)
-   [Traiter les fonctions d’énumération](#process-enumeration-functions)
-   [Fonctions de stratégie](#policy-functions)
-   [Fonctions de thread](#thread-functions)
-   [Fonctions d’attributs étendus de processus et de thread](#process-and-thread-extended-attribute-functions)
-   [Fonctions WOW64](#wow64-functions)
-   [Fonctions d’objet de traitement](#job-object-functions)
-   [Fonctions du pool de threads](#thread-pool-functions)
-   [Fonctions du service de classement des threads](#thread-ordering-service-functions)
-   [Fonctions du service Planificateur de classes multimédias](#multimedia-class-scheduler-service-functions)
-   [Fonctions Fiber](#fiber-functions)
-   [Fonctions de prise en charge de NUMA](#numa-support-functions)
-   [Fonctions du processeur](#processor-functions)
-   [Fonctions de planification en mode utilisateur](#user-mode-scheduling-functions)
-   [Fonctions obsolètes](#obsolete-functions)

## <a name="dispatch-queue-function"></a>Fonction de file d’attente Dispatch

La fonction suivante crée un [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).



| Fonction                                                                   | Description                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDispatcherQueueController**](/windows/desktop/api/DispatcherQueue/nf-dispatcherqueue-createdispatcherqueuecontroller) | Crée un [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller) qui gère la durée de vie d’un [DispatcherQueue](/uwp/api/windows.system.dispatcherqueue) qui exécute des tâches en file d’attente par ordre de priorité sur un autre thread. |



 

## <a name="process-functions"></a>Traiter les fonctions

Les fonctions suivantes sont utilisées avec les [processus](child-processes.md).



| Fonction                                                                 | Description                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)                                   | Crée un processus et son thread principal.                                                                                                                                                 |
| [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)                       | Crée un processus et son thread principal. Le nouveau processus s’exécute dans le contexte de sécurité de l’utilisateur représenté par le jeton spécifié.                                                    |
| [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw)               | Crée un processus et son thread principal. Le nouveau processus exécute ensuite le fichier exécutable spécifié dans le contexte de sécurité des informations d’identification spécifiées (utilisateur, domaine et mot de passe).      |
| [**CreateProcessWithTokenW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithtokenw)               | Crée un processus et son thread principal. Le nouveau processus s’exécute dans le contexte de sécurité du jeton spécifié.                                                                            |
| [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)                                       | Termine le processus appelant et tous ses threads.                                                                                                                                                 |
| [**FlushProcessWriteBuffers**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushprocesswritebuffers)             | Vide la file d’attente d’écriture de chaque processeur qui exécute un thread du processus en cours.                                                                                                    |
| [**FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa)                 | Libère un bloc de chaînes d’environnement.                                                                                                                                                         |
| [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea)                                 | Récupère la chaîne de ligne de commande pour le processus en cours.                                                                                                                                    |
| [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess)                           | Récupère un pseudo-handle pour le processus en cours.                                                                                                                                            |
| [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid)                       | Récupère l’identificateur de processus du processus appelant.                                                                                                                                      |
| [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)           | Récupère le nombre de processeurs sur lesquels le thread actuel s’exécutait pendant l’appel à cette fonction.                                                                                     |
| [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings)                   | Récupère le bloc d’environnement pour le processus actuel.                                                                                                                                      |
| [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable)                 | Récupère la valeur de la variable spécifiée à partir du bloc d’environnement du processus appelant.                                                                                              |
| [**GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess)                         | Récupère l’état d’arrêt du processus spécifié.                                                                                                                                    |
| [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources)                               | Récupère le nombre de descripteurs d’objets d’interface utilisateur graphique (GUI) utilisés par le processus spécifié.                                                                                     |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Récupère des informations sur les processeurs logiques et le matériel associé.                                                                                                                          |
| [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass)                             | Récupère la classe de priorité pour le processus spécifié.                                                                                                                                       |
| [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask)                 | Récupère un masque d’affinité de processus pour le processus spécifié et le masque d’affinité système pour le système.                                                                                      |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)               | Récupère l’affinité de groupe de processeurs du processus spécifié.                                                                                                                              |
| [**GetProcessHandleCount**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)                   | Récupère le nombre de handles ouverts qui appartiennent au processus spécifié.                                                                                                                    |
| [**GetProcessID,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)                                     | Récupère l’identificateur de processus du processus spécifié.                                                                                                                                    |
| [**GetProcessIdOfThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread)                     | Récupère l’identificateur de processus du processus associé au thread spécifié.                                                                                                         |
| [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters)                     | Récupère des informations de gestion de comptes pour toutes les opérations d’e/s effectuées par le processus spécifié.                                                                                                   |
| [**GetProcessMitigationPolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy)         | Récupère les paramètres de stratégie d’atténuation pour le processus appelant.                                                                                                                                 |
| [**GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost)               | Récupère l’état du contrôle d’amélioration de la priorité du processus spécifié.                                                                                                                          |
| [**GetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessshutdownparameters)     | Récupère les paramètres d’arrêt pour le processus en cours d’appel.                                                                                                                              |
| [**Fonction getprocesstimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes)                               | Récupère les informations de minutage relatives au processus spécifié.                                                                                                                                 |
| [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion)                           | Récupère les numéros de version principale et secondaire du système sur lequel le processus spécifié s’attend à s’exécuter.                                                                                    |
| [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize)             | Récupère les tailles minimale et maximale du jeu de travail du processus spécifié.                                                                                                                 |
| [**GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex)         | Récupère les tailles minimale et maximale du jeu de travail du processus spécifié.                                                                                                                 |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)       | Récupère le temps de cycle que chaque processeur dans le groupe spécifié a passé à exécuter des appels de procédure différés (DPC) et des routines de service d’interruption (routines).                                         |
| [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow)                                 | Récupère le contenu de la structure [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) qui a été spécifiée lors de la création du processus appelant.                                                       |
| [**IsImmersiveProcess**](/windows/desktop/api/Winuser/nf-winuser-isimmersiveprocess)                         | Détermine si le processus appartient à une application du Windows Store.                                                                                                                                |
| [**NeedCurrentDirectoryForExePath**](/windows/win32/api/processenv/nf-processenv-needcurrentdirectoryforexepatha) | Détermine si le répertoire actif doit être inclus dans le chemin de recherche pour l’exécutable spécifié.                                                                                  |
| [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)                                       | Ouvre un objet processus local existant.                                                                                                                                                       |
| [**QueryFullProcessImageName**](/windows/desktop/api/WinBase/nf-winbase-queryfullprocessimagenamea)           | Récupère le nom complet de l’image exécutable pour le processus spécifié.                                                                                                                    |
| [**QueryProcessAffinityUpdateMode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprocessaffinityupdatemode) | Récupère le mode de mise à jour d’affinité du processus spécifié.                                                                                                                                  |
| [**QueryProcessCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryprocesscycletime)                   | Récupère la somme du temps de cycle de tous les threads du processus spécifié.                                                                                                                  |
| [**SetEnvironmentVariable ne contient**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable)                 | Définit la valeur d’une variable d’environnement pour le processus actuel.                                                                                                                            |
| [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass)                             | Définit la classe de priorité pour le processus spécifié.                                                                                                                                            |
| [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask)                 | Définit un masque d’affinité du processeur pour les threads d’un processus spécifié.                                                                                                                        |
| [**SetProcessAffinityUpdateMode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessaffinityupdatemode)     | Définit le mode de mise à jour d’affinité du processus spécifié.                                                                                                                                       |
| [**SetProcessInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessinformation)                   | Définit des informations pour le processus spécifié.                                                                                                                                                   |
| [**SetProcessMitigationPolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy)         | Définit la stratégie d’atténuation pour le processus appelant.                                                                                                                                           |
| [**SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost)               | Désactive la capacité du système à augmenter temporairement la priorité des threads du processus spécifié.                                                                                 |
| [**SetProcessRestrictionExemption**](/windows/desktop/api/Winuser/nf-winuser-setprocessrestrictionexemption) | Exempte le processus appelant des restrictions empêchant les processus de bureau d’interagir avec l’environnement des applications du Windows Store. Cette fonction est utilisée par les outils de développement et de débogage. |
| [**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)     | Définit les paramètres d’arrêt pour le processus en cours d’appel.                                                                                                                                   |
| [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize)             | Définit les tailles minimale et maximale de la plage de travail pour le processus spécifié.                                                                                                                     |
| [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex)         | Définit les tailles minimale et maximale de la plage de travail pour le processus spécifié.                                                                                                                     |
| [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)                             | Met fin au processus spécifié et à tous ses threads.                                                                                                                                      |



 

## <a name="process-enumeration-functions"></a>Traiter les fonctions d’énumération

Les fonctions suivantes sont utilisées pour énumérer les processus.



| Fonction                                                    | Description                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Récupère l’identificateur de processus pour chaque objet de processus dans le système.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Récupère des informations sur le premier processus rencontré dans un instantané système.    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Récupère des informations sur le processus suivant enregistré dans un instantané système.        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Récupère des informations sur les processus actifs sur le serveur Terminal Server spécifié. |



 

## <a name="policy-functions"></a>Fonctions de stratégie

Les fonctions suivantes sont utilisées avec la stratégie à l’ensemble du processus.



|                                                      |                                                       |
|------------------------------------------------------|-------------------------------------------------------|
| Fonction                                             | Description                                           |
| [**QueryProtectedPolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprotectedpolicy) | Interroge la valeur associée à une stratégie protégée. |
| [**SetProtectedPolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprotectedpolicy)     | Définit une stratégie protégée.                              |



 

## <a name="thread-functions"></a>Fonctions de thread

Les fonctions suivantes sont utilisées avec les [Threads](multiple-threads.md).



| Fonction                                                           | Description                                                                                                                                               |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput)                     | Attache le mécanisme de traitement d’entrée d’un thread à celui d’un autre thread.                                                                          |
| [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)                   | Crée un thread qui s’exécute dans l’espace d’adressage virtuel d’un autre processus.                                                                               |
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)               | Crée un thread qui s’exécute dans l’espace d’adressage virtuel d’un autre processus et spécifie éventuellement des attributs étendus tels que l’affinité de groupe de processeurs. |
| [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)                               | Crée un thread à exécuter dans l’espace d’adressage virtuel du processus appelant.                                                                      |
| [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)                                   | Met fin au thread appelant.                                                                                                                                  |
| [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread)                       | Récupère un pseudo-handle pour le thread actuel.                                                                                                         |
| [**GetCurrentThreadID,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid)                   | Récupère l’identificateur de thread du thread appelant.                                                                                                    |
| [**GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread)                     | Récupère l’état d’arrêt du thread spécifié.                                                                                                 |
| [**GetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-getthreaddescription)               | Récupère la description qui a été assignée à un thread en appelant [**SetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription).                                  |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)           | Récupère l’affinité de groupe de processeurs du thread spécifié.                                                                                           |
| [**GetThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadid)                                 | Récupère l’identificateur de thread du thread spécifié.                                                                                                  |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)     | Récupère le numéro de processeur du processeur idéal pour le thread spécifié.                                                                           |
| [**GetThreadInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadinformation)               | Récupère des informations sur le thread spécifié.                                                                                                         |
| [**GetThreadIOPendingFlag**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadiopendingflag)           | Détermine si un thread spécifié a des demandes d’e/s en attente.                                                                                       |
| [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority)                     | Récupère la valeur de priorité pour le thread spécifié.                                                                                                    |
| [**GetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost)           | Récupère l’état du contrôle d’amélioration de priorité du thread spécifié.                                                                                       |
| [**GetThreadTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadtimes)                           | Récupère les informations de minutage pour le thread spécifié.                                                                                                    |
| [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)                                   | Ouvre un objet thread existant.                                                                                                                          |
| [**QueryIdleProcessorCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime) | Récupère le temps de cycle pour le thread inactif de chaque processeur dans le système.                                                                             |
| [**QueryThreadCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-querythreadcycletime)               | Récupère le temps de cycle pour le thread spécifié.                                                                                                        |
| [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)                               | Décrémente le nombre de suspensions d’un thread.                                                                                                                      |
| [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask)             | Définit un masque d’affinité du processeur pour le thread spécifié.                                                                                                  |
| [**SetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription)               | Assigne une description à un thread.                                                                                                                        |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)           | Définit l’affinité de groupe de processeurs pour le thread spécifié.                                                                                               |
| [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor)         | Spécifie un processeur préféré pour un thread.                                                                                                             |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)     | Définit le processeur idéal pour le thread spécifié et récupère éventuellement le processeur idéal précédent.                                                  |
| [**SetThreadInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation)               | Définit des informations pour le thread spécifié.                                                                                                                |
| [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)                     | Définit la valeur de priorité pour le thread spécifié.                                                                                                         |
| [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost)           | Désactive la capacité du système à augmenter temporairement la priorité d’un thread.                                                                         |
| [**SetThreadStackGuarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee)         | Définit la garantie de la pile pour le thread appelant.                                                                                                          |
| [**Dormant**](/windows/win32/api/synchapi/nf-synchapi-sleep)                                             | Interrompt l’exécution du thread actuel pour un intervalle spécifié.                                                                                    |
| [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)                                         | Suspend le thread actuel jusqu’à ce que la condition spécifiée soit remplie.                                                                                         |
| [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread)                             | Suspend le thread spécifié.                                                                                                                            |
| [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)                           | Oblige le thread appelant à céder l'exécution à un autre thread prêt à s'exécuter sur le processeur actuel.                                             |
| [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)                         | Termine un thread.                                                                                                                                      |
| [**ThreadProc**](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))                                   | Fonction définie par l’application qui sert d’adresse de départ pour un thread.                                                                         |
| [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc)                                       | Alloue un index de stockage local des threads (TLS).                                                                                                             |
| [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree)                                         | Libère un index TLS.                                                                                                                                     |
| [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue)                                 | Récupère la valeur dans l’emplacement TLS du thread appelant pour un index TLS spécifié.                                                                           |
| [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue)                                 | Stocke une valeur dans l’emplacement TLS du thread appelant pour un index TLS spécifié.                                                                                |
| [**WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle)                       | Attend que le processus spécifié attende une entrée d’utilisateur sans aucune entrée en attente, ou jusqu’à ce que l’intervalle de délai d’attente soit écoulé.                            |



 

## <a name="process-and-thread-extended-attribute-functions"></a>Fonctions d’attributs étendus de processus et de thread

Les fonctions suivantes sont utilisées pour définir des attributs étendus pour la création de processus et de threads.



| Fonction                                                                       | Description                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DeleteProcThreadAttributeList**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-deleteprocthreadattributelist)         | Supprime la liste d’attributs spécifiée pour la création de processus et de threads.                            |
| [**InitializeProcThreadAttributeList**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist) | Initialise la liste d’attributs spécifiée pour la création de processus et de threads.                        |
| [**UpdateProcThreadAttribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute)                 | Met à jour l’attribut spécifié dans la liste d’attributs spécifiée pour la création de processus et de threads. |



 

## <a name="wow64-functions"></a>Fonctions WOW64

Les fonctions suivantes sont utilisées avec [WOW64](../winprog64/running-32-bit-applications.md).



| Fonction                                         | Description                                                                                                                            |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**IsWow64Message**](/windows/desktop/api/Winuser/nf-winuser-iswow64message)         | Détermine si le dernier message lu à partir de la file d’attente du thread actuel provient d’un processus WOW64.                              |
| [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)         | Détermine si le processus spécifié s’exécute sous WOW64.                                                                       |
| [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2)       | Détermine si le processus spécifié s’exécute sous WOW64 ; retourne également des informations supplémentaires sur l’architecture et le processus machine. |
| [**Wow64SuspendThread**](/windows/desktop/api/WinBase/nf-winbase-wow64suspendthread) | Suspend le thread WOW64 spécifié.                                                                                                   |



 

## <a name="job-object-functions"></a>Fonctions d’objet de traitement

Les fonctions suivantes sont utilisées avec les [objets de traitement](job-objects.md).



| Fonction                                                       | Description                                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject)   | Associe un processus à un objet de traitement existant.                                                    |
| [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)                     | Crée ou ouvre un objet de traitement.                                                                       |
| [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)                       | Détermine si le processus s’exécute dans le travail spécifié.                                      |
| [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta)                         | Ouvre un objet de traitement existant.                                                                        |
| [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) | Récupère les informations de limite et d’état de travail à partir de l’objet de traitement.                                       |
| [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)     | Définir des limites pour un objet de traitement.                                                                         |
| [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject)               | Met fin à tous les processus actuellement associés à la tâche.                                          |
| [**UserHandleGrantAccess**](/windows/desktop/api/Winuser/nf-winuser-userhandlegrantaccess)         | Accorde ou refuse l’accès à un objet utilisateur à un travail qui a une restriction d’interface utilisateur. |



 

## <a name="thread-pool-functions"></a>Fonctions du pool de threads

Les fonctions suivantes sont utilisées avec les [pools de threads](thread-pools.md).



| Fonction                                                                                   | Description                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallbackMayRunLong**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-callbackmayrunlong)                                           | Indique que le rappel peut ne pas retourner rapidement.                                                                                                                                                                                                 |
| [**CancelThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio)                                           | Annule la notification de la fonction [**StartThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio) .                                                                                                                                                          |
| [**CloseThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool)                                                 | Ferme le pool de threads spécifié.                                                                                                                                                                                                                   |
| [**CloseThreadpoolCleanupGroup**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup)                         | Ferme le groupe de nettoyage spécifié.                                                                                                                                                                                                                 |
| [**CloseThreadpoolCleanupGroupMembers**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers)           | Libère les membres du groupe de nettoyage spécifié, attend que toutes les fonctions de rappel se terminent, et annule éventuellement toutes les fonctions de rappel en suspens.                                                                                       |
| [**CloseThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolio)                                             | Libère l’objet de fin d’exécution d’e/s spécifié.                                                                                                                                                                                                       |
| [**CloseThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer)                                       | Libère l’objet de minuteur spécifié.                                                                                                                                                                                                                |
| [**CloseThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait)                                         | Libère l’objet d’attente spécifié.                                                                                                                                                                                                                 |
| [**CloseThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork)                                         | Libère l’objet de travail spécifié.                                                                                                                                                                                                                 |
| [**CreateThreadpool**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool)                                               | Alloue un nouveau pool de threads pour exécuter des rappels.                                                                                                                                                                                               |
| [**CreateThreadpoolCleanupGroup**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup)                       | Crée un groupe de nettoyage que les applications peuvent utiliser pour suivre un ou plusieurs rappels de pool de threads.                                                                                                                                                       |
| [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio)                                           | Crée un objet de fin d’exécution d’e/s.                                                                                                                                                                                                                |
| [**CreateThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer)                                     | Crée un objet de minuterie.                                                                                                                                                                                                                         |
| [**CreateThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait)                                       | Crée un nouvel objet d’attente.                                                                                                                                                                                                                          |
| [**CreateThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork)                                       | Crée un objet de travail.                                                                                                                                                                                                                          |
| [**DestroyThreadpoolEnvironment**](/windows/desktop/api/WinBase/nf-winbase-destroythreadpoolenvironment)                       | Supprime l’environnement de rappel spécifié. Appelez cette fonction lorsque l’environnement de rappel n’est plus nécessaire pour la création d’objets de pool de threads.                                                                                              |
| [**DisassociateCurrentThreadFromCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-disassociatecurrentthreadfromcallback)     | Supprime l’association entre la fonction de rappel en cours d’exécution et l’objet qui a initié le rappel. Le thread actuel n’est plus compté comme exécutant un rappel pour le compte de l’objet.                                      |
| [**FreeLibraryWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns)                   | Spécifie la DLL que le pool de threads déchargera lorsque le rappel en cours sera terminé.                                                                                                                                                             |
| [**InitializeThreadpoolEnvironment**](/windows/desktop/api/WinBase/nf-winbase-initializethreadpoolenvironment)                 | Initialise un environnement de rappel.                                                                                                                                                                                                                 |
| [**IsThreadpoolTimerSet**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-isthreadpooltimerset)                                       | Détermine si l’objet de minuteur spécifié est actuellement défini.                                                                                                                                                                                     |
| [**LeaveCriticalSectionWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-leavecriticalsectionwhencallbackreturns) | Spécifie la section critique libérée par le pool de threads lorsque le rappel en cours se termine.                                                                                                                                               |
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)                 | Récupère la réserve de piles et les tailles de validation pour les threads dans le pool de threads spécifié.                                                                                                                                                              |
| [**ReleaseMutexWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasemutexwhencallbackreturns)                 | Spécifie le mutex libéré par le pool de threads lorsque le rappel en cours est terminé.                                                                                                                                                          |
| [**ReleaseSemaphoreWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasesemaphorewhencallbackreturns)         | Spécifie le sémaphore libéré par le pool de threads lorsque le rappel en cours est terminé.                                                                                                                                                      |
| [**SetEventWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-seteventwhencallbackreturns)                         | Spécifie l’événement que le pool de threads définit quand le rappel en cours se termine.                                                                                                                                                              |
| [**SetThreadpoolCallbackCleanupGroup**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackcleanupgroup)             | Associe le groupe de nettoyage spécifié à l’environnement de rappel spécifié.                                                                                                                                                                     |
| [**SetThreadpoolCallbackLibrary**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbacklibrary)                       | Garantit que la DLL spécifiée reste chargée tant qu’il y a des rappels en attente.                                                                                                                                                           |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)                 | Spécifie que le rappel doit s’exécuter sur un thread persistant.                                                                                                                                                                                      |
| [**SetThreadpoolCallbackPool**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpool)                             | Définit le pool de threads à utiliser lors de la génération de rappels.                                                                                                                                                                                          |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)                     | Spécifie la priorité d’une fonction de rappel par rapport à d’autres éléments de travail dans le même pool de threads.                                                                                                                                                 |
| [**SetThreadpoolCallbackRunsLong**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackrunslong)                     | Indique que les rappels associés à cet environnement de rappel peuvent ne pas être retournés rapidement.                                                                                                                                                          |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)                     | Définit la réserve de piles et les tailles de validation pour les nouveaux threads dans le pool de threads spécifié.                                                                                                                                                               |
| [**SetThreadpoolThreadMaximum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum)                           | Définit le nombre maximal de threads pouvant être alloués par le pool de threads spécifié pour traiter les rappels.                                                                                                                                                |
| [**SetThreadpoolThreadMinimum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum)                           | Définit le nombre minimal de threads que le pool de threads spécifié doit mettre à disposition pour traiter les rappels.                                                                                                                                         |
| [**SetThreadpoolTimerEx**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimerex)                                       | Définit l’objet de la minuterie. Un thread de travail appelle le rappel de l’objet de minuteur après l’expiration du délai d’attente spécifié.                                                                                                                                       |
| [**SetThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer)                                           | Définit l’objet de la minuterie. Un thread de travail appelle le rappel de l’objet de minuteur après l’expiration du délai d’attente spécifié.                                                                                                                                       |
| [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait)                                             | Définit l’objet Wait. Un thread de travail appelle la fonction de rappel de l’objet d’attente une fois que le handle est signalé ou après l’expiration du délai d’attente spécifié.                                                                                           |
| [**SetThreadpoolWaitEx**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwaitex)                                         | Définit l’objet Wait. Un thread de travail appelle la fonction de rappel de l’objet d’attente une fois que le handle est signalé ou après l’expiration du délai d’attente spécifié.                                                                                           |
| [**StartThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio)                                             | Notifie le pool de threads que les opérations d’e/s peuvent éventuellement commencer pour l’objet de fin d’exécution d’e/s spécifié. Un thread de travail appelle la fonction de rappel de l’objet de fin d’exécution d’e/s une fois l’opération terminée sur le handle de fichier lié à cet objet. |
| [**SubmitThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork)                                       | Publie un objet de travail dans le pool de threads. Un thread de travail appelle la fonction de rappel de l’objet de travail.                                                                                                                                                  |
| [**TpInitializeCallbackEnviron**](/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron)                         | Initialise un environnement de rappel pour le pool de threads.                                                                                                                                                                                             |
| [**TpDestroyCallbackEnviron**](/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron)                               | Supprime l’environnement de rappel spécifié. Appelez cette fonction lorsque l’environnement de rappel n’est plus nécessaire pour la création d’objets de pool de threads.                                                                                              |
| [**TpSetCallbackActivationContext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext)                   | Affecte un contexte d’activation à l’environnement de rappel.                                                                                                                                                                                          |
| [**TpSetCallbackCleanupGroup**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup)                             | Associe le groupe de nettoyage spécifié à l’environnement de rappel spécifié.                                                                                                                                                                     |
| [**TpSetCallbackFinalizationCallback**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback)             | Indique une fonction à appeler lorsque l’environnement de rappel est finalisé.                                                                                                                                                                            |
| [**TpSetCallbackLongFunction**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction)                             | Indique que les rappels associés à cet environnement de rappel peuvent ne pas être retournés rapidement.                                                                                                                                                          |
| [**TpSetCallbackNoActivationContext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext)               | Indique que l’environnement de rappel n’a aucun contexte d’activation.                                                                                                                                                                                  |
| [**TpSetCallbackPersistent**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent)                                 | Spécifie que le rappel doit s’exécuter sur un thread persistant.                                                                                                                                                                                      |
| [**TpSetCallbackPriority**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority)                                     | Spécifie la priorité d’une fonction de rappel par rapport à d’autres éléments de travail dans le même pool de threads.                                                                                                                                                 |
| [**TpSetCallbackRaceWithDll**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll)                               | Garantit que la DLL spécifiée reste chargée tant qu’il y a des rappels en attente.                                                                                                                                                           |
| [**TpSetCallbackThreadpool**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool)                                 | Assigne un pool de threads à un environnement de rappel.                                                                                                                                                                                                    |
| [**TrySubmitThreadpoolCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-trysubmitthreadpoolcallback)                         | Demande qu’un thread de travail de pool de threads appelle la fonction de rappel spécifiée.                                                                                                                                                                     |
| [**WaitForThreadpoolIoCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooliocallbacks)                       | Attend la fin des rappels d’achèvement d’e/s en suspens et annule éventuellement les rappels en attente qui n’ont pas encore commencé à s’exécuter.                                                                                                           |
| [**WaitForThreadpoolTimerCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks)                 | Attend la fin des rappels de minuterie en attente et annule éventuellement les rappels en attente qui n’ont pas encore commencé à s’exécuter.                                                                                                                    |
| [**WaitForThreadpoolWaitCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks)                   | Attend la fin des rappels d’attente en attente et annule éventuellement les rappels en attente qui n’ont pas encore commencé à s’exécuter.                                                                                                                     |
| [**WaitForThreadpoolWorkCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolworkcallbacks)                   | Attend la fin des rappels de travail en suspens et annule éventuellement les rappels en attente qui n’ont pas encore commencé à s’exécuter.                                                                                                                     |



 

Les fonctions suivantes font partie de l’API de [regroupement de threads](thread-pooling.md) d’origine.



| Fonction                                                            | Description                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)        | Associe le port de terminaison d’e/s détenu par le pool de threads au descripteur de fichier spécifié. À la fin d’une demande d’e/s impliquant ce fichier, un thread de travail non-e/s exécutera la fonction de rappel spécifiée. |
| [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                      | Met en file d’attente un élément de travail vers un thread de travail dans le pool de threads.                                                                                                                                                              |
| [**RegisterWaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) | Dirige un thread d’attente dans le pool de threads à attendre sur l’objet.                                                                                                                                                        |
| [**UnregisterWaitEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-unregisterwaitex)                       | Attend que l’un ou l’ensemble des objets spécifiés soient à l’état signalé ou que l’intervalle de délai d’attente expire.                                                                                                            |



 

## <a name="thread-ordering-service-functions"></a>Fonctions du service de classement des threads

Les fonctions suivantes sont utilisées avec le [service de classement des threads](thread-ordering-service.md).



| Fonction                                                                   | Description                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**AvQuerySystemResponsiveness**](/windows/desktop/api/Avrt/nf-avrt-avquerysystemresponsiveness)         | Récupère le paramètre de réactivité du système utilisé par le service Planificateur de classes multimédias. |
| [**AvRtCreateThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup)     | Crée un groupe d’ordonnancement des threads.                                                            |
| [**AvRtCreateThreadOrderingGroupEx**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroupexa) | Crée un groupe d’ordonnancement des threads et associe le thread serveur à une tâche.               |
| [**AvRtDeleteThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup)     | Supprime le groupe d’ordonnancement de threads spécifié créé par l’appelant.                          |
| [**AvRtJoinThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup)         | Joint les threads clients à un groupe d’ordonnancement des threads.                                            |
| [**AvRtLeaveThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup)       | Permet aux threads clients de conserver un groupe d’ordonnancement des threads.                                    |
| [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup)     | Permet aux threads clients d’un groupe de commandes de thread d’attendre qu’ils s’exécutent.        |



 

## <a name="multimedia-class-scheduler-service-functions"></a>Fonctions du service Planificateur de classes multimédias

Les fonctions suivantes sont utilisées avec le [service Planificateur de classes multimédias](multimedia-class-scheduler-service.md).



| Fonction                                                                   | Description                                                                                           |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**AvRevertMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avrevertmmthreadcharacteristics) | Indique qu’un thread n’effectue plus de travail associé à la tâche spécifiée.              |
| [**AvSetMmMaxThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) | Associe le thread appelant aux tâches spécifiées.                                               |
| [**AvSetMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa)       | Associe le thread appelant à la tâche spécifiée.                                                |
| [**AvSetMmThreadPriority**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority)                     | Ajuste la priorité de thread du thread appelant par rapport à d’autres threads effectuant la même tâche. |



 

## <a name="fiber-functions"></a>Fonctions Fiber

Les fonctions suivantes sont utilisées avec les [fibres](fibers.md).



| Fonction                                                 | Description                                                                                                  |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**ConvertFiberToThread**](/windows/desktop/api/WinBase/nf-winbase-convertfibertothread)     | Convertit la fibre actuelle en un thread.                                                                    |
| [**ConvertThreadToFiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber)     | Convertit le thread actuel en une fibre.                                                                    |
| [**ConvertThreadToFiberEx**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiberex) | Convertit le thread actuel en une fibre.                                                                    |
| [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber)                       | Alloue un objet Fiber, lui assigne une pile et configure l’exécution pour qu’elle commence à l’adresse de début spécifiée. |
| [**CreateFiberEx**](/windows/desktop/api/WinBase/nf-winbase-createfiberex)                   | Alloue un objet Fiber, lui assigne une pile et configure l’exécution pour qu’elle commence à l’adresse de début spécifiée. |
| [**DeleteFiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber)                       | Supprime une fibre existante.                                                                                   |
| [**FiberProc**](/windows/win32/api/winbase/nc-winbase-pfiber_start_routine)                           | Fonction définie par l’application utilisée avec la fonction [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) .                   |
| [**FlsAlloc**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc)                             | Alloue un index FLS (Fiber local Storage).                                                                 |
| [**FlsFree**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree)                               | Libère un index FLS.                                                                                       |
| [**FlsGetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)                       | Récupère la valeur dans l’emplacement FLS de la fibre appelante pour un index FLS spécifié.                               |
| [**FlsSetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)                       | Stocke une valeur dans l’emplacement FLS de la fibre appelant pour un index FLS spécifié.                                    |
| [**IsThreadAFiber**](/windows/win32/api/fibersapi/nf-fibersapi-isthreadafiber)                 | Détermine si le thread actuel est une fibre.                                                            |
| [**SwitchToFiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber)                   | Planifie une fibre.                                                                                           |



 

## <a name="numa-support-functions"></a>Fonctions de prise en charge de NUMA

Les fonctions suivantes fournissent la [prise en charge de Numa](numa-support.md).



| Fonction                                                                 | Description                                                                                                                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)  | Réserve ou valide une zone de mémoire dans l’espace d’adressage virtuel du processus spécifié et spécifie le nœud NUMA pour la mémoire physique. |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Récupère des informations sur les processeurs logiques et le matériel associé.                                                                                   |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)         | Récupère la quantité de mémoire disponible dans le nœud spécifié.                                                                                        |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)     | Récupère la quantité de mémoire disponible dans le nœud spécifié sous la forme d’une valeur USHORT.                                                              |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)             | Récupère le nœud qui a actuellement le nombre le plus élevé.                                                                                              |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)       | Récupère le nœud NUMA associé à l’appareil sous-jacent pour un handle de fichier.                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)             | Récupère le masque de processeur pour le nœud spécifié.                                                                                                   |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)         | Récupère le masque de processeur pour le nœud NUMA spécifié sous la forme d’une valeur USHORT.                                                                            |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                     | Récupère le numéro de nœud pour le processeur spécifié.                                                                                                 |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                 | Récupère le numéro de nœud du processeur logique spécifié sous la forme d’une valeur USHORT.                                                                        |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                     | Récupère le numéro de nœud pour l’identificateur de proximité spécifié.                                                                                      |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                 | Récupère le nombre de nœuds sous la forme d’une valeur USHORT pour l’identificateur de proximité spécifié.                                                                    |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                        | Réserve ou valide une zone de mémoire dans l’espace d’adressage virtuel du processus spécifié et spécifie le nœud NUMA pour la mémoire physique. |



 

## <a name="processor-functions"></a>Fonctions du processeur

Les fonctions suivantes sont utilisées avec des processeurs logiques et des [groupes de processeurs](processor-groups.md).



| Fonction                                                                     | Description                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)                   | Retourne le nombre de processeurs actifs dans un groupe de processeurs ou dans le système.                                       |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)         | Retourne le nombre de groupes de processeurs actifs dans le système.                                                         |
| [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)               | Récupère le nombre de processeurs sur lesquels le thread actuel s’exécutait pendant l’appel à cette fonction.            |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)           | Récupère le groupe de processeurs et le numéro du processeur logique dans lequel le thread appelant s’exécute.            |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Récupère des informations sur les processeurs logiques et le matériel associé.                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Récupère des informations sur les relations entre les processeurs logiques et le matériel associé.                            |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)                 | Retourne le nombre maximal de processeurs logiques qu’un groupe de processeurs ou le système peut avoir.                      |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)       | Retourne le nombre maximal de groupes de processeurs que le système peut avoir.                                             |
| [**QueryIdleProcessorCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime)           | Récupère le temps de cycle pour le thread inactif de chaque processeur dans le système.                                        |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)       | Récupère la durée de cycle accumulée pour le thread inactif sur chaque processeur logique dans le groupe de processeurs spécifié. |



 

## <a name="user-mode-scheduling-functions"></a>Fonctions de planification de User-Mode

Les fonctions suivantes sont utilisées avec la planification en mode utilisateur (UMS).



| Fonction                                                               | Description                                                                                               |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)             | Crée une liste de saisie semi-automatique UMS.                                                                            |
| [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)               | Crée un contexte de thread UMS pour représenter un thread de travail UMS.                                            |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)             | Supprime la liste de saisie semi-automatique UMS spécifiée. La liste doit être vide.                                        |
| [**DeleteUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)               | Supprime le contexte de thread UMS spécifié. Le thread doit être arrêté.                                  |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) | Récupère les threads de travail UMS de la liste de saisie semi-automatique UMS spécifiée.                                      |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)               | Convertit le thread appelant en un thread de planificateur UMS.                                                  |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)                           | Exécute le thread de travail UMS spécifié.                                                                     |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)                     | Retourne le contexte de thread UMS du thread UMS appelant.                                                 |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)                       | Retourne le contexte de thread UMS suivant dans une liste de contextes de thread UMS.                                     |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)         | Récupère un handle vers l’événement associé à la liste de saisie semi-automatique UMS spécifiée.                        |
| [**GetUmsSystemThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-getumssystemthreadinformation) | Interroge si le thread spécifié est un thread UMS Scheduler, un thread de travail UMS ou un thread non UMS. |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)         | Récupère des informations sur le thread de travail UMS spécifié.                                              |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)             | Définit des informations de contexte spécifiques à l’application pour le thread de travail UMS spécifié.                        |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)                             | Fonction de point d’entrée du planificateur UMS définie par l’application associée à une liste de saisie semi-automatique UMS.         |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)                               | Donne le contrôle au thread UMS Scheduler sur lequel le thread de travail UMS appelant est en cours d’exécution.             |



 

## <a name="obsolete-functions"></a>Fonctions obsolètes

-   [**NtGetCurrentProcessorNumber**](ntgetcurrentprocessornumber.md)
-   [**NtQueryInformationProcess**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationprocess)
-   [**NtQueryInformationThread**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationthread)
-   [**WinExec**](/windows/desktop/api/WinBase/nf-winbase-winexec)
-   [**ZwQueryInformationProcess**](zwqueryinformationprocess.md)

 

 
