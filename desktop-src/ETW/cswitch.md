---
description: Cette classe est la classe de type d’événement pour les événements de changement de contexte. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 3f9f84d0-18a9-493c-b104-8236b2bd8404
title: CSwitch, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSwitch
- CSwitch.NewThreadId
- CSwitch.OldThreadId
- CSwitch.NewThreadPriority
- CSwitch.OldThreadPriority
- CSwitch.PreviousCState
- CSwitch.SpareByte
- CSwitch.OldThreadWaitReason
- CSwitch.OldThreadWaitMode
- CSwitch.OldThreadState
- CSwitch.OldThreadWaitIdealProcessor
- CSwitch.NewThreadWaitTime
- CSwitch.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 91004ca276140271e8d73c3fc226e83c4e03d1fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201705"
---
# <a name="cswitch-class"></a><span data-ttu-id="98806-104">CSwitch, classe</span><span class="sxs-lookup"><span data-stu-id="98806-104">CSwitch class</span></span>

<span data-ttu-id="98806-105">Cette classe est la classe de type d’événement pour les événements de changement de contexte.</span><span class="sxs-lookup"><span data-stu-id="98806-105">This class is the event type class for context switch events.</span></span>

<span data-ttu-id="98806-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="98806-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="98806-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98806-107">Syntax</span></span>

