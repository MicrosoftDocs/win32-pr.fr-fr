---
description: Signale quand un événement est abandonné suite à un dépassement de capacité de la file d’attente de remise.
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: Classe __EventQueueOverflowEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventQueueOverflowEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 058b03b8a3311aad805f47a04d20e9f1fa8c2477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520151"
---
# <a name="__eventqueueoverflowevent-class"></a><span data-ttu-id="cb80b-103">\_\_EventQueueOverflowEvent, classe</span><span class="sxs-lookup"><span data-stu-id="cb80b-103">\_\_EventQueueOverflowEvent class</span></span>

<span data-ttu-id="cb80b-104">La classe système **\_ \_ EventQueueOverflowEvent** indique quand un événement est abandonné suite à un dépassement de capacité de la file d’attente de remise.</span><span class="sxs-lookup"><span data-stu-id="cb80b-104">The **\_\_EventQueueOverflowEvent** system class reports when an event is dropped as a result of delivery queue overflow.</span></span>

<span data-ttu-id="cb80b-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cb80b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cb80b-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="cb80b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb80b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb80b-107">Syntax</span></span>

``` syntax
class __EventQueueOverflowEvent : __EventDroppedEvent
{
  uint32              CurrentQueueSize;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="cb80b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cb80b-108">Members</span></span>

<span data-ttu-id="cb80b-109">La classe **\_ \_ EventQueueOverflowEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb80b-109">The **\_\_EventQueueOverflowEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="cb80b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb80b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb80b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb80b-111">Properties</span></span>

<span data-ttu-id="cb80b-112">La classe **\_ \_ EventQueueOverflowEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb80b-112">The **\_\_EventQueueOverflowEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb80b-113">**CurrentQueueSize**</span><span class="sxs-lookup"><span data-stu-id="cb80b-113">**CurrentQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb80b-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb80b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb80b-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb80b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb80b-116">Taille actuelle de la file d’attente, en octets.</span><span class="sxs-lookup"><span data-stu-id="cb80b-116">Current queue size, in bytes.</span></span> <span data-ttu-id="cb80b-117">La valeur par défaut de cette propriété est 10 Mo pour toutes les files d’attente combinées.</span><span class="sxs-lookup"><span data-stu-id="cb80b-117">This property defaults to 10 MB for all queues combined.</span></span>

</dd> <dt>

<span data-ttu-id="cb80b-118">**Event**</span><span class="sxs-lookup"><span data-stu-id="cb80b-118">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb80b-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="cb80b-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cb80b-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb80b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb80b-121">Événement d’intérêt.</span><span class="sxs-lookup"><span data-stu-id="cb80b-121">Event of interest.</span></span> <span data-ttu-id="cb80b-122">Cette propriété est héritée de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="cb80b-122">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb80b-123">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="cb80b-123">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb80b-124">Type de données : **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="cb80b-124">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="cb80b-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb80b-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb80b-126">Référence au consommateur prévu.</span><span class="sxs-lookup"><span data-stu-id="cb80b-126">Reference to the intended consumer.</span></span> <span data-ttu-id="cb80b-127">Cette propriété est héritée de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="cb80b-127">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb80b-128">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="cb80b-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb80b-129">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="cb80b-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="cb80b-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb80b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb80b-131">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="cb80b-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="cb80b-132">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="cb80b-132">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb80b-133">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="cb80b-133">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb80b-134">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cb80b-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cb80b-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb80b-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb80b-136">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="cb80b-136">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="cb80b-137">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="cb80b-137">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="cb80b-138">Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="cb80b-138">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="cb80b-139">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="cb80b-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="cb80b-140">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cb80b-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb80b-141">Notes</span><span class="sxs-lookup"><span data-stu-id="cb80b-141">Remarks</span></span>

<span data-ttu-id="cb80b-142">Seuls les utilisateurs disposant de privilèges d’administrateur peuvent recevoir cet événement.</span><span class="sxs-lookup"><span data-stu-id="cb80b-142">Only users with administrator privileges are able to receive this event.</span></span> <span data-ttu-id="cb80b-143">La classe **\_ \_ EventQueueOverflowEvent** est dérivée de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="cb80b-143">The **\_\_EventQueueOverflowEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

<span data-ttu-id="cb80b-144">Pour plus d’informations, consultez la propriété [**MaximumQueueSize**](--eventconsumer.md) dans la classe [**\_ \_ EventConsumer**](--eventconsumer.md) et la propriété [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) dans la classe **\_ WMISetting Win32** .</span><span class="sxs-lookup"><span data-stu-id="cb80b-144">For more information, see the [**MaximumQueueSize**](--eventconsumer.md) property in the [**\_\_EventConsumer**](--eventconsumer.md) class and the [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property in the **Win32\_WMISetting** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb80b-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb80b-145">Requirements</span></span>



| <span data-ttu-id="cb80b-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb80b-146">Requirement</span></span> | <span data-ttu-id="cb80b-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb80b-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="cb80b-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb80b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="cb80b-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb80b-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="cb80b-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb80b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="cb80b-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb80b-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="cb80b-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cb80b-152">Namespace</span></span><br/>                | <span data-ttu-id="cb80b-153">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="cb80b-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="cb80b-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb80b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb80b-155">**\_\_EventDroppedEvent**</span><span class="sxs-lookup"><span data-stu-id="cb80b-155">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="cb80b-156">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="cb80b-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

