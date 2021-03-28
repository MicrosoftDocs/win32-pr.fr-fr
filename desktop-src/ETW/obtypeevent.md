---
description: Représente la classe de type d’événement pour les événements de type objet liés au début et à la fin de la collecte de données.
ms.assetid: 16b21f61-e734-4f51-9b11-e507b5957107
title: ObTypeEvent, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTypeEvent
- ObTypeEvent.ObjectType
- ObTypeEvent.Reserved
- ObTypeEvent.TypeName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d80d5fbe57565d64e9ea53587d7a2c3488e6cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115766"
---
# <a name="obtypeevent-class"></a><span data-ttu-id="92cc2-103">ObTypeEvent, classe</span><span class="sxs-lookup"><span data-stu-id="92cc2-103">ObTypeEvent class</span></span>

<span data-ttu-id="92cc2-104">Représente la classe de type d’événement pour les événements de type objet liés au début et à la fin de la collecte de données.</span><span class="sxs-lookup"><span data-stu-id="92cc2-104">Represents the event type class for object type events related to the beginning and end of data collection.</span></span> <span data-ttu-id="92cc2-105">Cet événement implique le mappage des valeurs d’index de type avec les noms de types.</span><span class="sxs-lookup"><span data-stu-id="92cc2-105">This event involves the mapping of the type index values to the type names.</span></span>

<span data-ttu-id="92cc2-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="92cc2-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="92cc2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92cc2-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{36,37}, EventTypeName{TypeDCStart,TypeDCEnd}]
class ObTypeEvent : ObTrace
{
  uint16 ObjectType;
  uint16 Reserved;
  string TypeName;
};
```

## <a name="members"></a><span data-ttu-id="92cc2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="92cc2-108">Members</span></span>

<span data-ttu-id="92cc2-109">La classe **ObTypeEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="92cc2-109">The **ObTypeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="92cc2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92cc2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92cc2-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92cc2-111">Properties</span></span>

<span data-ttu-id="92cc2-112">La classe **ObTypeEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="92cc2-112">The **ObTypeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92cc2-113">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="92cc2-113">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92cc2-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92cc2-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92cc2-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92cc2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92cc2-116">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="92cc2-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="92cc2-117">Type d'objet.</span><span class="sxs-lookup"><span data-stu-id="92cc2-117">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="92cc2-118">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="92cc2-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92cc2-119">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92cc2-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92cc2-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92cc2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92cc2-121">Qualificateurs : [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="92cc2-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="92cc2-122">Réservé.</span><span class="sxs-lookup"><span data-stu-id="92cc2-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="92cc2-123">**TypeName**</span><span class="sxs-lookup"><span data-stu-id="92cc2-123">**TypeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92cc2-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92cc2-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92cc2-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92cc2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92cc2-126">Qualificateurs : [**format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="92cc2-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="92cc2-127">Nom du type.</span><span class="sxs-lookup"><span data-stu-id="92cc2-127">The type name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92cc2-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="92cc2-128">Requirements</span></span>



| <span data-ttu-id="92cc2-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92cc2-129">Requirement</span></span> | <span data-ttu-id="92cc2-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="92cc2-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92cc2-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92cc2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="92cc2-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92cc2-132">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="92cc2-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92cc2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="92cc2-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92cc2-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="92cc2-135">MOF</span><span class="sxs-lookup"><span data-stu-id="92cc2-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92cc2-136"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92cc2-136"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




