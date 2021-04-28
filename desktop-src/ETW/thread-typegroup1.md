---
description: 'Classe Thread_TypeGroup1 : cette classe est la classe de type d’événement pour les événements de début et de fin de thread. La syntaxe suivante est simplifiée à partir du code MOF.'
ms.assetid: d9e3e33a-0e59-4753-a8d8-5320cbae9d95
title: Classe Thread_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_TypeGroup1
- Thread_TypeGroup1.ProcessId
- Thread_TypeGroup1.TThreadId
- Thread_TypeGroup1.StackBase
- Thread_TypeGroup1.StackLimit
- Thread_TypeGroup1.UserStackBase
- Thread_TypeGroup1.UserStackLimit
- Thread_TypeGroup1.Affinity
- Thread_TypeGroup1.Win32StartAddr
- Thread_TypeGroup1.TebBase
- Thread_TypeGroup1.SubProcessTag
- Thread_TypeGroup1.BasePriority
- Thread_TypeGroup1.PagePriority
- Thread_TypeGroup1.IoPriority
- Thread_TypeGroup1.ThreadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9693bef4449cc076710a74dd9cef88ae608754b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105707"
---
# <a name="thread_typegroup1-class"></a><span data-ttu-id="cdf6a-104">\_Classe TypeGroup1 du thread</span><span class="sxs-lookup"><span data-stu-id="cdf6a-104">Thread\_TypeGroup1 class</span></span>

