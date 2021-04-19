---
description: Signale un événement de création d’espace de noms, qui est un type d’événement intrinsèque généré lorsqu’un nouvel espace de noms est ajouté à l’espace de noms actuel.
ms.assetid: 50b9860a-d6e8-4dab-a7d0-09da9dd37b6b
ms.tgt_platform: multiple
title: Classe __NamespaceCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 8432bcfb2c96c70b91a7f0d187297217082e2d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534602"
---
# <a name="__namespacecreationevent-class"></a><span data-ttu-id="8ed04-103">\_\_NamespaceCreationEvent, classe</span><span class="sxs-lookup"><span data-stu-id="8ed04-103">\_\_NamespaceCreationEvent class</span></span>

<span data-ttu-id="8ed04-104">La classe système **\_ \_ NamespaceCreationEvent** signale un événement de création d’espace de noms, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) généré lorsqu’un nouvel espace de noms est ajouté à l’espace de noms actuel.</span><span class="sxs-lookup"><span data-stu-id="8ed04-104">The **\_\_NamespaceCreationEvent** system class reports a namespace creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a new namespace is added to the current namespace.</span></span>

<span data-ttu-id="8ed04-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8ed04-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8ed04-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8ed04-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ed04-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ed04-107">Syntax</span></span>

``` syntax
class __NamespaceCreationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="8ed04-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8ed04-108">Members</span></span>

<span data-ttu-id="8ed04-109">La classe **\_ \_ NamespaceCreationEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8ed04-109">The **\_\_NamespaceCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="8ed04-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8ed04-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ed04-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8ed04-111">Properties</span></span>

<span data-ttu-id="8ed04-112">La classe **\_ \_ NamespaceCreationEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8ed04-112">The **\_\_NamespaceCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8ed04-113">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="8ed04-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed04-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="8ed04-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8ed04-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8ed04-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed04-116">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="8ed04-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="8ed04-117">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="8ed04-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ed04-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="8ed04-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed04-119">Type de données : **\_ \_ espace de noms**</span><span class="sxs-lookup"><span data-stu-id="8ed04-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="8ed04-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8ed04-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed04-121">Copie de l’instance d' [**\_ \_ espace de noms**](--namespace.md) qui a été créée.</span><span class="sxs-lookup"><span data-stu-id="8ed04-121">Copy of the [**\_\_Namespace**](--namespace.md) instance that was created.</span></span> <span data-ttu-id="8ed04-122">La propriété **Name** de l’instance d' **\_ \_ espace de noms** indique l’espace de noms qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="8ed04-122">The **Name** property of the **\_\_Namespace** instance indicates which namespace was created.</span></span> <span data-ttu-id="8ed04-123">Cette propriété est héritée de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="8ed04-123">This property is inherited from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ed04-124">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="8ed04-124">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed04-125">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8ed04-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8ed04-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8ed04-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed04-127">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="8ed04-127">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="8ed04-128">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="8ed04-128">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="8ed04-129">Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="8ed04-129">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="8ed04-130">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="8ed04-130">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="8ed04-131">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8ed04-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ed04-132">Notes</span><span class="sxs-lookup"><span data-stu-id="8ed04-132">Remarks</span></span>

<span data-ttu-id="8ed04-133">La classe **\_ \_ NamespaceCreationEvent** est dérivée de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="8ed04-133">The **\_\_NamespaceCreationEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ed04-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ed04-134">Requirements</span></span>



| <span data-ttu-id="8ed04-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ed04-135">Requirement</span></span> | <span data-ttu-id="8ed04-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ed04-136">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8ed04-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ed04-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8ed04-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ed04-138">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8ed04-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ed04-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8ed04-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ed04-140">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8ed04-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8ed04-141">Namespace</span></span><br/>                | <span data-ttu-id="8ed04-142">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="8ed04-142">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8ed04-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ed04-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ed04-144">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="8ed04-144">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="8ed04-145">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="8ed04-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

