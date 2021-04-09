---
description: Signale un événement de modification d’instance, qui est un type d’événement intrinsèque généré lorsqu’une instance change dans l’espace de noms.
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: Classe __InstanceModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e644db16b6638bbc87006819e186540a9ce1874e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866905"
---
# <a name="__instancemodificationevent-class"></a><span data-ttu-id="adcc4-103">\_\_InstanceModificationEvent, classe</span><span class="sxs-lookup"><span data-stu-id="adcc4-103">\_\_InstanceModificationEvent class</span></span>

<span data-ttu-id="adcc4-104">La classe système **\_ \_ InstanceModificationEvent** signale un événement de modification d’instance, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) généré lorsqu’une instance change dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="adcc4-104">The **\_\_InstanceModificationEvent** system class reports an instance modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance changes in the namespace.</span></span>

<span data-ttu-id="adcc4-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="adcc4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="adcc4-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="adcc4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="adcc4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adcc4-107">Syntax</span></span>

``` syntax
class __InstanceModificationEvent : __InstanceOperationEvent
{
  object PreviousInstance;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="adcc4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="adcc4-108">Members</span></span>

<span data-ttu-id="adcc4-109">La classe **\_ \_ InstanceModificationEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="adcc4-109">The **\_\_InstanceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="adcc4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="adcc4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="adcc4-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="adcc4-111">Properties</span></span>

<span data-ttu-id="adcc4-112">La classe **\_ \_ InstanceModificationEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="adcc4-112">The **\_\_InstanceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="adcc4-113">**PreviousInstance**</span><span class="sxs-lookup"><span data-stu-id="adcc4-113">**PreviousInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adcc4-114">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="adcc4-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="adcc4-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="adcc4-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="adcc4-116">Copie de l’instance avant modification.</span><span class="sxs-lookup"><span data-stu-id="adcc4-116">Copy of the instance prior to modification.</span></span>

</dd> <dt>

<span data-ttu-id="adcc4-117">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="adcc4-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adcc4-118">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="adcc4-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="adcc4-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="adcc4-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="adcc4-120">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="adcc4-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="adcc4-121">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="adcc4-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="adcc4-122">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="adcc4-122">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adcc4-123">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="adcc4-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="adcc4-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="adcc4-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="adcc4-125">Nouvelle version de l’instance modifiée.</span><span class="sxs-lookup"><span data-stu-id="adcc4-125">New version of the changed instance.</span></span> <span data-ttu-id="adcc4-126">Cette propriété est héritée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="adcc4-126">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="adcc4-127">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="adcc4-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adcc4-128">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="adcc4-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="adcc4-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="adcc4-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="adcc4-130">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="adcc4-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="adcc4-131">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="adcc4-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="adcc4-132">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="adcc4-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="adcc4-133">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="adcc4-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="adcc4-134">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="adcc4-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="adcc4-135">Notes</span><span class="sxs-lookup"><span data-stu-id="adcc4-135">Remarks</span></span>

<span data-ttu-id="adcc4-136">La classe **\_ \_ InstanceModificationEvent** est dérivée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="adcc4-136">The **\_\_InstanceModificationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="adcc4-137">**Modification d’une ressource : \_ \_ InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="adcc4-137">**Modification of a resource: \_\_InstanceModificationEvent**</span></span>

<span data-ttu-id="adcc4-138">Supposons que vous soupçonnez qu’une application de gestion que vous utilisez modifie par erreur le type de démarrage d’un service sur l’un de vos serveurs.</span><span class="sxs-lookup"><span data-stu-id="adcc4-138">Suppose you suspect that a management application you are using is erroneously changing the startup type of a service on one of your servers.</span></span> <span data-ttu-id="adcc4-139">Vous souhaitez écrire un script WMI pour surveiller toutes les modifications apportées à la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="adcc4-139">You want to write a WMI script to monitor any modifications made to the configuration of the service.</span></span> <span data-ttu-id="adcc4-140">Dès qu’une modification est apportée à un service, son TargetInstance correspondant reflète la modification.</span><span class="sxs-lookup"><span data-stu-id="adcc4-140">As soon as a modification is made to a service, its corresponding TargetInstance reflects the modification.</span></span>

<span data-ttu-id="adcc4-141">Si vous enregistrez votre intérêt dans cet événement, une modification de la configuration du service entraîne la création d’une instance de la classe **\_ \_ InstanceModificationEvent** .</span><span class="sxs-lookup"><span data-stu-id="adcc4-141">If you register your interest in this event, a modification to the configuration of the service results in the creation of an instance of the **\_\_InstanceModificationEvent** class.</span></span>

<span data-ttu-id="adcc4-142">Les requêtes de notification qui demandent la notification de la modification d’une ressource et utilisent des événements intrinsèques utilisent une syntaxe similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="adcc4-142">Notification queries that request notification of the modification of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a><span data-ttu-id="adcc4-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="adcc4-143">Examples</span></span>

<span data-ttu-id="adcc4-144">L’exemple VBScript d' [événement de modification de processus Monitor](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) sur la Galerie TechNet utilise **\_ \_ InstanceModificationEvent** pour surveiller la première occurrence d’un événement de modification d’instance WMI pour le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="adcc4-144">The [Monitor process modification event](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) VBScript sample on TechNet Gallery uses **\_\_InstanceModificationEvent** to monitor the first occurrence of a WMI instance modification event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="adcc4-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adcc4-145">Requirements</span></span>



| <span data-ttu-id="adcc4-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adcc4-146">Requirement</span></span> | <span data-ttu-id="adcc4-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="adcc4-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="adcc4-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adcc4-148">Minimum supported client</span></span><br/> | <span data-ttu-id="adcc4-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="adcc4-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="adcc4-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adcc4-150">Minimum supported server</span></span><br/> | <span data-ttu-id="adcc4-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adcc4-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="adcc4-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="adcc4-152">Namespace</span></span><br/>                | <span data-ttu-id="adcc4-153">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="adcc4-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="adcc4-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adcc4-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adcc4-155">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="adcc4-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="adcc4-156">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="adcc4-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

