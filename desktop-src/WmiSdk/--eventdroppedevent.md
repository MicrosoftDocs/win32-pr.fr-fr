---
description: Représente l’occurrence d’un événement qui est supprimé. Un événement supprimé est un événement qui n’est pas remis à un consommateur d’événements.
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: Classe __EventDroppedEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventDroppedEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4e9f68328a3c5c455c98e85a65d53156da6eeada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523339"
---
# <a name="__eventdroppedevent-class"></a><span data-ttu-id="ae82c-104">\_\_EventDroppedEvent, classe</span><span class="sxs-lookup"><span data-stu-id="ae82c-104">\_\_EventDroppedEvent class</span></span>

<span data-ttu-id="ae82c-105">La classe système **\_ \_ EventDroppedEvent** représente l’occurrence d’un événement qui est supprimé.</span><span class="sxs-lookup"><span data-stu-id="ae82c-105">The **\_\_EventDroppedEvent** system class represents the occurrence of an event that is dropped.</span></span> <span data-ttu-id="ae82c-106">Un événement supprimé est un événement qui n’est pas remis à un consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="ae82c-106">A dropped event is an event that is not delivered to an event consumer.</span></span>

<span data-ttu-id="ae82c-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ae82c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ae82c-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ae82c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae82c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae82c-109">Syntax</span></span>

``` syntax
class __EventDroppedEvent : __SystemEvent
{
  __Event             Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="ae82c-110">Membres</span><span class="sxs-lookup"><span data-stu-id="ae82c-110">Members</span></span>

<span data-ttu-id="ae82c-111">La classe **\_ \_ EventDroppedEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ae82c-111">The **\_\_EventDroppedEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="ae82c-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ae82c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae82c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ae82c-113">Properties</span></span>

<span data-ttu-id="ae82c-114">La classe **\_ \_ EventDroppedEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ae82c-114">The **\_\_EventDroppedEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae82c-115">**Event**</span><span class="sxs-lookup"><span data-stu-id="ae82c-115">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae82c-116">Type de données : **\_ \_ événement**</span><span class="sxs-lookup"><span data-stu-id="ae82c-116">Data type: **\_\_Event**</span></span>
</dt> <dt>

<span data-ttu-id="ae82c-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ae82c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae82c-118">Événement qui est supprimé.</span><span class="sxs-lookup"><span data-stu-id="ae82c-118">Event that is dropped.</span></span>

</dd> <dt>

<span data-ttu-id="ae82c-119">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="ae82c-119">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae82c-120">Type de données : **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="ae82c-120">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="ae82c-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ae82c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae82c-122">Référence à une instance de [**\_ \_ EventConsumer**](--eventconsumer.md) qui représente le consommateur permanent que vous identifiez pour recevoir un événement.</span><span class="sxs-lookup"><span data-stu-id="ae82c-122">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the permanent consumer you identify to receive an event.</span></span> <span data-ttu-id="ae82c-123">Différents consommateurs permanents qui s’abonnent à un événement peuvent continuer à recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="ae82c-123">Different permanent consumers that subscribe to an event can continue to receive the event.</span></span>

</dd> <dt>

<span data-ttu-id="ae82c-124">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="ae82c-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae82c-125">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ae82c-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ae82c-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ae82c-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae82c-127">Descripteur utilisé par un fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir un événement.</span><span class="sxs-lookup"><span data-stu-id="ae82c-127">Descriptor that an event provider uses to determine the users who can receive an event.</span></span> <span data-ttu-id="ae82c-128">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="ae82c-128">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae82c-129">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="ae82c-129">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae82c-130">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae82c-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae82c-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ae82c-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae82c-132">Valeur unique qui indique l’heure de génération d’un événement.</span><span class="sxs-lookup"><span data-stu-id="ae82c-132">Unique value that indicates the time when an event is generated.</span></span> <span data-ttu-id="ae82c-133">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="ae82c-133">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="ae82c-134">Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="ae82c-134">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="ae82c-135">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="ae82c-135">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="ae82c-136">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ae82c-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae82c-137">Notes</span><span class="sxs-lookup"><span data-stu-id="ae82c-137">Remarks</span></span>

<span data-ttu-id="ae82c-138">La classe **\_ \_ EventDroppedEvent** est dérivée de [**\_ \_ SystemEvent**](--systemevent.md).</span><span class="sxs-lookup"><span data-stu-id="ae82c-138">The **\_\_EventDroppedEvent** class is derived from [**\_\_SystemEvent**](--systemevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae82c-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae82c-139">Requirements</span></span>



| <span data-ttu-id="ae82c-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae82c-140">Requirement</span></span> | <span data-ttu-id="ae82c-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae82c-141">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ae82c-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae82c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ae82c-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae82c-143">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ae82c-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae82c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ae82c-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae82c-145">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ae82c-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ae82c-146">Namespace</span></span><br/>                | <span data-ttu-id="ae82c-147">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="ae82c-147">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ae82c-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae82c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae82c-149">**\_\_SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="ae82c-149">**\_\_SystemEvent**</span></span>](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[<span data-ttu-id="ae82c-150">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="ae82c-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

