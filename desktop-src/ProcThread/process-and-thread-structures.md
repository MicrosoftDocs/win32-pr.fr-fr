---
description: Cette rubrique répertorie les structures utilisées avec les processus, les threads, les processeurs, les objets de travail et la planification en mode utilisateur (UMS).
ms.assetid: dbb50193-4c67-494e-9c46-2ac3106fac9a
title: Structures de processus et de threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59b2b4a8209c3f1f9fb3163c849fa2c229d2bdf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106539090"
---
# <a name="process-and-thread-structures"></a><span data-ttu-id="91f8e-103">Structures de processus et de threads</span><span class="sxs-lookup"><span data-stu-id="91f8e-103">Process and Thread Structures</span></span>

<span data-ttu-id="91f8e-104">Cette rubrique répertorie les structures utilisées avec les processus, les threads, les processeurs, les objets de travail et la planification en mode utilisateur (UMS).</span><span class="sxs-lookup"><span data-stu-id="91f8e-104">This topic lists structures that are used with processes, threads, processors, job objects, and user-mode scheduling (UMS).</span></span>

## <a name="process-and-thread-structures"></a><span data-ttu-id="91f8e-105">Structures de processus et de threads</span><span class="sxs-lookup"><span data-stu-id="91f8e-105">Process and Thread Structures</span></span>

<span data-ttu-id="91f8e-106">Les structures suivantes sont utilisées avec les processus et les threads :</span><span class="sxs-lookup"><span data-stu-id="91f8e-106">The following structures are used with processes and threads:</span></span>

