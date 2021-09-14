---
description: Cette rubrique répertorie les structures utilisées avec les processus, les threads, les processeurs, les objets de travail et la planification en mode utilisateur (UMS).
ms.assetid: dbb50193-4c67-494e-9c46-2ac3106fac9a
title: Structures de processus et de threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59b2b4a8209c3f1f9fb3163c849fa2c229d2bdf5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007112"
---
# <a name="process-and-thread-structures"></a>Structures de processus et de threads

Cette rubrique répertorie les structures utilisées avec les processus, les threads, les processeurs, les objets de travail et la planification en mode utilisateur (UMS).

## <a name="process-and-thread-structures"></a>Structures de processus et de threads

Les structures suivantes sont utilisées avec les processus et les threads :

-   [**\_informations sur la mémoire de l’application \_**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [**\_État AR**](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [**descripteur de CACHE \_**](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [**compteurs d’e/s \_**](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [**préférence d’ORIENTATION \_**](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [**\_données LDR \_ PEB**](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [**\_informations sur le processus**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [**\_informations d' \_ épuisement de la mémoire du processus \_**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [**\_ \_ stratégie ASLR d’atténuation des processus \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [**\_ \_ stratégie de signature binaire \_ \_ de l’atténuation du processus**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [**stratégie de protection du workflow de contrôle de l’atténuation des processus \_ \_ \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [**\_ \_ stratégie DEP de l’atténuation des processus \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [**\_ \_ stratégie de code dynamique \_ d’atténuation des processus \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [**\_ \_ stratégie de \_ \_ désactivation du point d’extension \_ d’atténuation de processus**](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [**\_ \_ stratégie de \_ désactivation de la police d’atténuation des processus \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [**\_stratégie de chargement d’image d’atténuation de processus \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [**\_stratégie de \_ \_ vérification du handle \_ strict \_ de l’atténuation du processus**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [**\_ \_ stratégie de \_ \_ désactivation de l’appel système \_ d’atténuation des processus**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [**\_paramètres du \_ processus \_ utilisateur RTL**](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [**STARTUPINFOEX**](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [**TEB**](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a>Structures de processeur

Les structures suivantes sont utilisées avec les processeurs et les groupes de processeurs :

-   [**relation du CACHE \_**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [**affinité de groupe \_**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [**relation de groupe \_**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [**\_relation de nœud NUMA \_**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [**\_informations sur le groupe de processeurs \_**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [**Numéro de processeur \_**](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [**relation de processeur \_**](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [**\_ \_ informations sur l’ensemble de PROCESSEURs système \_**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [**\_ \_ informations sur le processeur logique système \_**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [**\_ \_ informations sur le processeur logique système \_ \_ ex**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a>Structure de file d’attente du répartiteur

La structure suivante est utilisée pour créer un [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).

-   [**DispatcherQueueOptions**](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a>Structures d’objets de tâche

Les structures suivantes sont utilisées avec les objets de travail :

-   [**JOBOBJECT \_ associer \_ le \_ port de terminaison**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [**\_informations de \_ comptabilité de base JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**JOBOBJECT \_ \_ les informations de gestion de base et d' \_ e/s \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [**\_ \_ informations sur les limites de base de JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**\_liste d' \_ ID de processus de base JOBOBJECT \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [**JOBOBJECT \_ \_ restrictions de l’interface utilisateur de base \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**JOBOBJECT \_ fin \_ des \_ \_ informations d’heure \_ de la tâche**](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [**\_ \_ informations sur la limite étendue JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**\_ \_ informations sur la limite de sécurité JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a>Structures de planification de User-Mode

Les structures suivantes sont utilisées avec UMS :

-   [**\_attributs de création de \_ thread UMS \_**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [**\_ \_ informations de démarrage du planificateur \_ UMS**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [**\_ \_ informations sur le thread système UMS \_**](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