<span data-ttu-id="cdf6a-105">Cette classe est la classe de type d’événement pour les événements de début et de fin de thread.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="cdf6a-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdf6a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdf6a-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_TypeGroup1 : Thread
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 Affinity;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
  uint8  BasePriority;
  uint8  PagePriority;
  uint8  IoPriority;
  uint8  ThreadFlags;
};
```

## <a name="members"></a><span data-ttu-id="cdf6a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cdf6a-108">Members</span></span>

<span data-ttu-id="cdf6a-109">La classe **thread \_ TypeGroup1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cdf6a-109">The **Thread\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="cdf6a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cdf6a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdf6a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cdf6a-111">Properties</span></span>

<span data-ttu-id="cdf6a-112">La classe **thread \_ TypeGroup1** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-112">The **Thread\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cdf6a-113">Affinité</span><span class="sxs-lookup"><span data-stu-id="cdf6a-113">Affinity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-116">Qualificateurs : WmiDataId (7), pointeur</span><span class="sxs-lookup"><span data-stu-id="cdf6a-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-117">Ensemble des processeurs sur lesquels le thread est autorisé à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-117">The set of processors on which the thread is allowed to run.</span></span>

</dd> <dt>

<span data-ttu-id="cdf6a-118">BasePriority</span><span class="sxs-lookup"><span data-stu-id="cdf6a-118">BasePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-119">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-121">Qualificateurs : WmiDataId (11)</span><span class="sxs-lookup"><span data-stu-id="cdf6a-121">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-122">Priorité du planificateur du thread (consultez la fonction [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) ).</span><span class="sxs-lookup"><span data-stu-id="cdf6a-122">The scheduler priority of the thread (see the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function).</span></span>

</dd> <dt>

<span data-ttu-id="cdf6a-123">IoPriority</span><span class="sxs-lookup"><span data-stu-id="cdf6a-123">IoPriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-124">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-126">Qualificateurs : WmiDataId (13)</span><span class="sxs-lookup"><span data-stu-id="cdf6a-126">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-127">Indicateur de priorité d’e/s pour la planification d’IOs généré par le thread.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-127">An IO priority hint for scheduling IOs generated by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="cdf6a-128">PagePriority</span><span class="sxs-lookup"><span data-stu-id="cdf6a-128">PagePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-129">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-131">Qualificateurs : WmiDataId (12)</span><span class="sxs-lookup"><span data-stu-id="cdf6a-131">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-132">Indicateur de priorité de page mémoire pour les pages mémoire accessibles par le thread.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-132">A memory page priority hint for memory pages accessed by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="cdf6a-133">ProcessId</span><span class="sxs-lookup"><span data-stu-id="cdf6a-133">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-136">Qualificateurs : WmiDataId (1), format ("x")</span><span class="sxs-lookup"><span data-stu-id="cdf6a-136">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-137">Identificateur de processus du thread impliqué dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-137">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="cdf6a-138">StackBase</span><span class="sxs-lookup"><span data-stu-id="cdf6a-138">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-141">Qualificateurs : WmiDataId (3), pointeur</span><span class="sxs-lookup"><span data-stu-id="cdf6a-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-142">Adresse de base de la pile du thread.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-142">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="cdf6a-143">StackLimit</span><span class="sxs-lookup"><span data-stu-id="cdf6a-143">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-144">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-146">Qualificateurs : WmiDataId (4), pointeur</span><span class="sxs-lookup"><span data-stu-id="cdf6a-146">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-147">Limite de la pile du thread.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-147">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="cdf6a-148">SubProcessTag</span><span class="sxs-lookup"><span data-stu-id="cdf6a-148">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-151">Qualificateurs : WmiDataId (10), format ("x")</span><span class="sxs-lookup"><span data-stu-id="cdf6a-151">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-152">Identifie le service si le thread appartient à un service ; Sinon, zéro.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-152">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="cdf6a-153">TebBase</span><span class="sxs-lookup"><span data-stu-id="cdf6a-153">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-154">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-156">Qualificateurs : WmiDataId (9), pointeur</span><span class="sxs-lookup"><span data-stu-id="cdf6a-156">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-157">Adresse de base du bloc de l’environnement du thread.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-157">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="cdf6a-158">ThreadFlags</span><span class="sxs-lookup"><span data-stu-id="cdf6a-158">ThreadFlags</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-159">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-161">Qualificateurs : WmiDataId (14)</span><span class="sxs-lookup"><span data-stu-id="cdf6a-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-162">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-162">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cdf6a-163">TThreadId</span><span class="sxs-lookup"><span data-stu-id="cdf6a-163">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-164">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-166">Qualificateurs : WmiDataId (2), format ("x")</span><span class="sxs-lookup"><span data-stu-id="cdf6a-166">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-167">Identificateur de thread du thread impliqué dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-167">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="cdf6a-168">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="cdf6a-168">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-169">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-171">Qualificateurs : WmiDataId (5), pointeur</span><span class="sxs-lookup"><span data-stu-id="cdf6a-171">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-172">Adresse de base de la pile du mode utilisateur du thread.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-172">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="cdf6a-173">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="cdf6a-173">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-174">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-176">Qualificateurs : WmiDataId (6), pointeur</span><span class="sxs-lookup"><span data-stu-id="cdf6a-176">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-177">Limite de la pile du mode utilisateur du thread.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-177">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="cdf6a-178">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="cdf6a-178">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdf6a-179">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cdf6a-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdf6a-181">Qualificateurs : WmiDataId (8), pointeur</span><span class="sxs-lookup"><span data-stu-id="cdf6a-181">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cdf6a-182">Adresse de début de la fonction à exécuter par ce thread.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-182">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdf6a-183">Notes </span><span class="sxs-lookup"><span data-stu-id="cdf6a-183">Remarks</span></span>

<span data-ttu-id="cdf6a-184">Les types d’événements DCStart et DCEnd énumèrent les threads en cours d’exécution au moment où la session du noyau démarre et se termine, respectivement.</span><span class="sxs-lookup"><span data-stu-id="cdf6a-184">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdf6a-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdf6a-185">Requirements</span></span>



| <span data-ttu-id="cdf6a-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdf6a-186">Requirement</span></span> | <span data-ttu-id="cdf6a-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdf6a-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cdf6a-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdf6a-188">Minimum supported client</span></span><br/> | <span data-ttu-id="cdf6a-189">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdf6a-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cdf6a-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdf6a-190">Minimum supported server</span></span><br/> | <span data-ttu-id="cdf6a-191">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdf6a-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cdf6a-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdf6a-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdf6a-193">**Thread**</span><span class="sxs-lookup"><span data-stu-id="cdf6a-193">**Thread**</span></span>](thread.md)
</dt> </dl>

 

 
