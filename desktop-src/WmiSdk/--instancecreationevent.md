---
description: Signale un événement de création d’instance, qui est un type d’événement intrinsèque qui est généré quand une nouvelle instance est ajoutée à l’espace de noms.
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: Classe __InstanceCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29bdefbe1db20cd8b55b74433061b6c0cf152378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210223"
---
# <a name="__instancecreationevent-class"></a><span data-ttu-id="e91ac-103">\_\_InstanceCreationEvent, classe</span><span class="sxs-lookup"><span data-stu-id="e91ac-103">\_\_InstanceCreationEvent class</span></span>

<span data-ttu-id="e91ac-104">La classe système **\_ \_ InstanceCreationEvent** signale un événement de création d’instance, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) qui est généré quand une nouvelle instance est ajoutée à l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e91ac-104">The **\_\_InstanceCreationEvent** system class reports an instance creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a new instance is added to the namespace.</span></span>

<span data-ttu-id="e91ac-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e91ac-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e91ac-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e91ac-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e91ac-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e91ac-107">Syntax</span></span>

``` syntax
class __InstanceCreationEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="e91ac-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e91ac-108">Members</span></span>

<span data-ttu-id="e91ac-109">La classe **\_ \_ InstanceCreationEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e91ac-109">The **\_\_InstanceCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="e91ac-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e91ac-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e91ac-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e91ac-111">Properties</span></span>

<span data-ttu-id="e91ac-112">La classe **\_ \_ InstanceCreationEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e91ac-112">The **\_\_InstanceCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e91ac-113">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="e91ac-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91ac-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="e91ac-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e91ac-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e91ac-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e91ac-116">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="e91ac-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="e91ac-117">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="e91ac-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91ac-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="e91ac-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91ac-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="e91ac-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e91ac-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e91ac-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e91ac-121">Copie de l’instance qui a été créée.</span><span class="sxs-lookup"><span data-stu-id="e91ac-121">Copy of the instance that was created.</span></span> <span data-ttu-id="e91ac-122">Cette propriété est héritée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="e91ac-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91ac-123">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="e91ac-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91ac-124">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e91ac-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e91ac-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e91ac-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e91ac-126">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="e91ac-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="e91ac-127">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="e91ac-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="e91ac-128">Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="e91ac-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="e91ac-129">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="e91ac-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="e91ac-130">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e91ac-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e91ac-131">Notes</span><span class="sxs-lookup"><span data-stu-id="e91ac-131">Remarks</span></span>

<span data-ttu-id="e91ac-132">La classe **\_ \_ InstanceCreationEvent** est dérivée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="e91ac-132">The **\_\_InstanceCreationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="e91ac-133">**Création d’une ressource : \_ \_ InstanceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="e91ac-133">**Creation of a resource: \_\_InstanceCreationEvent**</span></span>

<span data-ttu-id="e91ac-134">Supposons que vous soyez intéressé par la réception d’une notification si le bloc-notes est exécuté sur un ordinateur donné.</span><span class="sxs-lookup"><span data-stu-id="e91ac-134">Suppose you are interested in receiving a notification if Notepad is run on a certain computer.</span></span> <span data-ttu-id="e91ac-135">Quand le bloc-notes s’exécute, un processus correspondant est créé.</span><span class="sxs-lookup"><span data-stu-id="e91ac-135">When Notepad runs, a corresponding process is created.</span></span> <span data-ttu-id="e91ac-136">Les processus peuvent être gérés à l’aide de WMI et sont représentés par la \_ classe de processus Win32.</span><span class="sxs-lookup"><span data-stu-id="e91ac-136">Processes can be managed by using WMI and are represented by the Win32\_Process class.</span></span> <span data-ttu-id="e91ac-137">Lorsque le bloc-notes commence à s’exécuter, une instance correspondante de la \_ classe de processus Win32 devient disponible via WMI.</span><span class="sxs-lookup"><span data-stu-id="e91ac-137">When Notepad starts running, a corresponding instance of the Win32\_Process class becomes available through WMI.</span></span> <span data-ttu-id="e91ac-138">Si vous avez enregistré votre intérêt dans cet événement (en émettant la requête de notification d’événement appropriée), la disponibilité de cette instance entraîne la création d’une instance de la classe **\_ \_ InstanceCreationEvent** .</span><span class="sxs-lookup"><span data-stu-id="e91ac-138">If you have registered your interest in this event (by issuing the appropriate event notification query), the availability of this instance results in the creation of an instance of the **\_\_InstanceCreationEvent** class.</span></span>

<span data-ttu-id="e91ac-139">Les requêtes de notification qui demandent la notification de la création d’une ressource et utilisent des événements intrinsèques utilisent une syntaxe similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="e91ac-139">Notification queries that request notification of the creation of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

<span data-ttu-id="e91ac-140">Pour plus d’informations sur l’utilisation de **\_ \_ InstanceCreationEvent** comme moyen de surveiller les systèmes de fichiers, consultez [WMI et surveillance du système de fichiers](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) sur CodeProject.</span><span class="sxs-lookup"><span data-stu-id="e91ac-140">For a larger discussion of using **\_\_InstanceCreationEvent** as a way to monitor file systems, see [WMI and File System Monitoring](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) on CodeProject.</span></span>

## <a name="examples"></a><span data-ttu-id="e91ac-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="e91ac-141">Examples</span></span>

<span data-ttu-id="e91ac-142">L’exemple de création d’un [événement WMI permanent pour surveiller les fichiers](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell sur la Galerie TechNet utilise **\_ \_ InstanceCreationEvent** dans le cadre d’un script complexe pour configurer une inscription d’événement WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="e91ac-142">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a complex script to set up a permanent WMI event registration.</span></span>

<span data-ttu-id="e91ac-143">L’exemple PowerShell d' [événements permanents WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) sur la Galerie TechNet utilise **\_ \_ InstanceCreationEvent** dans le cadre d’un script de démonstration pour la configuration d’une inscription d’événement permanent.</span><span class="sxs-lookup"><span data-stu-id="e91ac-143">The [PowerShell WMI Permanent Events](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a demonstration script for setting up a permanent event registration.</span></span>

<span data-ttu-id="e91ac-144">L’exemple VBScript d' [événement de création de processus Monitor](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) sur TechNet utilise **\_ \_ InstanceCreationEvent** pour surveiller le premier événement de création d’instance WMI pour le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="e91ac-144">The [Monitor process creation event](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) VBScript sample on TechNet uses **\_\_InstanceCreationEvent** to monitors the first WMI instance creation event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="e91ac-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e91ac-145">Requirements</span></span>



| <span data-ttu-id="e91ac-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e91ac-146">Requirement</span></span> | <span data-ttu-id="e91ac-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="e91ac-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e91ac-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e91ac-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e91ac-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e91ac-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e91ac-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e91ac-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e91ac-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e91ac-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e91ac-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e91ac-152">Namespace</span></span><br/>                | <span data-ttu-id="e91ac-153">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="e91ac-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e91ac-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e91ac-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e91ac-155">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="e91ac-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="e91ac-156">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="e91ac-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

