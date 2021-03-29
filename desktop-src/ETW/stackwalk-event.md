---
description: Cette classe est la classe de type d’événement pour les événements de suivi de pile.
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: Classe StackWalk_Event
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk_Event
- StackWalk_Event.EventTimeStamp
- StackWalk_Event.StackProcess
- StackWalk_Event.StackThread
- StackWalk_Event.Stack1
- StackWalk_Event.Stack192
api_type:
- NA
api_location: ''
ms.openlocfilehash: 746a7f2a9b5f6bb6316bf0d0e20e5645cea15a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973414"
---
# <a name="stackwalk_event-class"></a><span data-ttu-id="f926f-103">\_Classe d’événements StackWalk</span><span class="sxs-lookup"><span data-stu-id="f926f-103">StackWalk\_Event class</span></span>

<span data-ttu-id="f926f-104">Cette classe est la classe de type d’événement pour les événements de suivi de pile.</span><span class="sxs-lookup"><span data-stu-id="f926f-104">This class is the event type class for stack tracing events.</span></span>

<span data-ttu-id="f926f-105">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f926f-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f926f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f926f-106">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"Stack"}]
class StackWalk_Event : StackWalk
{
  uint64 EventTimeStamp;
  uint32 StackProcess;
  uint32 StackThread;
  uint32 Stack1;
  uint32 Stack192;
};
```

## <a name="members"></a><span data-ttu-id="f926f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f926f-107">Members</span></span>

<span data-ttu-id="f926f-108">La classe d' **\_ événements StackWalk** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f926f-108">The **StackWalk\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="f926f-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f926f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f926f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f926f-110">Properties</span></span>

<span data-ttu-id="f926f-111">La classe d' **\_ événements StackWalk** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f926f-111">The **StackWalk\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f926f-112">**EventTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="f926f-112">**EventTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f926f-113">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f926f-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f926f-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f926f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f926f-115">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="f926f-115">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="f926f-116">Horodatage de l’événement d’origine à partir de l’en-tête de l’événement.</span><span class="sxs-lookup"><span data-stu-id="f926f-116">Original event time stamp from the event header.</span></span> <span data-ttu-id="f926f-117">Utilisez cet horodatage pour faire correspondre la pile à un événement.</span><span class="sxs-lookup"><span data-stu-id="f926f-117">Use this time stamp to match the stack to an event.</span></span>

</dd> <dt>

<span data-ttu-id="f926f-118">**Stack1**</span><span class="sxs-lookup"><span data-stu-id="f926f-118">**Stack1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f926f-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f926f-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f926f-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f926f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f926f-121">Qualificateurs : WmiDataId (4), pointeur</span><span class="sxs-lookup"><span data-stu-id="f926f-121">Qualifiers: WmiDataId(4), pointer</span></span>
</dt> </dl>

<span data-ttu-id="f926f-122">Adresse de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f926f-122">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="f926f-123">**Stack192**</span><span class="sxs-lookup"><span data-stu-id="f926f-123">**Stack192**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f926f-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f926f-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f926f-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f926f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f926f-126">Qualificateurs : WmiDataId (195), pointeur</span><span class="sxs-lookup"><span data-stu-id="f926f-126">Qualifiers: WmiDataId(195), pointer</span></span>
</dt> </dl>

<span data-ttu-id="f926f-127">Adresse de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f926f-127">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="f926f-128">**StackProcess**</span><span class="sxs-lookup"><span data-stu-id="f926f-128">**StackProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f926f-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f926f-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f926f-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f926f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f926f-131">Qualificateurs : WmiDataId (2), format ("x")</span><span class="sxs-lookup"><span data-stu-id="f926f-131">Qualifiers: WmiDataId(2), format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f926f-132">Identificateur de processus de l’événement d’origine.</span><span class="sxs-lookup"><span data-stu-id="f926f-132">The process identifier of the original event.</span></span>

</dd> <dt>

<span data-ttu-id="f926f-133">**StackThread**</span><span class="sxs-lookup"><span data-stu-id="f926f-133">**StackThread**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f926f-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f926f-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f926f-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f926f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f926f-136">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="f926f-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="f926f-137">Identificateur de thread de l’événement d’origine.</span><span class="sxs-lookup"><span data-stu-id="f926f-137">The thread identifier of the original event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f926f-138">Notes</span><span class="sxs-lookup"><span data-stu-id="f926f-138">Remarks</span></span>

<span data-ttu-id="f926f-139">Notez que la classe n’affiche pas toutes les propriétés **Stack \* n**\* qui existent entre **Stack1** et **Stack192**.</span><span class="sxs-lookup"><span data-stu-id="f926f-139">Note that the class does not show all of the **Stack\*n**\* properties that exist between **Stack1** and **Stack192**.</span></span> <span data-ttu-id="f926f-140">Utilisez la taille de l’événement pour déterminer le nombre de propriétés de **pile \* n**\* qui contiennent des adresses valides.</span><span class="sxs-lookup"><span data-stu-id="f926f-140">Use the size of the event to determine how many **Stack\*n**\* properties contain valid addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="f926f-141">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f926f-141">Requirements</span></span>



| <span data-ttu-id="f926f-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f926f-142">Requirement</span></span> | <span data-ttu-id="f926f-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="f926f-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f926f-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f926f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f926f-145">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f926f-145">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f926f-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f926f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f926f-147">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f926f-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




