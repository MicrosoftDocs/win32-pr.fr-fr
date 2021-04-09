---
description: Signale un événement de modification d’espace de noms, qui est un type d’événement intrinsèque qui est généré lors de la modification d’un espace de noms.
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: Classe __NamespaceModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceModificationEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5af5783d3ebfbfb4b7842cb86b1919f8dbed1365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759442"
---
# <a name="__namespacemodificationevent-class"></a><span data-ttu-id="3ec97-103">\_\_NamespaceModificationEvent, classe</span><span class="sxs-lookup"><span data-stu-id="3ec97-103">\_\_NamespaceModificationEvent class</span></span>

<span data-ttu-id="3ec97-104">La classe système **\_ \_ NamespaceModificationEvent** signale un événement de modification d’espace de noms, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) qui est généré lors de la modification d’un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="3ec97-104">The **\_\_NamespaceModificationEvent** system class reports a namespace modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a namespace is modified.</span></span>

<span data-ttu-id="3ec97-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3ec97-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3ec97-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="3ec97-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec97-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ec97-107">Syntax</span></span>

``` syntax
class __NamespaceModificationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace PreviousNamespace;
  uint8       SECURITY_DESCRIPTOR [];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="3ec97-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3ec97-108">Members</span></span>

<span data-ttu-id="3ec97-109">La classe **\_ \_ NamespaceModificationEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3ec97-109">The **\_\_NamespaceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="3ec97-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3ec97-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ec97-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3ec97-111">Properties</span></span>

<span data-ttu-id="3ec97-112">La classe **\_ \_ NamespaceModificationEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3ec97-112">The **\_\_NamespaceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ec97-113">**PreviousNamespace**</span><span class="sxs-lookup"><span data-stu-id="3ec97-113">**PreviousNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec97-114">Type de données : **\_ \_ espace de noms**</span><span class="sxs-lookup"><span data-stu-id="3ec97-114">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="3ec97-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ec97-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec97-116">Copie de la version d’origine d’une instance d' [**\_ \_ espace de noms**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec97-116">Copy of the original version of a [**\_\_Namespace**](--namespace.md) instance.</span></span> <span data-ttu-id="3ec97-117">La propriété **Name** de cette instance identifie l’espace de noms modifié.</span><span class="sxs-lookup"><span data-stu-id="3ec97-117">The **Name** property of this instance identifies the namespace that is modified.</span></span>

</dd> <dt>

<span data-ttu-id="3ec97-118">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="3ec97-118">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec97-119">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="3ec97-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3ec97-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ec97-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec97-121">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="3ec97-121">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="3ec97-122">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="3ec97-122">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ec97-123">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="3ec97-123">**SECURITY\_DESCRIPTOR**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec97-124">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="3ec97-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3ec97-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ec97-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec97-126">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir un événement.</span><span class="sxs-lookup"><span data-stu-id="3ec97-126">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="3ec97-127">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="3ec97-127">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="3ec97-128">Une liste de contrôle d’accès (ACL) **null** dans le [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) accorde un accès illimité à tout le monde en permanence.</span><span class="sxs-lookup"><span data-stu-id="3ec97-128">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="3ec97-129">Pour plus d’informations, consultez [création d’un descripteur de sécurité pour un nouvel objet](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="3ec97-129">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="3ec97-130">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="3ec97-130">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec97-131">Type de données : **\_ \_ espace de noms**</span><span class="sxs-lookup"><span data-stu-id="3ec97-131">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="3ec97-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ec97-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec97-133">Copie de l’instance de l' [**\_ \_ espace de noms**](--namespace.md) qui est modifiée.</span><span class="sxs-lookup"><span data-stu-id="3ec97-133">Copy of the [**\_\_Namespace**](--namespace.md) instance that is modified.</span></span> <span data-ttu-id="3ec97-134">La propriété **Name** de l’instance d' **\_ \_ espace de noms** indique l’espace de noms modifié.</span><span class="sxs-lookup"><span data-stu-id="3ec97-134">The **Name** property of the **\_\_Namespace** instance indicates the namespace that is modified.</span></span> <span data-ttu-id="3ec97-135">Cette propriété est héritée de la classe [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="3ec97-135">This property is inherited from class [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ec97-136">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="3ec97-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec97-137">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ec97-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ec97-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ec97-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec97-139">Valeur unique qui indique l’heure à laquelle un événement est généré.</span><span class="sxs-lookup"><span data-stu-id="3ec97-139">Unique value that indicates the time that an event is generated.</span></span> <span data-ttu-id="3ec97-140">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="3ec97-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="3ec97-141">Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="3ec97-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="3ec97-142">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="3ec97-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="3ec97-143">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3ec97-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ec97-144">Notes</span><span class="sxs-lookup"><span data-stu-id="3ec97-144">Remarks</span></span>

<span data-ttu-id="3ec97-145">La classe **\_ \_ NamespaceModificationEvent** est dérivée de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="3ec97-145">The **\_\_NamespaceModificationEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

<span data-ttu-id="3ec97-146">Les seules différences entre l’espace de noms cible et l’espace de noms précédent sont les qualificateurs et les propriétés, à l’exception de [**Name**](--namespace.md).</span><span class="sxs-lookup"><span data-stu-id="3ec97-146">The only differences between the target namespace and the previous namespace is the qualifiers and properties except [**Name**](--namespace.md).</span></span>

<span data-ttu-id="3ec97-147">Notez que la propriété [**Name**](--namespace.md) d’une instance d' **\_ \_ espace de noms** ne peut pas changer car les espaces de noms ne peuvent pas être renommés.</span><span class="sxs-lookup"><span data-stu-id="3ec97-147">Note that the [**Name**](--namespace.md) property of a **\_\_Namespace** instance cannot change because namespaces cannot be renamed.</span></span> <span data-ttu-id="3ec97-148">Pour modifier le nom d’un espace de noms, l’instance d' **\_ \_ espace de noms** doit être supprimée et recréée avec un nouveau nom.</span><span class="sxs-lookup"><span data-stu-id="3ec97-148">To modify the name of a namespace, the **\_\_Namespace** instance must be deleted and re-created with a new name.</span></span> <span data-ttu-id="3ec97-149">Par conséquent, les événements de modification d’espace de noms sont générés lorsqu’une modification est apportée à des qualificateurs et des propriétés autres que **Name**.</span><span class="sxs-lookup"><span data-stu-id="3ec97-149">Therefore, namespace modification events are generated when a change occurs to qualifiers and properties other than **Name**.</span></span> <span data-ttu-id="3ec97-150">Un événement de modification d’espace de noms n’est pas généré lorsqu’un type de modification se produit dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="3ec97-150">A namespace modification event is not generated when any kind of change occurs within the namespace.</span></span> <span data-ttu-id="3ec97-151">Un événement de modification d’espace de noms est généré uniquement lors de la modification d’une instance d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="3ec97-151">A namespace modification event is generated only when a namespace instance is modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ec97-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ec97-152">Requirements</span></span>



| <span data-ttu-id="3ec97-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ec97-153">Requirement</span></span> | <span data-ttu-id="3ec97-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec97-154">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3ec97-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ec97-155">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec97-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ec97-156">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3ec97-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ec97-157">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec97-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ec97-158">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="3ec97-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3ec97-159">Namespace</span></span><br/>                | <span data-ttu-id="3ec97-160">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="3ec97-160">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="3ec97-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ec97-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec97-162">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="3ec97-162">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="3ec97-163">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="3ec97-163">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

