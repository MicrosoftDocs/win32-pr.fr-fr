---
description: La \_ \_ classe système MethodInvocationEvent est définie, mais n’est pas implémentée.
ms.assetid: ea736e44-a6bc-41e5-abc5-9e21a5504f44
ms.tgt_platform: multiple
title: Classe __MethodInvocationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodInvocationEvent
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: bc7e8d70d027caf31a90d49abc490c2de2d52fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203974"
---
# <a name="__methodinvocationevent-class"></a><span data-ttu-id="00b92-103">\_\_MethodInvocationEvent, classe</span><span class="sxs-lookup"><span data-stu-id="00b92-103">\_\_MethodInvocationEvent class</span></span>

<span data-ttu-id="00b92-104">La classe système **\_ \_ MethodInvocationEvent** est définie, mais n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="00b92-104">The **\_\_MethodInvocationEvent** system class is defined but is not implemented.</span></span>

<span data-ttu-id="00b92-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="00b92-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="00b92-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="00b92-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="00b92-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00b92-107">Syntax</span></span>

``` syntax
class __MethodInvocationEvent : __InstanceOperationEvent
{
  string       Method;
  __Parameters Parameters;
  boolean      PreCall;
  uint8        SECURITY_DESCRIPTOR[];
  object       TargetInstance;
  uint64       TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="00b92-108">Membres</span><span class="sxs-lookup"><span data-stu-id="00b92-108">Members</span></span>

<span data-ttu-id="00b92-109">La classe **\_ \_ MethodInvocationEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="00b92-109">The **\_\_MethodInvocationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="00b92-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00b92-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00b92-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00b92-111">Properties</span></span>

<span data-ttu-id="00b92-112">La classe **\_ \_ MethodInvocationEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="00b92-112">The **\_\_MethodInvocationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00b92-113">**Méthode**</span><span class="sxs-lookup"><span data-stu-id="00b92-113">**Method**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b92-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00b92-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00b92-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00b92-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00b92-116">Méthode appelée pour déclencher l’événement.</span><span class="sxs-lookup"><span data-stu-id="00b92-116">Method invoked to trigger the event.</span></span>

</dd> <dt>

<span data-ttu-id="00b92-117">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="00b92-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b92-118">Type de données : **\_ \_ paramètres**</span><span class="sxs-lookup"><span data-stu-id="00b92-118">Data type: **\_\_Parameters**</span></span>
</dt> <dt>

<span data-ttu-id="00b92-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00b92-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00b92-120">Référence à une instance qui représente les paramètres d’entrée et de sortie de l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="00b92-120">Reference to an instance that represents the input and output parameters of the method call.</span></span>

</dd> <dt>

<span data-ttu-id="00b92-121">**Préappel**</span><span class="sxs-lookup"><span data-stu-id="00b92-121">**PreCall**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b92-122">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="00b92-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00b92-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00b92-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00b92-124">Si la **valeur est true**, l’événement est déclenché avant l’appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="00b92-124">If **TRUE**, the event is raised before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="00b92-125">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="00b92-125">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b92-126">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="00b92-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="00b92-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00b92-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00b92-128">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="00b92-128">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="00b92-129">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="00b92-129">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="00b92-130">Pour plus d’informations, consultez [descripteurs de sécurité](/windows/desktop/SecAuthZ/security-descriptors).</span><span class="sxs-lookup"><span data-stu-id="00b92-130">For more information, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

</dd> <dt>

<span data-ttu-id="00b92-131">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="00b92-131">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b92-132">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="00b92-132">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="00b92-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00b92-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00b92-134">Instance sur laquelle la méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="00b92-134">Instance the method is invoked on.</span></span> <span data-ttu-id="00b92-135">Cette propriété est héritée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="00b92-135">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="00b92-136">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="00b92-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00b92-137">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="00b92-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="00b92-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00b92-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00b92-139">Valeur unique qui indique l’heure à laquelle un événement est généré.</span><span class="sxs-lookup"><span data-stu-id="00b92-139">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="00b92-140">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="00b92-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="00b92-141">Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="00b92-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="00b92-142">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="00b92-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="00b92-143">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="00b92-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00b92-144">Notes</span><span class="sxs-lookup"><span data-stu-id="00b92-144">Remarks</span></span>

<span data-ttu-id="00b92-145">La classe **\_ \_ MethodInvocationEvent** est dérivée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="00b92-145">The **\_\_MethodInvocationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00b92-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00b92-146">Requirements</span></span>



| <span data-ttu-id="00b92-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00b92-147">Requirement</span></span> | <span data-ttu-id="00b92-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="00b92-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="00b92-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00b92-149">Minimum supported client</span></span><br/> | <span data-ttu-id="00b92-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00b92-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="00b92-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00b92-151">Minimum supported server</span></span><br/> | <span data-ttu-id="00b92-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00b92-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="00b92-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="00b92-153">Namespace</span></span><br/>                | <span data-ttu-id="00b92-154">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="00b92-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="00b92-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00b92-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00b92-156">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="00b92-156">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="00b92-157">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="00b92-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

