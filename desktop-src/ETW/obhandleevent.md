---
description: Représente la classe de type d’événement pour les événements de création ou de clôture de handle.
ms.assetid: 39d27cdf-fa51-4fb1-8998-7150ca627eff
title: ObHandleEvent, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleEvent
- ObHandleEvent.Handle
- ObHandleEvent.Object
- ObHandleEvent.ObjectName
- ObHandleEvent.ObjectType
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae293684bd09322c7193035d374e5e2bad21447f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973430"
---
# <a name="obhandleevent-class"></a><span data-ttu-id="3f3ed-103">ObHandleEvent, classe</span><span class="sxs-lookup"><span data-stu-id="3f3ed-103">ObHandleEvent class</span></span>

<span data-ttu-id="3f3ed-104">Représente la classe de type d’événement pour les événements de création ou de clôture de handle.</span><span class="sxs-lookup"><span data-stu-id="3f3ed-104">Represents the event type class for handle creation or closure events.</span></span>

<span data-ttu-id="3f3ed-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3f3ed-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f3ed-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f3ed-106">Syntax</span></span>

``` syntax
[Dynamic, EventType{32,33}, EventTypeName{CreateHandle,CloseHandle}]
class ObHandleEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
};
```

## <a name="members"></a><span data-ttu-id="3f3ed-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3f3ed-107">Members</span></span>

<span data-ttu-id="3f3ed-108">La classe **ObHandleEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3f3ed-108">The **ObHandleEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="3f3ed-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3f3ed-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f3ed-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3f3ed-110">Properties</span></span>

<span data-ttu-id="3f3ed-111">La classe **ObHandleEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3f3ed-111">The **ObHandleEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f3ed-112">**Handle**</span><span class="sxs-lookup"><span data-stu-id="3f3ed-112">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3ed-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f3ed-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f3ed-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3ed-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f3ed-115">Qualificateurs : [**format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="3f3ed-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="3f3ed-116">Handle d’objet.</span><span class="sxs-lookup"><span data-stu-id="3f3ed-116">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="3f3ed-117">**Object**</span><span class="sxs-lookup"><span data-stu-id="3f3ed-117">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3ed-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f3ed-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f3ed-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3ed-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f3ed-120">Qualificateurs : [**format**](event-tracing-mof-qualifiers.md) ("x"), [**pointeur**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="3f3ed-120">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="3f3ed-121">Objet.</span><span class="sxs-lookup"><span data-stu-id="3f3ed-121">The object.</span></span>

</dd> <dt>

<span data-ttu-id="3f3ed-122">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="3f3ed-122">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3ed-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f3ed-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f3ed-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3ed-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f3ed-125">Qualificateurs : [**format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="3f3ed-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="3f3ed-126">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="3f3ed-126">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="3f3ed-127">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="3f3ed-127">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f3ed-128">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f3ed-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f3ed-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f3ed-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f3ed-130">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="3f3ed-130">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="3f3ed-131">Type d'objet.</span><span class="sxs-lookup"><span data-stu-id="3f3ed-131">The object type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f3ed-132">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3f3ed-132">Requirements</span></span>



| <span data-ttu-id="3f3ed-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f3ed-133">Requirement</span></span> | <span data-ttu-id="3f3ed-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f3ed-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f3ed-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f3ed-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3f3ed-136">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f3ed-136">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3f3ed-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f3ed-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3f3ed-138">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f3ed-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3f3ed-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3f3ed-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f3ed-140"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f3ed-140"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




