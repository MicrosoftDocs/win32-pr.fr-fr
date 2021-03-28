---
description: Cette classe est la classe de type d’événement pour les événements de début et de fin de thread. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Classe Thread_V2_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2_TypeGroup1
- Thread_V2_TypeGroup1.ProcessId
- Thread_V2_TypeGroup1.TThreadId
- Thread_V2_TypeGroup1.StackBase
- Thread_V2_TypeGroup1.StackLimit
- Thread_V2_TypeGroup1.UserStackBase
- Thread_V2_TypeGroup1.UserStackLimit
- Thread_V2_TypeGroup1.StartAddr
- Thread_V2_TypeGroup1.Win32StartAddr
- Thread_V2_TypeGroup1.TebBase
- Thread_V2_TypeGroup1.SubProcessTag
api_type:
- NA
api_location: ''
ms.openlocfilehash: c89d573f4eda2580002bedfd0ad17eb9b50c1575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203420"
---
# <a name="thread_v2_typegroup1-class"></a><span data-ttu-id="470ef-104">\_ \_ Classe TypeGroup1 du thread v2</span><span class="sxs-lookup"><span data-stu-id="470ef-104">Thread\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="470ef-105">Cette classe est la classe de type d’événement pour les événements de début et de fin de thread.</span><span class="sxs-lookup"><span data-stu-id="470ef-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="470ef-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="470ef-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="470ef-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="470ef-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V2_TypeGroup1 : Thread_V2
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
};
```

## <a name="members"></a><span data-ttu-id="470ef-108">Membres</span><span class="sxs-lookup"><span data-stu-id="470ef-108">Members</span></span>

<span data-ttu-id="470ef-109">La **classe \_ \_ TypeGroup1 du thread v2** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="470ef-109">The **Thread\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="470ef-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="470ef-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="470ef-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="470ef-111">Properties</span></span>

<span data-ttu-id="470ef-112">La **classe \_ \_ TypeGroup1 du thread v2** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="470ef-112">The **Thread\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="470ef-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="470ef-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470ef-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="470ef-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="470ef-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="470ef-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470ef-116">Qualificateurs : WmiDataId (1), format ("x")</span><span class="sxs-lookup"><span data-stu-id="470ef-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="470ef-117">Identificateur de processus du thread impliqué dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="470ef-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="470ef-118">StackBase</span><span class="sxs-lookup"><span data-stu-id="470ef-118">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470ef-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="470ef-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="470ef-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="470ef-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470ef-121">Qualificateurs : WmiDataId (3), pointeur</span><span class="sxs-lookup"><span data-stu-id="470ef-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="470ef-122">Adresse de base de la pile du thread.</span><span class="sxs-lookup"><span data-stu-id="470ef-122">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="470ef-123">StackLimit</span><span class="sxs-lookup"><span data-stu-id="470ef-123">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470ef-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="470ef-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="470ef-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="470ef-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470ef-126">Qualificateurs : WmiDataId (4), pointeur</span><span class="sxs-lookup"><span data-stu-id="470ef-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="470ef-127">Limite de la pile du thread.</span><span class="sxs-lookup"><span data-stu-id="470ef-127">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="470ef-128">StartAddr</span><span class="sxs-lookup"><span data-stu-id="470ef-128">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470ef-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="470ef-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="470ef-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="470ef-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470ef-131">Qualificateurs : WmiDataId (7), pointeur</span><span class="sxs-lookup"><span data-stu-id="470ef-131">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="470ef-132">Adresse mémoire à laquelle le suivi démarre.</span><span class="sxs-lookup"><span data-stu-id="470ef-132">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="470ef-133">SubProcessTag</span><span class="sxs-lookup"><span data-stu-id="470ef-133">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470ef-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="470ef-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="470ef-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="470ef-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470ef-136">Qualificateurs : WmiDataId (10), format ("x")</span><span class="sxs-lookup"><span data-stu-id="470ef-136">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="470ef-137">Identifie le service si le thread appartient à un service ; Sinon, zéro.</span><span class="sxs-lookup"><span data-stu-id="470ef-137">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="470ef-138">TebBase</span><span class="sxs-lookup"><span data-stu-id="470ef-138">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470ef-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="470ef-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="470ef-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="470ef-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470ef-141">Qualificateurs : WmiDataId (9), pointeur</span><span class="sxs-lookup"><span data-stu-id="470ef-141">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="470ef-142">Adresse de base du bloc de l’environnement du thread.</span><span class="sxs-lookup"><span data-stu-id="470ef-142">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="470ef-143">TThreadId</span><span class="sxs-lookup"><span data-stu-id="470ef-143">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470ef-144">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="470ef-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="470ef-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="470ef-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470ef-146">Qualificateurs : WmiDataId (2), format ("x")</span><span class="sxs-lookup"><span data-stu-id="470ef-146">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="470ef-147">Identificateur de thread du thread impliqué dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="470ef-147">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="470ef-148">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="470ef-148">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470ef-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="470ef-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="470ef-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="470ef-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470ef-151">Qualificateurs : WmiDataId (5), pointeur</span><span class="sxs-lookup"><span data-stu-id="470ef-151">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="470ef-152">Adresse de base de la pile du mode utilisateur du thread.</span><span class="sxs-lookup"><span data-stu-id="470ef-152">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="470ef-153">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="470ef-153">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470ef-154">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="470ef-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="470ef-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="470ef-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470ef-156">Qualificateurs : WmiDataId (6), pointeur</span><span class="sxs-lookup"><span data-stu-id="470ef-156">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="470ef-157">Limite de la pile du mode utilisateur du thread.</span><span class="sxs-lookup"><span data-stu-id="470ef-157">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="470ef-158">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="470ef-158">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470ef-159">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="470ef-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="470ef-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="470ef-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470ef-161">Qualificateurs : WmiDataId (8), pointeur</span><span class="sxs-lookup"><span data-stu-id="470ef-161">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="470ef-162">Adresse de début de la fonction à exécuter par ce thread.</span><span class="sxs-lookup"><span data-stu-id="470ef-162">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="470ef-163">Notes</span><span class="sxs-lookup"><span data-stu-id="470ef-163">Remarks</span></span>

<span data-ttu-id="470ef-164">Les types d’événements DCStart et DCEnd énumèrent les threads en cours d’exécution au moment où la session du noyau démarre et se termine, respectivement.</span><span class="sxs-lookup"><span data-stu-id="470ef-164">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="470ef-165">Spécifications</span><span class="sxs-lookup"><span data-stu-id="470ef-165">Requirements</span></span>



| <span data-ttu-id="470ef-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="470ef-166">Requirement</span></span> | <span data-ttu-id="470ef-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="470ef-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="470ef-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="470ef-168">Minimum supported client</span></span><br/> | <span data-ttu-id="470ef-169">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="470ef-169">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="470ef-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="470ef-170">Minimum supported server</span></span><br/> | <span data-ttu-id="470ef-171">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="470ef-171">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="470ef-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="470ef-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="470ef-173">**Thread**</span><span class="sxs-lookup"><span data-stu-id="470ef-173">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="470ef-174">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="470ef-174">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




