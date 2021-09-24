---
title: Fournisseurs système
description: Activez les événements du fournisseur de trace système avec EnableTraceEx2.
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: f32b31f1c1a59c3a1507a37279def248f57e66e2
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520306"
---
# <a name="system-providers"></a>Fournisseurs système
 
à compter de Windows 10 SDK build 20348, les événements du fournisseur de Trace système peuvent être activés de la même façon que les autres fournisseurs ETW, avec [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).  Les différents indicateurs et [masques de groupe](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) associés au fournisseur de trace système ont été mappés aux nouveaux fournisseurs de suivi, appelés fournisseurs système et Mots clés correspondants.  
 
Comme pour l’activation directe du fournisseur de trace système, les fournisseurs système peuvent uniquement être activés par une session avec la [EVENT_TRACE_SYSTEM_LOGGER_MODE](./logging-mode-constants.md) définie.

## <a name="system-provider-reference"></a>Référence du fournisseur système

* [Fournisseur ALPC système](#system-alpc-provider)
* [Fournisseur de configuration système](#system-config-provider)
* [Fournisseur d’UC système](#system-cpu-provider)
* [Fournisseur d’hyperviseur système](#system-hypervisor-provider)
* [Fournisseur d’interruptions système](#system-interrupt-provider)
* [Fournisseur d’e/s système](#system-io-provider)
* [Fournisseur de filtres d’e/s système](#system-io-filter-provider)
* [Fournisseur de verrouillage système](#system-lock-provider)
* [Fournisseur de mémoire système](#system-memory-provider)
* [Fournisseur d’objets système](#system-object-provider)
* [Fournisseur d’alimentation du système](#system-power-provider)
* [Fournisseur de processus système](#system-process-provider)
* [Fournisseur de profils système](#system-profile-provider)
* [Fournisseur de Registre système](#system-registry-provider)
* [Fournisseur du planificateur système](#system-scheduler-provider)
* [Fournisseur syscall système](#system-syscall-provider)
* [Fournisseur de la minuterie système](#system-timer-provider)
 
### <a name="system-alpc-provider"></a>Fournisseur ALPC système

Fournit des événements liés au système ALPC.

GUID : SystemAlpcProviderGuid {fcb9baaf-E529-4980-92e9-ced1a6aadfdf}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_ALPC_KW_GENERAL | PERF_ALPC, EVENT_TRACE_FLAG_ALPC |
 
### <a name="system-config-provider"></a>Fournisseur de configuration système 

Fournit des événements de configuration du système.

GUID : SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_CONFIG_KW_SYSTEM | PERF_SYSCFG_SYSTEM |
| SYSTEM_CONFIG_KW_GRAPHICS | PERF_SYSCFG_GRAPHICS |
| SYSTEM_CONFIG_KW_STORAGE | PERF_SYSCFG_STORAGE |
| SYSTEM_CONFIG_KW_NETWORK | PERF_SYSCFG_NETWORK |
| SYSTEM_CONFIG_KW_SERVICES | PERF_SYSCFG_SERVICES |
| SYSTEM_CONFIG_KW_PNP | PERF_SYSCFG_PNP |
| SYSTEM_CONFIG_KW_OPTICAL | PERF_SYSCFG_OPTICAL |
 
### <a name="system-cpu-provider"></a>Fournisseur d’UC système 

Fournit des événements liés au processeur.

GUID : SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_CPU_KW_CONFIG | PERF_CPU_CONFIG |
| SYSTEM_CPU_KW_CACHE_FLUSH | PERF_CACHE_FLUSH |
| SYSTEM_CPU_KW_SPEC_CONTROL | PERF_SPEC_CONTROL |
 
### <a name="system-hypervisor-provider"></a>Fournisseur d’hyperviseur système 

Fournit des événements liés à l’hyperviseur.

GUID : SystemHypervisorProviderGuid {bafa072a-918a-4BED-B622-bc152097098f}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_HYPERVISOR_KW_PROFILE | PERF_HV_PROFILE |
| SYSTEM_HYPERVISOR_KW_CALLOUTS | PERF_HV_CALLOUTS |
| SYSTEM_HYPERVISOR_KW_VTL_CHANGE | PERF_VTL_CHANGE |
 
### <a name="system-interrupt-provider"></a>Fournisseur d’interruptions système 

Fournit des événements relatifs aux appels DPC et aux interruptions.

GUID : SystemInterruptProviderGuid {d4bbee17-b545-4888-858B-744169015b25}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_INTERRUPT_KW_GENERAL | PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT |
| SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT | PERF_CLOCK_INTERRUPT |
| SYSTEM_INTERRUPT_KW_DPC | PERF_DPC, EVENT_TRACE_FLAG_DPC |
| SYSTEM_INTERRUPT_KW_DPC_QUEUE | PERF_DPC_QUEUE |
| SYSTEM_INTERRUPT_KW_WDF_DPC | PERF_WDF_DPC |
| SYSTEM_INTERRUPT_KW_WDF_INTERRUPT | PERF_WDF_INTERRUPT |
| SYSTEM_INTERRUPT_KW_IPI | PERF_IPI |
 
 
### <a name="system-io-provider"></a>Fournisseur d’e/s système 

Fournit des événements liés à plusieurs types d’e/s, y compris le disque, le cache et le réseau.

GUID : SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_IO_KW_DISK | EVENT_TRACE_FLAG_DISK_IO |
| SYSTEM_IO_KW_DISK_INIT | PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT |
| SYSTEM_IO_KW_FILENAME | PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO |
| SYSTEM_IO_KW_SPLIT | PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO |
| SYSTEM_IO_KW_FILE | PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO |
| SYSTEM_IO_KW_OPTICAL | PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT |
| SYSTEM_IO_KW_OPTICAL_INIT | PERF_OPTICAL_IO_INIT |
| SYSTEM_IO_KW_DRIVERS | PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER |
| SYSTEM_IO_KW_CC | PERF_CC |
| SYSTEM_IO_KW_NETWORK | PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP |

Remarque : l’activation du mot clé SYSTEM_IO_KW_DRIVERS active automatiquement SYSTEM_IO_KW_FILENAME également.  La SYSTEM_IO_KW_FILENAME est également activée automatiquement lorsque le fournisseur de mémoire système est activé à l’aide du mot clé SYSTEM_MEMORY_KW_MEMORY.
 
### <a name="system-io-filter-provider"></a>Fournisseur de filtres d’e/s système 

Fournit des événements liés au filtrage des e/s, y compris le minutage et les échecs.

GUID : SystemIoFilterProviderGuid {fbd09363-9E22-4661-b8bf-e7a34b535b8c}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_IOFILTER_KW_GENERAL | PERF_FLT_IO |
| SYSTEM_IOFILTER_KW_INIT | PERF_FLT_IO_INIT |
| SYSTEM_IOFILTER_KW_FASTIO | PERF_FLT_FASTIO |
| SYSTEM_IOFILTER_KW_FAILURE | PERF_FLT_IO_FAILURE |
 
### <a name="system-lock-provider"></a>Fournisseur de verrouillage système 

Fournit des événements relatifs aux mécanismes de verrouillage du noyau.

GUID : SystemLockProviderGuid {721ddfd3-DACC-4e1e-B26A-a2cb31d4705a}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_LOCK_KW_SPINLOCK | PERF_SPINLOCK |
| SYSTEM_LOCK_KW_SPINLOCK_COUNTERS | PERF_SPINLOCK_CNTRS |
| SYSTEM_LOCK_KW_SYNC_OBJECTS | PERF_SYNC_OBJECTS |
 
### <a name="system-memory-provider"></a>Fournisseur de mémoire système 

Fournit des événements liés au gestionnaire de mémoire.

GUID : SystemMemoryProviderGuid {82958ca9-b6cd-47F8-A3A8-03ae85a4bc24}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_MEMORY_KW_GENERAL | PERF_MEMORY |
| SYSTEM_MEMORY_KW_HARD_FAULTS | PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS |
| SYSTEM_MEMORY_KW_ALL_FAULTS | PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS |
| SYSTEM_MEMORY_KW_POOL | PERF_POOL |
| SYSTEM_MEMORY_KW_MEMINFO | PERF_MEMINFO |
| SYSTEM_MEMORY_KW_PFSECTION | PERF_PFSECTION |
| SYSTEM_MEMORY_KW_MEMINFO_WS | PERF_MEMINFO_WS |
| SYSTEM_MEMORY_KW_HEAP | PERF_HEAP |
| SYSTEM_MEMORY_KW_WS | PERF_WS |
| SYSTEM_MEMORY_KW_CONTMEM_GEN | PERF_CONTMEM_GEN |
| SYSTEM_MEMORY_KW_VIRTUAL_ALLOC | PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC |
| SYSTEM_MEMORY_KW_FOOTPRINT | PERF_FOOTPRINT |
| SYSTEM_MEMORY_KW_SESSION | PERF_SESSION |
| SYSTEM_MEMORY_KW_REFSET | PERF_REFSET |
| SYSTEM_MEMORY_KW_VAMAP | PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP |

Remarques : 
* L’activation du mot clé SYSTEM_MEMORY_KW_MEMORY active automatiquement SYSTEM_IO_KW_FILENAME sur le fournisseur d’e/s système.
* Les événements activés par l’SYSTEM_MEMORY_KW_POOL prennent en charge un filtre de balise de pool, pour écrire des événements de manière sélective uniquement pour certaines balises de pool.  Il est configuré en tant que [filtre schématisés](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) sur le fournisseur de mémoire système.  Le filtre PoolTag est construit comme suit :

    ```cpp
    {
    EVENT_FILTER_HEADER Header; 
    ULONG PoolTags[ETW_MAX_POOLTAG_FILTER];
    }
    ```

* Le [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) doit être initialisé avec l’ID défini sur SYSTEM_MEMORY_POOL_FILTER_ID et le champ Taille défini sur la taille de l’en-tête plus la partie utilisée du tableau PoolTags.  

* Chaque balise de pool est une chaîne de 4 caractères stockée en tant que ULONG dans le filtre.  
 
 
### <a name="system-object-provider"></a>Fournisseur d’objets système 

Fournit des événements liés au gestionnaire d’objets.

GUID : SystemObjectProviderGuid {febd7460-3d1d-47eb-AF49-c9eeb1e146f2}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_OBJECT_KW_HANDLE | PERF_OB_HANDLE |
| SYSTEM_OBJECT_KW_OBJECT | PERF_OB_OBJECT |
 
### <a name="system-power-provider"></a>Fournisseur d’alimentation du système 

Fournit des événements relatifs à l’état d’alimentation du système.

GUID : SystemPowerProviderGuid {c134884a-32D5-4488-80e5-14ed7abb8269}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_POWER_KW_GENERAL | PERF_POWER |
| SYSTEM_POWER_KW_HIBER_RUNDOWN | PERF_HIBER_RUNDOWN |
| SYSTEM_POWER_KW_PROCESSOR_IDLE | PERF_PROCESSOR_IDLE |
| SYSTEM_POWER_KW_IDLE_SELECTION | PERF_IDLE_SELECTION |
| SYSTEM_POWER_KW_PPM_EXIT_LATENCY | PERF_PPM_EXIT_LATENCY |
 
### <a name="system-process-provider"></a>Fournisseur de processus système 

Fournit des événements relatifs au processus, y compris des informations de durée de vie, des événements de chargement d’image et des événements liés aux threads.

GUID : SystemProcessProviderGuid {151f55dc-467D-471F-83B5-5f889d46ff66}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_PROCESS_KW_GENERAL | PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS |
| SYSTEM_PROCESS_KW_INSWAP | PERF_PROCESS_INSWAP |
| SYSTEM_PROCESS_KW_FREEZE | PERF_PROCESS_FREEZE |
| SYSTEM_PROCESS_KW_PERF_COUNTER | PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS |
| SYSTEM_PROCESS_KW_WAKE_COUNTER | PERF_WAKE_COUNTER |
| SYSTEM_PROCESS_KW_WAKE_DROP | PERF_WAKE_DROP |
| SYSTEM_PROCESS_KW_WAKE_EVENT | PERF_WAKE_EVENT |
| SYSTEM_PROCESS_KW_DEBUG_EVENTS | PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS |
| SYSTEM_PROCESS_KW_DBGPRINT | PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT |
| SYSTEM_PROCESS_KW_JOB | PERF_JOB, EVENT_TRACE_FLAG_JOB |
| SYSTEM_PROCESS_KW_WORKER_THREAD | PERF_WORKER_THREAD |
| SYSTEM_PROCESS_KW_THREAD | PERF_THREAD, EVENT_TRACE_FLAG_THREAD |
| SYSTEM_PROCESS_KW_LOADER | PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD |
 
### <a name="system-profile-provider"></a>Fournisseur de profils système 

Fournit des événements de profilage.

GUID : SystemProfileProviderGuid {bfeb0324-1cee-496F-A409-2ac2b48a6322}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_PROFILE_KW_GENERAL | PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE |
| SYSTEM_PROFILE_KW_PMC_PROFILE | PERF_PMC_PROFILE |
 
### <a name="system-registry-provider"></a>Fournisseur de Registre système 

Fournit des événements liés au registre.

GUID : SystemRegistryProviderGuid {16156bd9-FAB4-4cfa-A232-89d1099058e3}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_REGISTRY_KW_GENERAL | PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY |
| SYSTEM_REGISTRY_KW_HIVE | PERF_REG_HIVE |
| SYSTEM_REGISTRY_KW_NOTIFICATION | PERF_REG_NOTIF |
 
### <a name="system-scheduler-provider"></a>Fournisseur du planificateur système 

Fournit des événements liés au planificateur.

GUID : SystemSchedulerProviderGuid {599a2a76-4d91-4910-9AC7-7d33f2e97a6c}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_SCHEDULER_KW_XSCHEDULER | PERF_XSCHEDULER |
| SYSTEM_SCHEDULER_KW_DISPATCHER | PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER |
| SYSTEM_SCHEDULER_KW_KERNEL_QUEUE | PERF_KERNEL_QUEUE |
| SYSTEM_SCHEDULER_KW_SHOULD_YIELD | PERF_SHOULD_YIELD |
| SYSTEM_SCHEDULER_KW_ANTI_STARVATION | PERF_ANTI_STARVATION |
| SYSTEM_SCHEDULER_KW_LOAD_BALANCER | PERF_LOAD_BALANCER |
| SYSTEM_SCHEDULER_KW_AFFINITY | PERF_AFFINITY |
| SYSTEM_SCHEDULER_KW_PRIORITY | PERF_PRIORITY |
| SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR | PERF_IDEAL_PROCESSOR |
| SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH | PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH |
 
### <a name="system-syscall-provider"></a>Fournisseur syscall système 

Fournit des événements avec des informations sur les appels système.

GUID : SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_SYSCALL_KW_GENERAL | PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL |
 
### <a name="system-timer-provider"></a>Fournisseur de la minuterie système 

Fournit des événements relatifs aux minuteries dans le noyau.

GUID : SystemTimerProviderGuid {4f061568-E215-499F-ab2e-eda0ae890a5b}

| Mot clé | Groupes et indicateurs hérités correspondants |
| ------- | ------------------------------------- |
| SYSTEM_TIMER_KW_GENERAL | PERF_TIMER |
| SYSTEM_TIMER_KW_CLOCK_TIMER | PERF_CLOCK_TIMER |
 
## <a name="remarks"></a>Remarques

Ce nouveau mécanisme d’activation s’ajoute aux méthodes préexistantes pour l’activation de ces événements.  Tout code qui s’est utilisé pour fonctionner continuera à le faire.
 
Les événements générés par le fournisseur de trace système ne changent pas en raison de cette nouvelle fonctionnalité.  Cela signifie que les événements sortants ne sont pas marqués comme étant émis par les fournisseurs système individuels.
 
Pour plus d’informations sur les définitions de mots clés et de GUID de fournisseur, consultez [evntrace. h](/windows/win32/api/evntrace/).

## <a name="see-also"></a>Voir aussi

[Configuration et démarrage d’une session SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)

[en-tête evntrace. h](/windows/win32/api/evntrace/)
