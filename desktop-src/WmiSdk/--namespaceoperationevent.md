---
description: Classe de base pour tous les événements intrinsèques liés à un espace de noms.
ms.assetid: 168637b1-217e-4b6d-bd07-25127b9e9f6c
ms.tgt_platform: multiple
title: Classe __NamespaceOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: d263af0eab5fc3899b45659bc8409a5e68776fe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521943"
---
# <a name="__namespaceoperationevent-class"></a><span data-ttu-id="e0bee-103">\_\_NamespaceOperationEvent, classe</span><span class="sxs-lookup"><span data-stu-id="e0bee-103">\_\_NamespaceOperationEvent class</span></span>

<span data-ttu-id="e0bee-104">La classe système **\_ \_ NamespaceOperationEvent** est une classe de base pour tous les événements intrinsèques liés à un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e0bee-104">The **\_\_NamespaceOperationEvent** system class is a base class for all intrinsic events that relate to a namespace.</span></span>

<span data-ttu-id="e0bee-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e0bee-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e0bee-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e0bee-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0bee-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0bee-107">Syntax</span></span>

``` syntax
class __NamespaceOperationEvent : __Event
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="e0bee-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e0bee-108">Members</span></span>

<span data-ttu-id="e0bee-109">La classe **\_ \_ NamespaceOperationEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e0bee-109">The **\_\_NamespaceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="e0bee-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0bee-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0bee-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0bee-111">Properties</span></span>

<span data-ttu-id="e0bee-112">La classe **\_ \_ NamespaceOperationEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e0bee-112">The **\_\_NamespaceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0bee-113">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="e0bee-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0bee-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="e0bee-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e0bee-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0bee-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0bee-116">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="e0bee-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="e0bee-117">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="e0bee-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0bee-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="e0bee-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0bee-119">Type de données : **\_ \_ espace de noms**</span><span class="sxs-lookup"><span data-stu-id="e0bee-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="e0bee-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0bee-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0bee-121">Espace de noms affecté par l’événement.</span><span class="sxs-lookup"><span data-stu-id="e0bee-121">Namespace affected by the event.</span></span> <span data-ttu-id="e0bee-122">Pour les événements de création, il s’agit de l’espace de noms nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="e0bee-122">For creation events, this is the newly created namespace.</span></span> <span data-ttu-id="e0bee-123">Pour les événements de modification, il s’agit de l’espace de noms modifié.</span><span class="sxs-lookup"><span data-stu-id="e0bee-123">For modification events, this is the changed namespace.</span></span> <span data-ttu-id="e0bee-124">Pour les événements de suppression, il s’agit de l’espace de noms supprimé.</span><span class="sxs-lookup"><span data-stu-id="e0bee-124">For deletion events, this is the deleted namespace.</span></span>

</dd> <dt>

<span data-ttu-id="e0bee-125">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="e0bee-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0bee-126">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e0bee-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e0bee-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0bee-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0bee-128">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="e0bee-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="e0bee-129">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="e0bee-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="e0bee-130">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="e0bee-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="e0bee-131">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="e0bee-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="e0bee-132">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e0bee-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0bee-133">Notes</span><span class="sxs-lookup"><span data-stu-id="e0bee-133">Remarks</span></span>

<span data-ttu-id="e0bee-134">La classe **\_ \_ NamespaceOperationEvent** est dérivée de [**\_ \_ Event**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="e0bee-134">The **\_\_NamespaceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="e0bee-135">Les instances de cette classe ne sont pas créées.</span><span class="sxs-lookup"><span data-stu-id="e0bee-135">Instances of this class are not created.</span></span> <span data-ttu-id="e0bee-136">WMI crée des instances de l’une des classes suivantes dérivées de cette classe :</span><span class="sxs-lookup"><span data-stu-id="e0bee-136">WMI creates instances of one of the following classes derived from this class:</span></span>

[<span data-ttu-id="e0bee-137">**\_\_NamespaceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="e0bee-137">**\_\_NamespaceCreationEvent**</span></span>](--namespacecreationevent.md)

[<span data-ttu-id="e0bee-138">**\_\_NamespaceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="e0bee-138">**\_\_NamespaceModificationEvent**</span></span>](--namespacemodificationevent.md)

[<span data-ttu-id="e0bee-139">**\_\_NamespaceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="e0bee-139">**\_\_NamespaceDeletionEvent**</span></span>](--namespacedeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="e0bee-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0bee-140">Requirements</span></span>



| <span data-ttu-id="e0bee-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0bee-141">Requirement</span></span> | <span data-ttu-id="e0bee-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0bee-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e0bee-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0bee-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e0bee-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0bee-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e0bee-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0bee-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e0bee-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0bee-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e0bee-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e0bee-147">Namespace</span></span><br/>                | <span data-ttu-id="e0bee-148">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="e0bee-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e0bee-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0bee-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0bee-150">**\_\_Événement**</span><span class="sxs-lookup"><span data-stu-id="e0bee-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="e0bee-151">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="e0bee-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="e0bee-152">Détermination du type d’événement à recevoir</span><span class="sxs-lookup"><span data-stu-id="e0bee-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

