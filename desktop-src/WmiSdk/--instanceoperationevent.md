---
description: Sert de classe de base pour tous les événements intrinsèques liés à une instance.
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: Classe __InstanceOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d3111b74c876cc7ffedb959eca7f46812ed92e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529405"
---
# <a name="__instanceoperationevent-class"></a><span data-ttu-id="397dc-103">\_\_InstanceOperationEvent, classe</span><span class="sxs-lookup"><span data-stu-id="397dc-103">\_\_InstanceOperationEvent class</span></span>

<span data-ttu-id="397dc-104">La classe système **\_ \_ InstanceOperationEvent** sert de classe de base pour tous les événements intrinsèques liés à une instance.</span><span class="sxs-lookup"><span data-stu-id="397dc-104">The **\_\_InstanceOperationEvent** system class serves as a base class for all intrinsic events that relate to an instance.</span></span>

<span data-ttu-id="397dc-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="397dc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="397dc-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="397dc-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="397dc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="397dc-107">Syntax</span></span>

``` syntax
class __InstanceOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="397dc-108">Membres</span><span class="sxs-lookup"><span data-stu-id="397dc-108">Members</span></span>

<span data-ttu-id="397dc-109">La classe **\_ \_ InstanceOperationEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="397dc-109">The **\_\_InstanceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="397dc-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="397dc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="397dc-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="397dc-111">Properties</span></span>

<span data-ttu-id="397dc-112">La classe **\_ \_ InstanceOperationEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="397dc-112">The **\_\_InstanceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="397dc-113">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="397dc-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="397dc-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="397dc-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="397dc-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="397dc-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="397dc-116">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="397dc-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="397dc-117">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="397dc-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="397dc-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="397dc-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="397dc-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="397dc-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="397dc-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="397dc-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="397dc-121">Instance affectée par l’événement.</span><span class="sxs-lookup"><span data-stu-id="397dc-121">Instance affected by the event.</span></span> <span data-ttu-id="397dc-122">Pour les événements de création, il s’agit de l’instance nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="397dc-122">For creation events, this is the newly created instance.</span></span> <span data-ttu-id="397dc-123">Pour les événements de modification, il s’agit de la nouvelle version de l’instance modifiée.</span><span class="sxs-lookup"><span data-stu-id="397dc-123">For modification events, this is the new version of the changed instance.</span></span> <span data-ttu-id="397dc-124">Pour les événements de suppression, il s’agit de l’instance supprimée.</span><span class="sxs-lookup"><span data-stu-id="397dc-124">For deletion events, this is the deleted instance.</span></span>

</dd> <dt>

<span data-ttu-id="397dc-125">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="397dc-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="397dc-126">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="397dc-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="397dc-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="397dc-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="397dc-128">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="397dc-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="397dc-129">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="397dc-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="397dc-130">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="397dc-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="397dc-131">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="397dc-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="397dc-132">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="397dc-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="397dc-133">Notes</span><span class="sxs-lookup"><span data-stu-id="397dc-133">Remarks</span></span>

<span data-ttu-id="397dc-134">La classe **\_ \_ InstanceOperationEvent** est dérivée de [**\_ \_ Event**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="397dc-134">The **\_\_InstanceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="397dc-135">Les instances de **\_ \_ InstanceOperationEvent** ne sont pas créées ; seules les instances de ses sous-classes sont créées.</span><span class="sxs-lookup"><span data-stu-id="397dc-135">Instances of **\_\_InstanceOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="397dc-136">Les classes suivantes dérivent de **\_ \_ InstanceOperationEvent**:</span><span class="sxs-lookup"><span data-stu-id="397dc-136">The following classes derive from **\_\_InstanceOperationEvent**:</span></span>

[<span data-ttu-id="397dc-137">**\_\_InstanceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="397dc-137">**\_\_InstanceCreationEvent**</span></span>](--instancecreationevent.md)

[<span data-ttu-id="397dc-138">**\_\_InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="397dc-138">**\_\_InstanceModificationEvent**</span></span>](--instancemodificationevent.md)

[<span data-ttu-id="397dc-139">**\_\_InstanceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="397dc-139">**\_\_InstanceDeletionEvent**</span></span>](--instancedeletionevent.md)

<span data-ttu-id="397dc-140">**Vue d’ensemble**</span><span class="sxs-lookup"><span data-stu-id="397dc-140">**Overview**</span></span>

<span data-ttu-id="397dc-141">De même qu’il existe une classe WMI qui représente chaque type de ressource système qui peut être gérée à l’aide de WMI, il existe une classe WMI qui représente chaque type d’événement WMI.</span><span class="sxs-lookup"><span data-stu-id="397dc-141">Just as there is a WMI class that represents each type of system resource that can be managed using WMI, there is a WMI class that represents each type of WMI event.</span></span> <span data-ttu-id="397dc-142">Lorsqu’un événement qui peut être surveillé par WMI se produit, une instance de la classe d’événements WMI correspondante est créée.</span><span class="sxs-lookup"><span data-stu-id="397dc-142">When an event that can be monitored by WMI occurs, an instance of the corresponding WMI event class is created.</span></span> <span data-ttu-id="397dc-143">Un événement WMI se produit lorsque cette instance est créée.</span><span class="sxs-lookup"><span data-stu-id="397dc-143">A WMI event occurs when that instance is created.</span></span>

<span data-ttu-id="397dc-144">Il existe trois types principaux de classes d’événements WMI, qui sont tous dérivés de la classe d' [**\_ \_ événements**](--event.md) WMI : les événements intrinsèques, les événements extrinsèques et les événements de minuterie.</span><span class="sxs-lookup"><span data-stu-id="397dc-144">There are three major types of WMI event classes, all of which are derived from the [**\_\_Event**](--event.md) WMI class: Intrinsic Events, Extrinsic Events, and Timer Events.</span></span> <span data-ttu-id="397dc-145">Les événements intrinsèques, à leur tour, sont représentés par trois classes distinctes dérivées de la classe d' **\_ \_ événements** : [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md), **\_ \_ InstanceOperationEvent** et [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="397dc-145">Intrinsic Events, in turn, are represented by three distinct classes derived from the **\_\_Event** class: [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md), **\_\_InstanceOperationEvent**, and [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="397dc-146">Événements intrinsèques</span><span class="sxs-lookup"><span data-stu-id="397dc-146">Intrinsic Events</span></span>

<span data-ttu-id="397dc-147">Les événements intrinsèques permettent de surveiller une ressource représentée par une classe dans le référentiel CIM.</span><span class="sxs-lookup"><span data-stu-id="397dc-147">Intrinsic events are used to monitor a resource represented by a class in the CIM repository.</span></span> <span data-ttu-id="397dc-148">Chaque ressource est représentée par une instance d’une classe.</span><span class="sxs-lookup"><span data-stu-id="397dc-148">Each resource is represented by an instance of a class.</span></span> <span data-ttu-id="397dc-149">Cela signifie que la surveillance d’une ressource à l’aide de WMI implique en fait la surveillance des instances qui correspondent à la ressource.</span><span class="sxs-lookup"><span data-stu-id="397dc-149">This means that monitoring a resource using WMI actually involves monitoring the instances that correspond to the resource.</span></span>

<span data-ttu-id="397dc-150">Vous pouvez également utiliser des événements intrinsèques pour surveiller les modifications apportées à un espace de noms ou à une classe dans le référentiel.</span><span class="sxs-lookup"><span data-stu-id="397dc-150">Intrinsic events can also be used to monitor changes to a namespace or class in the repository.</span></span> <span data-ttu-id="397dc-151">Toutefois, l’analyse des modifications apportées aux espaces de noms ou aux classes est une valeur limitée pour les administrateurs système.</span><span class="sxs-lookup"><span data-stu-id="397dc-151">However, monitoring changes to namespaces or classes is of limited value to system administrators.</span></span>

<span data-ttu-id="397dc-152">Un événement intrinsèque est représenté par une instance d’une classe dérivée de \_ \_ InstanceOperationEvent, \_ \_ NamespaceOperationEvent ou \_ \_ ClassOperationEvent.</span><span class="sxs-lookup"><span data-stu-id="397dc-152">An intrinsic event is represented by an instance of a class derived from \_\_InstanceOperationEvent, \_\_NamespaceOperationEvent, or \_\_ClassOperationEvent.</span></span> <span data-ttu-id="397dc-153">Toutes les modifications apportées aux instances dans WMI sont représentées par la \_ \_ classe InstanceOperationEvent et les classes dérivées de celle-ci : \_ \_ InstanceCreationEvent, \_ \_ InstanceModificationEvent et \_ \_ InstanceDeletionEvent.</span><span class="sxs-lookup"><span data-stu-id="397dc-153">Any changes to instances in WMI are represented by the \_\_InstanceOperationEvent class and the classes derived from it: \_\_InstanceCreationEvent, \_\_InstanceModificationEvent, and \_\_InstanceDeletionEvent.</span></span>

<span data-ttu-id="397dc-154">La surveillance des ressources à l’aide de WMI implique l’analyse des instances et toutes les modifications apportées aux instances sont représentées par \_ \_ InstanceOperationEvent et les classes qui en sont dérivées.</span><span class="sxs-lookup"><span data-stu-id="397dc-154">Monitoring resources using WMI involves monitoring instances and all changes to instances are represented by \_\_InstanceOperationEvent and the classes derived from it.</span></span> <span data-ttu-id="397dc-155">Cela signifie que les ressources d’analyse impliquent en fin de la surveillance des instances de \_ \_ classes dérivées de InstanceOperationEvent.</span><span class="sxs-lookup"><span data-stu-id="397dc-155">This means that monitoring resources ultimately involves monitoring instances of \_\_InstanceOperationEvent-derived classes.</span></span>

<span data-ttu-id="397dc-156">Vous inscrivez un intérêt pour les instances de l’une de ces classes en émettant une requête de notification exprimée dans WQL.</span><span class="sxs-lookup"><span data-stu-id="397dc-156">You register interest in instances of one of these classes by issuing a notification query expressed in WQL.</span></span> <span data-ttu-id="397dc-157">La requête utilise une syntaxe similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="397dc-157">The query uses syntax similar to the following:</span></span>

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

<span data-ttu-id="397dc-158">Pour plus d’informations sur l’utilisation des événements d’instance WMI pour surveiller l’activité des ordinateurs, consultez [Comment puis-je surveiller les différents types d’événements avec un seul script ?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span><span class="sxs-lookup"><span data-stu-id="397dc-158">For a longer discussion of using the WMI instance events to monitor computer activity, see [How Can I Monitor for Different Types of Events With Just One Script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span></span>

## <a name="examples"></a><span data-ttu-id="397dc-159">Exemples</span><span class="sxs-lookup"><span data-stu-id="397dc-159">Examples</span></span>

<span data-ttu-id="397dc-160">L’exemple de code VBScript d' [événement de processus Monitor](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) sur la Galerie TechNet utilise **\_ \_ InstanceOperationEvent** pour surveiller le premier événement d’instance WMI pour le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="397dc-160">The [Monitor process event](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript code sample on TechNet Gallery uses **\_\_InstanceOperationEvent** to monitors the first WMI instance event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="397dc-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="397dc-161">Requirements</span></span>



| <span data-ttu-id="397dc-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="397dc-162">Requirement</span></span> | <span data-ttu-id="397dc-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="397dc-163">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="397dc-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="397dc-164">Minimum supported client</span></span><br/> | <span data-ttu-id="397dc-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="397dc-165">Windows Vista</span></span><br/>       |
| <span data-ttu-id="397dc-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="397dc-166">Minimum supported server</span></span><br/> | <span data-ttu-id="397dc-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="397dc-167">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="397dc-168">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="397dc-168">Namespace</span></span><br/>                | <span data-ttu-id="397dc-169">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="397dc-169">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="397dc-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="397dc-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="397dc-171">**\_\_Événement**</span><span class="sxs-lookup"><span data-stu-id="397dc-171">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="397dc-172">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="397dc-172">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="397dc-173">Détermination du type d’événement à recevoir</span><span class="sxs-lookup"><span data-stu-id="397dc-173">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="397dc-174">Écriture dans un fichier journal basé sur un événement</span><span class="sxs-lookup"><span data-stu-id="397dc-174">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 

