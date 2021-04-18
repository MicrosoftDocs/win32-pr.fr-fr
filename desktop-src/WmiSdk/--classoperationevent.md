---
description: Est une classe de base pour tous les événements intrinsèques liés à une classe.
ms.assetid: 554bbabd-2639-40f5-8786-6df2188db0ec
ms.tgt_platform: multiple
title: Classe __ClassOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0c7a78219cec5c014e289dad4bf1cc29f0466a06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527003"
---
# <a name="__classoperationevent-class"></a><span data-ttu-id="f14e1-103">\_\_ClassOperationEvent, classe</span><span class="sxs-lookup"><span data-stu-id="f14e1-103">\_\_ClassOperationEvent class</span></span>

<span data-ttu-id="f14e1-104">La classe système **\_ \_ ClassOperationEvent** est une classe de base pour tous les événements intrinsèques liés à une classe.</span><span class="sxs-lookup"><span data-stu-id="f14e1-104">The **\_\_ClassOperationEvent** system class is a base class for all intrinsic events that relate to a class.</span></span>

<span data-ttu-id="f14e1-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f14e1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f14e1-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="f14e1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f14e1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f14e1-107">Syntax</span></span>

``` syntax
class __ClassOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="f14e1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="f14e1-108">Members</span></span>

<span data-ttu-id="f14e1-109">La classe **\_ \_ ClassOperationEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f14e1-109">The **\_\_ClassOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="f14e1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f14e1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f14e1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f14e1-111">Properties</span></span>

<span data-ttu-id="f14e1-112">La classe **\_ \_ ClassOperationEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f14e1-112">The **\_\_ClassOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f14e1-113">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="f14e1-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14e1-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="f14e1-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f14e1-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f14e1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f14e1-116">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="f14e1-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="f14e1-117">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="f14e1-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="f14e1-118">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="f14e1-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14e1-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="f14e1-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f14e1-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f14e1-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f14e1-121">Classe affectée par l’événement.</span><span class="sxs-lookup"><span data-stu-id="f14e1-121">Class affected by the event.</span></span> <span data-ttu-id="f14e1-122">Pour les événements de création, il s’agit de la classe nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="f14e1-122">For creation events, this is the newly created class.</span></span> <span data-ttu-id="f14e1-123">Pour les événements de modification, il s’agit de la nouvelle version de la classe modifiée.</span><span class="sxs-lookup"><span data-stu-id="f14e1-123">For modification events, this is the new version of the changed class.</span></span> <span data-ttu-id="f14e1-124">Pour les événements de suppression, il s’agit de la classe supprimée.</span><span class="sxs-lookup"><span data-stu-id="f14e1-124">For deletion events, this is the deleted class.</span></span>

</dd> <dt>

<span data-ttu-id="f14e1-125">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="f14e1-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14e1-126">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f14e1-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f14e1-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f14e1-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f14e1-128">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="f14e1-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="f14e1-129">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="f14e1-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="f14e1-130">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="f14e1-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="f14e1-131">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="f14e1-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="f14e1-132">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f14e1-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f14e1-133">Notes</span><span class="sxs-lookup"><span data-stu-id="f14e1-133">Remarks</span></span>

<span data-ttu-id="f14e1-134">La classe **\_ \_ ClassOperationEvent** est dérivée de [**\_ \_ Event**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="f14e1-134">The **\_\_ClassOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="f14e1-135">Les instances de **\_ \_ ClassOperationEvent** ne sont pas créées ; seules les instances de ses sous-classes sont créées.</span><span class="sxs-lookup"><span data-stu-id="f14e1-135">Instances of **\_\_ClassOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="f14e1-136">Les classes suivantes dérivent de **\_ \_ ClassOperationEvent**:</span><span class="sxs-lookup"><span data-stu-id="f14e1-136">The following classes derive from **\_\_ClassOperationEvent**:</span></span>

[<span data-ttu-id="f14e1-137">**\_\_ClassCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="f14e1-137">**\_\_ClassCreationEvent**</span></span>](--classcreationevent.md)

[<span data-ttu-id="f14e1-138">**\_\_ClassModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="f14e1-138">**\_\_ClassModificationEvent**</span></span>](--classmodificationevent.md)

[<span data-ttu-id="f14e1-139">**\_\_ClassDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="f14e1-139">**\_\_ClassDeletionEvent**</span></span>](--classdeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="f14e1-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f14e1-140">Requirements</span></span>



| <span data-ttu-id="f14e1-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f14e1-141">Requirement</span></span> | <span data-ttu-id="f14e1-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="f14e1-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f14e1-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f14e1-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f14e1-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f14e1-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f14e1-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f14e1-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f14e1-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f14e1-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f14e1-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f14e1-147">Namespace</span></span><br/>                | <span data-ttu-id="f14e1-148">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="f14e1-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f14e1-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f14e1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f14e1-150">**\_\_Événement**</span><span class="sxs-lookup"><span data-stu-id="f14e1-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="f14e1-151">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="f14e1-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="f14e1-152">Détermination du type d’événement à recevoir</span><span class="sxs-lookup"><span data-stu-id="f14e1-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

