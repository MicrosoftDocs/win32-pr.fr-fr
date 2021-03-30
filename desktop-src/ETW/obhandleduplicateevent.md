---
description: Représente la classe de type d’événement pour les événements de la duplication de handle.
ms.assetid: a933ffaa-8c99-4b87-ad00-4c40fa4d8d26
title: ObHandleDuplicateEvent, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleDuplicateEvent
- ObHandleDuplicateEvent.Object
- ObHandleDuplicateEvent.ObjectType
- ObHandleDuplicateEvent.SourceHandle
- ObHandleDuplicateEvent.TargetHandle
- ObHandleDuplicateEvent.TargetProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0f81ff9d85c0c5de8469f563db21e2054fa065f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973715"
---
# <a name="obhandleduplicateevent-class"></a><span data-ttu-id="be73d-103">ObHandleDuplicateEvent, classe</span><span class="sxs-lookup"><span data-stu-id="be73d-103">ObHandleDuplicateEvent class</span></span>

<span data-ttu-id="be73d-104">Représente la classe de type d’événement pour les événements de la duplication de handle.</span><span class="sxs-lookup"><span data-stu-id="be73d-104">Represents the event type class for handle duplication events.</span></span>

<span data-ttu-id="be73d-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="be73d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="be73d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be73d-106">Syntax</span></span>

``` syntax
[Dynamic, EventType(34), EventTypeName("DuplicateHandle")]
class ObHandleDuplicateEvent : ObTrace
{
  uint32 Object;
  uint16 ObjectType;
  uint32 SourceHandle;
  uint32 TargetHandle;
  uint32 TargetProcessId;
};
```

## <a name="members"></a><span data-ttu-id="be73d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="be73d-107">Members</span></span>

<span data-ttu-id="be73d-108">La classe **ObHandleDuplicateEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="be73d-108">The **ObHandleDuplicateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="be73d-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be73d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be73d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be73d-110">Properties</span></span>

<span data-ttu-id="be73d-111">La classe **ObHandleDuplicateEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="be73d-111">The **ObHandleDuplicateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be73d-112">**Object**</span><span class="sxs-lookup"><span data-stu-id="be73d-112">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be73d-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be73d-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be73d-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be73d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be73d-115">Qualificateurs : [**format**](event-tracing-mof-qualifiers.md) ("x"), [**pointeur**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="be73d-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="be73d-116">Objet.</span><span class="sxs-lookup"><span data-stu-id="be73d-116">The object.</span></span>

</dd> <dt>

<span data-ttu-id="be73d-117">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="be73d-117">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be73d-118">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be73d-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be73d-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be73d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be73d-120">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="be73d-120">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="be73d-121">Type d'objet.</span><span class="sxs-lookup"><span data-stu-id="be73d-121">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="be73d-122">**SourceHandle**</span><span class="sxs-lookup"><span data-stu-id="be73d-122">**SourceHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be73d-123">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be73d-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be73d-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be73d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be73d-125">Qualificateurs : [**format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="be73d-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="be73d-126">Handle de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="be73d-126">The handle of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="be73d-127">**TargetHandle**</span><span class="sxs-lookup"><span data-stu-id="be73d-127">**TargetHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be73d-128">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be73d-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be73d-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be73d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be73d-130">Qualificateurs : [**format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="be73d-130">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="be73d-131">Handle de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="be73d-131">The handle of the target object.</span></span>

</dd> <dt>

<span data-ttu-id="be73d-132">**TargetProcessId**</span><span class="sxs-lookup"><span data-stu-id="be73d-132">**TargetProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be73d-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be73d-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be73d-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be73d-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be73d-135">Qualificateurs : [**format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="be73d-135">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="be73d-136">Identificateur de processus de la cible.</span><span class="sxs-lookup"><span data-stu-id="be73d-136">The process identifier of the target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be73d-137">Spécifications</span><span class="sxs-lookup"><span data-stu-id="be73d-137">Requirements</span></span>



| <span data-ttu-id="be73d-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be73d-138">Requirement</span></span> | <span data-ttu-id="be73d-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="be73d-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be73d-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be73d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="be73d-141">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be73d-141">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="be73d-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be73d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="be73d-143">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be73d-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="be73d-144">MOF</span><span class="sxs-lookup"><span data-stu-id="be73d-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be73d-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be73d-145"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




