---
description: Représente la classe de type d’événement pour les événements de handle d’objet liés au début et à la fin de la collection de données.
ms.assetid: 96231819-f4ca-4c5c-bc19-4a76add5d3cf
title: ObHandleRundownEvent, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleRundownEvent
- ObHandleRundownEvent.Handle
- ObHandleRundownEvent.Object
- ObHandleRundownEvent.ObjectName
- ObHandleRundownEvent.ObjectType
- ObHandleRundownEvent.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5477acc1851d9799fe2bf68f9b867ab3f4c032fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973431"
---
# <a name="obhandlerundownevent-class"></a><span data-ttu-id="a99f0-103">ObHandleRundownEvent, classe</span><span class="sxs-lookup"><span data-stu-id="a99f0-103">ObHandleRundownEvent class</span></span>

<span data-ttu-id="a99f0-104">Représente la classe de type d’événement pour les événements de handle d’objet liés au début et à la fin de la collection de données.</span><span class="sxs-lookup"><span data-stu-id="a99f0-104">Represents the event type class for object handle events related to the beginning and end of data collection.</span></span> <span data-ttu-id="a99f0-105">Cet événement implique l’énumération de tous les descripteurs lorsque l’arrêt est effectué.</span><span class="sxs-lookup"><span data-stu-id="a99f0-105">This event involves the enumerating of all handles when rundown is performed.</span></span>

<span data-ttu-id="a99f0-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a99f0-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a99f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a99f0-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{38,39}, EventTypeName{HandleDCStart,HandleDCEnd}]
class ObHandleRundownEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="a99f0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a99f0-108">Members</span></span>

<span data-ttu-id="a99f0-109">La classe **ObHandleRundownEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a99f0-109">The **ObHandleRundownEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="a99f0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a99f0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a99f0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a99f0-111">Properties</span></span>

<span data-ttu-id="a99f0-112">La classe **ObHandleRundownEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a99f0-112">The **ObHandleRundownEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a99f0-113">**Handle**</span><span class="sxs-lookup"><span data-stu-id="a99f0-113">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a99f0-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a99f0-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a99f0-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a99f0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a99f0-116">Qualificateurs : [**format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="a99f0-116">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="a99f0-117">Handle d’objet.</span><span class="sxs-lookup"><span data-stu-id="a99f0-117">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="a99f0-118">**Object**</span><span class="sxs-lookup"><span data-stu-id="a99f0-118">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a99f0-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a99f0-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a99f0-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a99f0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a99f0-121">Qualificateurs : [**format**](event-tracing-mof-qualifiers.md) ("x"), [**pointeur**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="a99f0-121">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="a99f0-122">Objet.</span><span class="sxs-lookup"><span data-stu-id="a99f0-122">The object.</span></span>

</dd> <dt>

<span data-ttu-id="a99f0-123">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="a99f0-123">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a99f0-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a99f0-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a99f0-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a99f0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a99f0-126">Qualificateurs : [**format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="a99f0-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="a99f0-127">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="a99f0-127">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="a99f0-128">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="a99f0-128">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a99f0-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a99f0-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a99f0-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a99f0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a99f0-131">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="a99f0-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="a99f0-132">Type d'objet.</span><span class="sxs-lookup"><span data-stu-id="a99f0-132">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="a99f0-133">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="a99f0-133">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a99f0-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a99f0-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a99f0-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a99f0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a99f0-136">Qualificateurs : [**format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="a99f0-136">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="a99f0-137">Identificateur du processus.</span><span class="sxs-lookup"><span data-stu-id="a99f0-137">The process identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a99f0-138">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a99f0-138">Requirements</span></span>



| <span data-ttu-id="a99f0-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a99f0-139">Requirement</span></span> | <span data-ttu-id="a99f0-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="a99f0-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a99f0-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a99f0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a99f0-142">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a99f0-142">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a99f0-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a99f0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a99f0-144">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a99f0-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a99f0-145">MOF</span><span class="sxs-lookup"><span data-stu-id="a99f0-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a99f0-146"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a99f0-146"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




