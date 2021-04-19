---
description: Signale un événement de suppression d’espace de noms, qui est un type d’événement intrinsèque qui est généré lorsqu’un sous-espace de noms est supprimé de l’espace de noms actuel.
ms.assetid: f7160a90-562d-40d9-9189-32aaabcd81d0
ms.tgt_platform: multiple
title: Classe __NamespaceDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6e23f909718167760c02bbdb38e2a075d04bc516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534733"
---
# <a name="__namespacedeletionevent-class"></a><span data-ttu-id="53bed-103">\_\_NamespaceDeletionEvent, classe</span><span class="sxs-lookup"><span data-stu-id="53bed-103">\_\_NamespaceDeletionEvent class</span></span>

<span data-ttu-id="53bed-104">La classe système **\_ \_ NamespaceDeletionEvent** signale un événement de suppression d’espace de noms, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) qui est généré lorsqu’un sous-espace de noms est supprimé de l’espace de noms actuel.</span><span class="sxs-lookup"><span data-stu-id="53bed-104">The **\_\_NamespaceDeletionEvent** system class reports a namespace deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a sub-namespace is removed from the current namespace.</span></span>

<span data-ttu-id="53bed-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="53bed-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="53bed-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="53bed-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="53bed-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53bed-107">Syntax</span></span>

``` syntax
class __NamespaceDeletionEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="53bed-108">Membres</span><span class="sxs-lookup"><span data-stu-id="53bed-108">Members</span></span>

<span data-ttu-id="53bed-109">La classe **\_ \_ NamespaceDeletionEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="53bed-109">The **\_\_NamespaceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="53bed-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="53bed-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53bed-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="53bed-111">Properties</span></span>

<span data-ttu-id="53bed-112">La classe **\_ \_ NamespaceDeletionEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="53bed-112">The **\_\_NamespaceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53bed-113">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="53bed-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53bed-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="53bed-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="53bed-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53bed-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53bed-116">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir un événement.</span><span class="sxs-lookup"><span data-stu-id="53bed-116">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="53bed-117">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="53bed-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="53bed-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="53bed-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53bed-119">Type de données : **\_ \_ espace de noms**</span><span class="sxs-lookup"><span data-stu-id="53bed-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="53bed-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53bed-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53bed-121">Copie de l’instance d' [**\_ \_ espace de noms**](--namespace.md) qui est supprimée.</span><span class="sxs-lookup"><span data-stu-id="53bed-121">Copy of the [**\_\_Namespace**](--namespace.md) instance that is deleted.</span></span> <span data-ttu-id="53bed-122">La propriété **Name** de l’instance d' **\_ \_ espace de noms** identifie l’espace de noms qui est supprimé.</span><span class="sxs-lookup"><span data-stu-id="53bed-122">The **Name** property of the **\_\_Namespace** instance identifies the namespace that is deleted.</span></span> <span data-ttu-id="53bed-123">Cette propriété est héritée de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="53bed-123">This property is inherited from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="53bed-124">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="53bed-124">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53bed-125">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="53bed-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="53bed-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53bed-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53bed-127">Valeur unique qui indique l’heure à laquelle un événement est généré.</span><span class="sxs-lookup"><span data-stu-id="53bed-127">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="53bed-128">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="53bed-128">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="53bed-129">Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="53bed-129">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="53bed-130">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="53bed-130">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="53bed-131">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="53bed-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53bed-132">Notes</span><span class="sxs-lookup"><span data-stu-id="53bed-132">Remarks</span></span>

<span data-ttu-id="53bed-133">La classe **\_ \_ NamespaceDeletionEvent** est dérivée de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="53bed-133">The **\_\_NamespaceDeletionEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53bed-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53bed-134">Requirements</span></span>



| <span data-ttu-id="53bed-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53bed-135">Requirement</span></span> | <span data-ttu-id="53bed-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="53bed-136">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="53bed-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53bed-137">Minimum supported client</span></span><br/> | <span data-ttu-id="53bed-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53bed-138">Windows Vista</span></span><br/>       |
| <span data-ttu-id="53bed-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53bed-139">Minimum supported server</span></span><br/> | <span data-ttu-id="53bed-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53bed-140">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="53bed-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="53bed-141">Namespace</span></span><br/>                | <span data-ttu-id="53bed-142">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="53bed-142">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="53bed-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53bed-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53bed-144">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="53bed-144">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="53bed-145">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="53bed-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

