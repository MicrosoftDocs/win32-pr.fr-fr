---
description: Représente un événement de création de classe, qui est un type d’événement intrinsèque généré lorsqu’une nouvelle classe est ajoutée à l’espace de noms.
ms.assetid: a946a8eb-498c-4104-b80f-e520b0e62e36
ms.tgt_platform: multiple
title: Classe __ClassCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 18994ee7067e44a9199de9b62f7ff278a8bece00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523243"
---
# <a name="__classcreationevent-class"></a><span data-ttu-id="4f288-103">\_\_ClassCreationEvent, classe</span><span class="sxs-lookup"><span data-stu-id="4f288-103">\_\_ClassCreationEvent class</span></span>

<span data-ttu-id="4f288-104">La classe système **\_ \_ ClassCreationEvent** représente un événement de création de classe, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) généré lorsqu’une nouvelle classe est ajoutée à l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="4f288-104">The **\_\_ClassCreationEvent** system class represents a class creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a new class is added to the namespace.</span></span>

<span data-ttu-id="4f288-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4f288-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4f288-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4f288-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f288-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f288-107">Syntax</span></span>

``` syntax
class __ClassCreationEvent : __ClassOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="4f288-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4f288-108">Members</span></span>

<span data-ttu-id="4f288-109">La classe **\_ \_ ClassCreationEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4f288-109">The **\_\_ClassCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="4f288-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f288-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f288-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f288-111">Properties</span></span>

<span data-ttu-id="4f288-112">La classe **\_ \_ ClassCreationEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f288-112">The **\_\_ClassCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f288-113">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="4f288-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f288-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="4f288-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4f288-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f288-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f288-116">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="4f288-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="4f288-117">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="4f288-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f288-118">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="4f288-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f288-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="4f288-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4f288-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f288-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f288-121">Copie de la classe nouvellement créée signalée par l’événement de création de classe.</span><span class="sxs-lookup"><span data-stu-id="4f288-121">Copy of the newly created class reported by the class creation event.</span></span> <span data-ttu-id="4f288-122">Cette propriété est héritée de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="4f288-122">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f288-123">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="4f288-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f288-124">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4f288-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f288-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f288-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f288-126">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="4f288-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="4f288-127">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="4f288-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="4f288-128">Les informations sont au format UTC (Universal Time Coordinates).</span><span class="sxs-lookup"><span data-stu-id="4f288-128">The information is in the Universal Time Coordinates (UTC) format.</span></span> <span data-ttu-id="4f288-129">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="4f288-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="4f288-130">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4f288-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f288-131">Notes</span><span class="sxs-lookup"><span data-stu-id="4f288-131">Remarks</span></span>

<span data-ttu-id="4f288-132">La classe **\_ \_ ClassCreationEvent** est dérivée de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="4f288-132">The **\_\_ClassCreationEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f288-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f288-133">Requirements</span></span>



| <span data-ttu-id="4f288-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f288-134">Requirement</span></span> | <span data-ttu-id="4f288-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f288-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4f288-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f288-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4f288-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f288-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4f288-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f288-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4f288-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f288-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4f288-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4f288-140">Namespace</span></span><br/>                | <span data-ttu-id="4f288-141">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="4f288-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4f288-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f288-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f288-143">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="4f288-143">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="4f288-144">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="4f288-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

