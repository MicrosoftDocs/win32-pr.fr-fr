---
description: Représente un événement de modification de classe, qui est un type d’événement intrinsèque généré lorsqu’une classe est modifiée dans l’espace de noms.
ms.assetid: 77e8e025-d584-495d-98f8-71e7fb2c9698
ms.tgt_platform: multiple
title: Classe __ClassModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 3634b632fa9ab66f0da3e48bf77fab5875daf12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536672"
---
# <a name="__classmodificationevent-class"></a><span data-ttu-id="71f71-103">\_\_ClassModificationEvent, classe</span><span class="sxs-lookup"><span data-stu-id="71f71-103">\_\_ClassModificationEvent class</span></span>

<span data-ttu-id="71f71-104">La classe système **\_ \_ ClassModificationEvent** représente un événement de modification de classe, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) généré lorsqu’une classe est modifiée dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="71f71-104">The **\_\_ClassModificationEvent** system class represents a class modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a class is changed in the namespace.</span></span>

<span data-ttu-id="71f71-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="71f71-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="71f71-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="71f71-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f71-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71f71-107">Syntax</span></span>

``` syntax
class __ClassModificationEvent : __ClassOperationEvent
{
  object PreviousClass;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="71f71-108">Membres</span><span class="sxs-lookup"><span data-stu-id="71f71-108">Members</span></span>

<span data-ttu-id="71f71-109">La classe **\_ \_ ClassModificationEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="71f71-109">The **\_\_ClassModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="71f71-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="71f71-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71f71-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="71f71-111">Properties</span></span>

<span data-ttu-id="71f71-112">La classe **\_ \_ ClassModificationEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="71f71-112">The **\_\_ClassModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71f71-113">**PreviousClass**</span><span class="sxs-lookup"><span data-stu-id="71f71-113">**PreviousClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f71-114">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="71f71-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="71f71-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f71-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71f71-116">Copie de la version d’origine de la classe.</span><span class="sxs-lookup"><span data-stu-id="71f71-116">Copy of the original version of the class.</span></span>

</dd> <dt>

<span data-ttu-id="71f71-117">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="71f71-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f71-118">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="71f71-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="71f71-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f71-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71f71-120">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="71f71-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="71f71-121">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="71f71-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="71f71-122">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="71f71-122">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f71-123">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="71f71-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="71f71-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f71-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71f71-125">Copie de la classe récemment modifiée signalée par l’événement de modification de classe.</span><span class="sxs-lookup"><span data-stu-id="71f71-125">Copy of the newly modified class reported by the class modification event.</span></span> <span data-ttu-id="71f71-126">Cette propriété est héritée de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="71f71-126">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="71f71-127">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="71f71-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f71-128">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71f71-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71f71-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f71-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71f71-130">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="71f71-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="71f71-131">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="71f71-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="71f71-132">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="71f71-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="71f71-133">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="71f71-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="71f71-134">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="71f71-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71f71-135">Notes</span><span class="sxs-lookup"><span data-stu-id="71f71-135">Remarks</span></span>

<span data-ttu-id="71f71-136">La classe **\_ \_ ClassModificationEvent** est dérivée de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="71f71-136">The **\_\_ClassModificationEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="71f71-137">L’événement indique à la fois les versions nouvelles et anciennes de la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="71f71-137">The event reports both the new and old versions of the class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="71f71-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71f71-138">Requirements</span></span>



| <span data-ttu-id="71f71-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71f71-139">Requirement</span></span> | <span data-ttu-id="71f71-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="71f71-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="71f71-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71f71-141">Minimum supported client</span></span><br/> | <span data-ttu-id="71f71-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71f71-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="71f71-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71f71-143">Minimum supported server</span></span><br/> | <span data-ttu-id="71f71-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71f71-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="71f71-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="71f71-145">Namespace</span></span><br/>                | <span data-ttu-id="71f71-146">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="71f71-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="71f71-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71f71-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f71-148">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="71f71-148">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="71f71-149">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="71f71-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

