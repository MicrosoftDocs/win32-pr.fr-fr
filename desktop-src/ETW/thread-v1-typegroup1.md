---
description: Cette classe est la classe de type d’événement pour les événements de démarrage de thread. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 412de56f-4f54-46e8-ab60-d47371247e79
title: Classe Thread_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup1
- Thread_V1_TypeGroup1.ProcessId
- Thread_V1_TypeGroup1.TThreadId
- Thread_V1_TypeGroup1.StackBase
- Thread_V1_TypeGroup1.StackLimit
- Thread_V1_TypeGroup1.UserStackBase
- Thread_V1_TypeGroup1.UserStackLimit
- Thread_V1_TypeGroup1.StartAddr
- Thread_V1_TypeGroup1.Win32StartAddr
- Thread_V1_TypeGroup1.WaitMode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 13c419b417b614eb9022d1cb7c09a84ca705b3dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952237"
---
# <a name="thread_v1_typegroup1-class"></a><span data-ttu-id="b7395-104">\_ \_ Classe TypeGroup1 de thread v1</span><span class="sxs-lookup"><span data-stu-id="b7395-104">Thread\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="b7395-105">Cette classe est la classe de type d’événement pour les événements de démarrage de thread.</span><span class="sxs-lookup"><span data-stu-id="b7395-105">This class is the event type class for thread start events.</span></span>

<span data-ttu-id="b7395-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="b7395-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7395-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7395-107">Syntax</span></span>

``` syntax
[EventType{1, 3}, EventTypeName{"Start", "DCStart"}]
class Thread_V1_TypeGroup1 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  sint8  WaitMode;
};
```

## <a name="members"></a><span data-ttu-id="b7395-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b7395-108">Members</span></span>

<span data-ttu-id="b7395-109">La **classe \_ \_ TypeGroup1 du thread v1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b7395-109">The **Thread\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="b7395-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7395-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7395-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7395-111">Properties</span></span>

<span data-ttu-id="b7395-112">La **classe \_ \_ TypeGroup1 du thread v1** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b7395-112">The **Thread\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7395-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="b7395-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7395-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7395-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7395-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7395-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7395-116">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="b7395-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="b7395-117">Identificateur de processus du thread impliqué dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="b7395-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="b7395-118">**Windows Server 2003 :** Contient le qualificateur format ("x").</span><span class="sxs-lookup"><span data-stu-id="b7395-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b7395-119">StackBase</span><span class="sxs-lookup"><span data-stu-id="b7395-119">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7395-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7395-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7395-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7395-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7395-122">Qualificateurs : WmiDataId (3), pointeur</span><span class="sxs-lookup"><span data-stu-id="b7395-122">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b7395-123">Adresse de base de la pile du thread.</span><span class="sxs-lookup"><span data-stu-id="b7395-123">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="b7395-124">StackLimit</span><span class="sxs-lookup"><span data-stu-id="b7395-124">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7395-125">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7395-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7395-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7395-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7395-127">Qualificateurs : WmiDataId (4), pointeur</span><span class="sxs-lookup"><span data-stu-id="b7395-127">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b7395-128">Limite de la pile du thread.</span><span class="sxs-lookup"><span data-stu-id="b7395-128">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="b7395-129">StartAddr</span><span class="sxs-lookup"><span data-stu-id="b7395-129">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7395-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7395-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7395-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7395-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7395-132">Qualificateurs : WmiDataId (7), pointeur</span><span class="sxs-lookup"><span data-stu-id="b7395-132">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b7395-133">Adresse mémoire à laquelle le suivi démarre.</span><span class="sxs-lookup"><span data-stu-id="b7395-133">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="b7395-134">TThreadId</span><span class="sxs-lookup"><span data-stu-id="b7395-134">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7395-135">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7395-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7395-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7395-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7395-137">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="b7395-137">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="b7395-138">Identificateur de thread du thread impliqué dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="b7395-138">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="b7395-139">**Windows Server 2003 :** Contient le qualificateur format ("x").</span><span class="sxs-lookup"><span data-stu-id="b7395-139">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b7395-140">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="b7395-140">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7395-141">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7395-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7395-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7395-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7395-143">Qualificateurs : WmiDataId (5), pointeur</span><span class="sxs-lookup"><span data-stu-id="b7395-143">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b7395-144">Adresse de base de la pile du mode utilisateur du thread.</span><span class="sxs-lookup"><span data-stu-id="b7395-144">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="b7395-145">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="b7395-145">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7395-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7395-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7395-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7395-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7395-148">Qualificateurs : WmiDataId (6), pointeur</span><span class="sxs-lookup"><span data-stu-id="b7395-148">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b7395-149">Limite de la pile du mode utilisateur du thread.</span><span class="sxs-lookup"><span data-stu-id="b7395-149">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="b7395-150">WaitMode</span><span class="sxs-lookup"><span data-stu-id="b7395-150">WaitMode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7395-151">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="b7395-151">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="b7395-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7395-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7395-153">Qualificateurs : WmiDataId (9), format ("c")</span><span class="sxs-lookup"><span data-stu-id="b7395-153">Qualifiers: WmiDataId(9), Format("c")</span></span>
</dt> </dl>

<span data-ttu-id="b7395-154">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="b7395-154">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b7395-155">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="b7395-155">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7395-156">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7395-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7395-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7395-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7395-158">Qualificateurs : WmiDataId (8), pointeur</span><span class="sxs-lookup"><span data-stu-id="b7395-158">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b7395-159">Adresse de début de la fonction à exécuter par ce thread.</span><span class="sxs-lookup"><span data-stu-id="b7395-159">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7395-160">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b7395-160">Requirements</span></span>



| <span data-ttu-id="b7395-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7395-161">Requirement</span></span> | <span data-ttu-id="b7395-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7395-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b7395-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7395-163">Minimum supported client</span></span><br/> | <span data-ttu-id="b7395-164">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7395-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b7395-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7395-165">Minimum supported server</span></span><br/> | <span data-ttu-id="b7395-166">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7395-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b7395-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7395-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7395-168">**Thread \_ v1**</span><span class="sxs-lookup"><span data-stu-id="b7395-168">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