``` syntax
[EventType{36}, EventTypeName{"CSwitch"}]
class CSwitch : Thread_V2
{
  uint32 NewThreadId;
  uint32 OldThreadId;
  sint8  NewThreadPriority;
  sint8  OldThreadPriority;
  uint8  PreviousCState;
  sint8  SpareByte;
  sint8  OldThreadWaitReason;
  sint8  OldThreadWaitMode;
  sint8  OldThreadState;
  sint8  OldThreadWaitIdealProcessor;
  uint32 NewThreadWaitTime;
  uint32 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="98806-108">Membres</span><span class="sxs-lookup"><span data-stu-id="98806-108">Members</span></span>

<span data-ttu-id="98806-109">La classe **CSwitch** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="98806-109">The **CSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="98806-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98806-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98806-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98806-111">Properties</span></span>

<span data-ttu-id="98806-112">La classe **CSwitch** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="98806-112">The **CSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98806-113">**NewThreadId**</span><span class="sxs-lookup"><span data-stu-id="98806-113">**NewThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98806-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98806-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98806-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98806-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98806-116">Qualificateurs : WmiDataId (1), format ("x")</span><span class="sxs-lookup"><span data-stu-id="98806-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="98806-117">Nouvel ID de thread après le commutateur.</span><span class="sxs-lookup"><span data-stu-id="98806-117">New thread ID after the switch.</span></span>

</dd> <dt>

<span data-ttu-id="98806-118">**NewThreadPriority**</span><span class="sxs-lookup"><span data-stu-id="98806-118">**NewThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98806-119">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="98806-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="98806-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98806-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98806-121">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="98806-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="98806-122">Priorité de thread du nouveau thread.</span><span class="sxs-lookup"><span data-stu-id="98806-122">Thread priority of the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="98806-123">**NewThreadWaitTime**</span><span class="sxs-lookup"><span data-stu-id="98806-123">**NewThreadWaitTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98806-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98806-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98806-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98806-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98806-126">Qualificateurs : WmiDataId (11), format ("x")</span><span class="sxs-lookup"><span data-stu-id="98806-126">Qualifiers: WmiDataId(11), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="98806-127">Délai d’attente pour le nouveau thread.</span><span class="sxs-lookup"><span data-stu-id="98806-127">Wait time for the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="98806-128">**OldThreadId**</span><span class="sxs-lookup"><span data-stu-id="98806-128">**OldThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98806-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98806-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98806-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98806-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98806-131">Qualificateurs : WmiDataId (2), format ("x")</span><span class="sxs-lookup"><span data-stu-id="98806-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="98806-132">ID de thread précédent.</span><span class="sxs-lookup"><span data-stu-id="98806-132">Previous thread ID.</span></span>

</dd> <dt>

<span data-ttu-id="98806-133">**OldThreadPriority**</span><span class="sxs-lookup"><span data-stu-id="98806-133">**OldThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98806-134">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="98806-134">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="98806-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98806-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98806-136">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="98806-136">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="98806-137">Priorité de thread du thread précédent.</span><span class="sxs-lookup"><span data-stu-id="98806-137">Thread priority of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="98806-138">**OldThreadState**</span><span class="sxs-lookup"><span data-stu-id="98806-138">**OldThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98806-139">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="98806-139">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="98806-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98806-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98806-141">Qualificateurs : WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="98806-141">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="98806-142">État du thread précédent.</span><span class="sxs-lookup"><span data-stu-id="98806-142">State of the previous thread.</span></span> <span data-ttu-id="98806-143">Les valeurs d’État possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="98806-143">The following are the possible state values:</span></span>

| <span data-ttu-id="98806-144">État</span><span class="sxs-lookup"><span data-stu-id="98806-144">State</span></span> | <span data-ttu-id="98806-145">Description</span><span class="sxs-lookup"><span data-stu-id="98806-145">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="98806-146">0</span><span class="sxs-lookup"><span data-stu-id="98806-146">0</span></span>     | <span data-ttu-id="98806-147">Initialized</span><span class="sxs-lookup"><span data-stu-id="98806-147">Initialized</span></span>                                   |
| <span data-ttu-id="98806-148">1</span><span class="sxs-lookup"><span data-stu-id="98806-148">1</span></span>     | <span data-ttu-id="98806-149">Ready</span><span class="sxs-lookup"><span data-stu-id="98806-149">Ready</span></span>                                         |
| <span data-ttu-id="98806-150">2</span><span class="sxs-lookup"><span data-stu-id="98806-150">2</span></span>     | <span data-ttu-id="98806-151">Exécution en cours</span><span class="sxs-lookup"><span data-stu-id="98806-151">Running</span></span>                                       |
| <span data-ttu-id="98806-152">3</span><span class="sxs-lookup"><span data-stu-id="98806-152">3</span></span>     | <span data-ttu-id="98806-153">Standby</span><span class="sxs-lookup"><span data-stu-id="98806-153">Standby</span></span>                                       |
| <span data-ttu-id="98806-154">4</span><span class="sxs-lookup"><span data-stu-id="98806-154">4</span></span>     | <span data-ttu-id="98806-155">Terminé</span><span class="sxs-lookup"><span data-stu-id="98806-155">Terminated</span></span>                                    |
| <span data-ttu-id="98806-156">5</span><span class="sxs-lookup"><span data-stu-id="98806-156">5</span></span>     | <span data-ttu-id="98806-157">En attente</span><span class="sxs-lookup"><span data-stu-id="98806-157">Waiting</span></span>                                       |
| <span data-ttu-id="98806-158">6</span><span class="sxs-lookup"><span data-stu-id="98806-158">6</span></span>     | <span data-ttu-id="98806-159">Transition</span><span class="sxs-lookup"><span data-stu-id="98806-159">Transition</span></span>                                    |
| <span data-ttu-id="98806-160">7</span><span class="sxs-lookup"><span data-stu-id="98806-160">7</span></span>     | <span data-ttu-id="98806-161">DeferredReady (ajouté pour Windows Server 2003)</span><span class="sxs-lookup"><span data-stu-id="98806-161">DeferredReady (added for Windows Server 2003)</span></span> |



 

</dd> <dt>

<span data-ttu-id="98806-162">**OldThreadWaitIdealProcessor**</span><span class="sxs-lookup"><span data-stu-id="98806-162">**OldThreadWaitIdealProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98806-163">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="98806-163">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="98806-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98806-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98806-165">Qualificateurs : WmiDataId (10), format ("x")</span><span class="sxs-lookup"><span data-stu-id="98806-165">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="98806-166">Délai d’attente idéal du thread précédent.</span><span class="sxs-lookup"><span data-stu-id="98806-166">Ideal wait time of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="98806-167">**OldThreadWaitMode**</span><span class="sxs-lookup"><span data-stu-id="98806-167">**OldThreadWaitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98806-168">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="98806-168">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="98806-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98806-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98806-170">Qualificateurs : WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="98806-170">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="98806-171">Mode d’attente pour le thread précédent.</span><span class="sxs-lookup"><span data-stu-id="98806-171">Wait mode for the previous thread.</span></span> <span data-ttu-id="98806-172">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="98806-172">The following are the possible values:</span></span>

| <span data-ttu-id="98806-173">État</span><span class="sxs-lookup"><span data-stu-id="98806-173">State</span></span> | <span data-ttu-id="98806-174">Description</span><span class="sxs-lookup"><span data-stu-id="98806-174">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="98806-175">0</span><span class="sxs-lookup"><span data-stu-id="98806-175">0</span></span>     | <span data-ttu-id="98806-176">Kernelmode.</span><span class="sxs-lookup"><span data-stu-id="98806-176">KernelMode</span></span>  |
| <span data-ttu-id="98806-177">1</span><span class="sxs-lookup"><span data-stu-id="98806-177">1</span></span>     | <span data-ttu-id="98806-178">UserMode</span><span class="sxs-lookup"><span data-stu-id="98806-178">UserMode</span></span>    |



 

</dd> <dt>

<span data-ttu-id="98806-179">**OldThreadWaitReason**</span><span class="sxs-lookup"><span data-stu-id="98806-179">**OldThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98806-180">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="98806-180">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="98806-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98806-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98806-182">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="98806-182">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="98806-183">Raison de l’attente du thread précédent.</span><span class="sxs-lookup"><span data-stu-id="98806-183">Wait reason for the previous thread.</span></span> <span data-ttu-id="98806-184">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="98806-184">The following are the possible values:</span></span>

| <span data-ttu-id="98806-185">État</span><span class="sxs-lookup"><span data-stu-id="98806-185">State</span></span> | <span data-ttu-id="98806-186">Description</span><span class="sxs-lookup"><span data-stu-id="98806-186">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="98806-187">0</span><span class="sxs-lookup"><span data-stu-id="98806-187">0</span></span>     | <span data-ttu-id="98806-188">Executive</span><span class="sxs-lookup"><span data-stu-id="98806-188">Executive</span></span>         |
| <span data-ttu-id="98806-189">1</span><span class="sxs-lookup"><span data-stu-id="98806-189">1</span></span>     | <span data-ttu-id="98806-190">FreePage</span><span class="sxs-lookup"><span data-stu-id="98806-190">FreePage</span></span>          |
| <span data-ttu-id="98806-191">2</span><span class="sxs-lookup"><span data-stu-id="98806-191">2</span></span>     | <span data-ttu-id="98806-192">Du pagein.</span><span class="sxs-lookup"><span data-stu-id="98806-192">PageIn</span></span>            |
| <span data-ttu-id="98806-193">3</span><span class="sxs-lookup"><span data-stu-id="98806-193">3</span></span>     | <span data-ttu-id="98806-194">PoolAllocation</span><span class="sxs-lookup"><span data-stu-id="98806-194">PoolAllocation</span></span>    |
| <span data-ttu-id="98806-195">4</span><span class="sxs-lookup"><span data-stu-id="98806-195">4</span></span>     | <span data-ttu-id="98806-196">DelayExecution</span><span class="sxs-lookup"><span data-stu-id="98806-196">DelayExecution</span></span>    |
| <span data-ttu-id="98806-197">5</span><span class="sxs-lookup"><span data-stu-id="98806-197">5</span></span>     | <span data-ttu-id="98806-198">Interrompu</span><span class="sxs-lookup"><span data-stu-id="98806-198">Suspended</span></span>         |
| <span data-ttu-id="98806-199">6</span><span class="sxs-lookup"><span data-stu-id="98806-199">6</span></span>     | <span data-ttu-id="98806-200">UserRequest</span><span class="sxs-lookup"><span data-stu-id="98806-200">UserRequest</span></span>       |
| <span data-ttu-id="98806-201">7</span><span class="sxs-lookup"><span data-stu-id="98806-201">7</span></span>     | <span data-ttu-id="98806-202">WrExecutive</span><span class="sxs-lookup"><span data-stu-id="98806-202">WrExecutive</span></span>       |
| <span data-ttu-id="98806-203">8</span><span class="sxs-lookup"><span data-stu-id="98806-203">8</span></span>     | <span data-ttu-id="98806-204">WrFreePage</span><span class="sxs-lookup"><span data-stu-id="98806-204">WrFreePage</span></span>        |
| <span data-ttu-id="98806-205">9</span><span class="sxs-lookup"><span data-stu-id="98806-205">9</span></span>     | <span data-ttu-id="98806-206">WrPageIn</span><span class="sxs-lookup"><span data-stu-id="98806-206">WrPageIn</span></span>          |
| <span data-ttu-id="98806-207">10</span><span class="sxs-lookup"><span data-stu-id="98806-207">10</span></span>    | <span data-ttu-id="98806-208">WrPoolAllocation</span><span class="sxs-lookup"><span data-stu-id="98806-208">WrPoolAllocation</span></span>  |
| <span data-ttu-id="98806-209">11</span><span class="sxs-lookup"><span data-stu-id="98806-209">11</span></span>    | <span data-ttu-id="98806-210">WrDelayExecution</span><span class="sxs-lookup"><span data-stu-id="98806-210">WrDelayExecution</span></span>  |
| <span data-ttu-id="98806-211">12</span><span class="sxs-lookup"><span data-stu-id="98806-211">12</span></span>    | <span data-ttu-id="98806-212">WrSuspended</span><span class="sxs-lookup"><span data-stu-id="98806-212">WrSuspended</span></span>       |
| <span data-ttu-id="98806-213">13</span><span class="sxs-lookup"><span data-stu-id="98806-213">13</span></span>    | <span data-ttu-id="98806-214">WrUserRequest</span><span class="sxs-lookup"><span data-stu-id="98806-214">WrUserRequest</span></span>     |
| <span data-ttu-id="98806-215">14</span><span class="sxs-lookup"><span data-stu-id="98806-215">14</span></span>    | <span data-ttu-id="98806-216">WrEventPair</span><span class="sxs-lookup"><span data-stu-id="98806-216">WrEventPair</span></span>       |
| <span data-ttu-id="98806-217">15</span><span class="sxs-lookup"><span data-stu-id="98806-217">15</span></span>    | <span data-ttu-id="98806-218">WrQueue</span><span class="sxs-lookup"><span data-stu-id="98806-218">WrQueue</span></span>           |
| <span data-ttu-id="98806-219">16</span><span class="sxs-lookup"><span data-stu-id="98806-219">16</span></span>    | <span data-ttu-id="98806-220">WrLpcReceive</span><span class="sxs-lookup"><span data-stu-id="98806-220">WrLpcReceive</span></span>      |
| <span data-ttu-id="98806-221">17</span><span class="sxs-lookup"><span data-stu-id="98806-221">17</span></span>    | <span data-ttu-id="98806-222">WrLpcReply</span><span class="sxs-lookup"><span data-stu-id="98806-222">WrLpcReply</span></span>        |
| <span data-ttu-id="98806-223">18</span><span class="sxs-lookup"><span data-stu-id="98806-223">18</span></span>    | <span data-ttu-id="98806-224">WrVirtualMemory</span><span class="sxs-lookup"><span data-stu-id="98806-224">WrVirtualMemory</span></span>   |
| <span data-ttu-id="98806-225">19</span><span class="sxs-lookup"><span data-stu-id="98806-225">19</span></span>    | <span data-ttu-id="98806-226">WrPageOut</span><span class="sxs-lookup"><span data-stu-id="98806-226">WrPageOut</span></span>         |
| <span data-ttu-id="98806-227">20</span><span class="sxs-lookup"><span data-stu-id="98806-227">20</span></span>    | <span data-ttu-id="98806-228">WrRendezvous</span><span class="sxs-lookup"><span data-stu-id="98806-228">WrRendezvous</span></span>      |
| <span data-ttu-id="98806-229">21</span><span class="sxs-lookup"><span data-stu-id="98806-229">21</span></span>    | <span data-ttu-id="98806-230">WrKeyedEvent</span><span class="sxs-lookup"><span data-stu-id="98806-230">WrKeyedEvent</span></span>      |
| <span data-ttu-id="98806-231">22</span><span class="sxs-lookup"><span data-stu-id="98806-231">22</span></span>    | <span data-ttu-id="98806-232">WrTerminated</span><span class="sxs-lookup"><span data-stu-id="98806-232">WrTerminated</span></span>      |
| <span data-ttu-id="98806-233">23</span><span class="sxs-lookup"><span data-stu-id="98806-233">23</span></span>    | <span data-ttu-id="98806-234">WrProcessInSwap</span><span class="sxs-lookup"><span data-stu-id="98806-234">WrProcessInSwap</span></span>   |
| <span data-ttu-id="98806-235">24</span><span class="sxs-lookup"><span data-stu-id="98806-235">24</span></span>    | <span data-ttu-id="98806-236">WrCpuRateControl</span><span class="sxs-lookup"><span data-stu-id="98806-236">WrCpuRateControl</span></span>  |
| <span data-ttu-id="98806-237">25</span><span class="sxs-lookup"><span data-stu-id="98806-237">25</span></span>    | <span data-ttu-id="98806-238">WrCalloutStack</span><span class="sxs-lookup"><span data-stu-id="98806-238">WrCalloutStack</span></span>    |
| <span data-ttu-id="98806-239">26</span><span class="sxs-lookup"><span data-stu-id="98806-239">26</span></span>    | <span data-ttu-id="98806-240">WrKernel</span><span class="sxs-lookup"><span data-stu-id="98806-240">WrKernel</span></span>          |
| <span data-ttu-id="98806-241">27</span><span class="sxs-lookup"><span data-stu-id="98806-241">27</span></span>    | <span data-ttu-id="98806-242">WrResource</span><span class="sxs-lookup"><span data-stu-id="98806-242">WrResource</span></span>        |
| <span data-ttu-id="98806-243">28</span><span class="sxs-lookup"><span data-stu-id="98806-243">28</span></span>    | <span data-ttu-id="98806-244">WrPushLock</span><span class="sxs-lookup"><span data-stu-id="98806-244">WrPushLock</span></span>        |
| <span data-ttu-id="98806-245">29</span><span class="sxs-lookup"><span data-stu-id="98806-245">29</span></span>    | <span data-ttu-id="98806-246">WrMutex</span><span class="sxs-lookup"><span data-stu-id="98806-246">WrMutex</span></span>           |
| <span data-ttu-id="98806-247">30</span><span class="sxs-lookup"><span data-stu-id="98806-247">30</span></span>    | <span data-ttu-id="98806-248">WrQuantumEnd</span><span class="sxs-lookup"><span data-stu-id="98806-248">WrQuantumEnd</span></span>      |
| <span data-ttu-id="98806-249">31</span><span class="sxs-lookup"><span data-stu-id="98806-249">31</span></span>    | <span data-ttu-id="98806-250">WrDispatchInt</span><span class="sxs-lookup"><span data-stu-id="98806-250">WrDispatchInt</span></span>     |
| <span data-ttu-id="98806-251">32</span><span class="sxs-lookup"><span data-stu-id="98806-251">32</span></span>    | <span data-ttu-id="98806-252">WrPreempted</span><span class="sxs-lookup"><span data-stu-id="98806-252">WrPreempted</span></span>       |
| <span data-ttu-id="98806-253">33</span><span class="sxs-lookup"><span data-stu-id="98806-253">33</span></span>    | <span data-ttu-id="98806-254">WrYieldExecution</span><span class="sxs-lookup"><span data-stu-id="98806-254">WrYieldExecution</span></span>  |
| <span data-ttu-id="98806-255">34</span><span class="sxs-lookup"><span data-stu-id="98806-255">34</span></span>    | <span data-ttu-id="98806-256">WrFastMutex</span><span class="sxs-lookup"><span data-stu-id="98806-256">WrFastMutex</span></span>       |
| <span data-ttu-id="98806-257">35</span><span class="sxs-lookup"><span data-stu-id="98806-257">35</span></span>    | <span data-ttu-id="98806-258">WrGuardedMutex</span><span class="sxs-lookup"><span data-stu-id="98806-258">WrGuardedMutex</span></span>    |
| <span data-ttu-id="98806-259">36</span><span class="sxs-lookup"><span data-stu-id="98806-259">36</span></span>    | <span data-ttu-id="98806-260">WrRundown</span><span class="sxs-lookup"><span data-stu-id="98806-260">WrRundown</span></span>         |
| <span data-ttu-id="98806-261">37</span><span class="sxs-lookup"><span data-stu-id="98806-261">37</span></span>    | <span data-ttu-id="98806-262">MaximumWaitReason</span><span class="sxs-lookup"><span data-stu-id="98806-262">MaximumWaitReason</span></span> |



 

</dd> <dt>

<span data-ttu-id="98806-263">**PreviousCState**</span><span class="sxs-lookup"><span data-stu-id="98806-263">**PreviousCState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98806-264">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="98806-264">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="98806-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98806-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98806-266">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="98806-266">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="98806-267">Index de l’État C qui a été utilisé pour la dernière fois par le processeur.</span><span class="sxs-lookup"><span data-stu-id="98806-267">The index of the C-state that was last used by the processor.</span></span> <span data-ttu-id="98806-268">La valeur 0 représente l’état d’inactivité le plus clair avec des valeurs supérieures représentant des États C plus profonds.</span><span class="sxs-lookup"><span data-stu-id="98806-268">A value of 0 represents the lightest idle state with higher values representing deeper C-states.</span></span>

</dd> <dt>

<span data-ttu-id="98806-269">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="98806-269">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98806-270">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98806-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98806-271">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98806-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98806-272">Qualificateurs : WmiDataId (12)</span><span class="sxs-lookup"><span data-stu-id="98806-272">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="98806-273">Réservé.</span><span class="sxs-lookup"><span data-stu-id="98806-273">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="98806-274">**SpareByte**</span><span class="sxs-lookup"><span data-stu-id="98806-274">**SpareByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98806-275">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="98806-275">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="98806-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98806-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98806-277">Qualificateurs : WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="98806-277">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="98806-278">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="98806-278">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98806-279">Notes</span><span class="sxs-lookup"><span data-stu-id="98806-279">Remarks</span></span>

<span data-ttu-id="98806-280">Ces événements produisent un volume élevé d’événements.</span><span class="sxs-lookup"><span data-stu-id="98806-280">These events produce a high volume of events.</span></span>

## <a name="requirements"></a><span data-ttu-id="98806-281">Spécifications</span><span class="sxs-lookup"><span data-stu-id="98806-281">Requirements</span></span>



| <span data-ttu-id="98806-282">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98806-282">Requirement</span></span> | <span data-ttu-id="98806-283">Valeur</span><span class="sxs-lookup"><span data-stu-id="98806-283">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="98806-284">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98806-284">Minimum supported client</span></span><br/> | <span data-ttu-id="98806-285">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98806-285">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="98806-286">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98806-286">Minimum supported server</span></span><br/> | <span data-ttu-id="98806-287">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98806-287">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98806-288">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98806-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98806-289">**Thread**</span><span class="sxs-lookup"><span data-stu-id="98806-289">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="98806-290">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="98806-290">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




