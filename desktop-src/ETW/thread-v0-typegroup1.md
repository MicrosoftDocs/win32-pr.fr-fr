---
description: Cette classe est la classe de type d’événement pour les événements de thread. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: cc668fef-48fe-4948-8fe5-4351f7a033d1
title: Classe Thread_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V0_TypeGroup1
- Thread_V0_TypeGroup1.TThreadId
- Thread_V0_TypeGroup1.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f6fa7ae1f50e005fe8f66e918a4a8360a0e8f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972483"
---
# <a name="thread_v0_typegroup1-class"></a><span data-ttu-id="4c3da-104">Thread \_ v0, \_ classe TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="4c3da-104">Thread\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="4c3da-105">Cette classe est la classe de type d’événement pour les événements de thread.</span><span class="sxs-lookup"><span data-stu-id="4c3da-105">This class is the event type class for thread events.</span></span>

<span data-ttu-id="4c3da-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="4c3da-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c3da-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c3da-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V0_TypeGroup1 : Thread_V0
{
  uint32 TThreadId;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="4c3da-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4c3da-108">Members</span></span>

<span data-ttu-id="4c3da-109">La **classe \_ \_ TypeGroup1 du thread v0** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4c3da-109">The **Thread\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="4c3da-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4c3da-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c3da-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4c3da-111">Properties</span></span>

<span data-ttu-id="4c3da-112">La **classe \_ \_ TypeGroup1 du thread v0** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4c3da-112">The **Thread\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c3da-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="4c3da-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c3da-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c3da-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c3da-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c3da-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c3da-116">Qualificateurs : WmiDataId (2), format ("x")</span><span class="sxs-lookup"><span data-stu-id="4c3da-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="4c3da-117">Identificateur de processus du thread impliqué dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="4c3da-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="4c3da-118">TThreadId</span><span class="sxs-lookup"><span data-stu-id="4c3da-118">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c3da-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c3da-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c3da-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c3da-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c3da-121">Qualificateurs : WmiDataId (1), format ("x")</span><span class="sxs-lookup"><span data-stu-id="4c3da-121">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="4c3da-122">Identificateur de thread du thread impliqué dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="4c3da-122">Thread identifier of the thread involved in the event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c3da-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4c3da-123">Requirements</span></span>



| <span data-ttu-id="4c3da-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c3da-124">Requirement</span></span> | <span data-ttu-id="4c3da-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c3da-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4c3da-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c3da-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4c3da-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c3da-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4c3da-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c3da-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4c3da-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c3da-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4c3da-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c3da-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c3da-131">**Thread \_ v0**</span><span class="sxs-lookup"><span data-stu-id="4c3da-131">**Thread\_V0**</span></span>](thread-v0.md)
</dt> </dl>

 

 