-   [<span data-ttu-id="91f8e-107">**\_informations sur la mémoire de l’application \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-107">**APP\_MEMORY\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [<span data-ttu-id="91f8e-108">**\_État AR**</span><span class="sxs-lookup"><span data-stu-id="91f8e-108">**AR\_STATE**</span></span>](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [<span data-ttu-id="91f8e-109">**descripteur de CACHE \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-109">**CACHE\_DESCRIPTOR**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [<span data-ttu-id="91f8e-110">**compteurs d’e/s \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-110">**IO\_COUNTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [<span data-ttu-id="91f8e-111">**préférence d’ORIENTATION \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-111">**ORIENTATION\_PREFERENCE**</span></span>](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [<span data-ttu-id="91f8e-112">**PEB**</span><span class="sxs-lookup"><span data-stu-id="91f8e-112">**PEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [<span data-ttu-id="91f8e-113">**\_données LDR \_ PEB**</span><span class="sxs-lookup"><span data-stu-id="91f8e-113">**PEB\_LDR\_DATA**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [<span data-ttu-id="91f8e-114">**\_informations sur le processus**</span><span class="sxs-lookup"><span data-stu-id="91f8e-114">**PROCESS\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [<span data-ttu-id="91f8e-115">**\_informations d' \_ épuisement de la mémoire du processus \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-115">**PROCESS\_MEMORY\_EXHAUSTION\_INFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [<span data-ttu-id="91f8e-116">**\_ \_ stratégie ASLR d’atténuation des processus \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-116">**PROCESS\_MITIGATION\_ASLR\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [<span data-ttu-id="91f8e-117">**\_ \_ stratégie de signature binaire \_ \_ de l’atténuation du processus**</span><span class="sxs-lookup"><span data-stu-id="91f8e-117">**PROCESS\_MITIGATION\_BINARY\_SIGNATURE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [<span data-ttu-id="91f8e-118">**stratégie de protection du workflow de contrôle de l’atténuation des processus \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-118">**PROCESS\_MITIGATION\_CONTROL\_FLOW\_GUARD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [<span data-ttu-id="91f8e-119">**\_ \_ stratégie DEP de l’atténuation des processus \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-119">**PROCESS\_MITIGATION\_DEP\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [<span data-ttu-id="91f8e-120">**\_ \_ stratégie de code dynamique \_ d’atténuation des processus \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-120">**PROCESS\_MITIGATION\_DYNAMIC\_CODE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [<span data-ttu-id="91f8e-121">**\_ \_ stratégie de \_ \_ désactivation du point d’extension \_ d’atténuation de processus**</span><span class="sxs-lookup"><span data-stu-id="91f8e-121">**PROCESS\_MITIGATION\_EXTENSION\_POINT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [<span data-ttu-id="91f8e-122">**\_ \_ stratégie de \_ désactivation de la police d’atténuation des processus \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-122">**PROCESS\_MITIGATION\_FONT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [<span data-ttu-id="91f8e-123">**\_stratégie de chargement d’image d’atténuation de processus \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-123">**PROCESS\_MITIGATION\_IMAGE\_LOAD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [<span data-ttu-id="91f8e-124">**\_stratégie de \_ \_ vérification du handle \_ strict \_ de l’atténuation du processus**</span><span class="sxs-lookup"><span data-stu-id="91f8e-124">**PROCESS\_MITIGATION\_STRICT\_HANDLE\_CHECK\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [<span data-ttu-id="91f8e-125">**\_ \_ stratégie de \_ \_ désactivation de l’appel système \_ d’atténuation des processus**</span><span class="sxs-lookup"><span data-stu-id="91f8e-125">**PROCESS\_MITIGATION\_SYSTEM\_CALL\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [<span data-ttu-id="91f8e-126">**\_paramètres du \_ processus \_ utilisateur RTL**</span><span class="sxs-lookup"><span data-stu-id="91f8e-126">**RTL\_USER\_PROCESS\_PARAMETERS**</span></span>](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [<span data-ttu-id="91f8e-127">**STARTUPINFO**</span><span class="sxs-lookup"><span data-stu-id="91f8e-127">**STARTUPINFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [<span data-ttu-id="91f8e-128">**STARTUPINFOEX**</span><span class="sxs-lookup"><span data-stu-id="91f8e-128">**STARTUPINFOEX**</span></span>](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [<span data-ttu-id="91f8e-129">**TEB**</span><span class="sxs-lookup"><span data-stu-id="91f8e-129">**TEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a><span data-ttu-id="91f8e-130">Structures de processeur</span><span class="sxs-lookup"><span data-stu-id="91f8e-130">Processor Structures</span></span>

<span data-ttu-id="91f8e-131">Les structures suivantes sont utilisées avec les processeurs et les groupes de processeurs :</span><span class="sxs-lookup"><span data-stu-id="91f8e-131">The following structures are used with processors and processor groups:</span></span>

-   [<span data-ttu-id="91f8e-132">**relation du CACHE \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-132">**CACHE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [<span data-ttu-id="91f8e-133">**affinité de groupe \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-133">**GROUP\_AFFINITY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [<span data-ttu-id="91f8e-134">**relation de groupe \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-134">**GROUP\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [<span data-ttu-id="91f8e-135">**\_relation de nœud NUMA \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-135">**NUMA\_NODE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [<span data-ttu-id="91f8e-136">**\_informations sur le groupe de processeurs \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-136">**PROCESSOR\_GROUP\_INFO**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [<span data-ttu-id="91f8e-137">**Numéro de processeur \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-137">**PROCESSOR\_NUMBER**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [<span data-ttu-id="91f8e-138">**relation de processeur \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-138">**PROCESSOR\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [<span data-ttu-id="91f8e-139">**\_ \_ informations sur l’ensemble de PROCESSEURs système \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-139">**SYSTEM\_CPU\_SET\_INFORMATION**</span></span>](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [<span data-ttu-id="91f8e-140">**\_ \_ informations sur le processeur logique système \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-140">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [<span data-ttu-id="91f8e-141">**\_ \_ informations sur le processeur logique système \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="91f8e-141">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a><span data-ttu-id="91f8e-142">Structure de file d’attente du répartiteur</span><span class="sxs-lookup"><span data-stu-id="91f8e-142">Dispatcher Queue Structure</span></span>

<span data-ttu-id="91f8e-143">La structure suivante est utilisée pour créer un [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).</span><span class="sxs-lookup"><span data-stu-id="91f8e-143">The following structure is used to create a [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).</span></span>

-   [<span data-ttu-id="91f8e-144">**DispatcherQueueOptions**</span><span class="sxs-lookup"><span data-stu-id="91f8e-144">**DispatcherQueueOptions**</span></span>](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a><span data-ttu-id="91f8e-145">Structures d’objets de tâche</span><span class="sxs-lookup"><span data-stu-id="91f8e-145">Job Object Structures</span></span>

<span data-ttu-id="91f8e-146">Les structures suivantes sont utilisées avec les objets de travail :</span><span class="sxs-lookup"><span data-stu-id="91f8e-146">The following structures are used with job objects:</span></span>

-   [<span data-ttu-id="91f8e-147">**JOBOBJECT \_ associer \_ le \_ port de terminaison**</span><span class="sxs-lookup"><span data-stu-id="91f8e-147">**JOBOBJECT\_ASSOCIATE\_COMPLETION\_PORT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [<span data-ttu-id="91f8e-148">**\_informations de \_ comptabilité de base JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-148">**JOBOBJECT\_BASIC\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [<span data-ttu-id="91f8e-149">**JOBOBJECT \_ \_ les informations de gestion de base et d' \_ e/s \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-149">**JOBOBJECT\_BASIC\_AND\_IO\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [<span data-ttu-id="91f8e-150">**\_ \_ informations sur les limites de base de JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-150">**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [<span data-ttu-id="91f8e-151">**\_liste d' \_ ID de processus de base JOBOBJECT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-151">**JOBOBJECT\_BASIC\_PROCESS\_ID\_LIST**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [<span data-ttu-id="91f8e-152">**JOBOBJECT \_ \_ restrictions de l’interface utilisateur de base \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-152">**JOBOBJECT\_BASIC\_UI\_RESTRICTIONS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [<span data-ttu-id="91f8e-153">**JOBOBJECT \_ fin \_ des \_ \_ informations d’heure \_ de la tâche**</span><span class="sxs-lookup"><span data-stu-id="91f8e-153">**JOBOBJECT\_END\_OF\_JOB\_TIME\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [<span data-ttu-id="91f8e-154">**\_ \_ informations sur la limite étendue JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-154">**JOBOBJECT\_EXTENDED\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [<span data-ttu-id="91f8e-155">**\_ \_ informations sur la limite de sécurité JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-155">**JOBOBJECT\_SECURITY\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a><span data-ttu-id="91f8e-156">Structures de planification de User-Mode</span><span class="sxs-lookup"><span data-stu-id="91f8e-156">User-Mode Scheduling Structures</span></span>

<span data-ttu-id="91f8e-157">Les structures suivantes sont utilisées avec UMS :</span><span class="sxs-lookup"><span data-stu-id="91f8e-157">The following structures are used with UMS:</span></span>

-   [<span data-ttu-id="91f8e-158">**\_attributs de création de \_ thread UMS \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-158">**UMS\_CREATE\_THREAD\_ATTRIBUTES**</span></span>](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [<span data-ttu-id="91f8e-159">**\_ \_ informations de démarrage du planificateur \_ UMS**</span><span class="sxs-lookup"><span data-stu-id="91f8e-159">**UMS\_SCHEDULER\_STARTUP\_INFO**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [<span data-ttu-id="91f8e-160">**\_ \_ informations sur le thread système UMS \_**</span><span class="sxs-lookup"><span data-stu-id="91f8e-160">**UMS\_SYSTEM\_THREAD\_INFORMATION**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
