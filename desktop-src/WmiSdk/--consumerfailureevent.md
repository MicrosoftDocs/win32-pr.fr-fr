---
description: Représente l’occurrence d’un autre événement qui est supprimé en raison de l’échec d’un consommateur d’événements.
ms.assetid: bb6a1ce9-72a2-4528-8bc8-71ac053b6b1d
ms.tgt_platform: multiple
title: Classe __ConsumerFailureEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ConsumerFailureEvent
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 571785245c05d18678c10a65b192a25022fff8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539756"
---
# <a name="__consumerfailureevent-class"></a><span data-ttu-id="515e5-103">\_\_ConsumerFailureEvent, classe</span><span class="sxs-lookup"><span data-stu-id="515e5-103">\_\_ConsumerFailureEvent class</span></span>

<span data-ttu-id="515e5-104">La classe système **\_ \_ ConsumerFailureEvent** représente l’occurrence d’un autre événement qui est supprimé en raison de l’échec d’un consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="515e5-104">The **\_\_ConsumerFailureEvent** system class represents the occurrence of some other event that is being dropped because of the failure of an event consumer.</span></span>

<span data-ttu-id="515e5-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="515e5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="515e5-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="515e5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="515e5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="515e5-107">Syntax</span></span>

``` syntax
class __ConsumerFailureEvent : __EventDroppedEvent
{
  uint32              ErrorCode;
  string              ErrorDescription;
  object              ErrorObject;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="515e5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="515e5-108">Members</span></span>

<span data-ttu-id="515e5-109">La classe **\_ \_ ConsumerFailureEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="515e5-109">The **\_\_ConsumerFailureEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="515e5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="515e5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="515e5-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="515e5-111">Properties</span></span>

<span data-ttu-id="515e5-112">La classe **\_ \_ ConsumerFailureEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="515e5-112">The **\_\_ConsumerFailureEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="515e5-113">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="515e5-113">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="515e5-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="515e5-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="515e5-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="515e5-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="515e5-116">Code d’erreur retourné par le consommateur.</span><span class="sxs-lookup"><span data-stu-id="515e5-116">Error code returned by the consumer.</span></span>

</dd> <dt>

<span data-ttu-id="515e5-117">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="515e5-117">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="515e5-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="515e5-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="515e5-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="515e5-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="515e5-120">Description du code d’erreur étendue, si disponible.</span><span class="sxs-lookup"><span data-stu-id="515e5-120">Extended error code description, if available.</span></span>

</dd> <dt>

<span data-ttu-id="515e5-121">**ErrorObject**</span><span class="sxs-lookup"><span data-stu-id="515e5-121">**ErrorObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="515e5-122">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="515e5-122">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="515e5-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="515e5-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="515e5-124">Objet erroné.</span><span class="sxs-lookup"><span data-stu-id="515e5-124">Object in error.</span></span>

</dd> <dt>

<span data-ttu-id="515e5-125">**Event**</span><span class="sxs-lookup"><span data-stu-id="515e5-125">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="515e5-126">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="515e5-126">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="515e5-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="515e5-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="515e5-128">Événement erroné.</span><span class="sxs-lookup"><span data-stu-id="515e5-128">Event in error.</span></span> <span data-ttu-id="515e5-129">Cette propriété est héritée de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="515e5-129">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="515e5-130">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="515e5-130">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="515e5-131">Type de données : **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="515e5-131">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="515e5-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="515e5-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="515e5-133">Référence au consommateur prévu.</span><span class="sxs-lookup"><span data-stu-id="515e5-133">Reference to the intended consumer.</span></span> <span data-ttu-id="515e5-134">Cette propriété est héritée de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="515e5-134">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="515e5-135">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="515e5-135">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="515e5-136">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="515e5-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="515e5-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="515e5-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="515e5-138">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="515e5-138">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="515e5-139">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="515e5-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="515e5-140">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="515e5-140">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="515e5-141">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="515e5-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="515e5-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="515e5-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="515e5-143">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="515e5-143">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="515e5-144">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="515e5-144">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="515e5-145">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="515e5-145">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="515e5-146">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="515e5-146">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="515e5-147">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="515e5-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="515e5-148">Notes</span><span class="sxs-lookup"><span data-stu-id="515e5-148">Remarks</span></span>

<span data-ttu-id="515e5-149">La classe **\_ \_ ConsumerFailureEvent** est dérivée de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="515e5-149">The **\_\_ConsumerFailureEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="515e5-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="515e5-150">Requirements</span></span>



| <span data-ttu-id="515e5-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="515e5-151">Requirement</span></span> | <span data-ttu-id="515e5-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="515e5-152">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="515e5-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="515e5-153">Minimum supported client</span></span><br/> | <span data-ttu-id="515e5-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="515e5-154">Windows Vista</span></span><br/>       |
| <span data-ttu-id="515e5-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="515e5-155">Minimum supported server</span></span><br/> | <span data-ttu-id="515e5-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="515e5-156">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="515e5-157">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="515e5-157">Namespace</span></span><br/>                | <span data-ttu-id="515e5-158">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="515e5-158">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="515e5-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="515e5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="515e5-160">**\_\_EventDroppedEvent**</span><span class="sxs-lookup"><span data-stu-id="515e5-160">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="515e5-161">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="515e5-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

