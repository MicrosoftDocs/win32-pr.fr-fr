---
description: Cette classe est la classe de type d’événement pour les événements de thread Ready. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: ReadyThread, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: e10029c0397c16a5a5eb30be6e3db64c0baec596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862877"
---
# <a name="readythread-class"></a><span data-ttu-id="d6173-104">ReadyThread, classe</span><span class="sxs-lookup"><span data-stu-id="d6173-104">ReadyThread class</span></span>

<span data-ttu-id="d6173-105">Cette classe est la classe de type d’événement pour les événements de thread Ready.</span><span class="sxs-lookup"><span data-stu-id="d6173-105">This class is the event type class for ready thread events.</span></span>

<span data-ttu-id="d6173-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="d6173-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6173-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6173-107">Syntax</span></span>

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a><span data-ttu-id="d6173-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d6173-108">Members</span></span>

<span data-ttu-id="d6173-109">La classe **ReadyThread** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d6173-109">The **ReadyThread** class has these types of members:</span></span>

-   [<span data-ttu-id="d6173-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d6173-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6173-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d6173-111">Properties</span></span>

<span data-ttu-id="d6173-112">La classe **ReadyThread** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d6173-112">The **ReadyThread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6173-113">AdjustIncrement</span><span class="sxs-lookup"><span data-stu-id="d6173-113">AdjustIncrement</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6173-114">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="d6173-114">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="d6173-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6173-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6173-116">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="d6173-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="d6173-117">Valeur selon laquelle la priorité est ajustée.</span><span class="sxs-lookup"><span data-stu-id="d6173-117">The value by which the priority is being adjusted.</span></span>

</dd> <dt>

<span data-ttu-id="d6173-118">AdjustReason</span><span class="sxs-lookup"><span data-stu-id="d6173-118">AdjustReason</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6173-119">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="d6173-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="d6173-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6173-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6173-121">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="d6173-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="d6173-122">Raison de l’augmentation de la priorité.</span><span class="sxs-lookup"><span data-stu-id="d6173-122">The reason for the priority boost.</span></span>



| <span data-ttu-id="d6173-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6173-123">Value</span></span>                                                                        | <span data-ttu-id="d6173-124">Signification</span><span class="sxs-lookup"><span data-stu-id="d6173-124">Meaning</span></span>                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d6173-125"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d6173-125"><dt>0</dt></span></span> </dl> | <span data-ttu-id="d6173-126">Ignorez l’incrément.</span><span class="sxs-lookup"><span data-stu-id="d6173-126">Ignore the increment.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="d6173-127"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d6173-127"><dt>1</dt></span></span> </dl> | <span data-ttu-id="d6173-128">Appliquez l’incrément, qui va s’atténuer de façon incrémentielle à la fin de chaque Quantum.</span><span class="sxs-lookup"><span data-stu-id="d6173-128">Apply the increment, which will decay incrementally at the end of each quantum.</span></span><br/>                              |
| <dl> <span data-ttu-id="d6173-129"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d6173-129"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d6173-130">Appliquez l’incrément en guise d’augmentation qui va s’atténuer dans son intégralité à Quantum (généralement pour le don prioritaire).</span><span class="sxs-lookup"><span data-stu-id="d6173-130">Apply the increment as a boost that will decay in its entirety at quantum (typically for priority donation).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d6173-131">Indicateur</span><span class="sxs-lookup"><span data-stu-id="d6173-131">Flag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6173-132">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="d6173-132">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="d6173-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6173-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6173-134">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="d6173-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="d6173-135">Les indicateurs d’État possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d6173-135">The following are the possible state flags:</span></span>



| <span data-ttu-id="d6173-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6173-136">Value</span></span>                                                                          | <span data-ttu-id="d6173-137">Signification</span><span class="sxs-lookup"><span data-stu-id="d6173-137">Meaning</span></span>                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d6173-138"><dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="d6173-138"><dt>0x1</dt></span></span> </dl> | <span data-ttu-id="d6173-139">Le thread a été préparé à partir du DPC (appel de procédure différé).</span><span class="sxs-lookup"><span data-stu-id="d6173-139">The thread has been readied from DPC (deferred procedure call).</span></span><br/> |
| <dl> <span data-ttu-id="d6173-140"><dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="d6173-140"><dt>0x2</dt></span></span> </dl> | <span data-ttu-id="d6173-141">La pile du noyau est actuellement remplacée.</span><span class="sxs-lookup"><span data-stu-id="d6173-141">The kernel stack is currently swapped out.</span></span><br/>                      |
| <dl> <span data-ttu-id="d6173-142"><dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="d6173-142"><dt>0x4</dt></span></span> </dl> | <span data-ttu-id="d6173-143">L’espace d’adressage du processus est échangé.</span><span class="sxs-lookup"><span data-stu-id="d6173-143">The process address space is swapped out.</span></span><br/>                       |



 

<span data-ttu-id="d6173-144">Notez que lorsque la pile du noyau ou l’espace d’adressage du processus est échangé, il y a un événement ReadyThread supplémentaire après la pile du noyau ou l’espace d’adressage du processus est rétabli et le thread est prêt à être distribué.</span><span class="sxs-lookup"><span data-stu-id="d6173-144">Note that when the kernel stack or the process address space is swapped out, there will be an additional ReadyThread event after the kernel stack or the process address space has been swapped back in and the thread is made ready to be dispatched.</span></span>

</dd> <dt>

<span data-ttu-id="d6173-145">Réservé</span><span class="sxs-lookup"><span data-stu-id="d6173-145">Reserved</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6173-146">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="d6173-146">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="d6173-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6173-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6173-148">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="d6173-148">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="d6173-149">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d6173-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d6173-150">TThreadId</span><span class="sxs-lookup"><span data-stu-id="d6173-150">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6173-151">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6173-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6173-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6173-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6173-153">Qualificateurs : WmiDataId (1), format ("x")</span><span class="sxs-lookup"><span data-stu-id="d6173-153">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="d6173-154">Identificateur de thread du thread en cours de préparation pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d6173-154">The thread identifier of the thread being readied for execution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6173-155">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d6173-155">Requirements</span></span>



| <span data-ttu-id="d6173-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6173-156">Requirement</span></span> | <span data-ttu-id="d6173-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6173-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d6173-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6173-158">Minimum supported client</span></span><br/> | <span data-ttu-id="d6173-159">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6173-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d6173-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6173-160">Minimum supported server</span></span><br/> | <span data-ttu-id="d6173-161">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6173-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d6173-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6173-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6173-163">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="d6173-163">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




