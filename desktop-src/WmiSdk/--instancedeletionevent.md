---
description: Signale un événement de suppression d’instance, qui est un type d’événement intrinsèque généré lorsqu’une instance est supprimée de l’espace de noms.
ms.assetid: a370fc95-15e3-49c3-98de-2f40d742f207
ms.tgt_platform: multiple
title: Classe __InstanceDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 018bac665aa95393fc1a9c7e51ad42038e8b27c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520049"
---
# <a name="__instancedeletionevent-class"></a><span data-ttu-id="7845e-103">\_\_InstanceDeletionEvent, classe</span><span class="sxs-lookup"><span data-stu-id="7845e-103">\_\_InstanceDeletionEvent class</span></span>

<span data-ttu-id="7845e-104">La classe système **\_ \_ InstanceDeletionEvent** signale un événement de suppression d’instance, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) généré lorsqu’une instance est supprimée de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="7845e-104">The **\_\_InstanceDeletionEvent** system class reports an instance deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance is deleted from the namespace.</span></span>

<span data-ttu-id="7845e-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7845e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7845e-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="7845e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7845e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7845e-107">Syntax</span></span>

``` syntax
class __InstanceDeletionEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="7845e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7845e-108">Members</span></span>

<span data-ttu-id="7845e-109">La classe **\_ \_ InstanceDeletionEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7845e-109">The **\_\_InstanceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="7845e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7845e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7845e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7845e-111">Properties</span></span>

<span data-ttu-id="7845e-112">La classe **\_ \_ InstanceDeletionEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7845e-112">The **\_\_InstanceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7845e-113">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="7845e-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7845e-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="7845e-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7845e-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7845e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7845e-116">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="7845e-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="7845e-117">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="7845e-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="7845e-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="7845e-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7845e-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="7845e-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7845e-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7845e-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7845e-121">Copie de l’instance qui a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="7845e-121">Copy of the instance that was deleted.</span></span> <span data-ttu-id="7845e-122">Cette propriété est héritée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="7845e-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="7845e-123">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="7845e-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7845e-124">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7845e-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7845e-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7845e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7845e-126">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="7845e-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="7845e-127">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="7845e-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="7845e-128">Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="7845e-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="7845e-129">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="7845e-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="7845e-130">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="7845e-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7845e-131">Notes</span><span class="sxs-lookup"><span data-stu-id="7845e-131">Remarks</span></span>

<span data-ttu-id="7845e-132">La classe **\_ \_ InstanceDeletionEvent** est dérivée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="7845e-132">The **\_\_InstanceDeletionEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="7845e-133">**Suppression d’une ressource : \_ \_ InstanceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="7845e-133">**Deletion of a resource: \_\_InstanceDeletionEvent**</span></span>

<span data-ttu-id="7845e-134">Si vous souhaitez vous assurer qu’un programme antivirus spécifique continue à s’exécuter sur un ordinateur, vous pouvez écrire un script qui surveille les processus sur l’ordinateur pour déterminer s’ils arrêtent.</span><span class="sxs-lookup"><span data-stu-id="7845e-134">If you want to ensure that a particular antivirus scanner program continues to run on a computer, you can write a script that monitors the processes on the computer to determine whether any of them stop.</span></span>

<span data-ttu-id="7845e-135">Les requêtes de notification qui demandent la notification de la suppression d’une ressource et utilisent des événements intrinsèques utilisent une syntaxe similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="7845e-135">Notification queries that request notification of the deletion of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceDeletionEvent WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe' `

## <a name="examples"></a><span data-ttu-id="7845e-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="7845e-136">Examples</span></span>

<span data-ttu-id="7845e-137">L’exemple de code VBScript de l' [événement analyser le processus de suppression](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) dans la Galerie TechNet utilise **\_ \_ InstanceDeletionEvent** pour surveiller la première occurrence d’un événement de suppression d’instance WMI pour le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="7845e-137">The [Monitor process deletion event](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) VBScript code sample on TechNet Gallery uses **\_\_InstanceDeletionEvent** to monitor the first occurrence of a WMI instance deletion event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="7845e-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7845e-138">Requirements</span></span>



| <span data-ttu-id="7845e-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7845e-139">Requirement</span></span> | <span data-ttu-id="7845e-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="7845e-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7845e-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7845e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7845e-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7845e-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7845e-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7845e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7845e-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7845e-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="7845e-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7845e-145">Namespace</span></span><br/>                | <span data-ttu-id="7845e-146">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="7845e-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="7845e-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7845e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7845e-148">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="7845e-148">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="7845e-149">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="7845e-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

