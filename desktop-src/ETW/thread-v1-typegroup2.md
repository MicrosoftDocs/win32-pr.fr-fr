---
description: Cette classe est la classe de type d’événement pour les événements de fin de thread. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: c495bf22-04ce-4285-8e7e-152e4ab65823
title: Classe Thread_V1_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup2
- Thread_V1_TypeGroup2.ProcessId
- Thread_V1_TypeGroup2.TThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3e56590127b2317813d7431a1cc646fbe76e35a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527291"
---
# <a name="thread_v1_typegroup2-class"></a><span data-ttu-id="945c8-104">\_ \_ Classe TypeGroup2 de thread v1</span><span class="sxs-lookup"><span data-stu-id="945c8-104">Thread\_V1\_TypeGroup2 class</span></span>

<span data-ttu-id="945c8-105">Cette classe est la classe de type d’événement pour les événements de fin de thread.</span><span class="sxs-lookup"><span data-stu-id="945c8-105">This class is the event type class for thread end events.</span></span>

<span data-ttu-id="945c8-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="945c8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="945c8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="945c8-107">Syntax</span></span>

``` syntax
[EventType{2, 4}, EventTypeName{"End", "DCEnd"}]
class Thread_V1_TypeGroup2 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
};
```

## <a name="members"></a><span data-ttu-id="945c8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="945c8-108">Members</span></span>

<span data-ttu-id="945c8-109">La **classe \_ \_ TypeGroup2 du thread v1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="945c8-109">The **Thread\_V1\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="945c8-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="945c8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="945c8-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="945c8-111">Properties</span></span>

<span data-ttu-id="945c8-112">La **classe \_ \_ TypeGroup2 du thread v1** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="945c8-112">The **Thread\_V1\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="945c8-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="945c8-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="945c8-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="945c8-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="945c8-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="945c8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="945c8-116">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="945c8-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="945c8-117">Identificateur de processus du thread impliqué dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="945c8-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="945c8-118">**Windows Server 2003 :** Contient le qualificateur format ("x").</span><span class="sxs-lookup"><span data-stu-id="945c8-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="945c8-119">TThreadId</span><span class="sxs-lookup"><span data-stu-id="945c8-119">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="945c8-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="945c8-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="945c8-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="945c8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="945c8-122">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="945c8-122">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="945c8-123">Identificateur de thread du thread impliqué dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="945c8-123">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="945c8-124">**Windows Server 2003 :** Contient le qualificateur format ("x").</span><span class="sxs-lookup"><span data-stu-id="945c8-124">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="945c8-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="945c8-125">Requirements</span></span>



| <span data-ttu-id="945c8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="945c8-126">Requirement</span></span> | <span data-ttu-id="945c8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="945c8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="945c8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="945c8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="945c8-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="945c8-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="945c8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="945c8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="945c8-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="945c8-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="945c8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="945c8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="945c8-133">**Thread \_ v1**</span><span class="sxs-lookup"><span data-stu-id="945c8-133">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




